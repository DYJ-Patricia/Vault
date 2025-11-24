- 之前讲的基本都基于supervised learning，包括self-supervised learning(只是是机器自己给label罢了)
- RL和之前的machine learning是一样的框架，都是三个步骤
- 这次偏浅显地讲
- RL随机性非常非常大

# 概述
![[Pasted image 20251028093304.png]]
- 有两个东西，一个是Actor,一个是Environment
- Actor负责接收从Environment传来的Observation,并输出Action给Environment
- 这就近似于一个函数Action=f(Observation)
- 答对了，Environment会给Action奖励（Reward）

# Example(Playing Video Game)

![[Pasted image 20251028094125.png]]


# Step 1:Function with Unknown

![[Pasted image 20251028095048.png]]
- Policy Network和classifier没什么两样
- 经过一层soft-max layer，然后根据每个action的几率随机决定下一步动作

# Step 2:Define "Loss"

![[Pasted image 20251028100517.png]]
- 我们要最大化total reward(return)
- 负的total reward就相当于network里的loss

# Step 3:Optimization
![[Pasted image 20251028101853.png]]
- s和a这样子交替排列进行的sequence是Trajectory
- Reward相当于一个函数，根据s和a决定输出的r
- 找出即learn出一组参数，放在network中actor里能使reward越大越好
- 类比GAN,Actor相当于Generator,另外两个相当于Discriminator
- Actor努力找出能使Reward输出最大的参数
- 然而不一样的是，其中，Actor是network,而Environment和Reward是黑盒子
