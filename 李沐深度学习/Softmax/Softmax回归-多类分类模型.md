# 原理
- 做分类问题时用
- 把输出的数据做处理，输出的所有概率和为1且非负
- 真实值本来就是one-hot的，所以也相当于概率和为1
![[Pasted image 20251122164000.png]]

# Cross-entropy(交叉熵)
- 有了两个概率，用其计算loss
- 真实类别只有一个概率唯一，所以y_i直接为1

- ![[Pasted image 20251122164108.png]]

# 从头实现

## softmax
```
import torch
from IPython import display
from d2l import torch as d2l

batch_size=256
train_iter,test_iter=d2l.load_data_fashion_mnist(batch_size)


num_inputs=784
num_outputs=10

w=torch.normal(0,0.01,size=(num_inputs,num_outputs),requires_grad=True)
b=torch.zeros(num_outputs,requires_grad=True)


#给定矩阵X求和
X=torch.tensor([[1.0,2.0,3.0],[4.0,5.0,6.0]])
X.sum(0,keepdim=True),X.sum(1,keepdim=True)

#实现Softmax
def softmax(X):
    X_exp=torch.exp(X)
    #对每个样本的「指数化分数」求和，得到一个总和（这个总和是后续「归一化」的分母，确保所有概率之和为 1）。
    partition=X_exp.sum(1,keepdim=True)
    return X_exp / partition
    

#验证实现成功与否
X=torch.normal(0,1,(2,5))
X_prob=softmax(X)
X_prob,X_prob.sum(1)


 #实现softmax回归模型
def net(X):
    return softmax(torch.matmul(X.reshape((-1,w.shape[0])),w)+b)
    

```

函数逻辑：`图像展平 → 线性变换 → softmax归一化`，每一步的形状变化是关键，结合你的参数（`w.shape=(784,10)`，`b.shape=(10,)`）来看：

#### 1. 第一步：`X.reshape((-1, w.shape[0]))` → 图像展平（核心！）

- **作用**：把 2D 图像（28×28）转换成 1D 向量（784 维），才能和权重矩阵 `w` 做矩阵乘法。
- **参数解析**：
    - `reshape((-1, w.shape[0]))`：`-1` 表示「自动计算该维度的大小」，`w.shape[0]` 是 784（因为 `w` 是 `(784,10)`，输入维度 = 784）；
    - 目的：不管 `batch_size` 是多少，自动适配，把 `(batch_size, 1, 28, 28)` 转换成 `(batch_size, 784)`。
- **形状变化**：
    
    `(256, 1, 28, 28)` → `(256, 784)`（256 个样本，每个样本 784 个像素特征）。

#### 2. 第二步：`torch.matmul(..., w)` → 线性变换（矩阵乘法）

- **作用**：用权重矩阵 `w` 对展平后的特征做线性映射，得到每个类别的「原始分数」（logits）。
- **矩阵乘法规则**：前一个张量的最后一维，必须和后一个张量的第一维相等（这里 `784` 匹配 `w` 的第一维 `784`）。
- **形状变化**：
    
    `(256, 784)` × `(784, 10)` → `(256, 10)`（256 个样本，每个样本 10 个类别原始分数）。

#### 3. 第三步：`+ b` → 加偏置项（广播机制）

- **作用**：给每个类别的原始分数加一个偏置（补偿线性变换的偏移），让模型更灵活。
- **广播机制**：`b` 是 `(10,)` 的 1D 张量，会自动广播成 `(256, 10)`（每个样本的 10 个类别都加对应的偏置值）。
- **形状变化**：
    
    `(256, 10)` + `(10,)` → `(256, 10)`（维度不变，仅数值调整）。

#### 4. 第四步：`softmax(...)` → 归一化（转换成概率）

- **作用**：把线性变换后的「原始分数」（可能为负、无界）转换成「概率分布」（每个值 0~1，每行和为 1）。
- **形状变化**：
    
    `(256, 10)` → `(256, 10)`（维度不变，数值变成概率）。


## 交叉熵

```
#创建一个数据 y_hat
#其中包含 2 个样本在 3 个类别的预测概率，使用 y 作为 y_hat 中概率的索引
y=torch.tensor([0,2])
y_hat=torch.tensor([[0.1,0.3,0.6],[0.3,0.2,0.5]])
y_hat[[0,1],y]
```

