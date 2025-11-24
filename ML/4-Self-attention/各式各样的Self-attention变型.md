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
- 选择有代表性的key，数目由N变为K
- ==但是== ，可以改变query数量吗？Case by Case
- ![[Pasted image 20251015123037.png]]

### 怎么选出有代表性的key

- Compressed Attention:将一连串key sequence,用CNN扫过它，长的变短的，选出有代表性的key
- Linformer:![[Pasted image 20251015215528.png]]

## Attention机制的运算简化

![[Pasted image 20251015220102.png]]
- 两者结果一样，但运算量不一样
### 从数学角度看：
- ![[Pasted image 20251015221129.png]]
- ![[Pasted image 20251015221459.png]]
- ![[Pasted image 20251015221649.png]]

- 图中b1之和query的vector有关
- 蓝色和黄色的vector再求出来后，可以直接使用，再求b2,b3等时就不用重复运算
- ![[Pasted image 20251015222002.png]]
### 简化版流程
![[Pasted image 20251015222510.png]]

上图得到了b1分子的一项，分母类似

==接下来M个vector就不需要重算了==

![[Pasted image 20251015222831.png]]


### Realization(怎么拆分q,k)
![[Pasted image 20251015223026.png]]


### Synthesizer

- 不用q,k计算attention
- 把原本attention matrix的N乘N当作network中的N乘N个参数
- 则network中出了原本的weight,bias,又多加了attention weight
- 成了参数之后，输入不同的sequence,attention weight 都一样，performance不会变太差
- ![[Pasted image 20251015223542.png]]

### Attention free?

![[Pasted image 20251015223829.png]]

# Summary

Self attention有个benchmark 的corpus叫 long-range arena

![[Pasted image 20251015224028.png]]
