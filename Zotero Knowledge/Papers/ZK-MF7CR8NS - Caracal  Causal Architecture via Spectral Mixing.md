---
type: "literature-note"
title: "Caracal: Causal Architecture via Spectral Mixing"
aliases: ["Caracal: Causal Architecture via Spectral Mixing"]
zotero_keys: ["MF7CR8NS"]
year: 2026
authors: ["Bingzheng Gan", "Tianyi Zhang", "Yusu Li", "Jing Huang", "Wei Shi", "Yangkai Ding", "Tao Yu"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/ARXIV.2605.00292"
url: "https://arxiv.org/abs/2605.00292"
collections: ["01 Foundations"]
source_tags: ["Artificial Intelligence (cs.AI)", "FOS: Computer and information sciences", "Machine Learning (cs.LG)"]
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# Caracal: Causal Architecture via Spectral Mixing

[Zotero 条目 MF7CR8NS](zotero://select/library/items/MF7CR8NS)

[DOI 原文](https://doi.org/10.48550/arxiv.2605.00292)

[来源网页](https://arxiv.org/abs/2605.00292)

## 主题与知识联系

- [[Zotero Knowledge/Topics/01 Foundations/索引|01 Foundations]]

## 原始摘要

The scalability of Large Language Models to long sequences is hindered by the quadratic cost of attention and the limitations of positional encodings. To address these, we introduce Caracal, a novel architecture that replaces attention with a parameter-efficient, O(L log L) Multi-Head Fourier (MHF) module. Our contributions are threefold: (1) We leverage the Fast Fourier Transform (FFT) for sequence mixing, inherently addressing both bottlenecks mentioned above. (2) We apply a frequency-domain causal masking technique that enforces autoregressive capabilities via asymmetric padding and truncation, overcoming a critical barrier for Fourier-based generative models. (3) Unlike efficient models relying on hardware-specific implementations (e.g., Mamba), we uses standard library operators. This ensures robust portability, eliminating common deployment barriers. Evaluations demonstrate that Caracal performs competitively with Transformer and SSM baselines, offering a scalable and simple pathway for efficient long-sequence modeling. Code is available in Appendix E.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Other

[在 Zotero 查看](zotero://select/library/items/KJUQT8DJ)

## Other
Accepted by ICML 2026

## 附件与批注

### PDF

[打开 PDF](zotero://open-pdf/library/items/CQESW9G4)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
