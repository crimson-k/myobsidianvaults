---
type: "literature"
title: "Revisiting Visual Corruptions in LVLMs: A Shape-Texture Perspective on Model Failures"
aliases: ["ST-CD"]
zotero_keys: ["RBX3C67G"]
year: 2026
authors: ["Qiu, Xinkuan", "Kan, Meina", "He, Zhenliang", "Zhou, Yongbin", "Shan, Shiguang"]
venue: "CVPR 2026"
doi: ""
url: "https://openaccess.thecvf.com/content/CVPR2026/html/Qiu_Revisiting_Visual_Corruptions_in_LVLMs_A_Shape-Texture_Perspective_on_Model_CVPR_2026_paper.html"
collections: ["06 Alignment & Reliability/Robustness & OOD", "90 Projects/Pattern Recognition Course/Project 1/Group 2"]
tags: ["zotero", "literature", "course/pattern-recognition", "ppt/group-2"]
reading_status: "presentation-import"
ppt_role: "main"
ppt_pages: [65, 78]
imported_at: "2026-10-03"
---

# Revisiting Visual Corruptions in LVLMs: A Shape-Texture Perspective on Model Failures

[在 Zotero 打开](zotero://select/library/items/RBX3C67G) · [论文来源](https://openaccess.thecvf.com/content/CVPR2026/html/Qiu_Revisiting_Visual_Corruptions_in_LVLMs_A_Shape-Texture_Perspective_on_Model_CVPR_2026_paper.html) · [论文 PDF](https://openaccess.thecvf.com/content/CVPR2026/papers/Qiu_Revisiting_Visual_Corruptions_in_LVLMs_A_Shape-Texture_Perspective_on_Model_CVPR_2026_paper.pdf)

## 文献导读

从形状与纹理两个互补感知维度研究视觉退化，以边缘与拼图探针构造双路对比解码，并自适应融合校准信号。注意推理开销与启发式探针的适用边界。

## 主题与关联

[[Zotero Knowledge/Topics/06 Alignment & Reliability/Robustness & OOD/索引|06 Alignment & Reliability/Robustness & OOD]] · [[Zotero Knowledge/Topics/90 Projects/Pattern Recognition Course/Project 1/索引|项目一文献分享]]

以下为阅读比较建议，并非已经证实的文献依赖关系。

- [[Zotero Knowledge/Papers/ZK-CDHTS2WR - Learning Transferable Visual Models From Natural Language Supervision|CLIP]]
- [[Zotero Knowledge/Papers/ZK-TGBY7QJ9 - AGFT  Alignment-Guided Fine-Tuning for Zero-Shot Adversarial Robustness of Vision-Lan|AGFT]]
- [[Zotero Knowledge/Papers/ZK-28MFNY9F - CLIP is Strong Enough to Fight Back  Test-time Counterattacks towards Zero-shot Adver|TTC]]

## 原始摘要

Large vision-language models (LVLMs) are highly vulnerable to visual corruptions, substantially compromising their reliability and limiting real-world deployment. Prior work has attributed this degradation primarily to insufficient visual grounding and overreliance on language priors. However, these explanations often overlook the heterogeneous nature of corruptions, which perturb model perception in fundamentally different ways. We revisit this problem from a corruption-centric perspective and show that diverse corruptions can be organized along two complementary perceptual dimensions--shape and texture--which induce distinct failure modes. To address them, we propose Shape-Texture Dual-Path Contrastive Decoding (ST-CD), a training-free inference framework that constructs complementary contrastive views to diagnose and correct shape- and texture-induced biases through adaptive fusion. Experiments across multiple LVLMs and robustness benchmarks demonstrate that ST-CD consistently improves robustness under heterogeneous corruptions, suggesting that leveraging the complementarity between shape and texture provides a general and effective principle for building robust multimodal models.

来源：[论文官方页面](https://openaccess.thecvf.com/content/CVPR2026/html/Qiu_Revisiting_Visual_Corruptions_in_LVLMs_A_Shape-Texture_Perspective_on_Model_CVPR_2026_paper.html)。

## PPT 文献分享原页

来源：[第 2 组原 PPT](../Assets/Original%20PPTs/%E9%A1%B9%E7%9B%AE%E4%B8%80%E7%AC%AC%E4%BA%8C%E7%BB%84%E6%96%87%E7%8C%AE%E5%88%86%E4%BA%AB%EF%BC%88%E4%BF%AE%E6%94%B9%E7%89%88%EF%BC%89.pptx)，原文件第 65–78 页。

页面图保留原图表、公式和排版；下方折叠文本供搜索。汇报中的解释、教学示例和实验数字均属于来源材料，尚未逐项对照论文全文复核。

### 原 PPT 第 65 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-065.png]]

> [!quote]- 本页可搜索文字
> Revisiting Visual Corruptions in LVLMs:A Shape–Texture Perspective on Model Failures
>
> Qiu X, Kan M, He Z, et al. Revisiting Visual Corruptions in LVLMs: A Shape-Texture Perspective on Model Failures[C]//Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition. 2026: 40845-40854.
>
> 主讲人：张城2612192
>

### 原 PPT 第 66 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-066.png]]

> [!quote]- 本页可搜索文字
> LVLM视觉退化visual corruptions
>
> 视觉基础不足
>
> insufficient visual grounding
>
> 过度依赖语言先验
>
> overreliance on language priors
>
> 传统理论
>
> 形状shape
>
> 纹理texture
>
>  退化异质性
>
> 形状-纹理双路径对比解码”（ST-CD）框架
>
> Shape–Texture Dual-Path Contrastive Decoding
>
> Background
>

### 原 PPT 第 67 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-067.png]]

> [!quote]- 本页可搜索文字
> Related Works
>
> Shape–Texture Representations 
>
>  形状偏置模型在面对各种数据退化时具有更好的泛化能力，而纹理偏置模型则倾向于过拟合表面的外观模式。 [7]
>
>  利用自信息显式地解耦了形状与纹理特征，并选择性地抑制了纹理主导的区域。[32]
>
> 过度依赖任一线索都可能导致模型表现脆弱,主张利用线索冲突数据集进行平衡的表征学习。 [19]
>
> 在模糊或弹性形变等特定退化条件下，纹理信息甚至可能比形状信息更可靠。 [29]
>
> 这些研究共同表明，形状与纹理为视觉鲁棒性提供了互补的感知线索。
>

### 原 PPT 第 68 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-068.png]]

> [!quote]- 本页可搜索文字
> Related Works
>
> 视觉对比解码 Visual Contrastive Decoding
>
> 对比解码作为一种无需训练的方法，近期被提出用于增强大语言模型输出的可靠性 [12, 18, 34]
>
> Leng 等人 [16] 提出了视觉对比解码（VCD），该方法利用含噪图像变体构建对比 Logits，从而抑制过度自信或存在偏差的预测。
>
> 后续研究探索了其他形式的对比信号：
>
> M3ID [4] 和图像对比解码（ICD）[36] 依赖于纯文本上下文；
>
> 语言对比解码（LCD）[25] 引入误导性指令作为对比提示；
>
> 而视觉增强对比解码（VACoDe）[14] [15] 的研究则采用了多种图像增强技术。
>

### 原 PPT 第 69 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-069.png]]

> [!quote]- 本页可搜索文字
> 形状-纹理子空间中由破坏引起的特征偏移Corruption-induced feature shifts in shape-texture subspace
>
> 正交感知子空间的构建
>
> 用 LLaVA 的视觉编码器提取：
>
> 清晰图像均值特征	，
>
> 边缘图均值特征	     ，
>
> 以及拼图图均值特征
>
> 计算表征方向偏移向量：
>
> 利用 Gram-Schmidt 正交化，得到一组标准正交基 
>
> 对于任意退化图像集 c，计算其偏移向量在该子空间中的投影坐标：
>
> [1]Qiu X, Kan M, He Z, et al.fig2
>

### 原 PPT 第 70 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-070.png]]

> [!quote]- 本页可搜索文字
> Failure Modes under  Visual Corruptions
>
> 形状shape
>
> 纹理texture
>
> [1]Qiu X, Kan M, He Z, et al.fig1
>

### 原 PPT 第 71 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-071.png]]

> [!quote]- 本页可搜索文字
> 4. Methods
>

### 原 PPT 第 72 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-072.png]]

> [!quote]- 本页可搜索文字
> 5.Experimental Results
>

### 原 PPT 第 73 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-073.png]]

> [!quote]- 本页可搜索文字
> 5.Experimental Results
>

### 原 PPT 第 74 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-074.png]]

> [!quote]- 本页可搜索文字
> 消融实验
>
> Vanilla：无对比校准的原始基线模型。
>
> Diffusion Noise：前人 VCD 采用的扩散加噪图。
>
> Blank Image：M3ID 和 LCD 使用的纯黑/空白图像。
>
> Downsample：双线性插值下采样降质图。
>
> 通用数据增强：裁剪（Crop）、随机擦除（Erase）与水平翻转（Flip）。
>
> 论文提出的对偶探针：Canny 边缘提取（Canny Edge）与拼图打乱（Jigsaw Puzzle）
>

### 原 PPT 第 75 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-075.png]]

> [!quote]- 本页可搜索文字
> 消融实验
>
> 固定权重（Fixed Weights, Fix）：
>
> 沿用传统 VCD 的默认配置，固定权重不作动态改变，即 
>
> 基于距离的加权（Distance-Based Weights, Distance）：
>
> 以原始 Logit 与对比 Logit 之间的欧氏距离作为系数：
>
> 其直觉是两者的差异越大，代表受到的破坏影响越强，应给予越大的修正力。
>
> 基于信息熵的加权（Entropy-Based Weights, Entropy，论文默认方案）：
>
> 利用香农预测熵作为模型不确定度与探针可靠度的衡量指标：
>
> 数据驱动的可学习加权（Learned Weights, Learned）：
>
> 针对 30% 的破坏验证集提取频域特征 	（频域能直观显露高频噪声等退化模式），训练一个轻量化的 ResNet-18 网络直接回归拟合最佳权重：			      。
>

### 原 PPT 第 76 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-076.png]]

> [!quote]- 本页可搜索文字
> 论文的核心贡献
>
> 提出了“以退化为中心”的形状-纹理感知新视角：
>
> 设计了即插即用、免训练的双路对比解码框架（ST-CD）：
>
> 构建了优雅的信息论自适应双向门控机制：
>
>  全面的实证验证与高质量基准开源：
>

### 原 PPT 第 77 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-077.png]]

> [!quote]- 本页可搜索文字
> 不足与局限性
>
> 依然存在不可忽略的推理计算延迟与显存开销：
>
> 核心探针依赖传统图像处理启发式算子：
>
> 无监督熵权与数据驱动最佳权重之间仍存在性能鸿沟：
>
> 感知维度局限于中低层空间退化：
>

### 原 PPT 第 78 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-078.png]]

> [!quote]- 本页可搜索文字
> THANK  YOU
>
> 汇报人：张城2612192
>

## 我的阅读与思考

<!-- 在此补充个人笔记；导入内容与个人结论分开记录。 -->

[[Zotero Knowledge/知识库首页|知识库首页]]
