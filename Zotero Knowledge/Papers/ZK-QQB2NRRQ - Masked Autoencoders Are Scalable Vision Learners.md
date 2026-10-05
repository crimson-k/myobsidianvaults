---
type: "literature"
title: "Masked Autoencoders Are Scalable Vision Learners"
aliases: ["MAE"]
zotero_keys: ["QQB2NRRQ"]
year: 2022
authors: ["He, Kaiming", "Chen, Xinlei", "Xie, Saining", "Li, Yanghao", "Dollár, Piotr", "Girshick, Ross"]
venue: "CVPR 2022"
doi: ""
url: "https://arxiv.org/abs/2111.06377"
collections: ["02 Representation & Perception/Visual Representation Learning", "90 Projects/Pattern Recognition Course/Project 1/Group 1"]
tags: ["zotero", "literature", "course/pattern-recognition", "ppt/group-1"]
reading_status: "presentation-import"
ppt_role: "main"
ppt_pages: [15, 41]
imported_at: "2026-10-03"
---

# Masked Autoencoders Are Scalable Vision Learners

[在 Zotero 打开](zotero://select/library/items/QQB2NRRQ) · [论文来源](https://arxiv.org/abs/2111.06377) · [论文 PDF](https://arxiv.org/pdf/2111.06377)

## 文献导读

通过高比例随机遮挡构造图像重建任务，编码器只处理可见 patch，轻量解码器恢复像素。适合与对比学习比较预训练目标、计算成本及下游微调协议。

## 主题与关联

[[Zotero Knowledge/Topics/02 Representation & Perception/Visual Representation Learning/索引|02 Representation & Perception/Visual Representation Learning]] · [[Zotero Knowledge/Topics/90 Projects/Pattern Recognition Course/Project 1/索引|项目一文献分享]]

以下为阅读比较建议，并非已经证实的文献依赖关系。

- [[Zotero Knowledge/Papers/ZK-YMBWZADV - A Simple Framework for Contrastive Learning of Visual Representations|SimCLR]]
- [[Zotero Knowledge/Papers/ZK-3D4I5WS2 - Understanding Geometric Representations in Self-Supervised Vision Transformers via Su|Geometric Subspace Intervention]]
- [[Zotero Knowledge/Papers/ZK-MWND3NJ9 - Self-Supervised Visual Representation Learning  Pretrain-Finetuning or Joint Training|PFT vs JT]]

## 原始摘要

This paper shows that masked autoencoders (MAE) are scalable self-supervised learners for computer vision. Our MAE approach is simple: we mask random patches of the input image and reconstruct the missing pixels. It is based on two core designs. First, we develop an asymmetric encoder-decoder architecture, with an encoder that operates only on the visible subset of patches (without mask tokens), along with a lightweight decoder that reconstructs the original image from the latent representation and mask tokens. Second, we find that masking a high proportion of the input image, e.g., 75%, yields a nontrivial and meaningful self-supervisory task. Coupling these two designs enables us to train large models efficiently and effectively: we accelerate training (by 3x or more) and improve accuracy. Our scalable approach allows for learning high-capacity models that generalize well: e.g., a vanilla ViT-Huge model achieves the best accuracy (87.8%) among methods that use only ImageNet-1K data. Transfer performance in downstream tasks outperforms supervised pre-training and shows promising scaling behavior.

来源：[论文官方页面](https://arxiv.org/abs/2111.06377)。

## PPT 文献分享原页

来源：[第 1 组原 PPT](file:///C:/Users/amber/Documents/xwechat_files/wxid_ojd0ni9ss2gz12_0e91/msg/file/2026-09/%E9%A1%B9%E7%9B%AE%E4%B8%80%E7%AC%AC1%E5%B0%8F%E7%BB%84%281%29.pptx)，原文件第 15–41 页。

页面图保留原图表、公式和排版；下方折叠文本供搜索。汇报中的解释、教学示例和实验数字均属于来源材料，尚未逐项对照论文全文复核。

### 原 PPT 第 15 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-015.png]]

> [!quote]- 本页可搜索文字
> Masked Autoencoders Are Scalable Vision Learners. 
>
> 2612120 娄雅婷
>
> 项目第一组 序号2
>
> 2026/9/23
>
> 文献汇报
>

### 原 PPT 第 16 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-016.png]]

> [!quote]- 本页可搜索文字
> 目录
>
> CONTENTS
>
> 01
>
> 研究动机
>
> 02
>
> 现存痛点
>
> 03
>
> 解决方案
>
> 04
>
> 核心创新
>
> 05
>
> 有效性论证
>
> 06
>
> 结论与启发
>

### 原 PPT 第 17 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-017.png]]

> [!quote]- 本页可搜索文字
> 01
>
> 研究动机
>

### 原 PPT 第 18 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-018.png]]

> [!quote]- 本页可搜索文字
> 01
>
> 研究动机
>
> 在硬件快速发展的背景下，视觉模型很容易在一百万个图像上出现过拟合，并开始需要未公开的数亿张带标签图像。
>
> 研究背景
>
> 大模型越来越依赖海量标注数据：
>
> 是什么使得视觉和语言中的掩码自动编码有所不同？为什么 BERT 式的掩码自动编码在 NLP 中如此成功，而此前在视觉中却没有表现出同样的可扩展性？
>
> 在自然语言处理（NLP）中，自监督预训练能满足以上数据需求。主要包括基于GPT中的自回归语言建模和BERT中的掩码自动编码这两种解决方案， BERT式即去除一部分数据，并学习预测被去除的内容。这些方法现在能够训练包含超过一千亿参数的可泛化NLP模型。
>

### 原 PPT 第 19 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-019.png]]

> [!quote]- 本页可搜索文字
> 02
>
> 现存痛点
>

### 原 PPT 第 20 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-020.png]]

> [!quote]- 本页可搜索文字
> 02
>
> 现存痛点
>
> 在视觉领域，卷积网络（CNN）在过去十年中占据主导地位。卷积通常在规则网格上运行，将BERT中的诸如掩码 token 或位置嵌入等指示符集成到卷积网络中并非易事。
>
> 然而，随着视觉Transformer（ViT）的引入，这一架构差距已得到解决，不应再构成障碍。
>
> 图像 X 被切成 Patch：X={, ……, } 以后就和 NLP 的token 序列有了结构上的相似性。所以 ViT 为视觉的掩码自动编码提供了合适架构。
>
> 视觉和语言的架构不同
>

### 原 PPT 第 21 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-021.png]]

> [!quote]- 本页可搜索文字
> 02
>
> 现存痛点
>
> 语言是人类生成的信号，具有高度的语义性和信息密集性。当训练一个模型仅预测每个句子中几个缺失的单词时，这个任务似乎会引导出复杂的语言理解。
>
> 相反，图像是具有大量空间冗余的自然信号。例如，一个缺失的块可以从相邻块中恢复，而几乎不需要对部分、对象和场景有高级别的理解。
>
> 为了克服这种差异并鼓励学习有用的特征，论文表明一种简单的策略在计算机视觉中效果很好：掩码很大一部分随机块。这种策略在很大程度上减少了冗余，并创建了一个具有挑战性的自监督任务，该任务需要超越低级图像统计的整体理解。
>
> 语言和视觉之间的信息密度不同
>

### 原 PPT 第 22 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-022.png]]

> [!quote]- 本页可搜索文字
> 02
>
> 现存痛点
>
> 自动编码器的解码器将潜在表示映射回输入，在重建文本和图像时发挥不同作用。
>
> 在视觉中，解码器重建像素，因此其输出的语义级别低于常见的识别任务。这与语言相反。
>
> 在语言中，解码器预测包含丰富语义信息的缺失单词。虽然在BERT中解码器可以很简单（一个多层感知器），但论文发现对于图像，解码器设计在确定学习到的潜在表示的语义级别方面起着关键作用。
>
> 视觉解码器和语言解码器的角色不同
>

### 原 PPT 第 23 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-023.png]]

> [!quote]- 本页可搜索文字
> 03
>
> 解决方案
>

### 原 PPT 第 24 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-024.png]]

> [!quote]- 本页可搜索文字
> 图像
>
> 划分补丁
>
> 随机采样补丁，掩码75%，可见25%
>
> 对可见补丁使用重型ViT编码器
>
> 编码的可见补丁组合掩码token
>
> 轻量型解码器
>
> 预测掩码补丁，重建目标
>
> 论文提出了一种简单、有效且可扩展的非对称掩码自动编码器（MAE）形式用于视觉表示学习
>
> 03
>
> 解决方案
>

### 原 PPT 第 25 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-025.png]]

> [!quote]- 本页可搜索文字
> 随机采样补丁
>
> 将图像划分为规则的非重叠块，然后对补丁的一个子集按照均匀分布对随机补丁进行采样，不进行替换，并屏蔽（即删除）剩余的补丁。
>
> 具有高掩蔽率的随机采样（即去除的补丁的比率）在很大程度上消除了冗余，从而创建了一个无法通过从可见相邻补丁进行外推来轻松解决的任务。均匀分布防止了潜在的中心偏差，即图像中心附近有更多的遮蔽斑块。
>

### 原 PPT 第 26 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-026.png]]

> [!quote]- 本页可搜索文字
> MAE编码器
>
> 采用ViT编码器仅适用于可见的、未屏蔽的补丁。同标准ViT中一样，MAE编码器通过线性投影嵌入补丁，并添加位置嵌入，然后通过一系列Transformer块处理结果集。但MAE的编码器仅对全集的一小部分（25%）进行操作。移除遮蔽的补丁，不使用掩码令牌。这能够仅用有限的计算和内存来训练非常大的编码器。
>
> MAE解码器
>
> MAE解码器的输入是由编码的可见补丁和掩码token组成的全套token。每个掩码token都是一个共享的学习向量，指示是否存在要预测的遗漏补丁。为这个完整集合中的所有标记添加位置嵌入。
>
> MAE解码器仅在预训练期间用于执行图像重建任务。因此，解码器架构可以以独立于编码器设计的方式灵活设计。尝试使用非常小的解码器，比编码器更窄、更低。通过这种非对称设计，全套token仅由轻量级解码器处理，这大大缩短了预训练时间。
>

### 原 PPT 第 27 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-027.png]]

> [!quote]- 本页可搜索文字
> 重建目标
>
> MAE通过预测每个蒙版补丁的像素值来重建输入。解码器输出中的每个元素都是表示补丁的像素值向量，将其整形以形成重建图像。损失函数计算像素空间中重建图像和原始图像之间的均方误差（MSE）。
>
> MAE预训练
>
> 首先为每个输入补丁生成一个token。然后根据掩码比率随机关闭令牌列表并删除列表的最后一部分。此过程为编码器生成一小部分tokens，相当于在不替换的情况下对补丁进行采样。编码后将掩码标记列表附加到编码补丁列表中，并取消覆盖此完整列表，以将所有标记与其目标对齐。解码器应用于此添加了位置嵌入的完整列表。不需要稀疏操作，这种简单的实现引入的开销可以忽略不计，因为操作很快。
>

### 原 PPT 第 28 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-028.png]]

> [!quote]- 本页可搜索文字
> 04
>
> 核心创新
>

### 原 PPT 第 29 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-029.png]]

> [!quote]- 本页可搜索文字
> 04
>
> 核心创新
>
> 传统 Autoencoder
>
> MAE
>
> VS
>
> 传统的自动编码器将完整图像输入，之后采用重型编码器和重型解码器。
>
> 在MAE的非对称编码器—解码器中将掩码token转移到轻量型解码器会让计算量大幅减少。在这种设计下，非常高的掩码比例可以实现双赢：它优化了准确性，同时允许编码器仅处理一小部分的补丁，这可以将整体预训练时间减少或更多。同样减少内存消耗，使我们能够轻松地将MAE扩展到大型模型。
>
> 完整图像输入
>
> 重型编码器
>
> 重型解码器
>
> 可见补丁25%
>
> 重型编码器
>
> 完整token
>
> 轻量型解码器
>
> MAE 采用非对称编码器解码器
>

### 原 PPT 第 30 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-030.png]]

> [!quote]- 本页可搜索文字
> 04
>
> 核心创新
>
> MAE 采用非常高的掩码比例
>
> 高掩蔽率（75%）适用于精细调节和线性探索。
>

### 原 PPT 第 31 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-031.png]]

> [!quote]- 本页可搜索文字
> 04
>
> 核心创新
>
> MAE 的效率与可扩展性
>
> 掩码75%
>
> 编码器仅编码可见补丁25%
>
> FLOP减少3.3倍
>
> 2.8∼4.1倍加速
>

### 原 PPT 第 32 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-032.png]]

> [!quote]- 本页可搜索文字
> 05
>
> 有效性论证
>

### 原 PPT 第 33 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-033.png]]

> [!quote]- 本页可搜索文字
> 05
>
> 有效性论证
>
> 消融实验
>
> 探究 MAE 的性能来自哪里
>
> Ablation（消融实验）
>
> 主要结论
>
> Mask Ratio
>
> 75% 附近为最优
>
> Decoder depth
>
> 深度解码器可以提高线性探测精度
>
> Decoder width
>
> 解码器可以比编码器窄。
>
> Mask Token
>
> 没有掩码token的编码器更准确、更快
>
> Reconstruction
>
> 像素作为重建目标是有效的
>
> Augmentation
>
> 不依赖复杂增强
>
> Mask Strategy
>
> 随机采样效果最好
>
> MAE 的有效性不是依赖复杂组件，而是来自几个简单但彼此匹配的设计。
>

### 原 PPT 第 34 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-034.png]]

> [!quote]- 本页可搜索文字
> 05
>
> 有效性论证
>
> ImageNet-1K Results：与主流自监督方法比较
>
> 实验结果
>
> MAE在自监督预训练中，仅使用 ImageNet-1K 数据，无外部数据。得到的收益非常明显，精准度高，最高达到87.8%，且更简单更快。
>
> MAE可以很容易地扩大规模，并且与更大的模型相比有了稳步的改进：
>
> 从ViT-B  ViT-L  ViT-H
>
> 模型容量增大⇒表现增强
>
> 实验结论
>
> 但是实验重点不只是绝对的准确率，而是 MAE 可以稳定扩展到高容量 ViT。
>

### 原 PPT 第 35 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-035.png]]

> [!quote]- 本页可搜索文字
> 05
>
> 有效性论证
>
> MAE 预训练与监督预训练
>
> 实验结果
>
> 实验结论
>
> MAE的监督训练效果相比ViT原始论文中的ViT-L在IN1K中训练时会退化，其监督训练效果更好，但准确性饱和。
>
> MAE预训练仅使用IN1K，可以更好地通用化。对于容量更大的模型，从头开始训练的收益更大。MAE可以帮助扩大模型尺寸。
>

### 原 PPT 第 36 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-036.png]]

> [!quote]- 本页可搜索文字
> 05
>
> 有效性论证
>
> MAE 的部分微调
>
> 实验结果
>
> 实验结论
>
> 研究了一种部分微调协议：微调最后几层，同时冻结其他层。仅微调一个变压器块，可以显著提高精度，微调几个块可以获得接近全微调的精度。
>
> 与一种同ViT-L结果相对的MoCo v3方法进行比较。MoCo v3具有较高的线性探测精度但其所有部分精细调谐结果都比MAE差。
>
> 线性可分离性不是评估表示质量的唯一指标。线性探测与迁移学习性没有很好的相关性。
>

### 原 PPT 第 37 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-037.png]]

> [!quote]- 本页可搜索文字
> 05
>
> 有效性论证
>
> MAE 的迁移学习
>
> COCO上端到端地微调Mask R-CNN， MAE在所有配置下目标检测方面都表现更好
>
> 使用UperNet在ADE20K上进行实验，与监督预训练相比，MAE的预训练在语义分割方面显著提高了结果，基于像素的MAE也优于基于token的BEiT。与COCO的结果一致。
>

### 原 PPT 第 38 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-038.png]]

> [!quote]- 本页可搜索文字
> 05
>
> 有效性论证
>
> MAE 的迁移学习
>
> MAE不是ImageNet的专用特征，而是一般视觉表现
>
> 在iNaturalists上，MAE在完成分类任务时显示出很强的缩放行为：随着模型的增大，精度会大大提高。MAE远远超过了之前的最佳结果。在Places上，MAE表现优于之前的最佳结果。
>
> 比较作为MAE重建目标的像素与token 。虽然使用dVAE令牌优于使用非标准化像素，但在所有测试中它在统计上与使用标准化像素相似。表明MAE不需要标记化。
>

### 原 PPT 第 39 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-039.png]]

> [!quote]- 本页可搜索文字
> 06
>
> 结论与启发
>

### 原 PPT 第 40 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-040.png]]

> [!quote]- 本页可搜索文字
> 06
>
> 结论与启发
>
> MAE 的贡献不是发明了“遮住图像再恢复”这个想法，而是找到了掩码自动编码真正在视觉大模型上有效且可扩展的设计原则。
>
> 扩展良好的简单算法是深度学习的核心。简单方法如果具有好的缩放属性，价值可能高于复杂方法。
>
> 在计算机视觉中，尽管自监督学习取得了进展，但实际的预训练范式仍主要受到监督。在这项研究中的ImageNet和迁移学习中观察到，自动编码器——一种类似于NLP技术的简单自监督方法——提供了可扩展的好处。视觉中的自我监督学习现在可能正走上与NLP类似的轨道。
>
> 另一方面，图像和语言是不同性质的信号，必须仔细处理这种差异。图像只是记录的光，没有语义分解为单词的视觉模拟。我们不尝试删除对象，而是重新移动最有可能不会形成语义段的随机补丁。同样，MAE重建像素，这些像素不是语义实体。然而MAE能够推断出复杂的整体重构，表明它已经学习了许多视觉概念，即语义。假设这种行为是通过MAE内部丰富的隐藏表示方式发生的。希望这一观点将激励未来的工作。
>

### 原 PPT 第 41 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-041.png]]

> [!quote]- 本页可搜索文字
> 感谢老师指导
>
> 文献汇报
>
> 2612120 娄雅婷
>
> 项目第一组 序号2
>
> 2026/9/23
>

## 我的阅读与思考

<!-- 在此补充个人笔记；导入内容与个人结论分开记录。 -->

[[Zotero Knowledge/知识库首页|知识库首页]]
