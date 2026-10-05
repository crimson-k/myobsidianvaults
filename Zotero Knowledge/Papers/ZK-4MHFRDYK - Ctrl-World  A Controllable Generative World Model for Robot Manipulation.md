---
type: "literature-note"
title: "Ctrl-World: A Controllable Generative World Model for Robot Manipulation"
aliases: ["Ctrl-World: A Controllable Generative World Model for Robot Manipulation"]
zotero_keys: ["4MHFRDYK"]
year: 2026
authors: ["Yanjiang Guo", "Lucy Xiaoyang Shi", "Jianyu Chen", "Chelsea Finn"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2510.10125"
url: "http://arxiv.org/abs/2510.10125"
collections: ["04 World Models/Video-Based Interactive Simulation"]
source_tags: ["Artificial Intelligence (cs.AI)", "Computer Science - Artificial Intelligence", "Computer Science - Robotics", "FOS: Computer and information sciences", "Robotics (cs.RO)", "notion"]
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# Ctrl-World: A Controllable Generative World Model for Robot Manipulation

[Zotero 条目 4MHFRDYK](zotero://select/library/items/4MHFRDYK)

[DOI 原文](https://doi.org/10.48550/arxiv.2510.10125)

[来源网页](http://arxiv.org/abs/2510.10125)

## 主题与知识联系

- [[Zotero Knowledge/Topics/04 World Models/Video-Based Interactive Simulation/索引|04 World Models/Video-Based Interactive Simulation]]

概念地图：[[Zotero Knowledge/Concepts/动作接口与逆动力学|动作接口与逆动力学]]

## 原始摘要

Generalist robot policies can now perform a wide range of manipulation skills, but evaluating and improving their ability with unfamiliar objects and instructions remains a significant challenge. Rigorous evaluation requires a large number of realworld rollouts, while systematic improvement demands additional corrective data with expert labels. Both of these processes are slow, costly, and difficult to scale. World models offer a promising, scalable alternative by enabling policies to rollout within imagination space. However, a key challenge is building a controllable world model that can handle multi-step interactions with generalist robot policies. This requires a world model compatible with modern generalist policies by supporting multi-view prediction, fine-grained action control, and consistent long-horizon interactions, which is not achieved by previous works. In this paper, we make a step forward by introducing a controllable multi-view world model that can be used to evaluate and improve the instruction-following ability of generalist robot policies. Our model maintains long-horizon consistency with a pose-conditioned memory retrieval mechanism and achieves precise action control through framelevel action conditioning. Trained on the DROID dataset (95k trajectories, 564 scenes), our model generates spatially and temporally consistent trajectories under novel scenarios and new camera placements for over 20 seconds. We show that our method can accurately rank policy performance without real-world robot rollouts. Moreover, by synthesizing successful trajectories in imagination and using them for supervised fine-tuning, our approach can improve policy success by 44.7%.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Other

[在 Zotero 查看](zotero://select/library/items/XEQUJ9FF)

## Other
17 pages

### Comment: 17 pages

[在 Zotero 查看](zotero://select/library/items/IADJMAZJ)

Comment: 17 pages

## 附件与批注

### PDF

[打开 PDF](zotero://open-pdf/library/items/5YZNVVDK)

### Notion

[在 Zotero 查看附件](zotero://select/library/items/U73KPKN8)

附件笔记：

## Do not modify or delete!

This link attachment serves as a reference for
[Notero](https://github.com/dvanoni/notero)
so that it can properly update the Notion page for this item.

Last synced: 2026/5/27 20:11:32

### PDF

[打开 PDF](zotero://open-pdf/library/items/ZHHNLMTV)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
