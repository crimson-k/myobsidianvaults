---
type: "literature-note"
title: "Inference-time Physics Alignment of Video Generative Models with Latent World Models"
aliases: ["Inference-time Physics Alignment of Video Generative Models with Latent World Models"]
zotero_keys: ["DJ7Y6F24"]
year: 2026
authors: ["Jianhao Yuan", "Xiaofeng Zhang", "Felix Friedrich", "Nicolas Beltran-Velez", "Melissa Hall", "Reyhane Askari-Hemmat", "Xiaochuang Han", "Nicolas Ballas", "Michal Drozdzal", "Adriana Romero-Soriano"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/ARXIV.2601.10553"
url: "https://arxiv.org/abs/2601.10553"
collections: ["06 Alignment & Reliability/Physics Grounding & Rollout Verification"]
source_tags: ["Computer Vision and Pattern Recognition (cs.CV)", "FOS: Computer and information sciences"]
tags: ["zotero", "literature", "highlight", "concept/物理一致性与表征对齐", "concept-primary/物理一致性与表征对齐"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# Inference-time Physics Alignment of Video Generative Models with Latent World Models

[Zotero 条目 DJ7Y6F24](zotero://select/library/items/DJ7Y6F24)

[DOI 原文](https://doi.org/10.48550/arxiv.2601.10553)

[来源网页](https://arxiv.org/abs/2601.10553)

## 主题与知识联系

- [[Zotero Knowledge/Topics/06 Alignment & Reliability/Physics Grounding & Rollout Verification/索引|06 Alignment & Reliability/Physics Grounding & Rollout Verification]]

概念地图：[[Zotero Knowledge/Concepts/物理一致性与表征对齐|物理一致性与表征对齐]]

补充阅读入口：[[Zotero Knowledge/Topics/04 World Models/Latent & Object-Centric Dynamics/索引|04 World Models/Latent & Object-Centric Dynamics]]

## 原始摘要

State-of-the-art video generative models produce promising visual content yet often violate basic physics principles, limiting their utility. While some attribute this deficiency to insufficient physics understanding from pre-training, we find that the shortfall in physics plausibility also stems from suboptimal inference strategies. We therefore introduce WMReward and treat improving physics plausibility of video generation as an inference-time alignment problem. In particular, we leverage the strong physics prior of a latent world model (here, VJEPA-2) as a reward to search and steer multiple candidate denoising trajectories, enabling scaling test-time compute for better generation performance. Empirically, our approach substantially improves physics plausibility across image-conditioned, multiframe-conditioned, and text-conditioned generation settings, with validation from human preference study. Notably, in the ICCV 2025 Perception Test PhysicsIQ Challenge, we achieve a final score of 62.64%, winning first place and outperforming the previous state of the art by 7.42%. Our work demonstrates the viability of using latent world models to improve physics plausibility of video generation, beyond this specific instantiation or parameterization.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Other

[在 Zotero 查看](zotero://select/library/items/KIXF3ELK)

## Other
22 pages, 10 figures

## 附件与批注

### PDF

[打开 PDF](zotero://open-pdf/library/items/UPHF3AHN)

[批注 ERQCVNHG · 第 1 页](zotero://open-pdf/library/items/UPHF3AHN?annotation=ERQCVNHG&page=1)

> substantial work has focused on improving pre-training or post-training of video generative models by injecting physics information

[批注 CLWRI4IW · 第 1 页](zotero://open-pdf/library/items/UPHF3AHN?annotation=CLWRI4IW&page=1)

> ically plausible videos may be found in the manifold learned by the generative model and therefore has focused on devising inference-time methods to improve physics

[批注 B9JNQ6DS · 第 2 页](zotero://open-pdf/library/items/UPHF3AHN?annotation=B9JNQ6DS&page=2)

> VJEPA-2

[批注 P67YWDLD · 第 2 页](zotero://open-pdf/library/items/UPHF3AHN?annotation=P67YWDLD&page=2)

> inference-time alignment problem

[批注 IUZIYZXG · 第 2 页](zotero://open-pdf/library/items/UPHF3AHN?annotation=IUZIYZXG&page=2)

> WMReward by re-purposing VJEPA-2’s surprise score as a reward function and show that it can be effectively used both as a Best-of-N (BoN) selector and as a guidance signal during generation to improve the physics of videos.

[批注 LSCBKQ98 · 第 2 页](zotero://open-pdf/library/items/UPHF3AHN?annotation=LSCBKQ98&page=2)

> PhysicsIQ benchmark

[批注 C7JC4PNP · 第 2 页](zotero://open-pdf/library/items/UPHF3AHN?annotation=C7JC4PNP&page=2)

> 11.4% improvement over baselines in a human-preference study

[批注 3W655NQ2 · 第 3 页](zotero://open-pdf/library/items/UPHF3AHN?annotation=3W655NQ2&page=3)

> transfers the physics prior from a latent world model (e.g. , VJEPA-2) into a physics plausibility reward signal.

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-SRGTDGP2 - Revisiting Feature Prediction for Learning Visual Representations from Video|Revisiting Feature Prediction for Learning Visual Representations from Video]] — 强关联；本篇摘要提到模型 VJEPA（仅确认名称提及）。

<!-- content-relations:end -->
