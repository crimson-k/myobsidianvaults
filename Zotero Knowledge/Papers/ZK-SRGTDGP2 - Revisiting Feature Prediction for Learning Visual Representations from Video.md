---
type: "literature-note"
title: "Revisiting Feature Prediction for Learning Visual Representations from Video"
aliases: ["Revisiting Feature Prediction for Learning Visual Representations from Video"]
zotero_keys: ["SRGTDGP2"]
year: 2024
authors: ["Adrien Bardes", "Quentin Garrido", "Jean Ponce", "Xinlei Chen", "Michael Rabbat", "Yann LeCun", "Mahmoud Assran", "Nicolas Ballas"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2404.08471"
url: "http://arxiv.org/abs/2404.08471"
collections: ["02 Representation & Perception/Visual Representation Learning"]
source_tags: ["Computer Science - Artificial Intelligence", "Computer Science - Computer Vision and Pattern Recognition", "Computer Science - Machine Learning"]
tags: ["zotero", "literature", "concept/表征学习与世界模型", "concept-primary/表征学习与世界模型"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# Revisiting Feature Prediction for Learning Visual Representations from Video

[Zotero 条目 SRGTDGP2](zotero://select/library/items/SRGTDGP2)

[DOI 原文](https://doi.org/10.48550/arxiv.2404.08471)

[来源网页](http://arxiv.org/abs/2404.08471)

## 主题与知识联系

- [[Zotero Knowledge/Topics/02 Representation & Perception/Visual Representation Learning/索引|02 Representation & Perception/Visual Representation Learning]]

概念地图：[[Zotero Knowledge/Concepts/表征学习与世界模型|表征学习与世界模型]]

## 原始摘要

This paper explores feature prediction as a stand-alone objective for unsupervised learning from video and introduces V-JEPA, a collection of vision models trained solely using a feature prediction objective, without the use of pretrained image encoders, text, negative examples, reconstruction, or other sources of supervision. The models are trained on 2 million videos collected from public datasets and are evaluated on downstream image and video tasks. Our results show that learning by predicting video features leads to versatile visual representations that perform well on both motion and appearance-based tasks, without adaption of the model's parameters; e.g., using a frozen backbone. Our largest model, a ViT-H/16 trained only on videos, obtains 81.9% on Kinetics-400, 72.2% on Something-Something-v2, and 77.9% on ImageNet1K.

## 附件与批注

### Preprint PDF

[打开 PDF](zotero://open-pdf/library/items/953HUA89)

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/3T2UMJRL)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-EJEPANDU - V-JEPA 2  Self-Supervised Video Models Enable Understanding, Prediction and Planning|V-JEPA 2: Self-Supervised Video Models Enable Understanding, Prediction and Planning]] — 强关联；比较视频特征预测预训练与加入动作条件、机器人规划后的能力。
- [[Zotero Knowledge/Papers/ZK-PZKQUJNM - Self-Supervised Learning from Images with a Joint-Embedding Predictive Architecture|Self-Supervised Learning from Images with a Joint-Embedding Predictive Architecture]] — 强关联；共同采用表征预测而非像素重建；比较图像与视频的自监督目标。
- [[Zotero Knowledge/Papers/ZK-DJ7Y6F24 - Inference-time Physics Alignment of Video Generative Models with Latent World Models|Inference-time Physics Alignment of Video Generative Models with Latent World Models]] — 强关联；对方摘要提到模型 VJEPA（仅确认名称提及）。
- [[Zotero Knowledge/Papers/ZK-DHAVJTNT - Flow Matching in Feature Space for Stochastic World Modeling|Flow Matching in Feature Space for Stochastic World Modeling]] — 强关联；比较确定性视频特征预测与特征空间中的随机未来分布建模。

<!-- content-relations:end -->
