- 评估actor
- 定义：看到一个画面后，会得到的reward
- 算是一个期望值
- 相当于未卜先知，看到游戏画面，提前评估出discounted cumulated reward
- ![[Pasted image 20251102215957.png]]

# Critic怎么训练

## MC

- 玩完整场游戏才能得到训练资料

![[Pasted image 20251102220434.png]]
## TD
- 不用玩完整场游戏就能得到训练资料
- 虽然不知道两个输出应该是多少，但知道两者之差是r_t
- ![[Pasted image 20251102221528.png]]

## MC vs TD

![[Pasted image 20251102222358.png]]
- 两者算出来的value function的结果可能不同
- 但都可以说是正确的


# Version 3.5

## Critic怎么用在Actor上

![[Pasted image 20251102222635.png]]
- 书接上文，G也是需要初始化的，故引入baseline
- 那baseline怎么算呢，就用到了Critic
- ![[Pasted image 20251102222852.png]]
- b就是Critic输出的分数，即V_θ


## A_t=G'_t - V_θ(S_t)

![[Pasted image 20251102223607.png]]
### V_θ(S_t)

- 看到一个画面后，随机执行a_t,故而会分出很多条路径，对应很多action，G得出来就许多，平均下来就是V_θ(S_t)
- 这是预期值，还没真正实行

### G'_t

- 看到一个画面，玩完游戏了算G'_t

### 减去的结果

- 如果是正数，代表执行的结果比预期好
- 如果是负数，代表执行的结果比预期差

### 违和

- V_θ(S_t)有很多样
- 但是G'_t只有一个sample，为什么不是平均减去平均？

# Version 4(平均减去平均)

![[Pasted image 20251102224537.png]]
- ==这个版本就变成了：==
- 采取a_t这个action得到的期望reward(下面)减掉不采取a_t而是根据某个distribution sample出来的reward
- 得到







