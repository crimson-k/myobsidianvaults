---
type: "literature-note"
title: "USP: A Unified Sequence Parallelism Approach for Long Context Generative AI"
aliases: ["USP: A Unified Sequence Parallelism Approach for Long Context Generative AI"]
zotero_keys: ["4FTNYAYH"]
year: null
authors: ["Jiarui Fang", "Shangchun Zhao"]
venue: ""
venue_field: null
doi: ""
url: ""
collections: ["01 Foundations"]
source_tags: []
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# USP: A Unified Sequence Parallelism Approach for Long Context Generative AI

[Zotero 条目 4FTNYAYH](zotero://select/library/items/4FTNYAYH)

## 主题与知识联系

- [[Zotero Knowledge/Topics/01 Foundations/索引|01 Foundations]]

## 原始摘要

Sequence parallelism (SP), which divides the sequence dimension of input tensors across multiple computational devices, is becoming key to unlocking the longcontext capabilities of generative AI models. This paper investigates the state-ofthe-art SP approaches, i.e. DeepSpeed-Ulysses and Ring-Attention, and proposes a unified SP approach, which is more robust to transformer model architectures and network hardware topology. This paper compares the communication and memory cost of SP and existing parallelism, including data/tensor/zero/pipeline parallelism, and discusses the best practices for designing hybrid 4D parallelism involving SP. We achieved 47% MFU on two 8xA800 nodes using SP for the LLAMA3-8B model training using sequence length 208K. Our code is publicly available at https://github.com/feifeibear/long-context-attention.

## 附件与批注

### PDF

[打开 PDF](zotero://open-pdf/library/items/UUWPFZK7)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
