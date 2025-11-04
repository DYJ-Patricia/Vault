# 原理

- 大的network作为Teacher Net,小的作为Student Net根据Teacher Net训练出来
- ![[Pasted image 20251104214123.png]]
- 以字迹辨识的一个classifier为例，Teacher Net 得到input,输出distribution，Student Net不管正确答案是什么，只需要照着Teacher Net 的输出学习，不断趋近

# Tip : Temperature for Softmax

![[Pasted image 20251104220219.png]]
- 即在exponential前把每一个除以T
- T是hyper-parameter,需要直接调