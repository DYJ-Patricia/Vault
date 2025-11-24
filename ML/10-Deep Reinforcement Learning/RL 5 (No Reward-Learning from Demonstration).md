- reward在游戏里常用，但在真实场景不太能
- 而且人类制定的reward获取规则可能会使机器往另一个方向发展

# Imitation Learning

- 没有reward的情况下，机器和环境互动
- ![[Pasted image 20251103214850.png]]
- 记录人类与环境的互动，作为expert的示范

# Problems

## 1

![[Pasted image 20251103220057.png]]
- 机器和人类看到的环境不同，人类做出的行为不能给机器很好的训练

## 2
- 不知道什么行为该模仿，什么不该
- ![[Pasted image 20251103220545.png]]
# Inverse Reinforcement Learning
- 跟原来的RL相反
- 原来的RL是根据reward去学习
- 但是已经没有reward了
- 所以是通过demonstration of expert和environment去反推reward function长什么样子
- 有了reward function后再去训练一个optimal actor
- ![[Pasted image 20251103221350.png]]
## IRL图形化表达

![[Pasted image 20251103221546.png]]
## 与GAN有异曲同工之妙

![[Pasted image 20251103221732.png]]
# To Learn More

- 给一个画面，机器自己创造目标，来训练
- ![[Pasted image 20251103222320.png]]
