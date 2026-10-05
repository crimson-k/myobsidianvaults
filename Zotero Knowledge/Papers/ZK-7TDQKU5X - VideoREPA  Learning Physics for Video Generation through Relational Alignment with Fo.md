---
type: "literature-note"
title: "VideoREPA: Learning Physics for Video Generation through Relational Alignment with Foundation Models"
aliases: ["VideoREPA: Learning Physics for Video Generation through Relational Alignment with Foundation Models"]
zotero_keys: ["7TDQKU5X"]
year: 2025
authors: ["Xiangdong Zhang", "Jiaqi Liao", "Shaofeng Zhang", "Fanqing Meng", "Xiangpeng Wan", "Junchi Yan", "Yu Cheng"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2505.23656"
url: "http://arxiv.org/abs/2505.23656"
collections: ["06 Alignment & Reliability/Representation Alignment"]
source_tags: ["Computer Science - Computer Vision and Pattern Recognition"]
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# VideoREPA: Learning Physics for Video Generation through Relational Alignment with Foundation Models

[Zotero 条目 7TDQKU5X](zotero://select/library/items/7TDQKU5X)

[DOI 原文](https://doi.org/10.48550/arxiv.2505.23656)

[来源网页](http://arxiv.org/abs/2505.23656)

## 主题与知识联系

- [[Zotero Knowledge/Topics/06 Alignment & Reliability/Representation Alignment/索引|06 Alignment & Reliability/Representation Alignment]]

概念地图：[[Zotero Knowledge/Concepts/物理一致性与表征对齐|物理一致性与表征对齐]]

补充阅读入口：[[Zotero Knowledge/Topics/06 Alignment & Reliability/Physics Grounding & Rollout Verification/索引|06 Alignment & Reliability/Physics Grounding & Rollout Verification]]

## 原始摘要

Recent advancements in text-to-video (T2V) diffusion models have enabled high-fidelity and realistic video synthesis. However, current T2V models often struggle to generate physically plausible content due to their limited inherent ability to accurately understand physics. We found that while the representations within T2V models possess some capacity for physics understanding, they lag significantly behind those from recent video self-supervised learning methods. To this end, we propose a novel framework called VideoREPA, which distills physics understanding capability from video understanding foundation models into T2V models by aligning token-level relations. This closes the physics understanding gap and enable more physics-plausible generation. Specifically, we introduce the Token Relation Distillation (TRD) loss, leveraging spatio-temporal alignment to provide soft guidance suitable for finetuning powerful pre-trained T2V models, a critical departure from prior representation alignment (REPA) methods. To our knowledge, VideoREPA is the first REPA method designed for finetuning T2V models and specifically for injecting physical knowledge. Empirical evaluations show that VideoREPA substantially enhances the physics commonsense of baseline method, CogVideoX, achieving significant improvement on relevant benchmarks and demonstrating a strong capacity for generating videos consistent with intuitive physics. More video results are available at https://videorepa.github.io/.

## 附件与批注

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/NLND6MDK)

### Full Text PDF

[打开 PDF](zotero://open-pdf/library/items/UJNSF6DC)

[批注 C5PRRB9K · 第 1 页](zotero://open-pdf/library/items/UJNSF6DC?annotation=C5PRRB9K&page=1)

> video self-supervised learning methods

[批注 AQ4A6GXD · 第 1 页](zotero://open-pdf/library/items/UJNSF6DC?annotation=AQ4A6GXD&page=1)

> distills physics understanding capability from video understanding foundation models into T2V models by aligning token-level relations.

[批注 CKBFKFC5 · 第 1 页](zotero://open-pdf/library/items/UJNSF6DC?annotation=CKBFKFC5&page=1)

> To our knowledge, VideoREPA is the first REPA method designed for finetuning T2V models and specifically for injecting physical knowledge

[批注 3ZEYUV4N · 第 2 页](zotero://open-pdf/library/items/UJNSF6DC?annotation=3ZEYUV4N&page=2)

> To this end, this paper explores enhancing the physics-plausible video generation of T2V models using non-simulation strategies on open-domain datasets, aiming to achieve robust generalization and broad applicability.

[批注 GP2BNEJK · 第 2 页](zotero://open-pdf/library/items/UJNSF6DC?annotation=GP2BNEJK&page=2)

> self-supervised video understanding model, VideoMAEv2 (86M)

[批注 VNNL5DTL · 第 2 页](zotero://open-pdf/library/items/UJNSF6DC?annotation=VNNL5DTL&page=2)

> bridging the gap between foundation models and generative diffusion models, notably through Representation Alignment (REPA)

[批注 SML92656 · 第 2 页](zotero://open-pdf/library/items/UJNSF6DC?annotation=SML92656&page=2)

> directly applying REPA techniques to inject physics knowledge into text-to-video models proves infeasible due to several critical distinctions

[批注 RNBF6H43 · 第 2 页](zotero://open-pdf/library/items/UJNSF6DC?annotation=RNBF6H43&page=2)

> VideoREPA.

[批注 7EUHFBNJ · 第 2 页](zotero://open-pdf/library/items/UJNSF6DC?annotation=7EUHFBNJ&page=2)

> Token Relation Distillation

[批注 JCNHLJ9Z · 第 3 页](zotero://open-pdf/library/items/UJNSF6DC?annotation=JCNHLJ9Z&page=3)

> distilling physics knowledge from pre-trained SSL video encoders.

[批注 J52IRK3Y · 第 3 页](zotero://open-pdf/library/items/UJNSF6DC?annotation=J52IRK3Y&page=3)

> a novel feature alignment framework for video generation.

[批注 TJ2HGA8B · 第 3 页](zotero://open-pdf/library/items/UJNSF6DC?annotation=TJ2HGA8B&page=3)

> Token Relation Distillation loss to effectively distill physics knowledge from VFMs through token-relational alignment, enabling VDMs to generate videos that better adhere to physical laws.

[批注 WNZ7ZPN4 · 第 5 页](zotero://open-pdf/library/items/UJNSF6DC?annotation=WNZ7ZPN4&page=5)

> Token Relation Distillation loss

[批注 ZPUW7EBI · 第 5 页](zotero://open-pdf/library/items/UJNSF6DC?annotation=ZPUW7EBI&page=5)

> TRD aligns the relational structure (i.e., pairwise token similarities) between the internal representations in VDMs and those of a capable Video Foundation Model (e.g., VideoMAEv2). This relational alignment provides a softer guidance suitable for finetuning,

[批注 644BHXKI · 第 6 页](zotero://open-pdf/library/items/UJNSF6DC?annotation=644BHXKI&page=6)

> physics contained in spatial-temporal dynamics)

[批注 UDM3TK43 · 第 6 页](zotero://open-pdf/library/items/UJNSF6DC?annotation=UDM3TK43&page=6)

> . For VDMs, the 3D VAE encoder [55] compresses V into latent z. The hidden state ht = fθ(zt) of denoising transformer is derived from noisy latent zt. The ht is input into a trainable MLP hφ for dimension D alignment, i.e., hφ(ht) ∈ Rf×h×w×D.

[批注 UZUPMJEV · 第 6 页](zotero://open-pdf/library/items/UJNSF6DC?annotation=UZUPMJEV&page=6)

> Token Relation Distillation (TRD) loss,

[批注 7XKBFUWQ · 第 6 页](zotero://open-pdf/library/items/UJNSF6DC?annotation=7XKBFUWQ&page=6)

> feature dimensionality and input configuration for Video Foundation Models (VFMs)

[批注 EZYCZ66V · 第 7 页](zotero://open-pdf/library/items/UJNSF6DC?annotation=EZYCZ66V&page=7)

> CogVideoX

[批注 9PXTKFV5 · 第 7 页](zotero://open-pdf/library/items/UJNSF6DC?annotation=9PXTKFV5&page=7)

> VideoMAEv2

[批注 7I9FCC2Q · 第 7 页](zotero://open-pdf/library/items/UJNSF6DC?annotation=7I9FCC2Q&page=7)

> Videos are center-cropped and resized to 480×720.

[批注 6D5GBPHE · 第 14 页](zotero://open-pdf/library/items/UJNSF6DC?annotation=6D5GBPHE&page=14)

> Consistent with our alignment strategy, we extract these features from the 18th layer of the denoising network.

[批注 LXWR7QZF · 第 15 页](zotero://open-pdf/library/items/UJNSF6DC?annotation=LXWR7QZF&page=15)

> onsidering that the first encoded frame in the latent space of 3D VAE primarily serves to maintain semantic information [55], we exclude it from the alignment process to focus on dynamic content.

[批注 KPYTEKRH · 第 15 页](zotero://open-pdf/library/items/UJNSF6DC?annotation=KPYTEKRH&page=15)

> processing all frames at a reduced resolution.

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
