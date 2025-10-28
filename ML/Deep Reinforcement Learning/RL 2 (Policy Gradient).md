- 做optimization常用的演算法

# How to Control Actor

![[Pasted image 20251028102923.png]]
- a hat 就是相当于label，即ground truth
- 将输出a与a hat 算 cross-entropy,将e定义为loss,算loss最小时的参数是多少
- 如果不想采取a hat,算-e的最小值就行了

![[Pasted image 20251028103400.png]]

- 目前为止，这不就是supervised-learning吗？
- 是的，这跟训练个classifier一模一样

- 但是会有不同

![[Pasted image 20251028103735.png]]
- 每一个选择都有希望它发生或不发生的程度
- 现在把它乘e，一起算最小值