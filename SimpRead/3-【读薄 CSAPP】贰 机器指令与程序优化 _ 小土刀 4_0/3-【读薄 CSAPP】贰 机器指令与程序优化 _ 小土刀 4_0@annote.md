---
title: "【读薄 CSAPP】贰 机器指令与程序优化 | 小土刀 4.0"
alias: 
  - "【读薄 CSAPP】贰 机器指令与程序优化 | 小土刀 4.0"
created-date: 2026-04-27T22:24:05+0800
type: Simpread
banner: "https://www.wdxtub.com/_next/image?url=%2Fstatic%2Fimages%2Fcsapp%2F14531672465886.jpg&w=1920&q=75 "
banner_icon: 🔖
tag: 
idx: 3
---

# 【读薄 CSAPP】贰 机器指令与程序优化 | 小土刀 4.0

> [!example]- [🧷内部链接](<http://localhost:7026/unread/3>) [🌐外部链接](<>)    
> URI:: [🧷](<http://localhost:7026/unread/3>) [🌐](<>) 
> intURI:: [🧷内部链接](<http://localhost:7026/reading/3>)

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
>  **Description**:: 计算机能读懂的只有零和一，而我们用汇编去和计算机『感同身受』。
%%

> [!md] Metadata  
> **标题**:: [【读薄 CSAPP】贰 机器指令与程序优化 | 小土刀 4.0](https://www.wdxtub.com/blog/csapp/thin-csapp-2)  
> **日期**:: [[2026-04-27]]  

