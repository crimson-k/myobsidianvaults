---
type: "literature"
title: "Diffusion Bridge: Leveraging Diffusion Model to Reduce the Modality Gap Between Text and Vision for Zero-Shot Image Captioning"
aliases: ["Diffusion Bridge"]
zotero_keys: ["8MDVNFZD"]
year: 2025
authors: ["Lee, Jeong Ryong", "Shin, Yejee", "Son, Geonhui", "Hwang, Dosik"]
venue: "CVPR 2025"
doi: ""
url: "https://openaccess.thecvf.com/content/CVPR2025/html/Lee_Diffusion_Bridge_Leveraging_Diffusion_Model_to_Reduce_the_Modality_Gap_CVPR_2025_paper.html"
collections: ["06 Alignment & Reliability/Representation Alignment", "90 Projects/Pattern Recognition Course/Project 1/Group 2", "02 Representation & Perception/Vision-Language Representation"]
tags: ["zotero", "literature", "course/pattern-recognition", "ppt/group-2", "concept/跨模态对齐与模态间隙", "concept-primary/跨模态对齐与模态间隙"]
reading_status: "presentation-import"
ppt_role: "extension"
ppt_pages: [107, 107]
imported_at: "2026-10-03"
---

# Diffusion Bridge: Leveraging Diffusion Model to Reduce the Modality Gap Between Text and Vision for Zero-Shot Image Captioning

[在 Zotero 打开](zotero://select/library/items/8MDVNFZD) · [论文来源](https://openaccess.thecvf.com/content/CVPR2025/html/Lee_Diffusion_Bridge_Leveraging_Diffusion_Model_to_Reduce_the_Modality_Gap_CVPR_2025_paper.html) · [论文 PDF](https://openaccess.thecvf.com/content/CVPR2025/papers/Lee_Diffusion_Bridge_Leveraging_Diffusion_Model_to_Reduce_the_Modality_Gap_CVPR_2025_paper.pdf)

## 文献导读

以文本嵌入的扩散去噪过程将视觉表示转换为更接近文本分布的表示，用于零样本图像描述。PPT 仅在 C³ 的后续工作页介绍。

## 主题与关联

[[Zotero Knowledge/Topics/06 Alignment & Reliability/Representation Alignment/索引|06 Alignment & Reliability/Representation Alignment]] · [[Zotero Knowledge/Topics/90 Projects/Pattern Recognition Course/Project 1/索引|项目一文献分享]]

以下为阅读比较建议，并非已经证实的文献依赖关系。

- [[Zotero Knowledge/Papers/ZK-BYZ75H5L - Connect, Collapse, Corrupt  Learning Cross-Modal Tasks with Uni-Modal Data|C3]]
- [[Zotero Knowledge/Papers/ZK-I6438ULU - Diffusion-Link  Diffusion Probabilistic Model for Bridging the Audio-Text Modality Ga|Diffusion-Link]]

## 原始摘要

The modality gap between vision and text embeddings in CLIP presents a significant challenge for zero-shot image captioning, limiting effective cross-modal representation. Traditional approaches, such as noise injection and memory-based similarity matching, attempt to address this gap, yet these methods either rely on indirect alignment or relatively naive solutions with heavy computation. Diffusion Bridge introduces a novel approach to directly reduce this modality gap by leveraging Denoising Diffusion Probabilistic Models (DDPM), trained exclusively on text embeddings to model their distribution. Our approach is motivated by the observation that, while paired vision and text embeddings are relatively close, a modality gap still exists due to stable regions created by the contrastive loss. This gap can be interpreted as noise in cross-modal mappings, which we approximate as Gaussian noise. To bridge this gap, we employ a reverse diffusion process, where image embeddings are strategically introduced at an intermediate step in the reverse process, allowing them to be refined progressively toward the text embedding distribution. This process transforms vision embeddings into text-like representations closely aligned with paired text embeddings, effectively minimizing discrepancies between modalities. Experimental results demonstrate that these text-like vision embeddings significantly enhance alignment with their paired text embeddings, leading to improved zero-shot captioning performance on MSCOCO and Flickr30K. Diffusion Bridge achieves competitive results without reliance on memory banks or entity-driven methods, offering a novel pathway for cross-modal alignment and opening new possibilities for the application of diffusion models in multi-modal tasks. The source code is available at: https://github.com/mongeoroo/diffusion-bridge

来源：[论文官方页面](https://openaccess.thecvf.com/content/CVPR2025/html/Lee_Diffusion_Bridge_Leveraging_Diffusion_Model_to_Reduce_the_Modality_Gap_CVPR_2025_paper.html)。

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

- [[Zotero Knowledge/Papers/ZK-CDHTS2WR - Learning Transferable Visual Models From Natural Language Supervision|Learning Transferable Visual Models From Natural Language Supervision]] — 强关联；本篇摘要提到模型 CLIP（仅确认名称提及）。
- [[Zotero Knowledge/Papers/ZK-BYZ75H5L - Connect, Collapse, Corrupt  Learning Cross-Modal Tasks with Uni-Modal Data|Connect, Collapse, Corrupt: Learning Cross-Modal Tasks with Uni-Modal Data]] — 强关联；共同研究内容：对比学习与跨模态编码、模态间隙。
- [[Zotero Knowledge/Papers/ZK-I6438ULU - Diffusion-Link  Diffusion Probabilistic Model for Bridging the Audio-Text Modality Ga|Diffusion-Link: Diffusion Probabilistic Model for Bridging the Audio-Text Modality Gap]] — 强关联；共同研究内容：对比学习与跨模态编码、扩散生成架构、模态间隙。
- [[Zotero Knowledge/Papers/ZK-WFNXHCV8 - Modality Gap-Driven Subspace Alignment Training Paradigm For Multimodal Large Languag|Modality Gap-Driven Subspace Alignment Training Paradigm For Multimodal Large Language Models]] — 强关联；共同研究内容：对比学习与跨模态编码、模态间隙。
- [[Zotero Knowledge/Papers/ZK-TGBY7QJ9 - AGFT  Alignment-Guided Fine-Tuning for Zero-Shot Adversarial Robustness of Vision-Lan|AGFT: Alignment-Guided Fine-Tuning for Zero-Shot Adversarial Robustness of Vision-Language Models]] — 中关联；共同研究内容：模态间隙。

<!-- content-relations:end -->

<!-- research-integration:start -->
## 研究主题入口

- [[Zotero Knowledge/Topics/06 Alignment & Reliability/Representation Alignment/索引|06 Alignment & Reliability/Representation Alignment]]
- [[Zotero Knowledge/Topics/02 Representation & Perception/Vision-Language Representation/索引|02 Representation & Perception/Vision-Language Representation]]

## 概念比较入口

- [[Zotero Knowledge/Concepts/跨模态对齐与模态间隙|跨模态对齐与模态间隙]]
<!-- research-integration:end -->
