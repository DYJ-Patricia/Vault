- 先后学两个任务会遗忘第一个
- 同时学就不会
- Multi-task learning可以看作LLL的upper bound

# 不同评估模型好坏的方法
- ![[Pasted image 20251105233004.png]]

![[Pasted image 20251105233409.png]]
![[Pasted image 20251105233554.png]]

# LLL的三个解法

## Selective Synaptic(突触的) Plasticity(可塑性) (Regularization-base approach)

### 遗忘的原因

![[Pasted image 20251106200846.png]]

- 最开始初始参数是θ(0),通过gradient 训出参数θ(b),在task1上loss很小
- 把θ(b)放在task2上继续训练出θ(star)，再放到task1上后，表现变差了
- 这就叫forget

### Basic Idea
- 在参数上做限制
![[Pasted image 20251106202024.png]]

- L(θ)是原来的新的任务的loss
- 某些参数接近就好
- b(i)越大，越重要
![[Pasted image 20251106202409.png]]
- b(i)为0时，就没限制了，会造成遗忘
- b(i)无限大时，不会遗忘多少，但学不会新的任务
- b(i)一般自己设计

### b(i)怎么设出来的
- 每个方法算的方法不一样，用的资料也不一样
![[Pasted image 20251106203630.png]]
### Regularization-base approach早年方法

- 在gradient update的方向上做限制

![[Pasted image 20251106204930.png]]

- 先在task2上gradient参数，然后在task1上gradient，如果方向不太一致(内积小于0)，就修改g，把它变成g',g和g'要尽可能接近
- 但是task1得到g(b)是需要它自己的资料的，所以需要一点额外的空间
## Additional Neural Resource Allocation
### Progressive Neural Networks
- 比较费空间，每多一个任务进来就加一点空间，任务量不重的时候可以派上用场

![[Pasted image 20251106205503.png]]
### PackNet

- 先开一个大空间，每个任务用不同的参数
- ![[Pasted image 20251106205909.png]]
### 两者结合

![[Pasted image 20251106205933.png]]

## Memory Reply
