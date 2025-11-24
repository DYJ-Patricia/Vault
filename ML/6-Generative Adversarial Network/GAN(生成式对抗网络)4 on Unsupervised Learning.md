
- 目前为止，讲的都是用的supervised learning

# Learning from Unpaired Data
- 之前在unconditional generation上，输入为高斯distribution sample 出来的，输出为复杂的distribution
- 现在的conditional generation输入输出为 DomainX,DomainY
- ==但是套用真的可以吗？==
- 不可以，因为要与x输入有关系
![[Pasted image 20251017212416.png]]
## Problems

- 影像风格转化，没有成对资料
- 在3中讲的conditional generation中是用的成对资料训练，而在这里只有unpaired data
- 那就用Cycle GAN

## Cycle GAN

![[Pasted image 20251017213649.png]]
- 其中一方向的训练：
- 从原来的一个generator变成训练两个
- 如果只有一个的话，那么discriminator不能判断generated image与输入的关联性
- 需要另一个generator将y再反向生成x，比对其与初始输入的x的关联性

![[Pasted image 20251017214358.png]]

- 将单方向的转化变成双向，则是完整的Cycle GAN
- 将单个discriminator变成双个，一个判断是否为动漫人物，一个判断是否为真实人物