# Anomaly Detection 1
## Problem Formulation(问题描述)

- 如从前所说，机器学习就是不断找function
- 在异常侦测中，有了一组训练资料，我们需要找到一个function来检测input x是否与训练资料相似

## Application

- Fraud Detection:检测盗刷
- 网络系统入侵侦测
- Cancer Detection

## Binary Classification?

- 一组可以是宝可梦，当训练资料
- 但异常资料太多太杂，无法分类成另一类
- 并且异常资料很难收集
- 所以该问题不是单纯的二元分类

## Categories
![[Pasted image 20251022214546.png]]
- Training data with labels
- 在classification时讲过，可以用generative model做classification，deep learning也可以做
- 但是我们期待，机器训练之后可以把没看过的东西标注unknown


# Anomaly Detection 2(有标注的case)

![[Pasted image 20251022220214.png]]
- 在这里，classifier不止输出判断x来自于哪里
- 还要输出信心分数
- 分类器输出是distribution
- 算信心分数方数不唯一
- ![[Pasted image 20251022220515.png]]
-  还可以用entropy来算，比如上方entropy小，下方大

![[Pasted image 20251022221256.png]]
- 表现更好的计算信心分数的方法

# Anomaly Detection 3

## Dev Set(Validation Set)

- 用于训练集和测试集中间
- 在辛普森一家的该案例中，在训练资料中输入辛普森一家的图片，并labelled by 它对应的角色
- 而Dev Set中，图片是不是辛普森一家都可以，并且每张labelled by 这个图片是或否来自辛普森一家

## Example Framework
![[Pasted image 20251022222650.png]]
## 如何评估一个系统的好坏