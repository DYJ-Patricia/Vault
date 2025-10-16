# Network as Generator

- Network 的input由x和z（simple distribution 里sample出来的，是random的）构成
- 这个distribution的式子自己决定，够简单就行（知道formulation是什么）
- 随着z不同，输出y不同，输出就由单一数值变成了complex distribution
## Why distribution

- eg:小精灵走迷宫，向左向右都是对的，但不能同时向左向右，所以需要distribution
- 适用于有creativity的case,即同一input,不同输出


# Anime Face Generation

## Unconditional Generation

- 把x拿掉，则输入是z,输出为y
- z是由normal distribution sample 出来的low-dim vector
- 经过generator后输出的是high-dim vector

## Discriminantor

- 是一种neural network（即function）
- 输入一张图片，输出scalar(数值)，large means real,smaller value means fake
- 架构由自己设置，CNN或transformer等都可以用

## Basic Idea of GAN

- ![[Pasted image 20251016130126.png]]


- ![[Pasted image 20251016130420.png]]

## Algorithm

- 都是network,先初始化G,D
- ==step1,update descriminantor==
- 先随机sample出z,generator便输出很不像动画人物的图.从真实图
