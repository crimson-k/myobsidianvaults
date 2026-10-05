---
type: "literature-note"
title: "WristWorld: Generating Wrist-Views via 4D World Models for Robotic Manipulation"
aliases: ["WristWorld: Generating Wrist-Views via 4D World Models for Robotic Manipulation"]
zotero_keys: ["V4F8I7PZ"]
year: 2025
authors: ["Zezhong Qian", "Xiaowei Chi", "Yuming Li", "Shizun Wang", "Zhiyuan Qin", "Xiaozhu Ju", "Sirui Han", "Shanghang Zhang"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/ARXIV.2510.07313"
url: "https://arxiv.org/abs/2510.07313"
collections: ["03 Visual Generation/Cross-View & Ego-Exo Generation"]
source_tags: ["Computer Vision and Pattern Recognition (cs.CV)", "FOS: Computer and information sciences", "Robotics (cs.RO)"]
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# WristWorld: Generating Wrist-Views via 4D World Models for Robotic Manipulation

[Zotero 条目 V4F8I7PZ](zotero://select/library/items/V4F8I7PZ)

[DOI 原文](https://doi.org/10.48550/arxiv.2510.07313)

[来源网页](https://arxiv.org/abs/2510.07313)

## 主题与知识联系

- [[Zotero Knowledge/Topics/03 Visual Generation/Cross-View & Ego-Exo Generation/索引|03 Visual Generation/Cross-View & Ego-Exo Generation]]

概念地图：[[Zotero Knowledge/Concepts/几何先验与跨视角生成|几何先验与跨视角生成]]

补充阅读入口：[[Zotero Knowledge/Topics/04 World Models/3D & 4D Dynamics/索引|04 World Models/3D & 4D Dynamics]]

## 原始摘要

Wrist-view observations are crucial for VLA models as they capture fine-grained hand–object interactions that directly enhance manipulation performance. Yet large-scale datasets rarely include such recordings, resulting in a substantial gap between abundant anchor views and scarce wrist views. Existing world models cannot bridge this gap, as they require a wrist-view first frame and thus fail to generate wrist-view videos from anchor views alone. Amid this gap, recent visual geometry models such as VGGT emerge with precisely the geometric and cross-view priors that make it possible to address such extreme viewpoint shifts. Inspired by these insights, we propose WristWorld, the first 4D world model generates wrist-view videos solely from anchor views. WristWorld operates in two stages: (i) Reconstruction, which extends VGGT and incorporates our Spatial Projection Consistency (SPC) Loss to estimate geometrically consistent wrist-view poses and 4D point clouds; (ii) Generation, which employs our designed video generation model to synthesize temporally coherent wrist-view videos from the reconstructed perspective. Experiments on Droid, Calvin, and Franka Panda demonstrate stateof-the-art video generation with superior spatial consistency, while also improving VLA performance, raising the average task completion length on Calvin by 3.81% and closing 42.4% of the anchor-wrist view gap.

## 附件与批注

### PDF

[打开 PDF](zotero://open-pdf/library/items/ENE8Z6GJ)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
