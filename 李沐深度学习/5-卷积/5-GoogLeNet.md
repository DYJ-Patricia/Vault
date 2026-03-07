- NiN严重影响了该网络的设计

![[Pasted image 20260128141633.png]]

# Inception块

- imput之后分了四路
- 输出是concatenation层
- 所有四条路都没有改变高宽
- ![[Pasted image 20260128143525.png]]
- 白色框的卷积基本上是改变通道数的
- 蓝色框的拿来抽取信息：左边抽通道信息，右边三个抽取空间信息
- 输出通道为256个

跟单 3x3 或 5x5 卷积层比，Inception 块有更少的参数个数和计算复杂度

||#parameters|FLOPS|
|---|---|---|
|**Inception**|0.16 M|128 M|
|**3x3 Conv**|0.44 M|346 M|
|**5x5 Conv**|1.22 M|963 M|


# GoogLeNet

![[Pasted image 20260128145009.png]]

- 也是用了很多一乘一的卷积
- 最后通过一个全连接层映射到标号所要的类别数
- 不强求通道数等于类别数

## Stage1&2

- 通道数降低了8倍
- ![[Pasted image 20260128150107.png]]

## Stage 3

![[Pasted image 20260128152638.png]]

## Stage 4&5

![[Pasted image 20260128160004.png]]


# Inception 有各种后续变种

- Inception-BN (v2) - 使用 batch normalization（后面介绍）
- Inception-V3 - 修改了 Inception 块
    
    - 替换 5x5 为多个 3x3 卷积层
    - 替换 5x5 为 1x7 和 7x1 卷积层
    - 替换 3x3 为 1x3 和 3x1 卷积层
    - 更深
    
- Inception-V4 - 使用残差连接（后面介绍）

# 总结

- Inception 块用 4 条有不同超参数的卷积层和
    
    池化层的路来抽取不同的信息
    
    - 它的一个主要优点是模型参数小，计算复杂
        
        度低
    
- GoogleNet 使用了 9 个 Inception 块，是第一
    
    个达到上百层的网络
    - 后续有一系列改进