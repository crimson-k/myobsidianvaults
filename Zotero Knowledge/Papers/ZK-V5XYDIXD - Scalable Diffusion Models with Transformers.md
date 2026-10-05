---
type: "literature-note"
title: "Scalable Diffusion Models with Transformers"
aliases: ["Scalable Diffusion Models with Transformers"]
zotero_keys: ["V5XYDIXD"]
year: 2023
authors: ["William Peebles", "Saining Xie"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2212.09748"
url: "http://arxiv.org/abs/2212.09748"
collections: ["01 Foundations"]
source_tags: ["Computer Science - Computer Vision and Pattern Recognition", "Computer Science - Machine Learning"]
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# Scalable Diffusion Models with Transformers

[Zotero 条目 V5XYDIXD](zotero://select/library/items/V5XYDIXD)

[DOI 原文](https://doi.org/10.48550/arxiv.2212.09748)

[来源网页](http://arxiv.org/abs/2212.09748)

## 主题与知识联系

- [[Zotero Knowledge/Topics/01 Foundations/索引|01 Foundations]]

## 原始摘要

We explore a new class of diffusion models based on the transformer architecture. We train latent diffusion models of images, replacing the commonly-used U-Net backbone with a transformer that operates on latent patches. We analyze the scalability of our Diffusion Transformers (DiTs) through the lens of forward pass complexity as measured by Gflops. We find that DiTs with higher Gflops -- through increased transformer depth/width or increased number of input tokens -- consistently have lower FID. In addition to possessing good scalability properties, our largest DiT-XL/2 models outperform all prior diffusion models on the class-conditional ImageNet 512x512 and 256x256 benchmarks, achieving a state-of-the-art FID of 2.27 on the latter.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Comment: Code, project page and videos available at https://www.wpeebles.com/DiT

[在 Zotero 查看](zotero://select/library/items/GKJ7NE9P)

Comment: Code, project page and videos available at https://www.wpeebles.com/DiT

## 附件与批注

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/PAYTSZ8T)

### Full Text PDF

[打开 PDF](zotero://open-pdf/library/items/L2QAKUFX)

[批注 G7ZFZYRD · 第 1 页](zotero://open-pdf/library/items/L2QAKUFX?annotation=G7ZFZYRD&page=1)

> while transformers see widespread use in autoregressive models [3,6,43,47], they have seen less adoption in other generative modeling frameworks

批注评论：motivation 0

[批注 LXNQXTMS · 第 2 页](zotero://open-pdf/library/items/L2QAKUFX?annotation=LXNQXTMS&page=2)

> demystify

[批注 C9RFN8QM · 第 2 页](zotero://open-pdf/library/items/L2QAKUFX?annotation=C9RFN8QM&page=2)

> U-Net inductive bias is not crucial to the performance of diffusion models

批注评论：motivation 1

[批注 WIX35VWW · 第 2 页](zotero://open-pdf/library/items/L2QAKUFX?annotation=WIX35VWW&page=2)

> and they can be readily replaced with standard designs such as transformers

[批注 U8WPXAAM · 第 2 页](zotero://open-pdf/library/items/L2QAKUFX?annotation=U8WPXAAM&page=2)

> well-poised

[批注 69C4TTVR · 第 3 页](zotero://open-pdf/library/items/L2QAKUFX?annotation=69C4TTVR&page=3)

> adaptive layer norm, cross-attention and extra input tokens.

[批注 WSBC8RDZ · 第 3 页](zotero://open-pdf/library/items/L2QAKUFX?annotation=WSBC8RDZ&page=3)

> Adaptive layer norm works best.

[批注 ULP8BYYE · 第 4 页](zotero://open-pdf/library/items/L2QAKUFX?annotation=ULP8BYYE&page=4)

> Classifier-free guidance is widely-known to yield significantly improved samples over generic sampling techniques [21, 35, 46], and the trend holds for our DiT models

[批注 VZDZSJZD · 第 4 页](zotero://open-pdf/library/items/L2QAKUFX?annotation=VZDZSJZD&page=4)

> We aim to be as faithful to the standard transformer architecture as possible to retain its scaling properties.

[批注 T82MU3HL · 第 4 页](zotero://open-pdf/library/items/L2QAKUFX?annotation=T82MU3HL&page=4)

> apply standard ViT frequency-based positional embeddings (the sine-cosine version) to all input tokens.

[批注 UXLTU5WW · 第 4 页](zotero://open-pdf/library/items/L2QAKUFX?annotation=UXLTU5WW&page=4)

> sometimes process additional conditional information such as noise timesteps t, class labels c, natural language, etc.

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
