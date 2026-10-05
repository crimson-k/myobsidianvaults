---
type: "literature-note"
title: "Physically Embodied Gaussian Splatting: A Realtime Correctable World Model for Robotics"
aliases: ["Physically Embodied Gaussian Splatting: A Realtime Correctable World Model for Robotics"]
zotero_keys: ["E2RY6IUA"]
year: 2024
authors: ["Jad Abou-Chakra", "Krishan Rana", "Feras Dayoub", "Niko Sünderhauf"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2406.10788"
url: "http://arxiv.org/abs/2406.10788"
collections: ["04 World Models/3D & 4D Dynamics"]
source_tags: ["Computer Science - Robotics"]
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# Physically Embodied Gaussian Splatting: A Realtime Correctable World Model for Robotics

[Zotero 条目 E2RY6IUA](zotero://select/library/items/E2RY6IUA)

[DOI 原文](https://doi.org/10.48550/arxiv.2406.10788)

[来源网页](http://arxiv.org/abs/2406.10788)

## 主题与知识联系

- [[Zotero Knowledge/Topics/04 World Models/3D & 4D Dynamics/索引|04 World Models/3D & 4D Dynamics]]

补充阅读入口：[[Zotero Knowledge/Topics/06 Alignment & Reliability/Physics Grounding & Rollout Verification/索引|06 Alignment & Reliability/Physics Grounding & Rollout Verification]]

## 原始摘要

For robots to robustly understand and interact with the physical world, it is highly beneficial to have a comprehensive representation - modelling geometry, physics, and visual observations - that informs perception, planning, and control algorithms. We propose a novel dual Gaussian-Particle representation that models the physical world while (i) enabling predictive simulation of future states and (ii) allowing online correction from visual observations in a dynamic world. Our representation comprises particles that capture the geometrical aspect of objects in the world and can be used alongside a particle-based physics system to anticipate physically plausible future states. Attached to these particles are 3D Gaussians that render images from any viewpoint through a splatting process thus capturing the visual state. By comparing the predicted and observed images, our approach generates visual forces that correct the particle positions while respecting known physical constraints. By integrating predictive physical modelling with continuous visually-derived corrections, our unified representation reasons about the present and future while synchronizing with reality. Our system runs in realtime at 30Hz using only 3 cameras. We validate our approach on 2D and 3D tracking tasks as well as photometric reconstruction quality. Videos are found at https://embodied-gaussians.github.io/.

## 附件与批注

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/88LSUIAW)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
