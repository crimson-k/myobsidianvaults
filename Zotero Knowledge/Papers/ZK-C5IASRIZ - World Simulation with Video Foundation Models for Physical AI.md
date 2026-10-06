---
type: "literature-note"
title: "World Simulation with Video Foundation Models for Physical AI"
aliases: ["World Simulation with Video Foundation Models for Physical AI"]
zotero_keys: ["C5IASRIZ", "BSX3SLYB"]
year: 2025
authors: ["NVIDIA", ":", "Arslan Ali", "Junjie Bai", "Maciej Bala", "Yogesh Balaji", "Aaron Blakeman", "Tiffany Cai", "Jiaxin Cao", "Tianshi Cao", "Elizabeth Cha", "Yu-Wei Chao", "Prithvijit Chattopadhyay", "Mike Chen", "Yongxin Chen", "Yu Chen", "Shuai Cheng", "Yin Cui", "Jenna Diamond", "Yifan Ding", "Jiaojiao Fan", "Linxi Fan", "Liang Feng", "Francesco Ferroni", "Sanja Fidler", "Xiao Fu", "Ruiyuan Gao", "Yunhao Ge", "Jinwei Gu", "Aryaman Gupta", "Siddharth Gururani", "Imad El Hanafi", "Ali Hassani", "Zekun Hao", "Jacob Huffman", "Joel Jang", "Pooya Jannaty", "Jan Kautz", "Grace Lam", "Xuan Li", "Zhaoshuo Li", "Maosheng Liao", "Chen-Hsuan Lin", "Tsung-Yi Lin", "Yen-Chen Lin", "Huan Ling", "Ming-Yu Liu", "Xian Liu", "Yifan Lu", "Alice Luo", "Qianli Ma", "Hanzi Mao", "Kaichun Mo", "Seungjun Nah", "Yashraj Narang", "Abhijeet Panaskar", "Lindsey Pavao", "Trung Pham", "Morteza Ramezanali", "Fitsum Reda", "Scott Reed", "Xuanchi Ren", "Haonan Shao", "Yue Shen", "Stella Shi", "Shuran Song", "Bartosz Stefaniak", "Shangkun Sun", "Shitao Tang", "Sameena Tasmeen", "Lyne Tchapmi", "Wei-Cheng Tseng", "Jibin Varghese", "Andrew Z. Wang", "Hao Wang", "Haoxiang Wang", "Heng Wang", "Ting-Chun Wang", "Fangyin Wei", "Jiashu Xu", "Dinghao Yang", "Xiaodong Yang", "Haotian Ye", "Seonghyeon Ye", "Xiaohui Zeng", "Jing Zhang", "Qinsheng Zhang", "Kaiwen Zheng", "Andrew Zhu", "Yuke Zhu"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/ARXIV.2511.00062"
url: "https://arxiv.org/abs/2511.00062"
collections: ["04 World Models/Video-Based Interactive Simulation"]
source_tags: ["Artificial Intelligence (cs.AI)", "Computer Vision and Pattern Recognition (cs.CV)", "FOS: Computer and information sciences", "Machine Learning (cs.LG)", "Robotics (cs.RO)", "notion"]
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# World Simulation with Video Foundation Models for Physical AI

[Zotero 条目 C5IASRIZ](zotero://select/library/items/C5IASRIZ)

[DOI 原文](https://doi.org/10.48550/arxiv.2511.00062)

[来源网页](https://arxiv.org/abs/2511.00062)

## 主题与知识联系

- [[Zotero Knowledge/Topics/04 World Models/Video-Based Interactive Simulation/索引|04 World Models/Video-Based Interactive Simulation]]

## 原始摘要

We introduce [Cosmos-Predict2.5], the latest generation of the Cosmos World Foundation Models for Physical AI. Built on a flow-based architecture, [Cosmos-Predict2.5] unifies Text2World, Image2World, and Video2World generation in a single model and leverages [Cosmos-Reason1], a Physical AI visionlanguage model, to provide richer text grounding and finer control of world simulation. Trained on 200M curated video clips and refined with reinforcement learning-based post-training, [Cosmos-Predict2.5] achieves substantial improvements over [Cosmos-Predict1] in video quality and instruction alignment, with models released at 2B and 14B scales. These capabilities enable more reliable synthetic data generation, policy evaluation, and closed-loop simulation for robotics and autonomous systems. We further extend the family with [Cosmos-Transfer2.5], a control-net style framework for Sim2Real and Real2Real world translation. Despite being 3.5× smaller than [Cosmos-Transfer1], it delivers higher fidelity and robust long-horizon video generation. Together, these advances establish [Cosmos-Predict2.5] and [Cosmos-Transfer2.5] as versatile tools for scaling embodied intelligence. To accelerate research and deployment in Physical AI, we release source code, pretrained checkpoints, and curated benchmarks under the NVIDIA Open Model License at https://github.com/nvidia-cosmos/cosmos-predict2.5 and https://github.com/nvidia-cosmos/cosmos-transfer2.5. We hope these open resources lower the barrier to adoption and foster innovation in building the next generation of embodied intelligence.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### cosmos-predict2.5

[在 Zotero 查看](zotero://select/library/items/B7AUH8GC)

cosmos-predict2.5

## 附件与批注

### Notion

[在 Zotero 查看附件](zotero://select/library/items/JXCKH3AM)

附件笔记：

## Do not modify or delete!

This link attachment serves as a reference for
[Notero](https://github.com/dvanoni/notero)
so that it can properly update the Notion page for this item.

Last synced: 2026/5/27 20:11:33

### PDF

[打开 PDF](zotero://open-pdf/library/items/Y3BZM8GB)

[批注 CJXALHRU · 第 20 页](zotero://open-pdf/library/items/Y3BZM8GB?annotation=CJXALHRU&page=20)

> RNDS

[批注 24P4IZBX · 第 20 页](zotero://open-pdf/library/items/Y3BZM8GB?annotation=24P4IZBX&page=20)

> our smaller model accumulates fewer errors, demonstrates less hallucination, and maintains higher fidelity over long video sequences.

[批注 9XEN36PV · 第 33 页](zotero://open-pdf/library/items/Y3BZM8GB?annotation=9XEN36PV&page=33)

> we add an action embedder MLP that maps each action into a tensor. Instead of injecting this tensor directly, we incorporate it by adding it to the timestamp embeddings of the DiT modules.

## 合并条目与附件来源

- [Zotero 条目 BSX3SLYB](zotero://select/library/items/BSX3SLYB)
- [独立 PDF 版本（2025-10-28）](zotero://open-pdf/library/items/BSX3SLYB)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
