---
type: "literature-note"
title: "Causality in Video Diffusers is Separable from Denoising"
aliases: ["Causality in Video Diffusers is Separable from Denoising"]
zotero_keys: ["K22LEGKI"]
year: null
authors: ["Xingjian Bai", "Guande He", "Zhengqi Li", "Eli Shechtman", "Xun Huang", "Zongze Wu"]
venue: ""
venue_field: null
doi: ""
url: ""
collections: ["03 Visual Generation/General Video Generation"]
source_tags: []
tags: ["zotero", "literature", "concept/视频生成的因果化与流式推理", "concept-primary/视频生成的因果化与流式推理"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# Causality in Video Diffusers is Separable from Denoising

[Zotero 条目 K22LEGKI](zotero://select/library/items/K22LEGKI)

## 主题与知识联系

- [[Zotero Knowledge/Topics/03 Visual Generation/General Video Generation/索引|03 Visual Generation/General Video Generation]]

概念地图：[[Zotero Knowledge/Concepts/视频生成的因果化与流式推理|视频生成的因果化与流式推理]]

## 原始摘要

Causality — referring to temporal, uni-directional causeeffect relationships between components — underlies many complex generative processes, including videos, language, and robot trajectories. Current causal diffusion models entangle temporal reasoning with iterative denoising, applying causal attention across all layers, at every denoising step, and over the entire context. In this paper, we show that the causal reasoning in these models is separable from the multi-step denoising process. Through systematic probing of autoregressive video diffusers, we uncover two key regularities: (1) early layers produce highly similar features across denoising steps, indicating redundant computation along the diffusion trajectory; and (2) deeper layers exhibit sparse cross-frame attention and primarily perform intra-frame rendering. Motivated by these findings, we introduce Separable Causal Diffusion (SCD), a new architecture that explicitly decouples once-per-frame temporal reasoning, via a causal transformer encoder, from multi-step frame-wise rendering, via a lightweight diffusion decoder. Extensive experiments on both pretraining and post-training tasks across synthetic and real benchmarks show that SCD significantly improves throughput and per-frame latency while matching or surpassing the generation quality of strong causal diffusion baselines.

## 附件与批注

### PDF

[打开 PDF](zotero://open-pdf/library/items/VDMDMMZY)

[批注 6D27Z97C · 第 1 页](zotero://open-pdf/library/items/VDMDMMZY?annotation=6D27Z97C&page=1)

> Current causal diffusion models

[批注 YPJR5GBR · 第 1 页](zotero://open-pdf/library/items/VDMDMMZY?annotation=YPJR5GBR&page=1)

> early layers produce highly similar features across denoising steps, indicating redundant computation along the diffusion trajectory; and (2) deeper layers exhibit sparse cross-frame attention and primarily perform intra-frame rendering

[批注 76NWN8F8 · 第 1 页](zotero://open-pdf/library/items/VDMDMMZY?annotation=76NWN8F8&page=1)

> diffusion models typically perform multistep refinement for each frame, rather than generating in a single pass.

[批注 6FW765XP · 第 1 页](zotero://open-pdf/library/items/VDMDMMZY?annotation=6FW765XP&page=1)

> tightly entangles temporal reasoning with iterative denoising,

[批注 YCW5DGCB · 第 1 页](zotero://open-pdf/library/items/VDMDMMZY?annotation=YCW5DGCB&page=1)

> Is multi-step  arXiv:2602.10095v1 [cs.CV] 10 Feb 2026 refinement truly required for temporal reasoning?

[批注 YZUNP6NQ · 第 2 页](zotero://open-pdf/library/items/VDMDMMZY?annotation=YZUNP6NQ&page=2)

> temporal reasoning in AR models is separable from the denoising process

[批注 S3VHD6B2 · 第 2 页](zotero://open-pdf/library/items/VDMDMMZY?annotation=S3VHD6B2&page=2)

> causal reasoning in early layers is highly redundant across denoising timesteps, as indicated by the high similarity in middle-layer output features across denoising step

[批注 SBBYPR6P · 第 2 页](zotero://open-pdf/library/items/VDMDMMZY?annotation=SBBYPR6P&page=2)

> Separable Causal Diffusion

[批注 WVXEC8XA · 第 2 页](zotero://open-pdf/library/items/VDMDMMZY?annotation=WVXEC8XA&page=2)

> decoupled causal architecture in which a temporal causal-reasoning module operates once per frame,

[批注 KH3L4LMT · 第 2 页](zotero://open-pdf/library/items/VDMDMMZY?annotation=KH3L4LMT&page=2)

> while a lightweight frame-wise diffusion renderer handles visual refinement

[批注 576XTZU4 · 第 2 页](zotero://open-pdf/library/items/VDMDMMZY?annotation=576XTZU4&page=2)

> Concretely, a causal transformer reads the historical clean frame tokens through KV cache and produces a latent that summarizes the entities, layout, and expected motion from its context. This context latent is then reused across all denoising steps for that frame.

[批注 XJM5J3W3 · 第 5 页](zotero://open-pdf/library/items/VDMDMMZY?annotation=XJM5J3W3&page=5)

> Separable Causal Diffusion (SCD), an encoder–decoder–style design that disentangles temporal causal reasoning from iterative denoising

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
