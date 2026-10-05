---
type: "literature-note"
title: "GWM: Towards Scalable Gaussian World Models for Robotic Manipulation"
aliases: ["GWM: Towards Scalable Gaussian World Models for Robotic Manipulation"]
zotero_keys: ["NQ3U5HJE"]
year: 2025
authors: ["Guanxing Lu", "Baoxiong Jia", "Puhao Li", "Yixin Chen", "Ziwei Wang", "Yansong Tang", "Siyuan Huang"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2508.17600"
url: "http://arxiv.org/abs/2508.17600"
collections: ["04 World Models/3D & 4D Dynamics"]
source_tags: ["Computer Science - Artificial Intelligence", "Computer Science - Computer Vision and Pattern Recognition", "Computer Science - Machine Learning", "Computer Science - Robotics"]
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# GWM: Towards Scalable Gaussian World Models for Robotic Manipulation

[Zotero 条目 NQ3U5HJE](zotero://select/library/items/NQ3U5HJE)

[DOI 原文](https://doi.org/10.48550/arxiv.2508.17600)

[来源网页](http://arxiv.org/abs/2508.17600)

## 主题与知识联系

- [[Zotero Knowledge/Topics/04 World Models/3D & 4D Dynamics/索引|04 World Models/3D & 4D Dynamics]]

补充阅读入口：[[Zotero Knowledge/Topics/05 Robot Learning/Model-Based RL & Imagination/索引|05 Robot Learning/Model-Based RL & Imagination]]

## 原始摘要

Training robot policies within a learned world model is trending due to the inefficiency of real-world interactions. The established image-based world models and policies have shown prior success, but lack robust geometric information that requires consistent spatial and physical understanding of the three-dimensional world, even pre-trained on internet-scale video sources. To this end, we propose a novel branch of world model named Gaussian World Model (GWM) for robotic manipulation, which reconstructs the future state by inferring the propagation of Gaussian primitives under the effect of robot actions. At its core is a latent Diffusion Transformer (DiT) combined with a 3D variational autoencoder, enabling fine-grained scene-level future state reconstruction with Gaussian Splatting. GWM can not only enhance the visual representation for imitation learning agent by self-supervised future prediction training, but can serve as a neural simulator that supports model-based reinforcement learning. Both simulated and real-world experiments depict that GWM can precisely predict future scenes conditioned on diverse robot actions, and can be further utilized to train policies that outperform the state-of-the-art by impressive margins, showcasing the initial data scaling potential of 3D world model.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Comment: Published at ICCV 2025. Project page: https://gaussian-world-model.github.io/

[在 Zotero 查看](zotero://select/library/items/LM4BGW9K)

Comment: Published at ICCV 2025. Project page: https://gaussian-world-model.github.io/

## 附件与批注

### Full Text PDF

[打开 PDF](zotero://open-pdf/library/items/EI3G7QYQ)

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/STURMZQM)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
