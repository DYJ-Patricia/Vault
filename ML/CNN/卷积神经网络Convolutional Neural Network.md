# 与fully connected network不同
- 输入图片为三维Tensor，分为宽-高-颜色channel（RBG）
- 不需要把所有参数input，可能导致overfitting
- 改成每一个neural只考虑自己的receptive field(人为划分,can be overlapping,多个neural可同时侦测同一个field)
![[Pasted image 20251013223221.png]]
# 简化fully connected network的方式
## 简化1
- receptive field通常高度重叠，stride为hyper parameter
- kernel size=宽和高，padding补值
- ![[Pasted image 20251013224009.png]]
