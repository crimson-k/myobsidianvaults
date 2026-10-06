---
type: "literature"
title: "Learning Transferable Visual Models From Natural Language Supervision"
aliases: ["CLIP"]
zotero_keys: ["CDHTS2WR"]
year: 2021
authors: ["Radford, Alec", "Kim, Jong Wook", "Hallacy, Chris", "Ramesh, Aditya", "Goh, Gabriel", "Agarwal, Sandhini", "Sastry, Girish", "Askell, Amanda", "Mishkin, Pamela", "Clark, Jack", "Krueger, Gretchen", "Sutskever, Ilya"]
venue: "ICML 2021"
doi: ""
url: "https://arxiv.org/abs/2103.00020"
collections: ["02 Representation & Perception/Vision-Language Representation", "90 Projects/Pattern Recognition Course/Project 1/Group 2"]
tags: ["zotero", "literature", "course/pattern-recognition", "ppt/group-2"]
reading_status: "presentation-import"
ppt_role: "main"
ppt_pages: [1, 9]
imported_at: "2026-10-03"
---

# Learning Transferable Visual Models From Natural Language Supervision

[在 Zotero 打开](zotero://select/library/items/CDHTS2WR) · [论文来源](https://arxiv.org/abs/2103.00020) · [论文 PDF](https://arxiv.org/pdf/2103.00020)

## 文献导读

通过大规模图文对比学习形成共享嵌入空间，使用文字描述构造零样本分类器。阅读时区分预训练数据量、提示模板、零样本与有监督评测。

## 主题与关联

[[Zotero Knowledge/Topics/02 Representation & Perception/Vision-Language Representation/索引|02 Representation & Perception/Vision-Language Representation]] · [[Zotero Knowledge/Topics/90 Projects/Pattern Recognition Course/Project 1/索引|项目一文献分享]]

以下为阅读比较建议，并非已经证实的文献依赖关系。

- [[Zotero Knowledge/Papers/ZK-W84DWQI5 - LiT  Zero-Shot Transfer with Locked-image text Tuning|LiT]]
- [[Zotero Knowledge/Papers/ZK-2IQ6RLSK - Sigmoid Loss for Language Image Pre-Training|SigLIP]]
- [[Zotero Knowledge/Papers/ZK-BYZ75H5L - Connect, Collapse, Corrupt  Learning Cross-Modal Tasks with Uni-Modal Data|C3]]

## 原始摘要

State-of-the-art computer vision systems are trained to predict a fixed set of predetermined object categories. This restricted form of supervision limits their generality and usability since additional labeled data is needed to specify any other visual concept. Learning directly from raw text about images is a promising alternative which leverages a much broader source of supervision. We demonstrate that the simple pre-training task of predicting which caption goes with which image is an efficient and scalable way to learn SOTA image representations from scratch on a dataset of 400 million (image, text) pairs collected from the internet. After pre-training, natural language is used to reference learned visual concepts (or describe new ones) enabling zero-shot transfer of the model to downstream tasks. We study the performance of this approach by benchmarking on over 30 different existing computer vision datasets, spanning tasks such as OCR, action recognition in videos, geo-localization, and many types of fine-grained object classification. The model transfers non-trivially to most tasks and is often competitive with a fully supervised baseline without the need for any dataset specific training. For instance, we match the accuracy of the original ResNet-50 on ImageNet zero-shot without needing to use any of the 1.28 million training examples it was trained on. We release our code and pre-trained model weights at this https URL .

来源：[论文官方页面](https://arxiv.org/abs/2103.00020)。

## PPT 文献分享原页

来源：[第 2 组原 PPT](../Assets/Original%20PPTs/%E9%A1%B9%E7%9B%AE%E4%B8%80%E7%AC%AC%E4%BA%8C%E7%BB%84%E6%96%87%E7%8C%AE%E5%88%86%E4%BA%AB%EF%BC%88%E4%BF%AE%E6%94%B9%E7%89%88%EF%BC%89.pptx)，原文件第 1–9 页。

页面图保留原图表、公式和排版；下方折叠文本供搜索。汇报中的解释、教学示例和实验数字均属于来源材料，尚未逐项对照论文全文复核。

### 原 PPT 第 1 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-001.png]]

> [!quote]- 本页可搜索文字
> 汇报人：张忠睿 2612125
>
> 2026年9月30日
>
> Learning Transferable Visual Models From Natural Language Supervision（CLIP）
>
> 通过“图片——文本对”让模型学习到可迁移的视觉概念
>
> TONGJI UNIVERSITY
>
> 从自然语言监督中学习可迁移的视觉模型
>
> ICML 2021
>

### 原 PPT 第 2 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-002.png]]

> [!quote]- 本页可搜索文字
> 研究动机：固定类别监督的局限
>
> 02 / 09
>
> 已有范式：类别先确定，再收集标注
>
> 研究目标：让语言描述参与视觉学习
>
> 问题一：监督信息受固定标签限制
>
> 传统分类将“猫、狗、汽车”编码为离散标签。
>
> 类别之间的语义关系，以及图片中的属性、动作和背景信息，难以通过单一类别标签充分表达。
>
> 问题二：换任务往往需要重新标注
>
> 食物识别、遥感分类或细粒度识别有不同的类别体系。
>
> 为每个任务收集训练数据、拟合分类头，会限制模型的迁移范围与使用灵活性。
>
> 监督来源：互联网已有的图像与文字
>
> 标题、描述和相关文本能够提供更丰富的概念信息。
>
> 将自然语言作为学习信号，减少对专门人工类别标注的依赖。
>
> 任务接口：用文字告诉模型识别什么
>
> 预训练后，把候选类别写成文本，与图像表示比较。
>
> 核心问题是：自然语言监督能否形成可迁移的视觉表示，并支持零样本分类？
>
> 本文的研究动机不只是提高一个数据集上的准确率，而是研究：自然语言监督能否形成可迁移的视觉表示，让同一个模型支持不同任务？
>

### 原 PPT 第 3 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-003.png]]

> [!quote]- 本页可搜索文字
> 方法选择：为什么采用对比学习
>
> 03 / 09
>
> 让模型学什么？
>
>     ——直接生成描述，学习目标过于复杂
>
> 同一张图片可以对应多种正确表述。逐词预测不仅要理解图像，还要学习措辞与句子顺序，训练效率成为扩大规模的限制。
>
> 对比学习只判断“哪一对相互匹配”
>
> 保留整段文本的语义作为监督，不要求模型逐字生成描述。通过匹配与不匹配图文的比较，学习可用于识别的共同表示。
>
> 方法选择依据：优先提高视觉迁移的学习效率，
>
> 使自然语言监督能够扩展到大规模图文数据。
>
> 读图：同样处理图片数量下，对比目标的零样本准确率更高。
>
> 4× 指相对于词袋预测基线的样本效率。
>

### 原 PPT 第 4 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-004.png]]

> [!quote]- 本页可搜索文字
> 预训练数据基础：用网络图文扩大监督
>
> 04 / 09
>
> WIT：4 亿个图文对
>
> 如何构建
>
> 从公开互联网收集图像及相关文本。约 50 万个查询词扩大概念覆盖，每个查询最多保留 2 万对，进行近似平衡。
>
> 为什么需要更大规模
>
> COCO、Visual Genome 的图片规模约十万量级。YFCC100M 过滤出英文自然语言标题或描述后，约剩 1500 万张。
>
> 数据角色
>
> 用途与代表任务
>
> 预训练：WIT
>
> 学习图像与文本的语义对应
>
> 下游评测
>
> ImageNet、Food101、Cars 等分类任务
>
> 跨领域评测
>
> EuroSAT、文字识别、动作识别等
>
> 零样本的准确含义：
>
> 不使用目标数据集的标注图片拟合分类器。
>
> 它不保证预训练从未见过相关概念或近似图片。
>

### 原 PPT 第 5 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-005.png]]

> [!quote]- 本页可搜索文字
> 方法框架：训练对齐，推理匹配
>
> 05 / 09
>
> 预训练：学习图文共同表示
>
> 图像和文本分别编码，投影到同一维度并归一化。
>
> 比较批内所有图文组合，提高真实配对的相似度。
>
> 推理：候选文字成为分类器
>
> 将类别写成句子，编码为类别向量。
>
> 新图片与这些向量比较，选出最匹配的类别。
>

### 原 PPT 第 6 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-006.png]]

> [!quote]- 本页可搜索文字
> 架构设计：两个编码器如何协同
>
> 06 / 09
>
> 模块
>
> 具体设计
>
> 在方法中的作用
>
> 图像编码器
>
> 改进 ResNet 或 Vision Transformer
>
> 提取可迁移的图像特征
>
> 文本编码器
>
> Transformer；使用句末标记的表示
>
> 把不同长度的文字转为整体语义向量
>
> 共享表示空间
>
> 线性投影 + L2 归一化
>
> 统一特征维度，让两种模态可比较
>
> 匹配与优化
>
> 缩放余弦相似度 + 双向交叉熵
>
> 让真实配对相对其他组合获得更高分
>
> 训练组织
>
> 两个编码器从零训练，批量 32,768，训练 32 轮。
>
> 大批量增加负样本，也增加显存与通信负担。
>
> 设计特点
>
> 以双编码器和共享空间为核心，保持训练目标简洁。
>
> 类别文本向量可以缓存，供推理时复用。
>

### 原 PPT 第 7 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-007.png]]

> [!quote]- 本页可搜索文字
> 任务迁移：用语言构造分类器
>
> 07 / 09
>
> 步骤一：用文本明确候选类别
>
> 把 dog 写成 “A photo of a dog.”，为每类生成文本向量。
>
> 文字描述同时表达类别含义和任务上下文。
>
> 步骤二：计算图像与类别的相似度
>
> 新图片经过图像编码器，与全部类别向量比较。
>
> 编码器参数固定，直接选择相似度最高的类别。
>
> 步骤三：通过提示词减少表达偏差
>
> 完整句子比孤立词语更接近训练文本。
>
> 增加“卫星照片”等上下文，或平均多个模板的文本表示。
>
> 原图验证：提示词设计与集成有效。
>
> 提示词也是方法的一部分，结果会受措辞与候选类别集合影响。
>

### 原 PPT 第 8 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-008.png]]

> [!quote]- 本页可搜索文字
> 实验归纳：证据怎样支撑结论
>
> 08 / 09
>
> 零样本迁移：16 / 27 个数据集领先
>
> 比较对象为 ResNet-50 特征上的监督线性分类器。
>
> 说明迁移具有竞争力，同时任务差异明显。
>
> 鲁棒性：比较相近原分布准确率的模型
>
> 通过艺术图、草图、不同拍摄条件等数据验证迁移。
>
> 结论限于论文测试的自然分布变化。
>

### 原 PPT 第 9 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-009.png]]

> [!quote]- 本页可搜索文字
> 优势与局限：方法的适用边界
>
> 09 / 09
>
> 优势：灵活的监督与任务接口
>
> 局限：能力、数据与计算的边界
>
> 降低目标任务的标注依赖
>
> 通过自然语言构造分类器，在多种任务上直接迁移。
>
> 新类别可以改写为文本，不必总是重训分类头。
>
> 可复用的视觉与语言表示
>
> 冻结后的图像特征也可支持监督分类与少样本适配。
>
> 共享空间提供图文匹配能力，扩大使用方式。
>
> 识别能力并不等同于全面理解
>
> 计数、距离判断、部分专业领域仍然较弱。
>
> 输出仍受给定的候选类别集合限制。
>
> 规模带来收益，也带来代价
>
> 网络数据含噪声和偏见，重叠检测不能证明绝对无污染。
>
> 最大 ViT 使用 256 张 V100 训练 12 天。
>

## 我的阅读与思考

<!-- 在此补充个人笔记；导入内容与个人结论分开记录。 -->

[[Zotero Knowledge/知识库首页|知识库首页]]
