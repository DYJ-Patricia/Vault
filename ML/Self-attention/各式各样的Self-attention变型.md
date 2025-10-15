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
