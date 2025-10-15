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

- 假设y轴是query,x轴为key
- 前两row标红，代表