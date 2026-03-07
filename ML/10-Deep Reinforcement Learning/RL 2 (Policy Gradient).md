- 做optimization常用的演算法

# How to Control Actor

![[Pasted image 20251028102923.png]]
- a hat 就是相当于label，即ground truth
- 将输出a与a hat 算 cross-entropy,将e定义为loss,算loss最小时的参数是多少
- 如果不想采取a hat,算-e的最小值就行了

![[Pasted image 20251028103400.png]]

- 目前为止，这不就是supervised-learning吗？
- 是的，这跟训练个classifier一模一样

- 但是会有不同

![[Pasted image 20251028103735.png]]
- 每一个选择都有希望它发生或不发生的程度
- 现在把它乘e，一起算最小值

# 多版本讲解
## Version 1

![[Pasted image 20251101100356.png]]
- 但是这个版本有问题：把r_N归功于遥远的a_1不太好吧

## Version 2

![[Pasted image 20251101102030.png]]
## Version 3

![[Pasted image 20251101102611.png]]
- reward是相对的，如果全都得出正数，并不代表所有行为都是好的，所以需要引入baseline

# Policy Gradient怎么操作

- 之前的收集资料在for loop之外
- 而RL在之外
- ![[Pasted image 20251101103242.png]]
- 所有每update一次参数，就得再收集一次资料
- ![[Pasted image 20251101103436.png]]
- 这里收集资料和与环境互动的actor最好是同一个，即On-policy

## On-policy vs Off-policy

![[Pasted image 20251101104249.png]]

![[Pasted image 20251101104408.png]]


# Collecting Training Data : Exploration

- actor的随机性很重要
- ![[Pasted image 20251101104635.png]]
