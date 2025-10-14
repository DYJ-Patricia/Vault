# Seq2Seq Module

__Encoder+Decoder__

## Encoder

![[Pasted image 20251014172430.png]]
==encoder==内部结构
![[Pasted image 20251014172804.png]]
### ==实际上，transformer里做的事情更复杂==

- Residual connection是另一种network结构
- 此处的normalization是layer norm,比batch norm更简单，不用考虑batch的资讯
- batch是对不同example,不同feature的同一个dimension