
# 第一种解释
## 与fully connected network不同
- 输入图片为三维Tensor，input值为向量，分为宽-高-颜色channel（RBG）,eg:彩色图片channel为3，黑白为1
- 不需要把所有参数input，可能导致overfitting
- 故不需要侦测一整张图片
- 改成每一个neural只考虑自己的receptive field(人为划分,can be overlapping,多个neural可同时侦测同一个field)
![[Pasted image 20251013223221.png]]
## 简化fully connected network的方式（Typical Setting）
### 简化1
- receptive field通常高度重叠，stride为hyper parameter
- kernel size=宽和高，padding补值
- ![[Pasted image 20251013224009.png]]
### 简化2（同一个pattern出现在不同区域怎么办）
- 解决：把两个区域的neural参数调成一样
- ![[Pasted image 20251013224753.png]]
- ![[Pasted image 20251013225008.png]]
### fully connected network弹性被receptive field和sharing parameter双重限制,即成为CNN
![[Pasted image 20251013225527.png]]

# 第二种解释

