# Theory

![[Pasted image 20251016152956.png]]
- Div 相当于network中的loss function
- Divergence就是P(G)和P(data)两者之间的差异
- 我们需要从Generator中找出可以使loss最小的一组参数

## How to compute divergence

- 虽然不知道两者的distribution,但是可以sample from them
- 要依靠Discriminator来计算