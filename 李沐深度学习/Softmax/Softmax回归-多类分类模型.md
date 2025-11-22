# 原理
- 做分类问题时用
- 把输出的数据做处理，输出的所有概率和为1且非负
- 真实值本来就是one-hot的，所以也相当于概率和为1
![[Pasted image 20251122164000.png]]

# Cross-entropy(交叉熵)
- 有了两个概率，用其计算loss
- 真实类别只有一个概率唯一，所以y_i直接为1

- ![[Pasted image 20251122164108.png]]

# 实现

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


```