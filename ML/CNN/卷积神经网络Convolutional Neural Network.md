
# 第一种解释
## 与fully connected network不同
- 输入图片为三维Tensor，input值为向量，分为长-宽-颜色channel（RBG）,eg:彩色图片channel为3，黑白为1
- 不需要把所有参数input，可能导致overfitting
- 故不需要侦测一整张图片
- 改成每一个neural只考虑自己的receptive field(人为划分,can be overlapping,多个neural可同时侦测同一个field)
![[Pasted image 20251013223221.png]]
## 简化fully connected network的方式（Typical Setting）
### 简化1
- receptive field通常高度重叠，stride为hyper parameter
- kernel size=长和宽，padding补值
- ![[Pasted image 20251013224009.png]]
### 简化2（同一个pattern出现在不同区域怎么办）
- 解决：把两个区域的neural参数调成一样
- ![[Pasted image 20251013224753.png]]
- ![[Pasted image 20251013225008.png]]
### fully connected network弹性被receptive field和sharing parameter双重限制,即成为CNN
![[Pasted image 20251013225527.png]]

# 第二种解释

![[Pasted image 20251013230427.png]]

- ==filter里数值未知，需要gradient decent找出==
![[Pasted image 20251013230823.png]]
## 在第一层layer中（假设channel为1）
- 假设数值已知，逐步移动计算，如图。对角线刚好与Filter相同且数值最大的左上和左下角为需要监测的Feature
- 每个Filter都做一遍操作
- ==假设有64个filter，则生成有64组数字的Feature Map==
- ==Feature Map可以被看做是一张包含64个channel的image==
## 在第二层layer中
- 第一层convolution化后，第二层layer开始convolution
- channel，即高度，由3变为64
- ![[Pasted image 20251013232503.png]]
- 不用担心filter 3-3的大小不够侦测比较大的pattern，相反，==layer深度越深，范围越大。==同样的大小，在原图上变成了5-5.

# 共通

不同区域的neural share parameter就相当于把filter扫过一张图片，而这组

![[Pasted image 20251013233210.png]]
