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

![[Pasted image 20251024220621.png]]
- 两个方法都可以测量
- 第一种：四个方格各自改变一点
- 第二种：四个方格中只有一个改动浮动大
- 两种的L2-norm相同
- 但是第二种的L-infinity大得多

# Attack Approach

## 先不考虑constraint(x0和x之间有threshold的限制)
![[Pasted image 20251024221239.png]]
- 和训练一个模型相似
- 首先初始化，就不从random开始了，从input的x0开始初始化
- 然后递归算gradient descent,每个iteration里算g，但是这次不管network了，求出的Loss这次是和初始input相比较，所以是求x向量每一个对Loss的偏微分
- 求出来的结果乘上learning rate,再被x一减，就得到新的x

## 考虑constraint

![[Pasted image 20251024222242.png]]

- 在无限制的基础上，如果update后，如果x与x_t差距超过threshold，则如右下图就近更正

- 关于attack变型，分optimize和constraint上变化

## 最快的方法（可过simple baseline）

- ![[Pasted image 20251024222722.png]]
- 只跑一个iteration
- 一击必杀，最后一定落在边框上

![[Pasted image 20251024222918.png]]
- 多做几个iteration,表现更好，可以过medium baseline
- 但是有出界的风险
