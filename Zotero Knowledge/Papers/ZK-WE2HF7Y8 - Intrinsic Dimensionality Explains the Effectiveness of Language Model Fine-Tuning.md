---
type: "literature"
title: "Intrinsic Dimensionality Explains the Effectiveness of Language Model Fine-Tuning"
aliases: ["Intrinsic Dimensionality"]
zotero_keys: ["WE2HF7Y8"]
year: 2021
authors: ["Aghajanyan, Armen", "Zettlemoyer, Luke", "Gupta, Sonal"]
venue: "ACL-IJCNLP 2021"
doi: ""
url: "https://arxiv.org/abs/2012.13255"
collections: ["06 Alignment & Reliability/Adaptation & Generalization", "90 Projects/Pattern Recognition Course/Project 1/Group 1"]
tags: ["zotero", "literature", "course/pattern-recognition", "ppt/group-1"]
reading_status: "presentation-import"
ppt_role: "extension"
ppt_pages: [59, 59]
imported_at: "2026-10-03"
---

# Intrinsic Dimensionality Explains the Effectiveness of Language Model Fine-Tuning

[在 Zotero 打开](zotero://select/library/items/WE2HF7Y8) · [论文来源](https://arxiv.org/abs/2012.13255) · [论文 PDF](https://arxiv.org/pdf/2012.13255)

## 文献导读

用有效内在维度解释语言模型微调所需的少量自由度，是 PPT 中引出 LoRA 的前置阅读。本文仅在第一组第 59 页被介绍，没有独立完整汇报。

## 主题与关联

[[Zotero Knowledge/Topics/06 Alignment & Reliability/Adaptation & Generalization/索引|06 Alignment & Reliability/Adaptation & Generalization]] · [[Zotero Knowledge/Topics/90 Projects/Pattern Recognition Course/Project 1/索引|项目一文献分享]]

以下为阅读比较建议，并非已经证实的文献依赖关系。

- [[Zotero Knowledge/Papers/ZK-SE2PQKZ8 - LoRA  Low-Rank Adaptation of Large Language Models|LoRA]]

## 原始摘要

Although pretrained language models can be fine-tuned to produce state-of-the-art results for a very wide range of language understanding tasks, the dynamics of this process are not well understood, especially in the low data regime. Why can we use relatively vanilla gradient descent algorithms (e.g., without strong regularization) to tune a model with hundreds of millions of parameters on datasets with only hundreds or thousands of labeled examples? In this paper, we argue that analyzing fine-tuning through the lens of intrinsic dimension provides us with empirical and theoretical intuitions to explain this remarkable phenomenon. We empirically show that common pre-trained models have a very low intrinsic dimension; in other words, there exists a low dimension reparameterization that is as effective for fine-tuning as the full parameter space. For example, by optimizing only 200 trainable parameters randomly projected back into the full space, we can tune a RoBERTa model to achieve 90\% of the full parameter performance levels on MRPC. Furthermore, we empirically show that pre-training implicitly minimizes intrinsic dimension and, perhaps surprisingly, larger models tend to have lower intrinsic dimension after a fixed number of pre-training updates, at least in part explaining their extreme effectiveness. Lastly, we connect intrinsic dimensionality with low dimensional task representations and compression based generalization bounds to provide intrinsic-dimension-based generalization bounds that are independent of the full parameter count.

来源：[论文官方页面](https://arxiv.org/abs/2012.13255)。

## PPT 文献分享原页

来源：[第 1 组原 PPT](../Assets/Original%20PPTs/%E9%A1%B9%E7%9B%AE%E4%B8%80%E7%AC%AC1%E5%B0%8F%E7%BB%84%281%29.pptx)，原文件第 59–59 页。

页面图保留原图表、公式和排版；下方折叠文本供搜索。汇报中的解释、教学示例和实验数字均属于来源材料，尚未逐项对照论文全文复核。

> 本文是延伸阅读，共享一张后续工作介绍页，PPT 没有对它进行完整独立汇报。

### 原 PPT 第 59 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-059.png]]

> [!quote]- 本页可搜索文字
> 思路启发：从低维适配到低秩更新
>
> 前置工作
>
> Aghajanyan et al.
>
> Intrinsic Dimensionality Explains the Effectiveness of Language Model Fine-Tuning
>
> ACL-IJCNLP 2021 (Outstanding Paper)
>
> 现象:模型参数很多，但任务适配只需要较少有效自由度。
>
> LoRA的思想迁移
>
> 1
>
> 启发，而未进行严格
>
> 数学推导
>
> LoRA 的进一步假设：
>
> 权重更新 ΔW 具有低内在秩
>
> 对 ΔW 做低秩参数化
>
> 受到前人工作启发，考虑低内在维度问题
>
> 2
>
> 任务适配只需要少数有效方向
>
> 3
>
> 4
>
> 59
>

## 我的阅读与思考

<!-- 在此补充个人笔记；导入内容与个人结论分开记录。 -->

[[Zotero Knowledge/知识库首页|知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-SE2PQKZ8 - LoRA  Low-Rank Adaptation of Large Language Models|LoRA: Low-Rank Adaptation of Large Language Models]] — 强关联；共同研究内容：低秩与参数高效微调、语言模型与语言表征。
- [[Zotero Knowledge/Papers/ZK-RAH7V3N7 - Low-Rank Rescaled Vision Transformer Fine-Tuning  A Residual Design Approach|Low-Rank Rescaled Vision Transformer Fine-Tuning: A Residual Design Approach]] — 中关联；共同研究内容：低秩与参数高效微调。

<!-- content-relations:end -->
