# 原理
- AlexNet 比 LeNet 更深更大
    
    来得到更好的精度
- 能不能更深和更大？
- 选项
    - 更多的全连接层（太贵）
    - 更多的卷积层
    - 将卷积层组合成块
## VGG块
![[Pasted image 20260127212959.png]]

![[Pasted image 20260127213157.png]]


# 进度

- LeNet (1995)
    
    - 2 卷积 + 池化层
    - 2 全连接层
    
- AlexNet
    
    - 更大更深
    - ReLu, Dropout, 数据增强
    
- VGG
    - 更大更深的 AlexNet（重复的 VGG 块）


![[Pasted image 20260127213340.png]]
- VGG计算量更大
- 计算更慢
# 总结

- VGG 使用可重复使用的卷积块来构建深度卷积神经网络
- 不同的卷积块个数和超参数可以得到不同复杂度的变种


# 代码

- 该示例为VGG-11架构的代码：8层卷积+三层全连接

```
import torch
from torch import nn
from d2l import torch as d2l


def vgg_block(num_convs, in_channels, out_channels):
    layers = []
    for _ in range(num_convs):
        layers.append(nn.Conv2d(in_channels, out_channels,
                                kernel_size=3, padding=1))
        layers.append(nn.ReLU())
        in_channels = out_channels
    layers.append(nn.MaxPool2d(kernel_size=2,stride=2))
    return nn.Sequential(*layers)
```


```
conv_arch = ((1, 64), (1, 128), (2, 256), (2, 512), (2, 512))
```

```
def vgg(conv_arch):  
    conv_blks = []  
    in_channels = 1  
    # 卷积层部分  
    for (num_convs, out_channels) in conv_arch:  
        conv_blks.append(vgg_block(num_convs, in_channels, out_channels))  
        in_channels = out_channels  
  
    return nn.Sequential(  
        *conv_blks, nn.Flatten(),  
        # 全连接层部分  
        nn.Linear(out_channels * 7 * 7, 4096), nn.ReLU(), nn.Dropout(0.5),  
        nn.Linear(4096, 4096), nn.ReLU(), nn.Dropout(0.5),  
        nn.Linear(4096, 10))  
  
net = vgg(conv_arch)
```
![[Pasted image 20260127215319.png]]
