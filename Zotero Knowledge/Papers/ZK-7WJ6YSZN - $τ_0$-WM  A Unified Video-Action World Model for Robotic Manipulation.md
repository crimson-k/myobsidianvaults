---
type: "literature-note"
title: "$τ_0$-WM: A Unified Video-Action World Model for Robotic Manipulation"
aliases: ["$τ_0$-WM: A Unified Video-Action World Model for Robotic Manipulation"]
zotero_keys: ["7WJ6YSZN"]
year: 2026
authors: ["Pengfei Zhou", "Shengcong Chen", "Di Chen", "Jiaxu Wang", "Rongjun Jin", "Bingwen Zhu", "Yike Pan", "Songen Gu", "Kuanning Wang", "Shufeng Nan", "Xingyu Qiu", "Chenhao Qiu", "Pu Yang", "Yunuo Cai", "Jianxiong Gao", "Yifan Li", "Yanwei Fu", "Xiangyu Yue", "Zhi Chen", "Jianlan Luo"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2606.01027"
url: "http://arxiv.org/abs/2606.01027"
collections: ["05 Robot Learning/World-Action Models"]
source_tags: ["Computer Science - Robotics"]
tags: ["zotero", "literature", "concept/世界动作模型与未来预测的作用", "concept-primary/世界动作模型与未来预测的作用"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# $τ_0$-WM: A Unified Video-Action World Model for Robotic Manipulation

[Zotero 条目 7WJ6YSZN](zotero://select/library/items/7WJ6YSZN)

[DOI 原文](https://doi.org/10.48550/arxiv.2606.01027)

[来源网页](http://arxiv.org/abs/2606.01027)

## 主题与知识联系

- [[Zotero Knowledge/Topics/05 Robot Learning/World-Action Models/索引|05 Robot Learning/World-Action Models]]

概念地图：[[Zotero Knowledge/Concepts/世界动作模型与未来预测的作用|世界动作模型与未来预测的作用]]

补充阅读入口：[[Zotero Knowledge/Topics/04 World Models/Video-Based Interactive Simulation/索引|04 World Models/Video-Based Interactive Simulation]]

## 原始摘要

Robotic manipulation requires models that generate executable actions while anticipating and evaluating their future consequences before physical execution. We present $τ_0$-World Model ($τ_0$-WM), a unified video-action world model that integrates policy learning, video prediction, and action evaluation within a single future-predictive framework. Built on a shared video diffusion backbone, $τ_0$-WM provides two complementary interfaces. First, a video action model jointly predicts future visual latents and continuous action chunks from multi-view observations, language instructions, and robot state. Second, an action-conditioned video simulator rolls out candidate action chunks into multi-view futures and predicts dense task-progress scores. The model is trained on approximately $27{,}300$ hours of real-robot teleoperation, UMI-style interaction, egocentric human videos, and rollout or failure trajectories using modality-specific supervision masks. At inference time, $τ_0$-WM uses test-time computation to sample action candidates, rank them with re-denoising consistency, and invoke simulator-based rectification for low-quality candidates. On challenging long-horizon and fine-grained robotic manipulation tasks, $τ_0$-WM shows superior performance over other relevant baselines.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Comment: Our project homepge: https://finch.agibot.com/research/tau0-wm

[在 Zotero 查看](zotero://select/library/items/4YYH7QEQ)

Comment: Our project homepge: https://finch.agibot.com/research/tau0-wm

## 附件与批注

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/R3UFUIBM)

### Full Text PDF

[打开 PDF](zotero://open-pdf/library/items/CP9UFHKC)

[批注 D8M8KXQ7 · 第 1 页](zotero://open-pdf/library/items/CP9UFHKC?annotation=D8M8KXQ7&page=1)

> τ0-WM uses test-time computation to sample action candidates, rank them with redenoising consistency, and invoke simulator-based rectification for low-quality candidate

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-4MHFRDYK - Ctrl-World  A Controllable Generative World Model for Robot Manipulation|Ctrl-World: A Controllable Generative World Model for Robot Manipulation]] — 中关联；共同研究内容：动作条件预测、机器人操作、长时程误差与记忆。
- [[Zotero Knowledge/Papers/ZK-KH5XN2WV - DyWA  Dynamics-adaptive World Action Model for Generalizable Non-prehensile Manipulat|DyWA: Dynamics-adaptive World Action Model for Generalizable Non-prehensile Manipulation]] — 中关联；共同研究内容：世界动作模型、机器人操作。

<!-- content-relations:end -->
