---
type: "literature"
title: "CLIP is Strong Enough to Fight Back: Test-time Counterattacks towards Zero-shot Adversarial Robustness of CLIP"
aliases: ["TTC"]
zotero_keys: ["28MFNY9F"]
year: 2025
authors: ["Xing, Songlong", "Zhao, Zhengyu", "Sebe, Nicu"]
venue: "CVPR 2025"
doi: ""
url: "https://arxiv.org/abs/2503.03613"
collections: ["06 Alignment & Reliability/Robustness & OOD", "90 Projects/Pattern Recognition Course/Project 1/Group 2"]
tags: ["zotero", "literature", "course/pattern-recognition", "ppt/group-2"]
reading_status: "presentation-import"
ppt_role: "main"
ppt_pages: [121, 129]
imported_at: "2026-10-03"
---

# CLIP is Strong Enough to Fight Back: Test-time Counterattacks towards Zero-shot Adversarial Robustness of CLIP

[在 Zotero 打开](zotero://select/library/items/28MFNY9F) · [论文来源](https://arxiv.org/abs/2503.03613) · [论文 PDF](https://arxiv.org/pdf/2503.03613)

## 文献导读

利用对抗样本的异常局部稳定性，在测试时优化输入扰动，使 CLIP 嵌入离开当前错误区域。模型参数冻结，但增加推理计算，也需检查自适应攻击。

## 主题与关联

[[Zotero Knowledge/Topics/06 Alignment & Reliability/Robustness & OOD/索引|06 Alignment & Reliability/Robustness & OOD]] · [[Zotero Knowledge/Topics/90 Projects/Pattern Recognition Course/Project 1/索引|项目一文献分享]]

以下为阅读比较建议，并非已经证实的文献依赖关系。

- [[Zotero Knowledge/Papers/ZK-TGBY7QJ9 - AGFT  Alignment-Guided Fine-Tuning for Zero-Shot Adversarial Robustness of Vision-Lan|AGFT]]
- [[Zotero Knowledge/Papers/ZK-RBX3C67G - Revisiting Visual Corruptions in LVLMs  A Shape-Texture Perspective on Model Failures|ST-CD]]

## 原始摘要

Despite its prevalent use in image-text matching tasks in a zero-shot manner, CLIP has been shown to be highly vulnerable to adversarial perturbations added onto images. Recent studies propose to finetune the vision encoder of CLIP with adversarial samples generated on the fly, and show improved robustness against adversarial attacks on a spectrum of downstream datasets, a property termed as zero-shot robustness. In this paper, we show that malicious perturbations that seek to maximise the classification loss lead to `falsely stable' images, and propose to leverage the pre-trained vision encoder of CLIP to counterattack such adversarial images during inference to achieve robustness. Our paradigm is simple and training-free, providing the first method to defend CLIP from adversarial attacks at test time, which is orthogonal to existing methods aiming to boost zero-shot adversarial robustness of CLIP. We conduct experiments across 16 classification datasets, and demonstrate stable and consistent gains compared to test-time defence methods adapted from existing adversarial robustness studies that do not rely on external networks, without noticeably impairing performance on clean images. We also show that our paradigm can be employed on CLIP models that have been adversarially finetuned to further enhance their robustness at test time. Our code is available \href{ this https URL }{here}.

来源：[论文官方页面](https://arxiv.org/abs/2503.03613)。

## PPT 文献分享原页

来源：[第 2 组原 PPT](../Assets/Original%20PPTs/%E9%A1%B9%E7%9B%AE%E4%B8%80%E7%AC%AC%E4%BA%8C%E7%BB%84%E6%96%87%E7%8C%AE%E5%88%86%E4%BA%AB%EF%BC%88%E4%BF%AE%E6%94%B9%E7%89%88%EF%BC%89.pptx)，原文件第 121–129 页。

页面图保留原图表、公式和排版；下方折叠文本供搜索。汇报中的解释、教学示例和实验数字均属于来源材料，尚未逐项对照论文全文复核。

### 原 PPT 第 121 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-121.png]]

> [!quote]- 本页可搜索文字
> CLIP is Strong Enough to Fight Back
>
> Test-time Counterattacks towards Zero-shot
>
> Adversarial Robustness of CLIP
>
> From False Stability to Test-time Counterattack
>
> 汇报人：袁珩翔
>
> 同济大学 · 电子与信息工程学院
>

### 原 PPT 第 122 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-122.png]]

> [!quote]- 本页可搜索文字
> 研究背景
>
> 研究动机
>
> 关键发现
>
> TTC 方法
>
> 创新点
>
> 实验结果
>
> 总结讨论
>
> CLIP 的零样本分类与对抗攻击
>
> Shared Embedding Space
>
> Image
>
> →
>
> Vision Encoder
>
> →
>
> Image Embedding
>
> Text Prompt
>
> →
>
> Text Encoder
>
> →
>
> Text Embedding
>
> ↘
>
> Cosine
>
> Similarity
>
> ↗
>
> ↓  Zero-shot Prediction
>
> screwdriver  →  lighter  →  screwdriver
>
> Adversarial Perturbation：人眼近似不变，预测可能改变
>

### 原 PPT 第 123 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-123.png]]

> [!quote]- 本页可搜索文字
> 研究背景
>
> 研究动机
>
> 关键发现
>
> TTC 方法
>
> 创新点
>
> 实验结果
>
> 总结讨论
>
> 为何不直接重新训练 CLIP？
>
> Existing Defenses
>
> AFT
>
> Adversarial images → Vision Encoder → update θ
>
> APT
>
> Adversarial images → Text Prompts → update tokens
>
> Limitations
>
> Training cost ↑
>
> Generalization may degrade
>
> Clean accuracy may drop
>
> CLIP is already a strong pretrained foundation model
>
> →  Reuse its representation instead of retraining?
>
> Method / Optimize / Stage
>
> AFT    Vision Encoder    Training
>
> APT    Text Prompts      Training
>
> TTC    Test Input         Inference
>
> Research Question   →   Can CLIP defend itself at test time?
>

### 原 PPT 第 124 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-124.png]]

> [!quote]- 本页可搜索文字
> 研究背景
>
> 研究动机
>
> 关键发现
>
> TTC 方法
>
> 创新点
>
> 实验结果
>
> 总结讨论
>
> False Stability：对抗图像的异常局部行为
>
> Clean / Adversarial image  →  noise n  →  Vision Encoder  →  embedding drift τ
>
> Small-noise regime: 1/255–4/255
>
> adv. τ < clean τ  (both datasets)
>
> Drift Ratio
>
> τ = ‖fθ(x+n) − fθ(x)‖ / ‖fθ(x)‖
>
> x: image · n: random noise · fθ: vision encoder
>
> Observation
>
> small noise → unusually low drift
>
> ↓  Hypothesis
>
> may occupy a wrong local region
>
> ↓  Design Intuition
>
> push the embedding away
>
> False Stability directly motivates TTC.
>

### 原 PPT 第 125 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-125.png]]

> [!quote]- 本页可搜索文字
> 研究背景
>
> 研究动机
>
> 关键发现
>
> TTC 方法
>
> 创新点
>
> 实验结果
>
> 总结讨论
>
> TTC：测试时优化输入扰动
>
> Test-time workflow
>
> ① Test image x
>
> ② Compute τ
>
> Is τ low?
>
> ↓
>
> ↓
>
> No → Stop
>
> Yes → PGD counterattack
>
> ↙
>
> ↘
>
> N-step updates  →  weighted perturbations
>
> ↓  x + δₜₜ꜀  →  CLIP prediction
>
> Optimization Objective
>
> δₜₜ꜀ = arg maxδ
>
> ‖fθ(x+δ) − fθ(x)‖
>
> Move the new embedding away
>
> from the current embedding.
>
> Frozen Vision Encoder  ·  No Finetuning  ·  Optimize Input
>

### 原 PPT 第 126 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-126.png]]

> [!quote]- 本页可搜索文字
> 研究背景
>
> 研究动机
>
> 关键发现
>
> TTC 方法
>
> 创新点
>
> 实验结果
>
> 总结讨论
>
> 创新：让 CLIP 利用自身表示防御
>
> Observation
>
> False Stability
>
> ↓
>
> Hypothesis
>
> Adversarial samples may occupy
>
> a wrong local stable region
>
> ↓
>
> Defense Design
>
> Maximize embedding drift
>
> ↓
>
> Execution
>
> Test-time gradient-based
>
> input optimization
>
> Latent-space intuition
>
> clean semantic region
>
> ↘ adversarial attack
>
> ×
>
> false-stable region
>
> ↗ TTC: move away
>
> Innovation = Observation → Hypothesis → Defense Design
>
> PGD is the optimization tool, not the core novelty.
>
> Scope: attacks maximizing CLIP classification loss
>

### 原 PPT 第 127 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-127.png]]

> [!quote]- 本页可搜索文字
> 研究背景
>
> 研究动机
>
> 关键发现
>
> TTC 方法
>
> 创新点
>
> 实验结果
>
> 总结讨论
>
> 实验设计：作者从四个方面验证 TTC
>
> ① Generality
>
> Is TTC dataset-specific?
>
> 16 classification datasets
>
> Object · Fine-grained · Scene · Domain-specific
>
> CIFAR10 · ImageNet · OxfordPets · SUN397 · EuroSAT
>
> ② Robustness
>
> Does it survive stronger attacks?
>
> PGD  ·  CW
>
> Attack budgets: εₐ = 1/255 · 4/255
>
> Changes in strength and attack form
>
> ③ Comparison
>
> Better than alternatives?
>
> Test-time defenses
>
> RN · TTE · Anti-adversary · HD
>
> Finetuning: TeCoA · PMG-AFT · FARE
>
> ④ Ablation & Compatibility
>
> Which components matter?
>
> Ablation: N · τₜₕᵣₑₛ · β
>
> Compatibility:
>
> TeCoA + TTC · PMG-AFT + TTC · FARE + TTC
>
> Validation design → diverse datasets, attack settings, baselines, and internal components
>

### 原 PPT 第 128 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-128.png]]

> [!quote]- 本页可搜索文字
> 研究背景
>
> 研究动机
>
> 关键发现
>
> TTC 方法
>
> 创新点
>
> 实验结果
>
> 总结讨论
>
> 实验结果：TTC 是否真的有效？
>
> 16 datasets · PGD/CW · Different attack budgets · Baselines & Ablations
>
> Paper Table 1 · selected averages
>
> PGD, εₐ = 1/255 · average over 16 datasets
>
> Method
>
> Robust Acc.
>
> Clean Acc.
>
> CLIP
>
> 2.70
>
> 61.51
>
> TTE
>
> 33.28
>
> 61.79
>
> Anti-adv
>
> 12.01
>
> 57.35
>
> HD
>
> 13.81
>
> 56.62
>
> TTC
>
> 39.17
>
> 59.75
>
> Robust: 2.70 → 39.17  (+36.47)
>
> Clean: 61.51 → 59.75  (−1.76)
>
> Paper Table 2 · stronger attack
>
> PGD, εₐ = 4/255
>
> Method
>
> Robust
>
> Clean
>
> CLIP
>
> 0.09
>
> 61.51
>
> TTC
>
> 20.63
>
> 55.99
>
> TTC remains effective at εₐ = 4/255.
>
> Figure 5 · effect of counterattack steps N
>
> CIFAR10
>
> ImageNet
>
> Few steps: weak defense · Too many: clean accuracy may decline
>
> Large robustness gain with limited clean-accuracy loss.
>
> Additional evidence: CW · τ/β ablations · TeCoA/PMG-AFT/FARE + TTC
>

### 原 PPT 第 129 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-129.png]]

> [!quote]- 本页可搜索文字
> 研究背景
>
> 研究动机
>
> 关键发现
>
> TTC 方法
>
> 创新点
>
> 实验结果
>
> 总结讨论
>
> 总结、局限与部署思考
>
> Research loop
>
> Observation → False Stability → TTC → Robustness Gain → Inference Cost
>
> Takeaways
>
> False Stability
>
> Test-time Counterattack
>
> CLIP Self-defense
>
> Limitations
>
> Extra inference-time computation
>
> N / threshold tuning
>
> Adaptive attacks may bypass TTC
>
> Deployment Perspective
>
> Robustness  ↔  Latency  ↔  Throughput
>
> TTC shifts part of the robustness cost from training to inference.
>

## 我的阅读与思考

<!-- 在此补充个人笔记；导入内容与个人结论分开记录。 -->

[[Zotero Knowledge/知识库首页|知识库首页]]
