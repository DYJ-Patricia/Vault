# Seq2Seq Module

__Encoder+Decoder__

## Encoder

![[Pasted image 20251014172430.png]]
==encoder==内部结构，上图灰框为Block
![[Pasted image 20251014172804.png]]
### ==实际上，transformer里做的事情更复杂==

- Residual connection是另一种network结构
- 此处的normalization是layer norm,比batch norm更简单，不用考虑batch的资讯
- ==batch==是对不同example,不同feature的同一个dimension计算
- ==layer==是对同一个example,同一个feature的不同dimension计算
- ![[Pasted image 20251014173930.png]]
- **红点所指处才是真正的==Block==输出**
- ![[Pasted image 20251014174231.png]]
- Feed Forword为一种fully connected network
- Block会重复多次

### 原始架构不一定Optimum

![[Pasted image 20251014174710.png]]


## Decoder

- 把Encoder输出到Decoder
- 输入时先添加一个BEGIN token
- 运作后输出END,机器自己决定output length

### Autoregressive（AT）

![[Pasted image 20251014212926.png]]
可能一步错，步步错

#### Masked Self-attention
==不考虑右边的==
![[Pasted image 20251014213322.png]]
**因为Decoder的output是一个一个产生的，只能考虑左边的东西**

### Non-autoregressive(NAT)

- NAT 速度比AT快
- NAT is usually worth than AT
- ![[Pasted image 20251014214603.png]]



 ## Encoder-Decoder

![[Pasted image 20251014215028.png]]


### Cross attention运作过程（Encoder-Decoder互动）
- 它在self-attention前就出来了
- ==Encoder提供k,Decoder提供q==
![[Pasted image 20251014215309.png]]

- 原始上看，encoder,decoder都有很多层，且decoder用encoder的最后一层
- 然而，可以创新，随意用encoder的任意一层叠加

## Training

==刚刚讲的都是模型训练好后怎么做testing的==

