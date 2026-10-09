---
type: "literature-note"
title: "Wan: Open and Advanced Large-Scale Video Generative Models"
aliases: ["Wan: Open and Advanced Large-Scale Video Generative Models"]
zotero_keys: ["ZR2LFUNE"]
year: 2025
authors: ["Team Wan", "Ang Wang", "Baole Ai", "Bin Wen", "Chaojie Mao", "Chen-Wei Xie", "Di Chen", "Feiwu Yu", "Haiming Zhao", "Jianxiao Yang", "Jianyuan Zeng", "Jiayu Wang", "Jingfeng Zhang", "Jingren Zhou", "Jinkai Wang", "Jixuan Chen", "Kai Zhu", "Kang Zhao", "Keyu Yan", "Lianghua Huang", "Mengyang Feng", "Ningyi Zhang", "Pandeng Li", "Pingyu Wu", "Ruihang Chu", "Ruili Feng", "Shiwei Zhang", "Siyang Sun", "Tao Fang", "Tianxing Wang", "Tianyi Gui", "Tingyu Weng", "Tong Shen", "Wei Lin", "Wei Wang", "Wenmeng Zhou", "Wente Wang", "Wenting Shen", "Wenyuan Yu", "Xianzhong Shi", "Xiaoming Huang", "Xin Xu", "Yan Kou", "Yangyu Lv", "Yifei Li", "Yijing Liu", "Yiming Wang", "Yingya Zhang", "Yitong Huang", "Yong Li", "You Wu", "Yu Liu", "Yulin Pan", "Yun Zheng", "Yuntao Hong", "Yupeng Shi", "Yutong Feng", "Zeyinzi Jiang", "Zhen Han", "Zhi-Fan Wu", "Ziyu Liu"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2503.20314"
url: "http://arxiv.org/abs/2503.20314"
collections: ["03 Visual Generation/General Video Generation"]
source_tags: ["Computer Science - Computer Vision and Pattern Recognition"]
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# Wan: Open and Advanced Large-Scale Video Generative Models

[Zotero 条目 ZR2LFUNE](zotero://select/library/items/ZR2LFUNE)

[DOI 原文](https://doi.org/10.48550/arxiv.2503.20314)

[来源网页](http://arxiv.org/abs/2503.20314)

## 主题与知识联系

- [[Zotero Knowledge/Topics/03 Visual Generation/General Video Generation/索引|03 Visual Generation/General Video Generation]]

## 原始摘要

This report presents Wan, a comprehensive and open suite of video foundation models designed to push the boundaries of video generation. Built upon the mainstream diffusion transformer paradigm, Wan achieves significant advancements in generative capabilities through a series of innovations, including our novel spatio-temporal variational autoencoder (VAE), scalable pre-training strategies, large-scale data curation, and automated evaluation metrics. These contributions collectively enhance the model’s performance and versatility. Specifically, Wan is characterized by four key features: Leading Performance: The 14B model of Wan, trained on a vast dataset comprising billions of images and videos, demonstrates the scaling laws of video generation with respect to both data and model size. It consistently outperforms the existing open-source models as well as state-ofthe-art commercial solutions across multiple internal and external benchmarks, demonstrating a clear and significant performance superiority. Comprehensiveness: Wan offers two capable models, i.e., 1.3B and 14B parameters, for efficiency and effectiveness respectively. It also covers multiple downstream applications, including image-to-video, instruction-guided video editing, and personal video generation, encompassing up to eight tasks. Meanwhile, Wan is the first model that can generate visual text in both Chinese and English, significantly enhancing its practical value. Consumer-Grade Efficiency: The 1.3B model demonstrates exceptional resource efficiency, requiring only 8.19 GB VRAM, making it compatible with a wide range of consumer-grade GPUs. It also exhibits superior performance compared to larger open-source models, showcasing remarkable efficiency for text-to-video. Openness: We open-source the entire series of Wan, including source code and all models, with the goal of fostering the growth of the video generation community. This openness seeks to significantly expand the creative possibilities of video production in the industry and provide academia with high-quality video foundation models. In addition, we conduct extensive experimental analyses covering various aspects of the proposed Wan, presenting detailed results and insights. We believe these findings and conclusions will significantly advance video generation technology. All the code and models are available at https://github.com/Wan-Video/Wan2.1.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Comment: 60 pages, 33 figures

[在 Zotero 查看](zotero://select/library/items/XG2RE7QX)

Comment: 60 pages, 33 figures

## 附件与批注

### PDF

[打开 PDF](zotero://open-pdf/library/items/ARJNJAMT)

[批注 VJI2KZDL · 第 14 页](zotero://open-pdf/library/items/ARJNJAMT?annotation=VJI2KZDL&page=14)

> effectively modeling spatio-temporal contextual relationships and embedding text conditions alongside time steps.

[批注 TI7LG2QE · 第 14 页](zotero://open-pdf/library/items/ARJNJAMT?annotation=TI7LG2QE&page=14)

> we employ an MLP with a Linear layer and a SiLU (Elfwing et al., 2018) layer to process the input time embeddings and predict six modulation parameters individually.

[批注 VA8ZT7P3 · 第 14 页](zotero://open-pdf/library/items/ARJNJAMT?annotation=VA8ZT7P3&page=14)

> MLP is shared across all transformer blocks,

[批注 YJ26QLTP · 第 14 页](zotero://open-pdf/library/items/ARJNJAMT?annotation=YJ26QLTP&page=14)

> same parameter scale.

[批注 TWAFTPBZ · 第 15 页](zotero://open-pdf/library/items/ARJNJAMT?annotation=TWAFTPBZ&page=15)

> Under fixed GPU-hour budgets,

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-ZYMGZC8K - Exo2EgoSyn  Unlocking Foundation Video Generation Models for Exocentric-to-Egocentric|Exo2EgoSyn: Unlocking Foundation Video Generation Models for Exocentric-to-Egocentric Video Synthesis]] — 强关联；对方摘要提到模型 WAN 2.2（仅确认名称提及）。

<!-- content-relations:end -->
