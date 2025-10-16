# Theory

![[Pasted image 20251016152956.png]]
- Div 相当于network中的loss function
- Divergence就是P(G)和P(data)两者之间的差异
- 我们需要从Generator中找出可以使loss最小的一组参数

## How to compute divergence

- 虽然不知道两者的distribution,但是可以sample from them
- 要依靠Discriminator来计算
![[Pasted image 20251016154600.png]]
- Objective Function是求最大，Loss Function是求最小
- 相关论文推导出，==max值和divergence是相关的==
- 很像train 一个二元classifier这个Function类似于negative cross entropy
- small divergence->hard to discriminate->small maxV(D,G)
- large divergence->easy to discriminate->large maxV(D,G)

![[Pasted image 20251016155702.png]]
- 于是可以用objective function替换原本的DIV(P(G),P(data))
- 红框里是给定generator,利用discriminator求使V最大的D
- 外面是求使红框框最小的G