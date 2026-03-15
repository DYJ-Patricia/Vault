
# Seq2Seq

![[Pasted image 20260315140808.png]]

# 编码器-解码器细节

![[Pasted image 20260315140831.png]]


# 训练


![[Pasted image 20260315141009.png]]

# 衡量

![[Pasted image 20260315141022.png]]


# 总结

- Seq2seq 从一个句子生成另一个句子
- 编码器和解码器都是 RNN
- 将编码器最后时间隐状态来初始解码器隐状态来完成信息传递
- 常用 BLEU 来衡量生成序列的好坏

