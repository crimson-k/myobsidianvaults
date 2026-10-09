---
type: "literature-note"
title: "Wan-Move: Motion-controllable Video Generation via Latent Trajectory Guidance"
aliases: ["Wan-Move: Motion-controllable Video Generation via Latent Trajectory Guidance"]
zotero_keys: ["DSRI4BLY"]
year: 2025
authors: ["Ruihang Chu", "Yefei He", "Zhekai Chen", "Shiwei Zhang", "Xiaogang Xu", "Bin Xia", "Dingdong Wang", "Hongwei Yi", "Xihui Liu", "Hengshuang Zhao", "Yu Liu", "Yingya Zhang", "Yujiu Yang"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2512.08765"
url: "http://arxiv.org/abs/2512.08765"
collections: ["03 Visual Generation/Camera & Motion Control"]
source_tags: ["Computer Science - Computer Vision and Pattern Recognition"]
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# Wan-Move: Motion-controllable Video Generation via Latent Trajectory Guidance

[Zotero 条目 DSRI4BLY](zotero://select/library/items/DSRI4BLY)

[DOI 原文](https://doi.org/10.48550/arxiv.2512.08765)

[来源网页](http://arxiv.org/abs/2512.08765)

## 主题与知识联系

- [[Zotero Knowledge/Topics/03 Visual Generation/Camera & Motion Control/索引|03 Visual Generation/Camera & Motion Control]]

## 原始摘要

We present Wan-Move, a simple and scalable framework that brings motion control to video generative models. Existing motion-controllable methods typically suffer from coarse control granularity and limited scalability, leaving their outputs insufficient for practical use. We narrow this gap by achieving precise and high-quality motion control. Our core idea is to directly make the original condition features motion-aware for guiding video synthesis. To this end, we first represent object motions with dense point trajectories, allowing fine-grained control over the scene. We then project these trajectories into latent space and propagate the first frame's features along each trajectory, producing an aligned spatiotemporal feature map that tells how each scene element should move. This feature map serves as the updated latent condition, which is naturally integrated into the off-the-shelf image-to-video model, e.g., Wan-I2V-14B, as motion guidance without any architecture change. It removes the need for auxiliary motion encoders and makes fine-tuning base models easily scalable. Through scaled training, Wan-Move generates 5-second, 480p videos whose motion controllability rivals Kling 1.5 Pro's commercial Motion Brush, as indicated by user studies. To support comprehensive evaluation, we further design MoveBench, a rigorously curated benchmark featuring diverse content categories and hybrid-verified annotations. It is distinguished by larger data volume, longer video durations, and high-quality motion annotations. Extensive experiments on MoveBench and the public dataset consistently show Wan-Move's superior motion quality. Code, models, and benchmark data are made publicly available.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Comment: NeurlPS 2025. Code and data available at https://github.com/ali-vilab/Wan-Move

[在 Zotero 查看](zotero://select/library/items/VCXCMMZT)

Comment: NeurlPS 2025. Code and data available at https://github.com/ali-vilab/Wan-Move

## 附件与批注

### Full Text PDF

[打开 PDF](zotero://open-pdf/library/items/PP7X9RC7)

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/6PHR72KW)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-CBZ7I94U - Motion Prompting  Controlling Video Generation with Motion Trajectories|Motion Prompting: Controlling Video Generation with Motion Trajectories]] — 中关联；共同研究内容：运动与轨迹控制。

<!-- content-relations:end -->
