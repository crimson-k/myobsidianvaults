---
type: "literature"
title: "LiT: Zero-Shot Transfer with Locked-image text Tuning"
aliases: ["LiT"]
zotero_keys: ["W84DWQI5"]
year: 2022
authors: ["Zhai, Xiaohua", "Wang, Xiao", "Mustafa, Basil", "Steiner, Andreas", "Keysers, Daniel", "Kolesnikov, Alexander", "Beyer, Lucas"]
venue: "CVPR 2022"
doi: ""
url: "https://arxiv.org/abs/2111.07991"
collections: ["02 Representation & Perception/Vision-Language Representation", "90 Projects/Pattern Recognition Course/Project 1/Group 2", "06 Alignment & Reliability/Adaptation & Generalization"]
tags: ["zotero", "literature", "course/pattern-recognition", "ppt/group-2", "concept/跨模态对齐与模态间隙", "concept/微调策略与泛化鲁棒性", "concept-primary/跨模态对齐与模态间隙"]
reading_status: "presentation-import"
ppt_role: "main"
ppt_pages: [10, 20]
imported_at: "2026-10-03"
---

# LiT: Zero-Shot Transfer with Locked-image text Tuning

[在 Zotero 打开](zotero://select/library/items/W84DWQI5) · [论文来源](https://arxiv.org/abs/2111.07991) · [论文 PDF](https://arxiv.org/pdf/2111.07991)

## 文献导读

锁定预训练图像编码器，只调整文本编码器以读出已有视觉表示。关注冻结位置与初始化方式如何影响零样本迁移和训练效率。

## 主题与关联

[[Zotero Knowledge/Topics/02 Representation & Perception/Vision-Language Representation/索引|02 Representation & Perception/Vision-Language Representation]] · [[Zotero Knowledge/Topics/90 Projects/Pattern Recognition Course/Project 1/索引|项目一文献分享]]

以下为阅读比较建议，并非已经证实的文献依赖关系。

- [[Zotero Knowledge/Papers/ZK-CDHTS2WR - Learning Transferable Visual Models From Natural Language Supervision|CLIP]]
- [[Zotero Knowledge/Papers/ZK-2IQ6RLSK - Sigmoid Loss for Language Image Pre-Training|SigLIP]]

## 原始摘要

This paper presents contrastive-tuning, a simple method employing contrastive training to align image and text models while still taking advantage of their pre-training. In our empirical study we find that locked pre-trained image models with unlocked text models work best. We call this instance of contrastive-tuning "Locked-image Tuning" (LiT), which just teaches a text model to read out good representations from a pre-trained image model for new tasks. A LiT model gains the capability of zero-shot transfer to new vision tasks, such as image classification or retrieval. The proposed LiT is widely applicable; it works reliably with multiple pre-training methods (supervised and unsupervised) and across diverse architectures (ResNet, Vision Transformers and MLP-Mixer) using three different image-text datasets. With the transformer-based pre-trained ViT-g/14 model, the LiT model achieves 85.2% zero-shot transfer accuracy on the ImageNet test set, and 82.5% on the challenging out-of-distribution ObjectNet test set.

来源：[论文官方页面](https://arxiv.org/abs/2111.07991)。

## PPT 文献分享原页

来源：[第 2 组原 PPT](../Assets/Original%20PPTs/%E9%A1%B9%E7%9B%AE%E4%B8%80%E7%AC%AC%E4%BA%8C%E7%BB%84%E6%96%87%E7%8C%AE%E5%88%86%E4%BA%AB%EF%BC%88%E4%BF%AE%E6%94%B9%E7%89%88%EF%BC%89.pptx)，原文件第 10–20 页。

页面图保留原图表、公式和排版；下方折叠文本供搜索。汇报中的解释、教学示例和实验数字均属于来源材料，尚未逐项对照论文全文复核。

### 原 PPT 第 10 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-010.png]]

> [!quote]- 本页可搜索文字
> LiT
>
> Zero-Shot Transfer with Locked-image Text Tuning
>
> 基于固定图像的文本调整机制的零样本迁移技术
>
> CVPR 2022
>
> Xiaohua Zhai, Xiao Wang, Basil Mustafa, Andreas Steiner, Daniel Keysers, Alexander Kolesnikov, Lucas Beyer. 
>
> Google Research
>
> 汇报人：2612189 闵孟宇
>
> 汇报日：2026/9/30
>

### 原 PPT 第 11 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-011.png]]

> [!quote]- 本页可搜索文字
> 汇报内容
>
> 迁移学习，零样本迁移，CLIP/ALIGN
>
> 研究动机
>
> 解耦与复用，Contrastive-tuning，LiT
>
> 研究方法
>
> 对外验证 →对内验证（整体到局部）→质量属性（Reliable、Efficient、Extensible）
>
> 实验设计
>
> 核心创新点，科研启示
>
> 总结与启发
>
> 01.
>
> 02.
>
> 03.
>
> 04.
>

### 原 PPT 第 12 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-012.png]]

> [!quote]- 本页可搜索文字
> 研究动机
>
> 研究方法
>
> 实验设计
>
> 总结与启发
>
> 迁移学习的范式与瓶颈
>
> Pre-train
>
> 大规模数据
> 学习通用图像表征
>
> Fine-tuning
>
> 任务特定监督数据
> 继续更新参数
>
> Downstream
>
> 分类 / 检测 / 医学图像…
>
> 缺点
>
> 每来一个新任务
>
> 仍需数据 + 微调
>
> Zero-shot Transfer
>
> 零样本迁移
>
> 不使用任务特定监督样本，不进行下游 fine-tuning，直接利用预训练知识完成迁移。
>

### 原 PPT 第 13 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-013.png]]

> [!quote]- 本页可搜索文字
> Image Tower
>
> 研究动机
>
> 研究方法
>
> 实验设计
>
> 总结与启发
>
> CLIP / ALIGN：Zero-shot 的已有解法与默认假设
>
> 默认假设
>
> Image Tower与 Text Tower都从头训练并共同更新
>
> Text Tower
>
> Image Embedding
>
> Text Embedding
>
> 图文对比学习
>
> Matched 更相似 UnMatched 更不同 
>
> 训练时
>
> 零样本迁移·eg猫狗分类
>
> image embedding
>
> “a photo of a cat”
> “a photo of a dog”
> 
>
> → 选择最相似文本
>
> text embedding
>
> ↓
>
> ↕计算相似度
>
> 一定最棒吗
>

### 原 PPT 第 14 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-014.png]]

> [!quote]- 本页可搜索文字
> 纯图像数据
>
> 优点：大规模，高质量
>
> 缺点：受限于预定义类别
>
> 研究动机
>
> 研究方法
>
> 实验设计
>
> 总结与启发
>
> LiT 的核心问题意识：为什么还要修改一个已经很强的图像塔？
>
> 问题：
>
> 已有高质量图像数据训练出的强image encoder时，
> 为什么还要在 noisy 图文数据上继续修改它？
>
> 强而通用的
> Image Encoder
>
> 两种数据
>
> 来源网页的图-文对
>
> 优点：语义范围广
>
> 缺点：noisy
>
> Image-Text对齐
>
> 更适合
>
> 更适合
>
> 所以：保护图像塔，让文本塔去“读懂” 图像空间。
>

### 原 PPT 第 15 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-015.png]]

> [!quote]- 本页可搜索文字
> 研究动机
>
> 研究方法
>
> 实验设计
>
> 总结与启发
>
> 核心思想：把“ 图像表征学习”与“图像-文本表征对齐”解耦
>
> 纯图像数据
>
> 学强图像表征
>
> 传统Contrastive Pre-training
>
> 同一份 image–text data
>
> Image Tower
>
> Text Tower
>
> Image Embedding
>
> Text Embedding
>
> 图-文
>
> 对比学习
>
> 自由的图文对
>
> 学习跨模态对齐
>
> LiT/Contrastive tuning
>
> 不同数据，各司其职
>

### 原 PPT 第 16 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-016.png]]

> [!quote]- 本页可搜索文字
> 研究动机
>
> 研究方法
>
> 实验设计
>
> 总结与启发
>
> Contrastive-tuning：以L / U / u 定义设计选择空间
>
> L
>
> U
>
> u
>
> 是否使用预训练模型：是
>
> 模型参数是否可更新：否
>
> 是否使用预训练模型：是
>
> 模型参数是否可更新：是
>
> 是否使用预训练模型：否
>
> 模型参数是否可更新：是
>
> CLIP / ALIGN
> 两塔从零训练
>
> uu
>
> 传统迁移学习，
>
> Pretrained->微调
>
> Uu
>
> LiT
>
> Locked image
>
>  tower
>
> Lu
>

### 原 PPT 第 17 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-017.png]]

> [!quote]- 本页可搜索文字
> 研究动机
>
> 研究方法
>
> 实验设计
>
> 总结与启发
>
> 实验设计
>
> SOTA Comparison
>
> Design Choices
>
> Image Pre-training
>
> Text Model
>
> De-duplication
>
> Technical Advantages
>
> Multilingual
>
> 实验逻辑：对外验证 →对内验证（整体到局部）→质量属性（Reliable、Efficient、Extensible）
>
> 在多个数据集上与已有SOTA比较，验证LiT 作为一个完整方法到底有没有效果
>
> 比较 L、U、u不同组合，使用不同超参及不同规模数据集验证LiT更优
>
> 什么样的图像塔最优？比较了图像塔的训练方式以及通用性的影响
>
> 什么样的文本塔最优？比较了图像塔的参数初始化方式、架构、数据量的影响
>
> 判断上下游任务的重复样本带来的数据泄露是否影响结果
>
> 分析LiT在工程上的优势，比如减少显存和训练时间
>
> 分析LiT能否扩展到非英语语言
>

### 原 PPT 第 18 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-018.png]]

> [!quote]- 本页可搜索文字
> 研究动机
>
> 研究方法
>
> 实验设计
>
> 总结与启发
>
> 创新总结
>
> Paper Fig. 3, Table 2, Fig. 4; §5.2
>
> 12 / 14
>
> 1
>
> Contrastive-tuning与LiT
>
> 重新审视传统图文对比学习的训练方式。不再默认图像塔和文本塔都必须从头联合训练，而是系统研究如何复用已有预训练模型进行图文对齐，并得到 LiT
>
> 2
>
> 问题解耦
>
> Decouple
>
> LiT 将传统图文对比学习解耦：先利用高质量视觉数据学习强 representation，再利用开放图文数据学习 vision-language alignment，让不同数据各自完成更擅长的任务。
>
> 3
>
> 模型复用
>
> Reuse
>
> Pretrained model 不应只被视为继续 fine-tuning 的 initialization，也可以作为已经积累好的 knowledge asset。对于已经具备的能力直接保留，只学习新任务真正缺失的部分。
>
> 方法创新
>
> 思想创新
>
> 思想创新
>

### 原 PPT 第 19 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-019.png]]

> [!quote]- 本页可搜索文字
> 研究动机
>
> 研究方法
>
> 实验设计
>
> 总结与启发
>
> 研究演进
>
> Paper Fig. 3, Table 2, Fig. 4; §5.2
>
> 12 / 14
>
> SigLiT
>
> ICCV2023
>
> 受启发：继续质疑默认设计是否有必要
>
> 取消默认的global softmax normalization，将Global Softmax 转为Pairwise Sigmoid
>
> LiT-Decoder
>
> CVPR2023
>
> 受启发：LiT能否用于更复杂任务
>
> 将把test encoder换成一个生成式 decoder,把研究范围扩展到了 captioning、VQA 和 OCR 等多任务视觉问题
>
> BLIP-2
>
> ICML2023
>
> 受启发：Image Encoder 和LLM 都很好，为什么要重新训练任何一端？
>
> 两端冻结，只训练一个轻量的桥梁，让两个已经训练好的强模型能够交流。
>
> LiT 的价值不只是“冻结 Image Encoder”，而是一种做减法的研究思维。
>
> 不盲目增加模型复杂度，而是重新审视默认范式，识别“不必要的学习”，解耦不同目标，并最大化复用已有知识。
>
> 核心启发
>

### 原 PPT 第 20 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-020.png]]

> [!quote]- 本页可搜索文字
> THANK YOU
>
> 谢谢聆听
>
> Q & A
>
> 14 / 14
>

## 我的阅读与思考

<!-- 在此补充个人笔记；导入内容与个人结论分开记录。 -->

[[Zotero Knowledge/知识库首页|知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-28MFNY9F - CLIP is Strong Enough to Fight Back  Test-time Counterattacks towards Zero-shot Adver|CLIP is Strong Enough to Fight Back: Test-time Counterattacks towards Zero-shot Adversarial Robustness of CLIP]] — 中关联；共同研究内容：对比学习与跨模态编码、鲁棒性与域外泛化。
- [[Zotero Knowledge/Papers/ZK-W8UL68IN - Fine-Tuning can Distort Pretrained Features and Underperform Out-of-Distribution|Fine-Tuning can Distort Pretrained Features and Underperform Out-of-Distribution]] — 中关联；共同研究内容：鲁棒性与域外泛化。

<!-- content-relations:end -->

<!-- research-integration:start -->
## 研究主题入口

- [[Zotero Knowledge/Topics/02 Representation & Perception/Vision-Language Representation/索引|02 Representation & Perception/Vision-Language Representation]]
- [[Zotero Knowledge/Topics/06 Alignment & Reliability/Adaptation & Generalization/索引|06 Alignment & Reliability/Adaptation & Generalization]]

## 概念比较入口

- [[Zotero Knowledge/Concepts/跨模态对齐与模态间隙|跨模态对齐与模态间隙]]
- [[Zotero Knowledge/Concepts/微调策略与泛化鲁棒性|微调策略与泛化鲁棒性]]
<!-- research-integration:end -->
