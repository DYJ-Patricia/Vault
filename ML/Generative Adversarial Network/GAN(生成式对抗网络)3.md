**GAN难train，其中最难之一是生成sequence**
# GAN for Sequence Generation

![[Pasted image 20251016180713.png]]
- 在GAN for sequence generation中，当Decoder作Generator时，参数的微小变化可能不会影响输出分布中分数最大的token，因此经过Discriminator的结果不变，无法计算微分 。
- 而CNN中的Max Pooling是一种确定性的下采样操作，它在局部区域内选择最大值，其结果只与局部区域内的数值大小有关，不存在因参数变化导致结果不变的问题，并且Max Pooling没有可训练参数，只是对特征图进行降维处理，不会出现类似Generator中因参数调整而结果不变的情况 。
- ==核心原因==是：CNN的Max Pooling本身无参数，参数变化只来自卷积层，而卷积层参数微调会改变特征图数值，Max Pooling会基于新数值重新选max，结果必然随参数变化。

- 具体拆解==两点关键差异==：
 
1. 参数归属不同：GAN的Decoder（Generator）是参数模型，所有输出依赖自身可训练参数；而Max Pooling是“无参数层”，它不参与参数更新，只对前序卷积层的输出做筛选。
​
2. 结果依赖不同：Decoder参数微调可能让“最优token选择”不变（比如top1概率仍属于同一个词），导致输出序列完全一样；但卷积层参数微调会改变特征图上每个像素的数值，Max Pooling会根据新的像素值重新挑选局部最大值，结果不可能完全不变。


- ==既然是不能用gradient descent train的问题，那可以用reinforcement learnig(RL)硬train==
- 但是，两个都超级难train！！！



