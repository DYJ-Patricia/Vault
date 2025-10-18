-  之前有label的训练是supervised learning
- 现在没了，self-supervised learning可以看作一种unsupervised learning
- BERT的network架构和transformer encoder一模一样
# Mask Input
- 输入句子，随机决定哪些token被mask（special token/替换成其它token），又随机决定替换方式（二选一）
- 被遮住的token输进去后从BERT输出，再输入到Linear Model做一个linear transform(就是乘个矩阵),然后经过softmax，输出一个distrisbution(一个非常长的向量)
- ![[Pasted image 20251018222859.png]]
- 机器输出的要尽可能和ground truth靠近
- ![[Pasted image 20251018222958.png]]

# Next Sentence Prediction

![[Pasted image 20251018224033.png]]

- 预测两个句子是不是该接在一起
- 但没什么用


# Downstream Tasks

- BERT像一个胚胎干细胞，可以分化去做任务
- 虽然只能解填空题，但还是能解各式各样的任务
- BERT分化成各式各样任务叫Fine-tune(微调)
- 在之前产生BERT的过程叫pre-train
- ![[Pasted image 20251018224605.png]]

# How to use BERT
## Case1

-  在该例子中，Linear 和BERT合在一起是完整的Sentiment Analysis 的Classification Model
- 训练中 Linear 和BERT都会用Gradient Ascend去update
- 只是现在Linear部分的参数是随机初始化的
- BERT的参数是由学会做填空题的BERT那里来的,也就是fine-tune后
- ![[Pasted image 20251018225822.png]]

## Case2

- 和普通的分类相比，BERT不是随机初始化的

![[Pasted image 20251018230423.png]]
、
## Case3

- 吃两个句子，吐出两个句子的关系
- 可以应用于立场分析
- ![[Pasted image 20251018230940.png]]
- ![[Pasted image 20251018230914.png]]

## Case4(HW7会用)

- 问答系统建立
- ![[Pasted image 20251018231315.png]]
- 整个里面只有两个需要Random Initialized的向量
- 分别拿来和document输出的向量内积
- 橙色部分乘出来，预测正确答案起的位置
- 蓝色预测结束位置
- ![[Pasted image 20251018231649.png]]

- ![[Pasted image 20251018231843.png]]
- BERT输入长度理论上没有限制，但实践上sequence有限制

## Seq2Seq
![[Pasted image 20251018232652.png]]
- 那怎么把Input弄坏
- ![[Pasted image 20251018232755.png]]
- 
# Training BERT is Challenging


