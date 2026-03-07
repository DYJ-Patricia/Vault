- 改变network架构来压缩
# Review: Standard CNN

- Feature map有多少channel，则filter有多少层，但filter数量自由决定
- 用filter去扫feature map，有几个filter，则输出的feature map有多少层
- ![[Pasted image 20251104223037.png]]
# Depthwise Separable Convolution

## 操作
- 分为两个步骤
### Depthwise Convolution(convolution layer的变型)
![[Pasted image 20251104223927.png]]
- filter数量和channel数量一样，即没有厚度
- 一个filter只管一个channel
- 故输出的map层数和之前输入的层数一样
- 但是，如果某个pattern跨channel了，单单这一层无法满足
### Pointwise Convolution

![[Pasted image 20251104224555.png]]
- 除了filter的大小必须是1* 1，其它与标准CNN一样
- 它专门管channel之间的关系

# Depthwise Separable Convolution vs Standard Convolution

![[Pasted image 20251104225517.png]]
- O偏大，先忽略不计
- 那k，即kernel size就很关键

# Low Rank Approximation

- 在network里，一层的W拆成两层：U,V
- 在W中间插一个没有activate function的Linear K
- 用到的参数会减少

![[Pasted image 20251104230056.png]]
- Depthwise Separable Convolution用的就是这个概念——把一层拆成两层
- ![[Pasted image 20251104230809.png]]
- 18->1
- 18->2->1

# Paper
![[Pasted image 20251104230926.png]]
