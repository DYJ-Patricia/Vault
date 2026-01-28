- 就是更深更大的LeNet
![[Pasted image 20260125225323.png]]

- 激活函数、pooling改变

![[Pasted image 20260125225915.png]]

![[Pasted image 20260125230624.png]]

![[Pasted image 20260125230818.png]]

# 更多细节

- 激活函数从 sigmoid 变到了 ReLu（减缓梯度消失）
- 隐藏全连接层后加入了丢弃层
- 数据增强

# 总结

- AlexNet 是更大更深的 LeNet，10x 参数个数，260x 计算复杂度
- 新进入了丢弃法，ReLU，最大池化层，和数据增强
- AlexNet 赢下了 2012 ImageNet 竞赛后，标志着新的一轮神经网络热潮的开始

# 代码实现

```
import torch from torch 
import nn from d2l 
import torch as d2l 
net = nn.Sequential( 
nn.Conv2d(1, 96, kernel_size=11, stride=4, padding=1), nn.ReLU(), 
nn.MaxPool2d(kernel_size=3, stride=2), 
nn.Conv2d(96, 256, kernel_size=5, padding=2), nn.ReLU(), nn.MaxPool2d(kernel_size=3, stride=2), 
nn.Conv2d(256, 384, kernel_size=3, padding=1), nn.ReLU(), 
nn.Conv2d(384, 384, kernel_size=3, padding=1), nn.ReLU(), 
nn.Conv2d(384, 256, kernel_size=3, padding=1), nn.ReLU(), nn.MaxPool2d(kernel_size=3, stride=2), nn.Flatten(), 
nn.Linear(6400, 4096), nn.ReLU(), nn.Dropout(p=0.5), 
nn.Linear(4096, 4096), nn.ReLU(), nn.Dropout(p=0.5), 
nn.Linear(4096, 10) )
```
