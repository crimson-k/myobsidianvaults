---
type: "literature"
title: "Diffusion-Link: Diffusion Probabilistic Model for Bridging the Audio-Text Modality Gap"
aliases: ["Diffusion-Link"]
zotero_keys: ["I6438ULU"]
year: 2025
authors: ["Nam, KiHyun", "Choi, Jongmin", "Lee, Hyeongkeun", "Heo, Jungwoo", "Chung, Joon Son"]
venue: "arXiv"
doi: ""
url: "https://arxiv.org/abs/2510.11330"
collections: ["06 Alignment & Reliability/Representation Alignment", "90 Projects/Pattern Recognition Course/Project 1/Group 2"]
tags: ["zotero", "literature", "course/pattern-recognition", "ppt/group-2", "concept/跨模态对齐与模态间隙", "concept-primary/跨模态对齐与模态间隙"]
reading_status: "presentation-import"
ppt_role: "extension"
ppt_pages: [107, 107]
imported_at: "2026-10-03"
---

# Diffusion-Link: Diffusion Probabilistic Model for Bridging the Audio-Text Modality Gap

[在 Zotero 打开](zotero://select/library/items/I6438ULU) · [论文来源](https://arxiv.org/abs/2510.11330) · [论文 PDF](https://arxiv.org/pdf/2510.11330)

## 文献导读

使用扩散模型桥接音频与文本嵌入，并引入拓扑约束。PPT 将它列为 Diffusion Bridge 的延伸工作，本次只保存第 107 页的介绍。

## 主题与关联

[[Zotero Knowledge/Topics/06 Alignment & Reliability/Representation Alignment/索引|06 Alignment & Reliability/Representation Alignment]] · [[Zotero Knowledge/Topics/90 Projects/Pattern Recognition Course/Project 1/索引|项目一文献分享]]

以下为阅读比较建议，并非已经证实的文献依赖关系。

- [[Zotero Knowledge/Papers/ZK-8MDVNFZD - Diffusion Bridge  Leveraging Diffusion Model to Reduce the Modality Gap Between Text |Diffusion Bridge]]
- [[Zotero Knowledge/Papers/ZK-BYZ75H5L - Connect, Collapse, Corrupt  Learning Cross-Modal Tasks with Uni-Modal Data|C3]]

## 原始摘要

Contrastive audio-language pretraining yields powerful joint representations, yet a persistent audio-text modality gap limits the benefits of coupling multimodal encoders with large language models (LLMs). We present Diffusion-Link, a diffusion-based modality-bridging module that generatively maps audio embeddings into the text-embedding distribution. The module is trained at the output embedding from the frozen multimodal encoder and implemented as a lightweight network with three residual MLP blocks. To assess the effect of Diffusion-Link on multimodal encoder-LLM coupling, we evaluate on Automatic Audio Captioning (AAC); to our knowledge, this is the first application of diffusion-based modality bridging to AAC. We report two results. (1) Modality-gap analysis: on similarity and geometric criteria, Diffusion-Link reduces the modality gap the most among prior diffusion-based methods and shows a collective migration of audio embeddings toward the text distribution. (2) Downstream AAC: attaching Diffusion-Link to the same multimodal LLM baseline achieves state-of-the-art on AudioCaps in both zero-shot and fully supervised captioning without external knowledge, with relative gains up to 52.5% and 7.5%, respectively. These findings show that closing the modality gap is pivotal for effective coupling between multimodal encoders and LLMs, and diffusion-based modality bridging offers a promising direction beyond knowledge-retrieval-centric designs. Code will be released upon acceptance this https URL

来源：[论文官方页面](https://arxiv.org/abs/2510.11330)。

## PPT 文献分享原页

来源：[第 2 组原 PPT](../Assets/Original%20PPTs/%E9%A1%B9%E7%9B%AE%E4%B8%80%E7%AC%AC%E4%BA%8C%E7%BB%84%E6%96%87%E7%8C%AE%E5%88%86%E4%BA%AB%EF%BC%88%E4%BF%AE%E6%94%B9%E7%89%88%EF%BC%89.pptx)，原文件第 107–107 页。

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

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-8MDVNFZD - Diffusion Bridge  Leveraging Diffusion Model to Reduce the Modality Gap Between Text |Diffusion Bridge: Leveraging Diffusion Model to Reduce the Modality Gap Between Text and Vision for Zero-Shot Image Captioning]] — 强关联；共同研究内容：对比学习与跨模态编码、扩散生成架构、模态间隙。
- [[Zotero Knowledge/Papers/ZK-WFNXHCV8 - Modality Gap-Driven Subspace Alignment Training Paradigm For Multimodal Large Languag|Modality Gap-Driven Subspace Alignment Training Paradigm For Multimodal Large Language Models]] — 强关联；共同研究内容：对比学习与跨模态编码、模态间隙。
- [[Zotero Knowledge/Papers/ZK-BYZ75H5L - Connect, Collapse, Corrupt  Learning Cross-Modal Tasks with Uni-Modal Data|Connect, Collapse, Corrupt: Learning Cross-Modal Tasks with Uni-Modal Data]] — 中关联；共同研究内容：对比学习与跨模态编码、模态间隙。

<!-- content-relations:end -->

<!-- research-integration:start -->
## 研究主题入口

- [[Zotero Knowledge/Topics/06 Alignment & Reliability/Representation Alignment/索引|06 Alignment & Reliability/Representation Alignment]]

## 概念比较入口

- [[Zotero Knowledge/Concepts/跨模态对齐与模态间隙|跨模态对齐与模态间隙]]
<!-- research-integration:end -->
