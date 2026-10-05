---
type: "literature-note"
title: "WALL-WM: Carving World Action Modeling at the Event Joints"
aliases: ["WALL-WM: Carving World Action Modeling at the Event Joints"]
zotero_keys: ["6TR77ECS"]
year: 2026
authors: ["Shalfun Li", "Victor Yao", "Charles Yang", "Truth Qu", "Regis Cheng", "Ryan Yu", "Howard Lu", "Newton Von", "Vincent Chen", "Yohann Tang", "Maeve Zhang", "Ellie Ma", "Gody Li", "Sage Yang", "Lorien Shu", "J. W. Gao", "Ethan Chen", "Colin Ye", "Yu Sun", "Elise Mon", "P. S. Zhang", "Neo Li", "Lily Li", "James Wang", "Ping Yang", "Chris Pan", "Lucy Liang", "Hang Su", "Roy Gan", "Hao Wang", "Qian Wang"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2606.01955"
url: "http://arxiv.org/abs/2606.01955"
collections: ["05 Robot Learning/World-Action Models"]
source_tags: ["Computer Science - Computer Vision and Pattern Recognition", "Computer Science - Robotics"]
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# WALL-WM: Carving World Action Modeling at the Event Joints

[Zotero 条目 6TR77ECS](zotero://select/library/items/6TR77ECS)

[DOI 原文](https://doi.org/10.48550/arxiv.2606.01955)

[来源网页](http://arxiv.org/abs/2606.01955)

## 主题与知识联系

- [[Zotero Knowledge/Topics/05 Robot Learning/World-Action Models/索引|05 Robot Learning/World-Action Models]]

## 原始摘要

WALL-WM is a World Action Model that shifts video-action learning from chunk-centric optimization to event-grounded Vision-Language-Action pretraining, using semantically coherent action events as the atomic unit of learning. Existing WAMs commonly initialize from multimodal or video foundation models and then optimize fixed-length action chunks conditioned directly on the current observation and instruction. Although convenient, this chunk-centric formulation creates a fundamental granularity mismatch. Language describes semantic goals and events, vision evolves through continuous scene dynamics, and actions operate at control-level timescales; forcing all three into the same fixed-length prediction window turns VLA training into short-horizon correlation fitting. WALL-WM addresses this mismatch by organizing both supervision and data around semantic events. Specifically, it pairs event-grounded VLA pretraining with a data ecosystem built from event-level captions and cluster-balanced sampling, enabling scalable learning over diverse behaviors, scenes, and task structures. From the same event-pretrained backbone, WALL-WM supports two complementary inference modes. The event mode consumes next-event descriptions and enables variable-length execution chunks, while the unified mode uses a VLM with Staircase Decoding to condition conventional fixed-length chunk inference while preserving a gradient-continuous VLA path. Together with Muon-optimizer-based large-scale pretraining infrastructure, WALL-WM provides a practical scale-up recipe for general-purpose WAMs. Experiments show that WALL-WM generalizes broadly across language, scenes, and tasks, achieving state-of-the-art performance in large-scale real-world generalization evaluation.

## 附件与批注

### Preprint PDF

[打开 PDF](zotero://open-pdf/library/items/CQS6AXBH)

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/IPZBTDQN)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
