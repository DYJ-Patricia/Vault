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
- 