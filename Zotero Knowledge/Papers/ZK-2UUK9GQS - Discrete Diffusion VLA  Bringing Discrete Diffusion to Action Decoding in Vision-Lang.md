---
type: "literature-note"
title: "Discrete Diffusion VLA: Bringing Discrete Diffusion to Action Decoding in Vision-Language-Action Policies"
aliases: ["Discrete Diffusion VLA: Bringing Discrete Diffusion to Action Decoding in Vision-Language-Action Policies"]
zotero_keys: ["2UUK9GQS"]
year: 2026
authors: ["Zhixuan Liang", "Yizhuo Li", "Tianshuo Yang", "Chengyue Wu", "Sitong Mao", "Liuao Pei", "Tian Nian", "Shunbo Zhou", "Xiaokang Yang", "Jiangmiao Pang", "Yao Mu", "Ping Luo"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2508.20072"
url: "http://arxiv.org/abs/2508.20072"
collections: ["05 Robot Learning/Vision-Language Policies"]
source_tags: ["Computer Science - Computer Vision and Pattern Recognition", "Computer Science - Machine Learning", "Computer Science - Robotics"]
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# Discrete Diffusion VLA: Bringing Discrete Diffusion to Action Decoding in Vision-Language-Action Policies

[Zotero 条目 2UUK9GQS](zotero://select/library/items/2UUK9GQS)

[DOI 原文](https://doi.org/10.48550/arxiv.2508.20072)

[来源网页](http://arxiv.org/abs/2508.20072)

## 主题与知识联系

- [[Zotero Knowledge/Topics/05 Robot Learning/Vision-Language Policies/索引|05 Robot Learning/Vision-Language Policies]]

## 原始摘要

Vision–Language–Action (VLA) models adapt large vision–language backbones to map images and instructions into robot actions. However, prevailing VLAs either generate actions autoregressively in a fixed left-to-right order with poor performance or attach separate diffusion heads outside the backbone that fragments information pathways and hinders unified, scalable architectures. Instead, we present Discrete Diffusion VLA that discretizes action chunks and models them with discrete diffusion pattern retaining progressive refinement inside the unified transformer backbone. Our method achieves an adaptive decoding order that resolves high-confidence action elements before harder ones and employs secondary re-masking to revisit uncertain predictions, enabling robust error correction. This design preserves pretrained vision-language priors, supports parallel decoding, and improves the efficiency. Discrete Diffusion VLA achieves 96.4% avg. success on LIBERO, 71.2% visual matching on SimplerEnv-Fractal, and 54.2% overall on SimplerEnv-Bridge. On out-of-distribution tests of LIBERO-Goal, our method exhibits only 0.8% language degradation versus 8.0% of parallel decoding, and 20.4% vision degradation versus 29.0% for continuous diffusion, demonstrating well retention of pretrained vision-language capabilities. We also conduct two real-robot evaluations on AgileX Cobot Magic platform to show the method’s effectiveness.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Comment: Accepted by ICML 2026. 17 pages

[在 Zotero 查看](zotero://select/library/items/W7YUEVWG)

Comment: Accepted by ICML 2026. 17 pages

## 附件与批注

### PDF

[打开 PDF](zotero://open-pdf/library/items/8VDT5KWF)

[批注 5862WBQG · 第 1 页](zotero://open-pdf/library/items/8VDT5KWF?annotation=5862WBQG&page=1)

> Our method achieves an adaptive decoding order that resolves high-confidence action elements before harder ones and employs secondary re-masking to revisit uncertain predictions, enabling robust error correction.

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