- 作用：按「样本索引 + 真实类别索引」，提取每个样本在「自己真实类别」上的预测概率。
- 索引逻辑（PyTorch 高级索引规则）：
    - 第一个索引 `[0, 1]`：指定要提取的「样本行」（第 0 行、第 1 行，即所有样本）；
    - 第二个索引 `y`（即 `[0, 2]`）：指定每个样本要提取的「类别列」（第 0 行取列 0，第 1 行取列 2）；
    - 组合起来：提取 `y_hat[0, 0]`（第 0 样本类别 0 的概率）和 `y_hat[1, 2]`（第 1 样本类别 2 的概率）。


```
#实现交叉熵损失函数
def cross_entropy(y_hat,y):
    return -torch.log(y_hat[range(len(y_hat)),y])

cross_entropy(y_hat,y)
```

![[Pasted image 20251122205812.png]]
#### 为什么要「提取真实类别的概率」？

交叉熵的核心思想是：**只关注模型对「真实类别」的预测准度**，不关心对其他类别的预测（比如第 0 样本，不管模型对类别 1、2 的概率是多少，只看类别 0 的概率）。这和分类任务的目标一致（只要预测对真实类别即可）。

## 继续实现
- 计算「模型预测正确的样本数占总样本数的比例」（准确率）:

```
#将预测类别与真实y元素进行比较
def accuracy(y_hat,y):
    if len(y_hat.shape)>1 and y_hat.shape[1]>1:
        y_hat=y_hat.argmax(axis=1)
    cmp=y_hat.type(y.dtype)==y
    return float(cmp.type(y.dtype).sum())

accuracy(y_hat,y) / len(y)


def evaluate_accuracy(net, data_iter):
    """计算在指定数据集上模型的精度。"""
    if isinstance(net, torch.nn.Module):
        net.eval()  # 将模型设置为评估模式
    metric = Accumulator(2)  # 正确预测数、预测总数
    for X, y in data_iter:
        metric.add(accuracy(net(X), y), y.numel())
    return metric[0] / metric[1]
    
#实现Accumulator
class Accumulator:
    """在`n`个变量上累加。"""
    def __init__(self, n):
        self.data = [0.0] * n

    def add(self, *args):
        self.data = [a + float(b) for a, b in zip(self.data, args)]

    def reset(self):
        self.data = [0.0] * len(self.data)

    def __getitem__(self, idx):
        return self.data[idx]

evaluate_accuracy(net, test_iter)
```

