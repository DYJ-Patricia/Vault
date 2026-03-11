`forward`（前向传播）和 `backward`（反向传播）是深度学习模型**训练的两个核心步骤**，前者算 “预测结果和损失”，后者算 “参数梯度”，共同完成模型参数的更新。

---

### ✅ 1. Forward（前向传播）

#### 核心逻辑：

从输入数据出发，按照模型的网络结构（卷积、全连接、激活函数等），一步步计算到输出，最终得到预测结果，并计算损失函数（如交叉熵、MSE）。

#### 通俗理解：

“顺着网络走一遍”，输入是数据，输出是**预测值**和**损失值**（衡量预测有多不准）。

#### 代码示例（PyTorch）：


``` python
import torch
import torch.nn as nn

# 定义简单模型
class SimpleModel(nn.Module):
    def __init__(self):
        super().__init__()
        self.linear = nn.Linear(10, 1)  # 线性层
    
    # 必须实现forward函数，定义前向传播逻辑
    def forward(self, x):
        return self.linear(x)

model = SimpleModel()
x = torch.randn(2, 10)  # 输入数据 [Batch=2, 特征数=10]

# 前向传播：输入→模型→预测值→损失
y_pred = model(x)  # 前向传播核心调用
y_true = torch.randn(2, 1)  # 真实标签
loss_fn = nn.MSELoss()
loss = loss_fn(y_pred, y_true)  # 计算损失
print("前向传播损失：", loss.item())
```

---

### ✅ 2. Backward（反向传播）

#### 核心逻辑：

从损失值出发，按照**链式法则**，反向计算每个模型参数（如权重、偏置）的梯度（导数），梯度表示 “参数变化一点点，损失会怎么变”。

#### 通俗理解：

“倒着走一遍网络”，输入是损失值，输出是**所有可训练参数的梯度**，目的是找到让损失变小的参数更新方向。

#### 代码示例（接上面）：



``` python
# 反向传播：计算梯度
loss.backward()  # 核心调用，自动计算所有参数的梯度

# 查看梯度（以线性层的权重为例）
print("线性层权重的梯度形状：", model.linear.weight.grad.shape)
print("线性层权重的梯度值：", model.linear.weight.grad)

# 用梯度更新参数（优化器做这件事）
optimizer = torch.optim.SGD(model.parameters(), lr=0.01)
optimizer.step()  # 根据梯度更新参数
optimizer.zero_grad()  # 清空梯度（避免累加）
```

---

### ✅ 关键关系 & 注意点

表格

|维度|Forward（前向传播）|Backward（反向传播）|
|---|---|---|
|方向|输入 → 隐藏层 → 输出|损失 → 输出 → 隐藏层 → 输入|
|计算目标|预测值、损失值|各参数的梯度|
|依赖|只依赖模型结构和输入数据|依赖前向传播的损失值|
|核心作用|评估模型预测效果|指导参数更新（减小损失）|

#### 重要细节：

1. `backward()` 只能对**标量**（如损失值）调用（因为梯度是对标量求导）；
2. 每次反向传播前要调用 `optimizer.zero_grad()`，否则梯度会累加（导致参数更新错误）；
3. 只有 `nn.Module` 中的可训练参数（默认 `requires_grad=True`）才会计算梯度。

---

### 总结

1. `forward` 是 “正向算损失”，定义模型的计算逻辑，是必须手动实现的；
2. `backward` 是 “反向算梯度”，PyTorch 自动根据链式法则计算，只需调用 `loss.backward()`；
3. 训练流程固定：`forward` 算损失 → `backward` 算梯度 → 优化器更新参数 → 重复至收敛。