# 概述
当input不是vector而是vector set时
![[Pasted image 20251014121440.png]]

## Output的分类：
### Each vector has a label(Sequence Labling)
- 输入和输出数量一样
- POS tagging 词性辨识
- Social Node
### The whole sequence has a label

- Sentiment analysis(positive/negative)
- 语者辨认
### Model decides the number of  labels itself

- seq2seq,如翻译，语音辨识

# Sequence Labling

### 如果单纯用fully connected network

- 做词性辨识时，I saw a saw,判断不出saw的不同词性
