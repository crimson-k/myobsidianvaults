---
type: "literature"
title: "SigLIP 2: Multilingual Vision-Language Encoders with Improved Semantic Understanding, Localization, and Dense Features"
aliases: ["SigLIP 2"]
zotero_keys: ["TVYG4KJ8"]
year: 2025
authors: ["Tschannen, Michael", "Gritsenko, Alexey", "Wang, Xiao", "Naeem, Muhammad Ferjad", "Alabdulmohsin, Ibrahim", "Parthasarathy, Nikhil", "Evans, Talfan", "Beyer, Lucas", "Xia, Ye", "Mustafa, Basil", "Hénaff, Olivier", "Harmsen, Jeremiah", "Steiner, Andreas", "Zhai, Xiaohua"]
venue: "arXiv"
doi: ""
url: "https://arxiv.org/abs/2502.14786"
collections: ["02 Representation & Perception/Vision-Language Representation", "90 Projects/Pattern Recognition Course/Project 1/Group 2"]
tags: ["zotero", "literature", "course/pattern-recognition", "ppt/group-2"]
reading_status: "presentation-import"
ppt_role: "extension"
ppt_pages: [53, 53]
imported_at: "2026-10-03"
---

# SigLIP 2: Multilingual Vision-Language Encoders with Improved Semantic Understanding, Localization, and Dense Features

[在 Zotero 打开](zotero://select/library/items/TVYG4KJ8) · [论文来源](https://arxiv.org/abs/2502.14786) · [论文 PDF](https://arxiv.org/pdf/2502.14786)

## 文献导读

延伸 SigLIP，结合多语言训练与更丰富的学习目标改进语义、定位和密集特征。PPT 仅在第二组第 53 页介绍，应进一步核读原论文。

## 主题与关联

[[Zotero Knowledge/Topics/02 Representation & Perception/Vision-Language Representation/索引|02 Representation & Perception/Vision-Language Representation]] · [[Zotero Knowledge/Topics/90 Projects/Pattern Recognition Course/Project 1/索引|项目一文献分享]]

以下为阅读比较建议，并非已经证实的文献依赖关系。

- [[Zotero Knowledge/Papers/ZK-2IQ6RLSK - Sigmoid Loss for Language Image Pre-Training|SigLIP]]

## 原始摘要

We introduce SigLIP 2, a family of new multilingual vision-language encoders that build on the success of the original SigLIP. In this second iteration, we extend the original image-text training objective with several prior, independently developed techniques into a unified recipe -- this includes captioning-based pretraining, self-supervised losses (self-distillation, masked prediction) and online data curation. With these changes, SigLIP 2 models outperform their SigLIP counterparts at all model scales in core capabilities, including zero-shot classification, image-text retrieval, and transfer performance when extracting visual representations for Vision-Language Models (VLMs). Furthermore, the new training recipe leads to significant improvements on localization and dense prediction tasks. We also train variants which support multiple resolutions and preserve the input's native aspect ratio. Finally, we train on a more diverse data-mixture that includes de-biasing techniques, leading to much better multilingual understanding and improved fairness. To allow users to trade off inference cost with performance, we release model checkpoints at four sizes: ViT-B (86M), L (303M), So400m (400M), and g (1B).

来源：[论文官方页面](https://arxiv.org/abs/2502.14786)。

## PPT 文献分享原页

来源：[第 2 组原 PPT](../Assets/Original%20PPTs/%E9%A1%B9%E7%9B%AE%E4%B8%80%E7%AC%AC%E4%BA%8C%E7%BB%84%E6%96%87%E7%8C%AE%E5%88%86%E4%BA%AB%EF%BC%88%E4%BF%AE%E6%94%B9%E7%89%88%EF%BC%89.pptx)，原文件第 53–53 页。

页面图保留原图表、公式和排版；下方折叠文本供搜索。汇报中的解释、教学示例和实验数字均属于来源材料，尚未逐项对照论文全文复核。

> 本文是延伸阅读，共享一张后续工作介绍页，PPT 没有对它进行完整独立汇报。

### 原 PPT 第 53 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-053.png]]

> [!quote]- 本页可搜索文字
> 延伸
>
> 15
>
> SigLIP 2（2025，Google）
>
> 动机：补原版两个短板 —— 多语言强但英文变弱；只做全局图文匹配，密集特征与定位能力弱。
>
> 手段：加入 captioning 生成式目标、用冻结教师做自蒸馏、掩码预测类目标（TIPS）、多语言数据扩充与去偏。
>
> 结果：多语言与英文同时提升，密集特征和定位任务明显改善，同等性能下训练更省。
>
> 档位：B / L / So400m / g，并新增可变分辨率的 NaFlex 版本。
>
> 被大量多模态模型当作视觉塔
>
> 后续工作
>
> 使用
>
> PaLI-3（同组，2023）
>
> 直接以 SigLIP 作视觉塔
>
> PaliGemma / PaliGemma 2（2024）
>
> 视觉塔为 SigLIP-So400m
>
> Idefics2（HuggingFace, 2024）
>
> 使用 SigLIP-SO400M
>
> Gemma 3（2025）
>
> SigLIP 系视觉编码器
>
> Prismatic VLMs / OpenVLA（2024）
>
> DINOv2 + SigLIP 特征融合
>
> 值得注意的分工：SigLIP 管语义对齐，DINOv2 管空间细节 —— 恰好补上原版密集特征的短板。
>
> 一篇只改损失函数的论文，最后成了多模态模型视觉编码器的常见默认选项之一。
>

## 我的阅读与思考

<!-- 在此补充个人笔记；导入内容与个人结论分开记录。 -->

[[Zotero Knowledge/知识库首页|知识库首页]]
