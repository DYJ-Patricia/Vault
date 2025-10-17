**GAN难train，其中最难之一是生成sequence**
# GAN for Sequence Generation

![[Pasted image 20251016180713.png]]
- 在GAN for sequence generation中，当Decoder作Generator时，参数的微小变化可能不会影响输出分布中分数最大的token，因此经过Discriminator的结果不变，无法计算微分 。
- 而CNN中的Max Pooling是一种确定性的下采样操作，它在局部区域内选择最大值，其结果只与局部区域内的数值大小有关，不存在因参数变化导致结果不变的问题，并且Max Pooling没有可训练参数，只是对特征图进行降维处理，不会出现类似Generator中因参数调整而结果不变的情况 。
- ==核心原因==是：CNN的Max Pooling本身无参数，参数变化只来自卷积层，而卷积层参数微调会改变特征图数值，Max Pooling会基于新数值重新选max，结果必然随参数变化。

- 具体拆解==两点关键差异==：
 
1. 参数归属不同：GAN的Decoder（Generator）是参数模型，所有输出依赖自身可训练参数；而Max Pooling是“无参数层”，它不参与参数更新，只对前序卷积层的输出做筛选。
​
2. 结果依赖不同：Decoder参数微调可能让“最优token选择”不变（比如top1概率仍属于同一个词），导致输出序列完全一样；但卷积层参数微调会改变特征图上每个像素的数值，Max Pooling会根据新的像素值重新挑选局部最大值，结果不可能完全不变。


- ==既然是不能用gradient descent train的问题，那可以用reinforcement learnig(RL)硬train==
- 但是，两个都超级难train！！！

# Evaluation of Generation

## Quality of Image

![[Pasted image 20251017102747.png]]
- 怎么判断Generator的好坏
- 一：作业上用人脸识别，数识别到的人脸数
- 二（most cases）:影像辨识系统。但是该方法不够，会遇到Mode collapse的问题。

![[Pasted image 20251017104406.png]]


## Diversity
### Mode Collapse

- 产生出来的来来去去是同一张图
- 因为generated data找到了一个舒适区，可以总是避过discriminator
- 解决：在训练Generator时一直都有checkpoint,在遇到mode collapse前调用之前的model

### Mode Dropping

- 它是指生成器只能生成训练集中的数据，难以生成非训练集的数据，即生成器完全忽略了真实数据中的某些模式，导致生成分布严重不完整。
- 例如，在生成人脸时，可能永远不会生成有胡须的人脸；在生成手写数字时，可能只生成数字 0、1、2，完全不生成 3~9。这是因为生成器不关心覆盖所有可能的样本，只专注于准确生成部分示例，类似于过拟合于训练集。
- 与 “Mode Collapse（模式坍塌）” 不同，“Mode Collapse” 是指生成器生成的样本多样性不足，倾向于生成几种高度相似的样本，但可能仍覆盖多个模式，而 “Mode Dropping” 则是生成器对某些模式完全不生成。

### Image Classifier 评估Diversity

![[Pasted image 20251017104154.png]]

- 过于集中，多样性不足

![[Pasted image 20251017104231.png]]


### Evaluation Measure

####  Inception Score
- Inception Score（IS， inception 分数）是评估生成对抗网络（GAN）等生成模型生成样本质量的常用指标之一，由谷歌团队在 2016 年提出，其核心思想是利用预训练的 Inception-v3 图像分类模型来衡量生成样本的 “质量” 和 “多样性”。

#### Frechet Inception Distance(FID)

![[Pasted image 20251017105329.png]]
- 把图片放入Inception Network后不要softmax输出后得到的图片
- 取出softmax之前的hidden layer产生的高维向量
- real image 与 generated image都丢进去，然后都拿出测量FID
- FID取值越小越好


# Conditio