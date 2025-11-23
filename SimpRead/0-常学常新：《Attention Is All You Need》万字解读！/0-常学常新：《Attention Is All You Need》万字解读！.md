---
url: https://zhuanlan.zhihu.com/p/703292893
title: 常学常新：《Attention Is All You Need》万字解读！
author: zhuanlan.zhihu.com
aliases: 
 - 常学常新：《Attention Is All You Need》万字解读！
date: 2025-11-23 23:55:30
tags:

banner: "https://pic1.zhimg.com/v2-434782544b0e3c9db79aa4879d2f8064_720w.jpg?source=172ae18b"
banner_icon: 🔖
---
大家好，我是木易，一个持续关注 AI 领域的互联网技术产品经理，国内 Top2 本科，美国 Top10 CS 研究生，MBA。我坚信 AI 是普通人变强的 “**外挂**”，所以创建了 “AI 信息 Gap” 这个公众号，专注于分享 AI 全维度知识，包括但不限于 **AI 科普**，**AI 工具测评**，**AI 效率提升**，**AI 行业洞察**。关注我，AI 之路不迷路，2024 我们一起变强。  

**语言理解**是对话的基础。当我们和 ChatGPT 这类 AI 工具对话时，大家有没有疑惑过，为什么 AI 模型能够理解我们所提的问题，所说的内容？

这一切的核心在于**自然语言处理**（NLP）和**深度学习**技术。LLM 模型，如 GPT 系列，能够通过复杂的神经网络架构来分析和理解文本，在输入序列中找到相关信息，并在生成响应时利用这些信息。当我们输入一个问题或陈述时，AI 模型会首先将文本分解成更小的单元（如单词或词组），然后利用预训练的语言模型来预测这些单元之间的关系和可能的下一步。预训练模型经过大量文本数据的训练，掌握了语言的结构、语法、语义以及各种上下文关系，从而能够理解并生成符合人类语言习惯的回答。

