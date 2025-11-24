
![[Pasted image 20251104203603.png]]
- 把没有用的参数剪掉
- 把大的network变小

# Frame

![[Pasted image 20251104204400.png]]
- 修剪的单位既可以用参数为单位，也可以以神经元为单位

# Practical Issue
## 剪枝参数(Weight Pruning)
![[Pasted image 20251104204802.png]]
- 剪去参数后，结构不对称，在pytorch不好做，因为一般都设置一次多少个
- 同时，GPU内的加速按照矩阵相乘加速，然而不对称的结构使加速困难
- 如果把剪去的参数设为0而不是删去，又失去了压缩的意义

## Neuron Pruning

![[Pasted image 20251104210316.png]]
- 剪掉神经元后，架构对称，改掉dimension就行
- GPU也好加速

# Why Pruning?

- 既然是把大的变小，为什么不直接train一个小的network呢？
- 因为大的更好train，比直接train小的正确率更高
## Lottery Ticket Hypothesis

![[Pasted image 20251104211415.png]]
-  原理：每一个network可以分为几个subnetwork,可能最后只有几个才train得起来
- 第一次剪枝后，小模型训练沿用之前大模型初始化的参数

![[Pasted image 20251104212357.png]]
## 打脸大乐透

![[Pasted image 20251104212658.png]]
- 论文中表述，只有learning rate 偏低，prune weight的情况下才观测得到大乐透假说中的内容