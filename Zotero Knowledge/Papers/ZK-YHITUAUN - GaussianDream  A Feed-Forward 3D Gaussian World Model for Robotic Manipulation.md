---
type: "literature-note"
title: "GaussianDream: A Feed-Forward 3D Gaussian World Model for Robotic Manipulation"
aliases: ["GaussianDream: A Feed-Forward 3D Gaussian World Model for Robotic Manipulation"]
zotero_keys: ["YHITUAUN"]
year: 2026
authors: ["Zijian Zhang", "Yuqing Jiang", "Qian Cheng", "Xiaofan Li", "Si Liu", "Ding Zhao", "Ping Luo", "Weitao Zhou", "Haibao Yu"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2605.20752"
url: "http://arxiv.org/abs/2605.20752"
collections: ["04 World Models/3D & 4D Dynamics"]
source_tags: ["Computer Science - Robotics"]
tags: ["zotero", "literature", "concept/世界动作模型与未来预测的作用", "concept-primary/世界动作模型与未来预测的作用"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# GaussianDream: A Feed-Forward 3D Gaussian World Model for Robotic Manipulation

[Zotero 条目 YHITUAUN](zotero://select/library/items/YHITUAUN)

[DOI 原文](https://doi.org/10.48550/arxiv.2605.20752)

[来源网页](http://arxiv.org/abs/2605.20752)

## 主题与知识联系

- [[Zotero Knowledge/Topics/04 World Models/3D & 4D Dynamics/索引|04 World Models/3D & 4D Dynamics]]

概念地图：[[Zotero Knowledge/Concepts/世界动作模型与未来预测的作用|世界动作模型与未来预测的作用]]

补充阅读入口：[[Zotero Knowledge/Topics/05 Robot Learning/Vision-Language Policies/索引|05 Robot Learning/Vision-Language Policies]]

## 原始摘要

Vision-language-action (VLA) policies have advanced language-conditioned robotic manipulation by transferring semantic priors from pretrained vision-language models to action generation. However, standard action-imitation learning often lacks sufficient modeling of explicit 3D spatial information, dense geometric supervision, and future environment evolution, all critical for precise robotic interaction. To address this, we propose \textbf{GaussianDream}, a feed-forward 3D Gaussian world-model plug-in. Specifically, we introduce learnable GaussianDream Queries in the encoder, enabling the model to capture current-frame 3D spatial structure and short-horizon future evolution. During training, the latent GaussianDream prefix is processed by a static reconstruction head and a future prediction head to produce current 3D Gaussian scene states and future Gaussian evolution states. The current branch is supervised by RGB rendering and depth, while the future branch uses future RGB, depth, and pseudo 3D scene-flow signals. During inference, GaussianDream discards all auxiliary heads and retains only the learned prefix to condition action generation, without test-time Gaussian reconstruction or future prediction. Experimental results demonstrate that GaussianDream achieves state-of-the-art performance across multiple robotic manipulation benchmarks, reaching \textbf{98.4\%} on LIBERO, \textbf{54.8\%} on RoboCasa Human-50, and \textbf{50.0\%} on real-robot tasks. Compared with existing 3D-enhanced VLA methods, GaussianDream achieves strong accuracy while providing higher inference efficiency than video-based world-model approaches.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Comment: 19 pages, 9 figures

[在 Zotero 查看](zotero://select/library/items/DKRAUAAA)

Comment: 19 pages, 9 figures

## 附件与批注

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/IV3LT6LV)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
