- Attention matrix可能过大导致计算量大
- 当sequence input 的N非常长时，self-attention dominates computation
- 为了加快，催生出了许多变型

# 变型

## Local Attention/Truncated Attention

- 只看左右两边附近的weight,其它区域的weight设为零。
- 与CNN很像。
## Stride Attention

- 自己设定stride，跳几个看左右两边的资讯。

## Global Attention

- ![[Pasted image 20251015114543.png]]

- 假设y轴是query,每一个row代表一个query,x轴为key,每一个column代表一个key
- 前两row标红，代表input sequence头两个位置是special token。前两个query要attend到其它的key。则前两个row都是有值的，都要计算attention
- 前两个column代表出了special token标定的其它query，也会attend不是special token的位置

==可以全都用，multi-attention有多个head,每个head use different pattern==

- Longformer:三个都用
- Big Bird：Longformer基础上加了Random Attention

## Clustering

- 为了focus重点,可以把attention value 小的直接设为0
- 那如何分辨呢？按照相似度用clustering分组

![[Pasted image 20251015120304.png]]

- 在attention matrix上，当query和key在同一个cluster时，才计算attention weight
- 其它直接设为0

==目前为止以上方法都是人为决定是否计算attention==

## Learnable Patterns(Sinkhorn Sorting Network)

- 另外learn一个network来决定要不要计算
- ![[Pasted image 20251015121553.png]]
- 先输出，后转化为所需的binary matrix
- 假设input为10乘10,100个vector1进NN里，有共用vector的情况1，变成了只要是10种vector，解析度变低


## Do we need full attention matrix?

- 在图中会有很多column出现redundant的情况，也许我们可以把图变成跟简练的形式



