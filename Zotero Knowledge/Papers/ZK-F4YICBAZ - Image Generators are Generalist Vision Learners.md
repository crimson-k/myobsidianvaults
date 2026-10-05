---
type: "literature-note"
title: "Image Generators are Generalist Vision Learners"
aliases: ["Image Generators are Generalist Vision Learners"]
zotero_keys: ["F4YICBAZ"]
year: 2026
authors: ["Valentin Gabeur", "Shangbang Long", "Songyou Peng", "Paul Voigtlaender", "Shuyang Sun", "Yanan Bao", "Karen Truong", "Zhicheng Wang", "Wenlei Zhou", "Jonathan T. Barron", "Kyle Genova", "Nithish Kannen", "Sherry Ben", "Yandong Li", "Mandy Guo", "Suhas Yogin", "Yiming Gu", "Huizhong Chen", "Oliver Wang", "Saining Xie", "Howard Zhou", "Kaiming He", "Thomas Funkhouser", "Jean-Baptiste Alayrac", "Radu Soricut"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2604.20329"
url: "http://arxiv.org/abs/2604.20329"
collections: ["02 Representation & Perception/Visual Representation Learning"]
source_tags: ["Computer Science - Artificial Intelligence", "Computer Science - Computer Vision and Pattern Recognition"]
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# Image Generators are Generalist Vision Learners

[Zotero 条目 F4YICBAZ](zotero://select/library/items/F4YICBAZ)

[DOI 原文](https://doi.org/10.48550/arxiv.2604.20329)

[来源网页](http://arxiv.org/abs/2604.20329)

## 主题与知识联系

- [[Zotero Knowledge/Topics/02 Representation & Perception/Visual Representation Learning/索引|02 Representation & Perception/Visual Representation Learning]]

## 原始摘要

Recent works show that image and video generators exhibit zero-shot visual understanding behaviors, in a way reminiscent of how LLMs develop emergent capabilities of language understanding and reasoning from generative pretraining. While it has long been conjectured that the ability to create visual content implies an ability to understand it, there has been limited evidence that generative vision models have developed strong understanding capabilities. In this work, we demonstrate that image generation training serves a role similar to LLM pretraining, and lets models learn powerful and general visual representations that enable SOTA performance on various vision tasks. We introduce Vision Banana, a generalist model built by instruction-tuning Nano Banana Pro (NBP) on a mixture of its original training data alongside a small amount of vision task data. By parameterizing the output space of vision tasks as RGB images, we seamlessly reframe perception as image generation. Our generalist model, Vision Banana, achieves SOTA results on a variety of vision tasks involving both 2D and 3D understanding, beating or rivaling zero-shot domain-specialists, including Segment Anything Model 3 on segmentation tasks, and the Depth Anything series on metric depth estimation. We show that these results can be achieved with lightweight instruction-tuning without sacrificing the base model's image generation capabilities. The superior results suggest that image generation pretraining is a generalist vision learner. It also shows that image generation serves as a unified and universal interface for vision tasks, similar to text generation's role in language understanding and reasoning. We could be witnessing a major paradigm shift for computer vision, where generative vision pretraining takes a central role in building Foundational Vision Models for both generation and understanding.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Comment: Project Page: http://vision-banana.github.io

[在 Zotero 查看](zotero://select/library/items/U7ZZ6F3E)

Comment: Project Page: http://vision-banana.github.io

## 附件与批注

### Full Text PDF

[打开 PDF](zotero://open-pdf/library/items/U7923JIX)

[批注 2JUAAPIT · 第 2 页](zotero://open-pdf/library/items/U7923JIX?annotation=2JUAAPIT&page=2)

> whether visual generative models are secretly generalist vision learners,

[批注 DUSBWKBL · 第 2 页](zotero://open-pdf/library/items/U7923JIX?annotation=DUSBWKBL&page=2)

> finetune a pretrained image generator with a small amount of computer vision data (depth estimation, surface normal estimation, segmentation, etc.). We then evaluate the resulting model on a wide variety of vision benchmarks. If the finetuned model performs at or near SOTA on these benchmarks, while retaining its image generation capabilities, then there is strong evidence that the image generator was indeed a foundation model for visual understanding – i.e., a generalist vision learner.

[批注 XIE6CW2Z · 第 2 页](zotero://open-pdf/library/items/U7923JIX?annotation=XIE6CW2Z&page=2)

> do not strictly follow the prompts to produce vision outputs in the desired formats that can be decoded back to vision outputs for computing quantitative metrics.

[批注 7YWYH2PJ · 第 3 页](zotero://open-pdf/library/items/U7923JIX?annotation=7YWYH2PJ&page=3)

> position a visual generative model as a “base” model and perform instruction-tuning to align the model to produce visual output in desired formats, in accordance with the prompts

[批注 W6J5DIFV · 第 3 页](zotero://open-pdf/library/items/U7923JIX?annotation=W6J5DIFV&page=3)

> First, it suggests that image generators are indeed generalist vision learners under the hood, with generative vision pretraining playing a foundational role similar to language model pretraining. Second, it suggests that image generation can serve as a universal interface for unified visual understanding, mirroring the role of text generation in language understanding and reasoning.

[批注 5RU4ILD2 · 第 4 页](zotero://open-pdf/library/items/U7923JIX?annotation=5RU4ILD2&page=4)

> instruction-tuning our base model, Nano Banana Pro, on a selection of vision tasks formatted in such invertible manners.

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/K2P3G74U)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
