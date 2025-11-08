# Learning to Initialize

## Model-Agnostic Meta-Learning(MAML)
- learn 初始化参数

### Reference
![[Pasted image 20251108195847.png]]

### MAML VS Pre-training
![[Pasted image 20251108202739.png]]
#### self-supervised learning提出之前
![[Pasted image 20251108202646.png]]
- 在提出之前，pre-training也可以认为是multi-task learning
- 所以multi-task learning一般当作Meta的baseline
- 那Meta-learning不就相当于domain adaptation?
- ![[Pasted image 20251108203057.png]]

#### MAML为什么好？

![[Pasted image 20251108210223.png]]
- 该篇paper认为是第二个原因

### MAML变型

![[Pasted image 20251108210336.png]]
# Optimizer
- learning rate可以被学出来吗？
![[Pasted image 20251108212501.png]]
# Network Architecture Search(NAS)

- 这时候optimization就不能微分了
- 用RL算
![[Pasted image 20251108213205.png]]

![[Pasted image 20251108213517.png]]
## 让其可以微分(DARTS)

![[Pasted image 20251108213617.png]]

# Data Processing

![[Pasted image 20251108213702.png]]

# Sample Reweighting
![[Pasted image 20251108213807.png]]
# Beyond Gradient Descend
- 可以完全摆脱Gradient Descend吗？
- 直接吃训练资料，输出训练好的参数
- 有些论文进展如下：
![[Pasted image 20251108214011.png]]
# 训练和测试不分界
![[Pasted image 20251108214200.png]]
- 输入训练和测试资料，输出测试的结果

# Application

![[Pasted image 20251108214413.png]]
- 那怎么找一堆N-ways K-shot的tasks呢？
- Omniglot作为benchmark的corpus

![[Pasted image 20251108214759.png]]
