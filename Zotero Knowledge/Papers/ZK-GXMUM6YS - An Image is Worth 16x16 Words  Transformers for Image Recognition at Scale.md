---
type: "literature-note"
title: "An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale"
aliases: ["An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale"]
zotero_keys: ["GXMUM6YS"]
year: 2021
authors: ["Alexey Dosovitskiy", "Lucas Beyer", "Alexander Kolesnikov", "Dirk Weissenborn", "Xiaohua Zhai", "Thomas Unterthiner", "Mostafa Dehghani", "Matthias Minderer", "Georg Heigold", "Sylvain Gelly", "Jakob Uszkoreit", "Neil Houlsby"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2010.11929"
url: "http://arxiv.org/abs/2010.11929"
collections: ["01 Foundations"]
source_tags: ["Computer Science - Artificial Intelligence", "Computer Science - Computer Vision and Pattern Recognition", "Computer Science - Machine Learning"]
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale

[Zotero 条目 GXMUM6YS](zotero://select/library/items/GXMUM6YS)

[DOI 原文](https://doi.org/10.48550/arxiv.2010.11929)

[来源网页](http://arxiv.org/abs/2010.11929)

## 主题与知识联系

- [[Zotero Knowledge/Topics/01 Foundations/索引|01 Foundations]]

## 原始摘要

While the Transformer architecture has become the de-facto standard for natural language processing tasks, its applications to computer vision remain limited. In vision, attention is either applied in conjunction with convolutional networks, or used to replace certain components of convolutional networks while keeping their overall structure in place. We show that this reliance on CNNs is not necessary and a pure transformer applied directly to sequences of image patches can perform very well on image classification tasks. When pre-trained on large amounts of data and transferred to multiple mid-sized or small image recognition benchmarks (ImageNet, CIFAR-100, VTAB, etc.), Vision Transformer (ViT) attains excellent results compared to state-of-the-art convolutional networks while requiring substantially fewer computational resources to train.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Comment: Fine-tuning code and pre-trained models are available at https://github.com/google-research/vision_transformer.

[在 Zotero 查看](zotero://select/library/items/JTG7ZA7T)

Comment: Fine-tuning code and pre-trained models are available at https://github.com/google-research/vision_transformer. ICLR camera-ready version with 2 small modifications: 1) Added a discussion of CLS vs GAP classifier in the appendix, 2) Fixed an error in exaFLOPs computation in Figure 5 and Table 6 (relative performance of models is basically not affected)

## 附件与批注

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/C4F4H2KZ)

### Full Text PDF

[打开 PDF](zotero://open-pdf/library/items/4TLKGZZF)

[批注 IPI7HNRR · 第 1 页](zotero://open-pdf/library/items/4TLKGZZF?annotation=IPI7HNRR&page=1)

> Inspired by the Transformer scaling successes in NLP, we experiment with applying a standard Transformer directly to images, with the fewest possible modifications.

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
