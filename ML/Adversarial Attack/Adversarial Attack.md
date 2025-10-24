- attacked image
- benign image
- 加入非常小的杂讯，使network输出的结果不同

# How to attack
![[Pasted image 20251024215630.png]]
- network参数固定情况下
- Non-targeted:负的y和y hat的cross entropy的最小，即两者差距最大
- Targeted:在前者基础上，还要与y target越近越好
- 两者的x变化（x和x0的差距）不能被人类察觉

## 怎么计算x，x0的差距

