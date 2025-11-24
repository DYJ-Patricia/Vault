# 概述
==当input不是vector而是vector set时，sequence有长有短==
![[Pasted image 20251014121440.png]]

## Output的分类：
### Each vector has a label(Sequence Labling)
- 输入和输出数量一样
- POS tagging 词性辨识
- Social Node
### The whole sequence has a label

- Sentiment analysis(positive/negative)
- 语者辨认
### Model decides the number of  labels itself

- seq2seq,如翻译，语音辨识

# Sequence Labling

### 如果单纯用fully connected network

- 做词性辨识时，I saw a saw,判断不出saw的不同词性
- 故需如HW2把前后几个vector一起投进模型
### 改成self-attention

- 模型会吃下一整个sequence并输出与输入数量相同的vector
- 每个vector都是考虑了整个sequence后得到的
- 最后把输出的vector丢入fully connected network（FC）去辨识
- 两者可以交替使用
- 在Attention is all you need Paper中提到Transformer中一个最重要的module是self-attention

## How Self-Attention Work

![[Pasted image 20251014124328.png]]
### 确定两个vector之间的relevant阿尔法

#### ==Dot-product(点积) ==
- 各自先乘两个矩阵matrix
![[Pasted image 20251014124816.png]]


#### Additive
- 把q,k相连后丢进一个activation function
![[Pasted image 20251014125030.png]]
### 流程

#### 先计算关联性

![[Pasted image 20251014125406.png]]

- a1自己也要算自己的key
- 然后投入soft-max(Softmax是一种激活函数，核心作用是将神经网络输出的任意实数（logits），转化为总和为1的概率分布，让结果可直接用于多分类任务的判断。)
- ![[Pasted image 20251014125734.png]]
- 后面的normalization中 ==soft max==最常见，但是投入任何activation function都行，有人试过ReLU
#### 抽取信息b1

![[Pasted image 20251014130446.png]]

## 矩阵角度的理解
![[Pasted image 20251014133544.png]]
==形成含四个column的matrix==

![[Pasted image 20251014133906.png]]
- k 倒置后做 inner product

- ![[Pasted image 20251014134128.png]]
- ![[Pasted image 20251014134359.png]]
 ###  总流程
 ![[Pasted image 20251014134625.png]]
 ==只有W是未知的，需要从training data找出来==


# Muti-Head Self-attention

==相关性有多种，则q,k,v都可以不止一个==

![[Pasted image 20251014135131.png]]
# Positional Encoding

- self-attention内无位置信息
- 但是可以再加一个each position has a uneque positional vector  ei
- 这个vector是hand-craft的
- 可以用function,network等方法训练出来

# 在image上与CNN相比

CNN: self-attention that can only attends in a receptive field
 
- CNN is simplified self-attention.
 
Self-attention: CNN with learnable receptive field
 
- Self-attention is the complex version of CNN.

==self-attention弹性更大，需要更多训练资料==

- 两个都可以一起用

# RNN

![[Pasted image 20251014141906.png]]
Self-attention加上某个东西就成了RNN

# GNN

![[Pasted image 20251014142336.png]]
