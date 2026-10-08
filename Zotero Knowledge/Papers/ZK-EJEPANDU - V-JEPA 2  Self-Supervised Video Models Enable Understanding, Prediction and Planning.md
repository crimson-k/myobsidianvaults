---
type: "literature-note"
title: "V-JEPA 2: Self-Supervised Video Models Enable Understanding, Prediction and Planning"
aliases: ["V-JEPA 2: Self-Supervised Video Models Enable Understanding, Prediction and Planning"]
zotero_keys: ["EJEPANDU"]
year: 2025
authors: ["Mido Assran", "Adrien Bardes", "David Fan", "Quentin Garrido", "Russell Howes", "Mojtaba", "Komeili", "Matthew Muckley", "Ammar Rizvi", "Claire Roberts", "Koustuv Sinha", "Artem Zholus", "Sergio Arnaud", "Abha Gejji", "Ada Martin", "Francois Robert Hogan", "Daniel Dugas", "Piotr Bojanowski", "Vasil Khalidov", "Patrick Labatut", "Francisco Massa", "Marc Szafraniec", "Kapil Krishnakumar", "Yong Li", "Xiaodong Ma", "Sarath Chandar", "Franziska Meier", "Yann LeCun", "Michael Rabbat", "Nicolas Ballas"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2506.09985"
url: "http://arxiv.org/abs/2506.09985"
collections: ["04 World Models/Latent & Object-Centric Dynamics"]
source_tags: ["Computer Science - Artificial Intelligence", "Computer Science - Computer Vision and Pattern Recognition", "Computer Science - Machine Learning", "Computer Science - Robotics"]
tags: ["zotero", "literature", "concept/表征学习与世界模型", "concept-primary/表征学习与世界模型"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# V-JEPA 2: Self-Supervised Video Models Enable Understanding, Prediction and Planning

[Zotero 条目 EJEPANDU](zotero://select/library/items/EJEPANDU)

[DOI 原文](https://doi.org/10.48550/arxiv.2506.09985)

[来源网页](http://arxiv.org/abs/2506.09985)

## 主题与知识联系

- [[Zotero Knowledge/Topics/04 World Models/Latent & Object-Centric Dynamics/索引|04 World Models/Latent & Object-Centric Dynamics]]

概念地图：[[Zotero Knowledge/Concepts/表征学习与世界模型|表征学习与世界模型]]

补充阅读入口：[[Zotero Knowledge/Topics/02 Representation & Perception/Visual Representation Learning/索引|02 Representation & Perception/Visual Representation Learning]] · [[Zotero Knowledge/Topics/05 Robot Learning/Planning & Inverse Control/索引|05 Robot Learning/Planning & Inverse Control]]

## 原始摘要

A major challenge for modern AI is to learn to understand the world and learn to act largely by observation. This paper explores a self-supervised approach that combines internet-scale video data with a small amount of interaction data (robot trajectories), to develop models capable of understanding, predicting, and planning in the physical world. We first pre-train an action-free joint-embedding-predictive architecture, V-JEPA 2, on a video and image dataset comprising over 1 million hours of internet video. V-JEPA 2 achieves strong performance on motion understanding (77.3 top-1 accuracy on Something-Something v2) and state-of-the-art performance on human action anticipation (39.7 recall-at-5 on Epic-Kitchens-100) surpassing previous task-specific models. Additionally, after aligning V-JEPA 2 with a large language model, we demonstrate state-of-the-art performance on multiple video question-answering tasks at the 8 billion parameter scale (e.g., 84.0 on PerceptionTest, 76.9 on TempCompass). Finally, we show how self-supervised learning can be applied to robotic planning tasks by post-training a latent action-conditioned world model, V-JEPA 2-AC, using less than 62 hours of unlabeled robot videos from the Droid dataset. We deploy V-JEPA 2-AC zero-shot on Franka arms in two different labs and enable picking and placing of objects using planning with image goals. Notably, this is achieved without collecting any data from the robots in these environments, and without any task-specific training or reward. This work demonstrates how self-supervised learning from web-scale data and a small amount of robot interaction data can yield a world model capable of planning in the physical world.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Comment: 48 pages, 19 figures

[在 Zotero 查看](zotero://select/library/items/UVACNBKE)

Comment: 48 pages, 19 figures

## 附件与批注

### Preprint PDF

[打开 PDF](zotero://open-pdf/library/items/IXH9TPLM)

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/ASNIDIJS)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