```
def train_epoch_ch3(net, train_iter, loss, updater):
    if isinstance(net, torch.nn.Module):
        net.train()
    metric = Accumulator(3)
    for X, y in train_iter:
        y_hat = net(X)
        l = loss(y_hat, y)
        if isinstance(updater, torch.optim.Optimizer):
            updater.zero_grad()
            l.backward()
            updater.step()
            metric.add(
                float(l) * len(y), accuracy(y_hat, y),
                y.size().numel()
            )
        else:
            l.sum().backward()
            updater(X.shape[0])
            metric.add(
                float(l.sum()), accuracy(y_hat, y), y.numel()
            )
    return metric[0] / metric[2], metric[1] / metric[2]
    
    
    #定义一个在动画中绘制数据的实用数据类

class Animator:
    """在动画中绘制数据的实用类（补全核心逻辑）"""
    def __init__(self, xlabel=None, ylabel=None, legend=None, xlim=None,
                 ylim=None, xscale='linear', yscale='linear',
                 fmts=('-', 'm--', 'g-.', 'r:'), nrows=1, ncols=1,
                 figsize=(3.5, 2.5)):
        if legend is None:
            legend = []
        d2l.use_svg_display()  # 使用SVG格式显示图像（更清晰）
        # 创建绘图窗口和坐标轴
        self.fig, self.axes = d2l.plt.subplots(nrows, ncols, figsize=figsize)
        if nrows * ncols == 1:
            self.axes = [self.axes,]  # 统一成列表格式，方便后续操作
        # 配置坐标轴的函数（xlabel、ylabel、图例等）
        self.config_axes = lambda: d2l.set_axes(
            self.axes[0], xlabel, ylabel, xlim, ylim, xscale, yscale, legend)
        self.X, self.Y, self.fmts = None, None, fmts  # 存储x/y数据和线条格式

    def add(self, x, y):
        """添加一个数据点到图像中，动态更新绘制"""
        if not hasattr(y, "__len__"):
            y = [y]  # 如果y是单个值（如准确率），转为列表，适配多曲线
        n = len(y)  # 曲线的数量（这里是3条：训练损失、训练acc、测试acc）
        
        # 如果x是单个值，转为与y长度一致的列表（每个曲线共享同一个x轴值，如epoch）
        if not hasattr(x, "__len__"):
            x = [x] * n
        
        # 初始化X和Y：存储每条曲线的x/y数据（X是列表的列表，Y同理）
        if not self.X:
            self.X = [[] for _ in range(n)]
        if not self.Y:
            self.Y = [[] for _ in range(n)]
        
        # 将新数据添加到对应曲线的列表中
        for i, (a, b) in enumerate(zip(x, y)):
            if a is not None and b is not None:
                self.X[i].append(a)  # 第i条曲线的x值
                self.Y[i].append(b)  # 第i条曲线的y值
        
        # 清空当前坐标轴，重新绘制所有曲线（避免多条曲线重叠混乱）
        self.axes[0].cla()
        for x, y, fmt in zip(self.X, self.Y, self.fmts):
            self.axes[0].plot(x, y, fmt)  # 绘制每条曲线（fmt是线条格式，如实线、虚线）
        
        self.config_axes()  # 应用坐标轴配置（显示xlabel、ylabel、图例等）
        display.display(self.fig)  # 在IPython中显示图像
        plt.draw()  # 强制刷新图像
        plt.pause(0.001)  # 暂停极短时间，让图像有时间渲染
        display.clear_output(wait=True)  # 清空输出，避免重复显示多个图像
```


## 总训练函数
```
#训练函数
def train_ch3(net, train_iter, test_iter, loss, num_epochs, updater):
    animator = Animator(xlabel='epoch', xlim=[1, num_epochs], ylim=[0.3, 0.9],
                        legend=['train loss', 'train acc', 'test acc'])
    for epoch in range(num_epochs):
        train_metrics = train_epoch_ch3(net, train_iter, loss, updater)
        test_acc = evaluate_accuracy(net, test_iter)
        animator.add(epoch + 1, train_metrics + (test_acc,))
    train_loss, train_acc = train_metrics
    
    
#小批量随机梯度下降来优化模型的损失函数
lr = 0.1

def updater(batch_size):
    return d2l.sgd([w, b], lr, batch_size)
```

## 开始训练

```
#训练模型10个迭代周期
num_epochs = 10
train_ch3(net, train_iter, test_iter, cross_entropy, num_epochs, updater)
```

## 对图像进行分类预测

```
# 对图像进行分类预测
def predict_ch3(net, test_iter, n=6):
    """预测标签（定义见第3章）。"""
    for X, y in test_iter:
        break
    trues = d2l.get_fashion_mnist_labels(y)
    preds = d2l.get_fashion_mnist_labels(net(X).argmax(axis=1))
    titles = [true + '\n' + pred for true, pred in zip(trues, preds)]
    d2l.show_images(X[0:n].reshape((n, 28, 28)), 1, n, titles=titles[0:n])

predict_ch3(net, test_iter)
```


# 简洁实现

```
import torch
from torch import nn
from d2l import torch as d2l

batch_size=256
train_iter,test_iter=d2l.load_data_fashion_mnist(batch_size)


# PyTorch不会隐式地调整输入的形状。
# 因此，我们定义了展平层（flatten）在线性层前调整网络输入的形状
net = nn.Sequential(nn.Flatten(), nn.Linear(784, 10))

def init_weights(m):
    if type(m) == nn.Linear:
        nn.init.normal_(m.weight, std=0.01)

net.apply(init_weights);


loss=nn.CrossEntropyLoss()


#使用学习率为 0.1 的小批量随机梯度下降作为优化算法
trainer=torch.optim.SGD(net.parameters(),lr=0.1)

```

- 训练函数沿用之前实现的

- 开始训练
```
#训练模型10个迭代周期
num_epochs = 10
train_ch3(net, train_iter, test_iter, loss, num_epochs, trainer)
```

![[Pasted image 20251122215221.png]]
