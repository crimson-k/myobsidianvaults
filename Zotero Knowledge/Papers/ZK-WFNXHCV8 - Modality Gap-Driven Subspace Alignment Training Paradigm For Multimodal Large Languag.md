---
type: "literature"
title: "Modality Gap-Driven Subspace Alignment Training Paradigm For Multimodal Large Language Models"
aliases: ["ReAlign / ReVision"]
zotero_keys: ["WFNXHCV8"]
year: 2026
authors: ["Yu, Xiaomin", "Xin, Yi", "Zhang, Yuhui", "Zhang, Wenjie", "Liu, Chonghan", "Zhao, Hanzhen", "Liu, Chen", "Hu, Xiaoxing", "Qiao, Ziyue", "Tang, Hao", "Hu, Xiaobin", "Qin, Chengwei", "Xiong, Hui", "Qiao, Yu", "Yan, Shuicheng"]
venue: "arXiv"
doi: ""
url: "https://arxiv.org/abs/2602.07026"
collections: ["06 Alignment & Reliability/Representation Alignment", "90 Projects/Pattern Recognition Course/Project 1/Group 2"]
tags: ["zotero", "literature", "course/pattern-recognition", "ppt/group-2"]
reading_status: "presentation-import"
ppt_role: "extension"
ppt_pages: [107, 107]
imported_at: "2026-10-03"
---

# Modality Gap-Driven Subspace Alignment Training Paradigm For Multimodal Large Language Models

[在 Zotero 打开](zotero://select/library/items/WFNXHCV8) · [论文来源](https://arxiv.org/abs/2602.07026) · [论文 PDF](https://arxiv.org/pdf/2602.07026)

## 文献导读

分析模态间隙中的子空间结构，提出面向多模态大模型的对齐训练范式。正式标题与 PPT 中的方法简称不同，以下保留官方标题与方法别名。

## 主题与关联

[[Zotero Knowledge/Topics/06 Alignment & Reliability/Representation Alignment/索引|06 Alignment & Reliability/Representation Alignment]] · [[Zotero Knowledge/Topics/90 Projects/Pattern Recognition Course/Project 1/索引|项目一文献分享]]

以下为阅读比较建议，并非已经证实的文献依赖关系。

- [[Zotero Knowledge/Papers/ZK-BYZ75H5L - Connect, Collapse, Corrupt  Learning Cross-Modal Tasks with Uni-Modal Data|C3]]
- [[Zotero Knowledge/Papers/ZK-Y364L7RZ - MultiLoReFT  Decoupling Shared and Modality-Specific Subspaces in Multimodal Learning|MultiLoReFT]]

## 原始摘要

Despite the success of multimodal contrastive learning in aligning visual and linguistic representations, a persistent geometric anomaly, the Modality Gap, remains: embeddings of distinct modalities expressing identical semantics occupy systematically offset regions. Prior approaches to bridge this gap are largely limited by oversimplified isotropic assumptions, hindering their application in large-scale scenarios. In this paper, we address these limitations by precisely characterizing the geometric shape of the modality gap and leveraging it for efficient model scaling. First, we propose the Fixed-frame Modality Gap Theory, which decomposes the modality gap within a frozen reference frame into stable biases and anisotropic residuals. Guided by this precise modeling, we introduce ReAlign, a training-free modality alignment strategy. Utilizing statistics from massive unpaired data, ReAlign aligns text representation into the image representation distribution via a three-step process comprising Anchor, Trace, and Centroid Alignment, thereby explicitly rectifying geometric misalignment. Building on ReAlign, we propose ReVision, a scalable training paradigm for Multimodal Large Language Models~(MLLMs). ReVision integrates ReAlign into the pretraining stage, enabling the model to learn the distribution of visual representations from unpaired text before visual instruction tuning, without the need for large-scale, high-quality image-text pairs. Our framework demonstrates that statistically aligned unpaired data can effectively substitute for expensive image-text pairs, offering a robust path for the efficient scaling of MLLMs.

来源：[论文官方页面](https://arxiv.org/abs/2602.07026)。

## PPT 文献分享原页

来源：[第 2 组原 PPT](file:///C:/Users/amber/Documents/xwechat_files/wxid_ojd0ni9ss2gz12_0e91/msg/file/2026-09/%E9%A1%B9%E7%9B%AE%E4%B8%80%E7%AC%AC%E4%BA%8C%E7%BB%84%E6%96%87%E7%8C%AE%E5%88%86%E4%BA%AB%EF%BC%88%E4%BF%AE%E6%94%B9%E7%89%88%EF%BC%89.pptx)，原文件第 107–107 页。

页面图保留原图表、公式和排版；下方折叠文本供搜索。汇报中的解释、教学示例和实验数字均属于来源材料，尚未逐项对照论文全文复核。

> 本文是延伸阅读，共享一张后续工作介绍页，PPT 没有对它进行完整独立汇报。

### 原 PPT 第 107 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-107.png]]

> [!quote]- 本页可搜索文字
> 7 论文总结与研究演进：后续文献如何承接 C³？
>
> 14 / 14
>
> [1] Diffusion Bridge, CVPR 2025, §3  [2] Diffusion-Link, arXiv:2510.11330v1, §1–2  [3] ReAlign/ReVision, arXiv:2602.07026v1, §2–5
>
> 研究启发：顺着前作的解释，继续检验假设、改进对齐方式，并扩展适用任务
>
> 01
>
> C³ 留下了什么？
>
> 1
>
> 把问题拆开
>
> 图文能匹配，不代表输入可互换。
>
> 整体偏移与样本残差需要区分。
>
> 2
>
> 让操作对应解释
>
> 去均值处理整体偏移；加噪声
>
> 训练提高解码器对扰动的容忍。
>
> 3
>
> 留下可继续追问的假设
>
> 残差该怎样建模？能否学习映射？
>
> 其他模态和大模型能否受益？
>
> 02
>
> 后续文献｜承接点与推进
>
> Diffusion
>
> Bridge
>
> CVPR 2025
>
> 直接承接 C³
>
> 从“适应残差”到“学习去噪映射”
>
> 沿用残差分析，学习文本表征的扩散去噪；
>
> 推理时将图像表征转为类文本表征。
>
> 承接 C³ 的几何分析与去均值处理。
>
> Diffusion-Link
>
> arXiv 2025 · v1
>
> 沿扩散桥接扩展
>
> 从图像—文本桥接到音频—文本桥接
>
> 接续 Diffusion Bridge，将音频映射到文本分布，
>
> 增加拓扑约束，并用于音频描述。
>
> 条件变化：桥接模块训练使用配对音频—文本。
>
> ReAlign /
>
> ReVision
>
> arXiv 2026 · v1
>
> 重新审视 C³ 假设
>
> 从各向同性近似到方向相关残差分析
>
> 提出统计对齐，并用于文字替代视觉预训练；
>
> 将模态间隙问题带入多模态大模型训练。
>
> 条件变化：第二阶段仍使用真实图像做指令微调。
>
> 右栏为后续论文的工作；两篇 arXiv 文献按所读预印本版本标注。
>

## 我的阅读与思考

<!-- 在此补充个人笔记；导入内容与个人结论分开记录。 -->

[[Zotero Knowledge/知识库首页|知识库首页]]