![](https://pic2.zhimg.com/v2-f659622b1e0e24d6357e4678c831920d_r.jpg)

在一众神经网络中，当下最靓的仔莫过于 **[Transformer](https://zhida.zhihu.com/search?content_id=244417806&content_type=Article&match_order=1&q=Transformer&zd_token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJ6aGlkYV9zZXJ2ZXIiLCJleHAiOjE3NjQwODU5OTIsInEiOiJUcmFuc2Zvcm1lciIsInpoaWRhX3NvdXJjZSI6ImVudGl0eSIsImNvbnRlbnRfaWQiOjI0NDQxNzgwNiwiY29udGVudF90eXBlIjoiQXJ0aWNsZSIsIm1hdGNoX29yZGVyIjoxLCJ6ZF90b2tlbiI6bnVsbH0.r-LMNQs9rzWXCHTev-3wmNypZU9CWMZpizYBn2wjQ3Y&zhida_source=entity) 架构**。

2017 年，一篇名为[《Attention Is All You Need》](https://zhida.zhihu.com/search?content_id=244417806&content_type=Article&match_order=1&q=%E3%80%8AAttention+Is+All+You+Need%E3%80%8B&zd_token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJ6aGlkYV9zZXJ2ZXIiLCJleHAiOjE3NjQwODU5OTIsInEiOiLjgIpBdHRlbnRpb24gSXMgQWxsIFlvdSBOZWVk44CLIiwiemhpZGFfc291cmNlIjoiZW50aXR5IiwiY29udGVudF9pZCI6MjQ0NDE3ODA2LCJjb250ZW50X3R5cGUiOiJBcnRpY2xlIiwibWF0Y2hfb3JkZXIiOjEsInpkX3Rva2VuIjpudWxsfQ.9dr3RD3T4inqU1PQVlPOs6_R00b4AobWbJoIRm-Kbbs&zhida_source=entity)的论文横空出世，并在接下来的几年内直至现在制霸了整个生成式 AI 领域。在这篇具有里程碑和突破性意义的论文中，8 名研究学者首次提出了 Transformer 这种神经网络架构，其独特之处在于完全基于**注意力机制**，摒弃了传统的循环和卷积操作。通过**[自注意力机制](https://zhida.zhihu.com/search?content_id=244417806&content_type=Article&match_order=1&q=%E8%87%AA%E6%B3%A8%E6%84%8F%E5%8A%9B%E6%9C%BA%E5%88%B6&zd_token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJ6aGlkYV9zZXJ2ZXIiLCJleHAiOjE3NjQwODU5OTIsInEiOiLoh6rms6jmhI_lipvmnLrliLYiLCJ6aGlkYV9zb3VyY2UiOiJlbnRpdHkiLCJjb250ZW50X2lkIjoyNDQ0MTc4MDYsImNvbnRlbnRfdHlwZSI6IkFydGljbGUiLCJtYXRjaF9vcmRlciI6MSwiemRfdG9rZW4iOm51bGx9.XbXK_N3SN1Kh55r1_2haf4XZHPrlq4VoOf0Kn5zkQ2A&zhida_source=entity)**（self-attention），Transformer 能够有效捕捉输入序列中的长距离依赖关系，使得模型在处理长文本时更为高效和准确。**[多头注意力机制](https://zhida.zhihu.com/search?content_id=244417806&content_type=Article&match_order=1&q=%E5%A4%9A%E5%A4%B4%E6%B3%A8%E6%84%8F%E5%8A%9B%E6%9C%BA%E5%88%B6&zd_token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJ6aGlkYV9zZXJ2ZXIiLCJleHAiOjE3NjQwODU5OTIsInEiOiLlpJrlpLTms6jmhI_lipvmnLrliLYiLCJ6aGlkYV9zb3VyY2UiOiJlbnRpdHkiLCJjb250ZW50X2lkIjoyNDQ0MTc4MDYsImNvbnRlbnRfdHlwZSI6IkFydGljbGUiLCJtYXRjaF9vcmRlciI6MSwiemRfdG9rZW4iOm51bGx9.sodoEyMVOD5rtl4NlaMUg4eS7gu1T7v-b04Up30UX0w&zhida_source=entity)**（multi-head attention）则进一步增强了模型的表达能力，使其能够同时关注输入序列中的不同部分，捕捉更加复杂的语义关系。

![](https://pic2.zhimg.com/v2-a1d54e1bd5b3b30027422f81082d3f39_r.jpg)

无论是机器翻译、文本生成，还是问答系统，Transformer 都显著提升了任务的效果和效率。引领了生成式 AI 浪潮，大家所熟知的 **GPT**，全称 **Generative Pre-trained Transformer**，就是基于 Transformer 架构开发的。这也是 GPT 的命名由来。GPT 系列模型通过预训练和微调提高了模型在 NLP 任务中的性能。预训练阶段，模型在海量文本数据上进行训练，学习语言的广泛知识和复杂模式。随后，通过微调，模型在特定任务上进一步优化，以达到更好的效果。

今天，就让我们把目光聚焦在这篇纲领之作——《Attention Is All You Need》。

## Abstract 摘要

《Attention Is All You Need》研究论文由 Ashish Vaswani、Noam Shazeer、Niki Parmar、Jakob Uszkoreit、Llion Jones、Aidan N. Gomez、Lukasz Kaiser 和 Illia Polosukhin 于 2017 年发表。这篇论文介绍了一种全新的神经网络架构——**Transformer**，它完全基于注意力机制，摒弃了传统的[循环神经网络](https://zhida.zhihu.com/search?content_id=244417806&content_type=Article&match_order=1&q=%E5%BE%AA%E7%8E%AF%E7%A5%9E%E7%BB%8F%E7%BD%91%E7%BB%9C&zd_token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJ6aGlkYV9zZXJ2ZXIiLCJleHAiOjE3NjQwODU5OTIsInEiOiLlvqrnjq_npZ7nu4_nvZHnu5wiLCJ6aGlkYV9zb3VyY2UiOiJlbnRpdHkiLCJjb250ZW50X2lkIjoyNDQ0MTc4MDYsImNvbnRlbnRfdHlwZSI6IkFydGljbGUiLCJtYXRjaF9vcmRlciI6MSwiemRfdG9rZW4iOm51bGx9.aXvgqaimUqkN4Y5wXTAbWgd-vXyPiCr95cRstgoe3Y0&zhida_source=entity)（RNN）和[卷积神经网络](https://zhida.zhihu.com/search?content_id=244417806&content_type=Article&match_order=1&q=%E5%8D%B7%E7%A7%AF%E7%A5%9E%E7%BB%8F%E7%BD%91%E7%BB%9C&zd_token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJ6aGlkYV9zZXJ2ZXIiLCJleHAiOjE3NjQwODU5OTIsInEiOiLljbfnp6_npZ7nu4_nvZHnu5wiLCJ6aGlkYV9zb3VyY2UiOiJlbnRpdHkiLCJjb250ZW50X2lkIjoyNDQ0MTc4MDYsImNvbnRlbnRfdHlwZSI6IkFydGljbGUiLCJtYXRjaF9vcmRlciI6MSwiemRfdG9rZW4iOm51bGx9.zLRDvPZmcjZVIDTU5Rqy6eqfNBFfaKm-Qdbn2TEgonE&zhida_source=entity)（CNN）中的循环和卷积操作。

当前，主流的序列转换模型（Sequence Transduction Model）大多建立在复杂的**循环神经网络**（RNN）或**卷积神经网络**（CNN）之上，这些模型通常配备有**编码器**（encoder）和**解码器**（decoder）。其中表现最出色的模型还会利用注意力机制来加强编码器与解码器之间的联系。我们提出了一种全新的网络架构——Transformer，它完全基于**注意力机制**，彻底摆脱了对循环和卷积操作的依赖。通过在两项机器翻译任务上的实验，我们发现这种模型不仅在翻译质量上更胜一筹，而且在并行处理能力和训练效率上都有显著提升。在 [WMT 2014](https://zhida.zhihu.com/search?content_id=244417806&content_type=Article&match_order=1&q=WMT+2014&zd_token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJ6aGlkYV9zZXJ2ZXIiLCJleHAiOjE3NjQwODU5OTIsInEiOiJXTVQgMjAxNCIsInpoaWRhX3NvdXJjZSI6ImVudGl0eSIsImNvbnRlbnRfaWQiOjI0NDQxNzgwNiwiY29udGVudF90eXBlIjoiQXJ0aWNsZSIsIm1hdGNoX29yZGVyIjoxLCJ6ZF90b2tlbiI6bnVsbH0.ncPFuEc0NsiM1H_u1Akkd2mNUwpSSdFcqZOQ4QRfcYU&zhida_source=entity) 英语到德语的翻译任务中，我们的模型 [BLEU](https://zhida.zhihu.com/search?content_id=244417806&content_type=Article&match_order=1&q=BLEU&zd_token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJ6aGlkYV9zZXJ2ZXIiLCJleHAiOjE3NjQwODU5OTIsInEiOiJCTEVVIiwiemhpZGFfc291cmNlIjoiZW50aXR5IiwiY29udGVudF9pZCI6MjQ0NDE3ODA2LCJjb250ZW50X3R5cGUiOiJBcnRpY2xlIiwibWF0Y2hfb3JkZXIiOjEsInpkX3Rva2VuIjpudWxsfQ.FMbwlJ59h0o5UX5CX1jujPTQ6aSPi1H_Hqyi3PsI3Z8&zhida_source=entity) 得分达到了 28.4，相较于之前的最佳成绩，包括那些集成了多个模型的结果，我们的得分提高了 2 个点（BLEU）。在英语到法语的翻译任务中，我们的模型仅用 3.5 天和 8 个 GPU 就训练出了达到 41.8 BLEU 得分的单一模型，这一成本远低于文献中报道的最佳模型。此外，我们还证明了 Transformer 模型不仅在大规模数据集上表现出色，即使在数据有限的情况下，也能成功应用于英语句法分析任务，显示出了极强的泛化能力。

### 序列转换模型（Sequence Transduction Model）

**序列转换模型**是一类用于将一种序列数据转换为另一种序列数据的神经网络模型。这类模型的关键在于能够理解和生成序列数据，并在输入和输出序列之间建立有效的映射关系。通过这种映射关系，序列转换模型能够在输入文本和目标文本之间找到语义和语法上的对应，从而实现高质量的翻译或生成任务。因此，序列转换模型在自然语言处理（NLP）任务中广泛应用，如机器翻译、语音识别和文本生成等。

典型的序列转换模型通常包括一个**编码器**（encoder）和一个**解码器**（decoder）。编码器负责将输入序列编码成一个固定长度的隐状态表示，而解码器则利用这个隐状态表示生成目标序列。在这些模型中，循环神经网络（RNN）和卷积神经网络（CNN）是从前最常见的架构。然而，2017 年以来，基于注意力机制的 **Transformer 架构**（即该论文介绍的架构）因其并行计算能力和处理长距离依赖关系的优势，成为序列转换任务中的新宠。

### 循环神经网络（RNN）

**循环神经网络**（Recurrent Neural Network，简称 RNN）是一种用于处理序列数据的神经网络架构。与传统的前馈神经网络不同，RNN 具有环形连接，使得信息能够在网络中循环流动。这种结构使 RNN 能够保留先前输入的信息，并将其用于当前的输出计算，因此特别适合处理时间序列数据或自然语言处理任务，如语音识别、机器翻译和文本生成。

RNN 的关键特性是它的**隐状态**（hidden state），这是一个包含网络在任意时间步的信息的向量。通过隐状态，RNN 可以记住前面的输入，从而在处理当前输入时考虑到上下文。然而，传统的 RNN 在处理长序列时会遇到**梯度消失和梯度爆炸**问题，这限制了其记忆长距离依赖的能力。

### 卷积神经网络（CNN）

**卷积神经网络**（Convolutional Neural Network，简称 CNN）是一种专门用于处理具有网格状拓扑结构数据的神经网络架构，如图像和视频。CNN 通过引入卷积层和池化层，能够有效地捕捉空间结构中的局部特征，特别适合处理二维图像数据。

CNN 的层次结构使其能够从低级特征到高级语义特征逐步提取信息，这种逐层提取和组合特征的方式，使得 CNN 在计算机视觉任务中取得了显著成功。随着深度学习的发展，CNN 的变种如 ResNet、Inception 等也被广泛应用于各种图像处理任务中。

## Introduction 引言

循环神经网络（RNN），特别是长短期记忆网络（LSTM）和门控循环单元（GRU），已经在序列建模和转换任务，例如语言建模和机器翻译中，确立了自己作为尖端技术的地位。众多研究者不断扩展循环语言模型和编码器 - 解码器架构的能力。

这些循环模型通过沿着序列的符号位置进行计算，生成一系列隐藏状态。每个隐藏状态 (h_t) 都是基于前一个状态 ( h_{t-1} ) 和当前位置 ( t ) 的输入来计算的。**这种计算的顺序特性限制了在训练样本中的并行化能力，随着序列的增长，这种限制变得尤为明显，因为内存的限制会阻碍跨多个样本的批处理**。尽管最近的技术进步，如分解技巧和条件计算，已经在计算效率上取得了显著提升，并且在某些情况下还提高了模型的性能，但顺序计算的基本限制依然存在。

**注意力机制**已经成为序列建模和转换模型中不可或缺的一部分，它允许模型在不考虑输入或输出序列中元素间距离的情况下，建立依赖关系。然而，除了少数例外，这些注意力机制通常与循环网络结合使用。

在本研究中，我们提出了一种名为 Transformer 的全新模型架构，它完全摒弃了循环结构，转而完全依赖于注意力机制来捕捉输入和输出之间的全局依赖性。这种架构极大地提高了并行化的能力，并且在仅经过八个 P100 GPU 十二小时的训练后，就能在翻译质量上达到前所未有的高水平。

## Background 背景

减少顺序计算的需求同样催生了扩展神经 GPU（Extended Neural GPU）、ByteNet 和 ConvS2S 等模型的发展。这些模型都采用卷积神经网络作为基础构件，能够并行地对所有输入和输出位置进行隐藏表示的计算。然而，在这些模型中，关联任意两个输入或输出位置的信号所需的操作数量会随着它们之间的距离增加而增加——ConvS2S 是线性增长，而 ByteNet 是按对数增长。这种特性使得学习**长距离依赖关系**变得更加具有挑战性。相比之下，Transformer 模型将这种操作数量简化为一个常数，尽管平均注意力权重可能会降低有效分辨率，我们通过多头注意力机制来克服这一问题。

**自注意力机制**（Self-attention），有时也称为**内部注意力机制**（Intra-attention），它能够将序列中不同位置的信息联系起来，以计算出序列的表示。这种机制已经在阅读理解、抽象摘要、文本蕴含以及学习与任务无关的句子表示等多种任务中显示出了卓越的性能。

端到端记忆网络，它们基于递归注意力机制而非依赖于序列对齐的循环机制，已在简单的语言问答和语言建模任务中展现出良好的效果。

Transformer 是首个完全基于自注意力机制来计算输入和输出表示的模型，它不依赖于传统的循环神经网络或卷积网络来进行序列对齐。在接下来的章节中，我们将详细介绍 Transformer 的结构，解释自注意力机制的原理，并讨论它与其他模型相比的优势。

## Model Architecture 模型架构

在神经序列转换领域，表现卓越的模型普遍采用**编码器 - 解码器**架构。编码器负责将输入的一系列符号（如 x1, x2, ..., xn）转换成一系列连续的向量表示 z（即 z1, z2, ..., zn）。一旦得到这一系列向量，解码器便基于它们逐个生成输出序列的符号（如 y1, y2, ..., ym）。每一步生成过程中，模型展现出自回归特性，即在生成新的符号时，会将之前生成的符号序列作为输入的一部分。

Transformer 模型正是基于这样的架构，它通过叠加自注意力机制和逐点全连接的层来构建编码器和解码器，这种设计在图 1 中以左右两半部分的形式展示。这种架构不仅优化了模型的运算效率，也为处理复杂的序列转换任务提供了强大的支持。

![](https://pic4.zhimg.com/v2-c7251a901278017cc995d1908391fca7_r.jpg)

### 编码器与解码器的多层结构

**编码器**：我们的编码器由 6 个相同的层堆叠而成。每层包含两个主要组件：首先是多头自注意力机制，其次是一个逐点相连的全连接前馈网络。在每个子层之后，我们实施了残差连接，并紧接着进行层归一化，公式表示为 LayerNorm(x + Sublayer(x))，其中 Sublayer(x) 代表子层的输出。为了保持残差连接的一致性，模型中所有的子层以及嵌入层都产生维度为 512 的输出向量。

**解码器**：解码器的结构与编码器类似，也是由 6 个相同层的堆叠构成。与编码器不同，解码器在每个层中增加了第三个子层，这个子层专门对编码器的输出进行多头自注意力处理。和编码器一样，我们在解码器的每个子层之后也采用了残差连接和层归一化。此外，我们对解码器的自注意力子层进行了特殊设计，以防止在预测时关注到当前及之后的位置。通过这种掩码处理，结合输出嵌入的偏移机制，我们确保了在预测序列中任意位置 i 的符号时，只能依赖于位置 i 之前已经生成的输出。这样的设计保证了解码过程的自回归特性。

### 注意力机制

注意力机制本质上是一种将查询（query）与一组键值对（key-value pairs）映射成输出的过程。在这个过程中，查询、键、值以及输出都是向量形式。输出是值的加权和，权重由查询与相应键的相容性决定，通过一个特定的函数计算得出。

![](https://pic2.zhimg.com/v2-de06b7306fd70f37e832a3a088ca6471_r.jpg)

【**进一步理解**】：注意力机制可以帮助神经网络专注于输入数据的相关部分，类似于人类在处理信息时会优先关注重要信息。

1.  **查询、键和值**：在注意力机制中，输入数据被分成三部分：查询（query）、键（key）和值（value）。这些都是向量：  
    

*   **查询（Q）**：表示你当前关注的点或问题。
*   **键（K）**：表示输入数据的不同特征。
*   **值（V）**：表示与键相关的实际信息或答案。

1.  **计算相关性**：首先，计算查询与所有键的相似度（相关性），这可以通过点积运算完成。相似度越高，表示这个键与查询越相关。  
    
2.  **加权求和**：将这些相似度通过 softmax 函数转换为概率权重，然后用这些权重对所有值进行加权求和。这样，模型输出一个综合了所有相关值的信息，突出重要信息而忽略不相关信息。  
    

可以把注意力机制想象成一个学生在阅读一本书。学生在读每一页时，不会平均分配注意力，而是会根据当前问题（查询）来重点关注相关的段落或句子（键和值）。例如，如果学生在回答历史问题时，他们会特别注意书中有关历史事件的部分，而忽略其他不相关的内容。

注意力机制通过计算查询与键的相似度，动态地调整对输入数据不同部分的关注程度，使得模型能够更有效地处理复杂的任务，特别是在需要理解和生成自然语言的情况下。

### 缩放点积注意力（Scaled Dot-Product Attention）

我们采用的注意力机制称为 “缩放点积注意力”。它涉及将查询和键的维度设为 (d_k)，将值的维度设为 (d_v)。计算查询与所有键的点积，然后除以 (\sqrt{d_k})，以此来缩放结果，并通过 softmax 函数获取每个值的权重。

在实践中，我们会对一组查询执行注意力函数，这些查询被组织成一个矩阵 Q。相应的，键和值则分别组织成矩阵 K 和 V，然后计算输出矩阵。

注意力函数有多种形式，包括加性注意力和点积（乘性）注意力。点积注意力与我们的机制相似，只是引入了缩放因子。加性注意力则使用一个带有单隐藏层的前馈网络来计算兼容性。尽管两者在理论上的复杂度相似，但点积注意力在实际应用中更为迅速和节省资源，因为它可以利用高效的矩阵乘法优化。

对于较小的 (d_k) 值，两种机制表现相近。但当 (d_k) 较大时，未缩放的点积注意力性能不如加性注意力。因此，我们通过引入缩放来解决这个问题。

### 多头注意力（Multi-Head Attention）

我们发现，相比于使用单一维度 (d_{model}) 的键、值和查询执行单一注意力函数，将查询、键和值分别线性投影 h 次到 (d_k)、(d_k) 和(d_v)的维度，然后在每个投影版本上并行执行注意力函数，能更有效地捕捉信息。这些并行得到的输出值会被拼接起来，并通过另一个线性层进行整合，形成最终的输出。

多头注意力使模型能够同时关注不同位置的多种特征信息。相比之下，单一注意力头往往会平均化这些信息，从而限制了模型的表达能力。

在我们的模型中，使用了 8 个并行的注意力头。由于每个头的维度较小，总体计算成本与单一头的全维度注意力相当。

### 注意力机制在 Transformer 模型中的应用

Transformer 模型通过以下三种方式应用多头注意力：

*   **编码器 - 解码器注意力层**：在这层中，查询来自前一个解码器层，而记忆键和值则来自编码器的输出。这允许解码器中的每个位置都能关注输入序列的所有位置。
*   **编码器自注意力层**：在这层中，所有的键、值和查询都源自编码器前一层的同一位置。编码器的每个位置都能关注到前一层的所有位置。
*   **解码器自注意力层**：这层允许解码器中的每个位置只关注到该位置之前的所有位置，以保持自回归的特性。通过在缩放点积注意力中引入掩码机制，我们能够实现这一点，掩码会将 softmax 操作中非法连接的输入值设为负无穷，从而排除这些连接。

### 逐位置前馈网络

在我们的编码器和解码器的每层中，除了注意力机制外，还融入了一个全连接的前馈网络。这个网络独立地对序列中的每个位置应用相同的操作，由两个线性变换组成，并通过一个 ReLU 激活函数连接。

尽管每个位置的线性变换操作是一致的，但每一层都使用独特的参数集。可以想象这如同两个核心尺寸为 1 的卷积操作。这个网络的输入和输出都是 512 维的向量，而中间层则是 2048 维的。

### 嵌入和 Softmax

与大多数序列转换模型一样，我们采用嵌入技术，将输入和输出的符号转换成 512 维的向量形式。此外，我们利用标准的线性变换和 softmax 函数，将解码器的输出转换为预测下一个符号出现的概率。在我们的模型里，嵌入层和 softmax 之前的线性变换共享同一个权重矩阵。在嵌入过程中，我们对权重进行了 (\sqrt{512}) 的缩放。

### 位置编码

由于我们的模型不包含递归或卷积结构，为了让模型能够识别序列中元素的顺序，我们需要引入一种方法来表示每个元素在序列中的位置信息。为此，在编码器和解码器的输入嵌入中，我们添加了位置编码。这些位置编码与嵌入向量维度相同，使得它们能够直接相加。存在多种位置编码的方法，可以是预先设定的，也可以是通过学习获得的。

在本研究中，我们采用了不同频率的正弦和余弦函数作为位置编码，这使得模型能够轻松捕捉序列中元素的相对位置。选择这种函数是基于这样的假设：它将简化模型学习基于相对位置的注意力机制，因为对于任何给定的偏移量，新位置的位置编码可以看作是原位置编码的线性变换。

我们也尝试了使用学习得到的位置嵌入，结果表明两种方法的效果几乎一样。我们选择正弦函数的原因是，它可能使模型能够适应比训练时遇到的序列更长的序列。

## 为什么选择自注意力

在这一部分，我们将自注意力层与通常用于将一个变长序列的符号表示（例如 x1, ..., xn）映射到等长序列（例如 z1, ..., zn）的循环和卷积层进行比较。我们考虑三个理想属性来解释我们为何使用自注意力。

首先是每层的**总计算复杂度**。其次是可以**并行化的计算量**，通过所需的最小序列操作数量来衡量。

第三个是网络中**长距离依赖的路径长度**。学习长距离依赖是许多序列转换任务中的关键挑战。影响学习这种依赖能力的一个关键因素是前后向信号在网络中必须穿越的路径长度。输入和输出序列中任意组合位置之间的路径越短，学习长距离依赖就越容易。因此，我们还比较了由不同层类型组成的网络中任意两个输入和输出位置之间的最大路径长度。

如表 1 所示，自注意力层通过恒定数量的序列执行操作连接所有位置，而循环层需要 O(n) 序列操作。在计算复杂度方面，当序列长度 n 小于表示维度 d 时，自注意力层比循环层更快，这在使用最先进机器翻译模型的句子表示中是最常见的情况，例如词片和字节对表示。为了提高涉及非常长序列任务的计算性能，自注意力可以被限制为只考虑以相应输出位置为中心的输入序列中的 r 大小邻域。这将使最大路径长度增加到 O(n/r)。我们计划在未来的工作中进一步探索这种方法。

![](https://pic3.zhimg.com/v2-cf296f1ab457c2733d40d9147e78933c_r.jpg)

具有核宽 k<n 的单个卷积层不会连接所有的输入和输出位置对。在连续核的情况下，这需要 O(n/k) 个卷积层堆叠，或者在扩张卷积的情况下需要 O(log k (n))，从而增加了网络中任意两个位置之间的最长路径长度。卷积层通常比循环层更昂贵，因子为 k。然而，可分离卷积大大减少了复杂度，到 O(k·n·d + n·d^2)。即使 k=n，可分离卷积的复杂度也等于自注意力层和逐点前馈层的组合，这是我们模型中采用的方法。

作为额外的好处，自注意力可能会产生更易于解释的模型。我们检查了我们模型中的注意力分布，并在附录中呈现和讨论了示例。不仅单个注意力头清楚地学会了执行不同的任务，而且许多头似乎表现出与句子的句法和语义结构相关的行为。

## Training 训练

**训练数据与批处理策略**：我们选择了广泛认可的 WMT 2014 英德翻译数据集作为训练基础，它包含了 450 万句对。这些句子通过字节对编码技术被转换成了大约 37000 个共享词汇的序列。在处理更大规模的英法翻译任务时，我们采用了包含 3600 万句对的 WMT 2014 英法数据集，并将其词汇分解为 32000 个词片单位。训练时，我们根据句子的近似长度将它们分批处理，确保每个批次包含约 25000 个源语言和目标语言的词汇。

**硬件配置与训练安排**：训练过程是在一台装备了 8 个 NVIDIA P100 GPU 的计算机上完成的。基础模型的训练速度大约是每步 0.4 秒，累计训练了 100,000 步，耗时大约 12 小时。对于更大型的模型，每步训练需要 1 秒，总共训练了 300,000 步，花费了大约 3.5 天的时间。

**优化器与正则化技术**：我们选用了 Adam 优化器来调整模型的权重，并根据一个特定的公式在训练过程中动态调整学习速率。为了增强模型的泛化能力和避免过拟合，我们实施了三种正则化策略：残差 Dropout、嵌入和位置编码的 Dropout，以及标签平滑。标签平滑技术通过在训练中引入轻微的不确定性，帮助模型在预测时更加谨慎，这虽然可能影响困惑度，但最终提升了模型的准确度和 BLEU 得分。这些方法共同确保了我们的模型在翻译任务上的性能和稳健性。

## Results 结果

**机器翻译领域的突破**：在 WMT 2014 英德翻译任务上，我们的 Transformer 大型模型以 28.4 的 BLEU 分数，超越了之前所有模型，包括集成模型，提高了 2.0 BLEU 的显著幅度。这一成绩是在 8 个 P100 GPU 上经过 3.5 天的密集训练后实现的。我们的基础模型同样表现出色，以更低的训练成本超越了之前发布的所有模型和集成模型。在英法翻译任务上，我们的模型以 41.0 的 BLEU 分数再次刷新记录，其训练成本仅为之前最先进模型的一小部分。无论是基础模型还是大型模型，我们都采用了多检查点平均和束搜索技术来进一步提升翻译质量和效率。

![](https://pic1.zhimg.com/v2-51b3fc09dc4a3f5b721ef876bd000b6a_r.jpg)

**模型变体的深入探究**：为了深入理解 Transformer 模型中不同组件的作用，我们在开发集上对模型进行了多种变体测试。测试结果揭示了注意力头数对性能的影响：单一注意力头的性能低于最佳设置，而过多的头数同样会降低翻译质量。我们还发现，减小注意力键的维度会损害模型性能，这表明设计更复杂的兼容性函数可能是有益的。更大的模型通常能带来更好的结果，而 Dropout 技术在防止过拟合方面起到了关键作用。此外，将正弦位置编码替换为学习的位置嵌入后，模型的性能几乎没有变化，显示出我们的模型在不同位置编码方案下都能保持稳定。

![](https://pic2.zhimg.com/v2-3867c0e622ac86e64a8144b1e5469b5f_r.jpg)

**英语成分句法分析的挑战**：Transformer 在英语成分句法分析任务上也展现了其强大的能力。尽管该任务具有挑战性——输出结构严格受限且通常比输入长得多——我们的模型在 Penn Treebank 的华尔街日报部分上的训练结果显示，无需特定任务调整，模型就能取得优异的性能，仅次于递归神经网络语法模型。与 RNN 序列到序列模型相比，Transformer 即使仅在较小规模的训练集上，也能实现超越 BerkeleyParser 的成果。这一发现进一步证明了 Transformer 模型不仅在机器翻译上，在其他自然语言处理任务上同样具有巨大的应用潜力。

![](https://pic1.zhimg.com/v2-d161be219d2d4b1ef6892870b6e0cefa_r.jpg)

## Conclusion 结论

在本研究中，我们提出了 **Transformer 模型**，这是一种开创性的**序列转换模型**，它完全依托于注意力机制，用多头自注意力取代了传统编码器 - 解码器架构中常见的循环层。这一创新使我们在翻译任务中实现了前所未有的训练速度提升。

在 WMT 2014 英语到德语和英语到法语的翻译任务上，Transformer 模型均达到了业界领先的水平，尤其在英语到德语的任务中，我们的最佳模型超越了之前所有报道的集成模型的成绩，这标志着我们模型的卓越性能。

我们对**基于注意力的模型**的未来充满期待，并计划将其应用于更多任务。我们期望将 Transformer 模型扩展到更广泛的领域，包括但不限于处理图像、音频和视频等非文本输入和输出的问题。同时，我们正着眼于研究局部的、受限的注意力机制，这将使我们能够更高效地处理大规模的输入和输出数据。

此外，**探索减少生成顺序性的方法**也是我们研究的重点之一。我们相信，通过持续的创新和优化，Transformer 模型将在未来开辟更多可能性，为自然语言处理和其他领域的任务提供更加强大和灵活的解决方案。

## 结语

我们在现实世界中是如何处理如此纷繁复杂的信息流的？**注意力**。我们的大脑通过注意力这一神奇的机制来筛选、聚焦，以理解和应对周围的环境。

AI 也是如此。Attention Is All You Need。

## 精选推荐

[使用 GPT-4o 模型的 5 种方法，总有一种适合你！](https://link.zhihu.com/?target=https%3A//mp.weixin.qq.com/s/gKfBSQGKVddW6sC3vPktcw)[关于最新模型 GPT-4o 的 14 条总结，都在这里！](https://link.zhihu.com/?target=https%3A//mp.weixin.qq.com/s/DGkx4jecKB1nQX6a3T262Q)[免费的 GPT4 终于要来了！OpenAI 直播发布会详细解读！](https://link.zhihu.com/?target=https%3A//mp.weixin.qq.com/s/R9t0XnDp1ki1_lV8bDj1VA)[春日暖阳，何不来看一场 OpenAI 的发布会](https://link.zhihu.com/?target=https%3A//mp.weixin.qq.com/s/-tLl9EAAo_MV6bVtegZ39A)

都读到这里了，点个赞鼓励一下吧，小手一赞，年薪百万！ 。关注我，AI 之路不迷路，原创技术文章第一时间推送 。