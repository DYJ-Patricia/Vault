# Meta Learning vs Self-supervised Learning

- BERT和MAML似乎都是找初始化参数
- 是相辅相成的，不互斥
- ![[Pasted image 20251109173023.png]]
- self-supervised learning可以为MAML提供初始化参数
- MAML再去找更好的初始化参数
- ![[Pasted image 20251109173605.png]]
- 两者各有所长各有所短
- ![[Pasted image 20251109173848.png]]
- MAML用在NLP上的paper

# Meta Learning vs Knowledge Distillation

- 正确率最高的老师不见得教出最好的学生
- 引进Meta,学会teach

## Learn to Teach

- Teacher Net updata的目标是让student net做得更好
![[Pasted image 20251109174501.png]]
# Meta Learning vs Domain Adaptation

![[Pasted image 20251109174607.png]]

## Meta Learning for Domain Generalization
- 在domain generalization中，训练阶段target domain的资料是拿不到的

![[Pasted image 20251109174941.png]]
- 那可以从training domain中抽一组来假扮target domain
![[Pasted image 20251109175050.png]]

# Meta Learning vs Life-long Learning

## 用Meta来解决LLL的遗忘

![[Pasted image 20251109175517.png]]

![[Pasted image 20251109175748.png]]
## Meta自己也会遇上遗忘

![[Pasted image 20251109175958.png]]

# 更多资料
![[Pasted image 20251109180109.png]]