---
title: "常学常新：《Attention Is All You Need》万字解读！"
alias: 
  - "常学常新：《Attention Is All You Need》万字解读！"
created-date: 2025-11-23T23:55:29+0800
type: Simpread
banner: "https://pic1.zhimg.com/v2-434782544b0e3c9db79aa4879d2f8064_720w.jpg?source=172ae18b "
banner_icon: 🔖
tag: 
idx: 0
---

# 常学常新：《Attention Is All You Need》万字解读！

> [!example]- [🧷内部链接](<http://localhost:7026/unread/0>) [🌐外部链接](<>)    
> URI:: [🧷](<http://localhost:7026/unread/0>) [🌐](<>) 
> intURI:: [🧷内部链接](<http://localhost:7026/reading/0>)

%%
> [!example]+ **Comments**  
> ```dataview
> TABLE 
>     WITHOUT ID
>     link(Source, dateformat(date(Source), "yyyy-MM-dd")) as Date___, 
>     regexreplace(rows.Comments,"^@@\[\[.+?\]\]\s","") as "Comments"
> FROM "journals"
> WHERE  contains(cmnt, this.file.name)
> FLATTEN cmnt as Comments
> WHERE contains(Comments, this.file.name)
> GROUP BY file.link as Source
> SORT rows.file.day desc
> ```
>  **Description**:: 大家好，我是木易，一个持续关注AI领域的互联网技术产品经理，国内Top2本科，美国Top10 CS研究生，MBA。我坚信AI是普通人变强的“外挂”，所以创建了“AI信息Gap”这个公众号，专注于分享AI全维度知识，包括但不限…
%%

> [!md] Metadata  
> **标题**:: [常学常新：《Attention Is All You Need》万字解读！](https://zhuanlan.zhihu.com/p/703292893)  
> **日期**:: [[2025-11-23]]  

## Annotations


> [!srhl6] [[SR0@常学常新：《Attention Is All You Need》万字解读！|📄]] <mark style="background-color: #ffb7da">Highlights</mark> [🧷](<http://localhost:7026/unread/0#id=1763913326826>) [🌐](<#id=1763913326826>)   
> 通过**[自注意力机制](https://zhida.zhihu.com/search?content_id=244417806&content_type=Article&match_order=1&q=%E8%87%AA%E6%B3%A8%E6%84%8F%E5%8A%9B%E6%9C%BA%E5%88%B6&zd_token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJ6aGlkYV9zZXJ2ZXIiLCJleHAiOjE3NjQwODU5OTIsInEiOiLoh6rms6jmhI_lipvmnLrliLYiLCJ6aGlkYV9zb3VyY2UiOiJlbnRpdHkiLCJjb250ZW50X2lkIjoyNDQ0MTc4MDYsImNvbnRlbnRfdHlwZSI6IkFydGljbGUiLCJtYXRjaF9vcmRlciI6MSwiemRfdG9rZW4iOm51bGx9.XbXK_N3SN1Kh55r1_2haf4XZHPrlq4VoOf0Kn5zkQ2A&zhida_source=entity)**（self-attention），Transformer 能够有效捕捉输入序列中的长距离依赖关系，使得模型在处理长文本时更为高效和准确。**[多头注意力机制](https://zhida.zhihu.com/search?content_id=244417806&content_type=Article&match_order=1&q=%E5%A4%9A%E5%A4%B4%E6%B3%A8%E6%84%8F%E5%8A%9B%E6%9C%BA%E5%88%B6&zd_token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJ6aGlkYV9zZXJ2ZXIiLCJleHAiOjE3NjQwODU5OTIsInEiOiLlpJrlpLTms6jmhI_lipvmnLrliLYiLCJ6aGlkYV9zb3VyY2UiOiJlbnRpdHkiLCJjb250ZW50X2lkIjoyNDQ0MTc4MDYsImNvbnRlbnRfdHlwZSI6IkFydGljbGUiLCJtYXRjaF9vcmRlciI6MSwiemRfdG9rZW4iOm51bGx9.sodoEyMVOD5rtl4NlaMUg4eS7gu1T7v-b04Up30UX0w&zhida_source=entity)**（multi-head attention）则进一步增强了模型的表达能力，使其能够同时关注输入序列中的不同部分，捕捉更加复杂的语义关系。
> ^sran-1763913326826


