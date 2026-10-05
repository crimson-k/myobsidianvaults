---
type: "literature-note"
title: "VisualPredicator: Learning Abstract World Models with Neuro-Symbolic Predicates for Robot Planning"
aliases: ["VisualPredicator: Learning Abstract World Models with Neuro-Symbolic Predicates for Robot Planning"]
zotero_keys: ["HCBLTGWY"]
year: 2025
authors: ["Yichao Liang", "Nishanth Kumar", "Hao Tang", "Adrian Weller", "Joshua B. Tenenbaum", "Tom Silver", "João F. Henriques", "Kevin Ellis"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2410.23156"
url: "http://arxiv.org/abs/2410.23156"
collections: ["05 Robot Learning/Planning & Inverse Control"]
source_tags: ["Computer Science - Artificial Intelligence", "Computer Science - Computer Vision and Pattern Recognition", "Computer Science - Machine Learning", "Computer Science - Robotics"]
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# VisualPredicator: Learning Abstract World Models with Neuro-Symbolic Predicates for Robot Planning

[Zotero 条目 HCBLTGWY](zotero://select/library/items/HCBLTGWY)

[DOI 原文](https://doi.org/10.48550/arxiv.2410.23156)

[来源网页](http://arxiv.org/abs/2410.23156)

## 主题与知识联系

- [[Zotero Knowledge/Topics/05 Robot Learning/Planning & Inverse Control/索引|05 Robot Learning/Planning & Inverse Control]]

补充阅读入口：[[Zotero Knowledge/Topics/04 World Models/Concepts & Design/索引|04 World Models/Concepts & Design]]

## 原始摘要

Broadly intelligent agents should form task-specific abstractions that selectively expose the essential elements of a task, while abstracting away the complexity of the raw sensorimotor space. In this work, we present Neuro-Symbolic Predicates, a first-order abstraction language that combines the strengths of symbolic and neural knowledge representations. We outline an online algorithm for inventing such predicates and learning abstract world models. We compare our approach to hierarchical reinforcement learning, vision-language model planning, and symbolic predicate invention approaches, on both in- and out-of-distribution tasks across five simulated robotic domains. Results show that our approach offers better sample complexity, stronger out-of-distribution generalization, and improved interpretability.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### 06/08/2026, 14:52:26

[在 Zotero 查看](zotero://select/library/items/V48DU58R)

**06/08/2026, 14:52:26**

**gpt-5-chat-latest:**

Here’s a synthesis of how *VISUALPREDICATOR: Learning Abstract World Models with Neuro-Symbolic Predicates for Robot Planning* (ICLR 2025) could contribute to **enhancing out-of-distribution (OOD) generalization** and **long-horizon future action prediction** in the context of an **action-conditioned world model** like the one proposed in *DOI: 10.48550/ARXIV.2510.24161* (presumably a next-generation world model, 2026):

### 1. Core Idea: Abstract, Neuro-Symbolic World Modeling

The paper introduces **Neuro-Symbolic Predicates (NSPs)** — compositional, interpretable abstractions that bridge perception and logic.  
They combine:

- **Neural perception via VLM calls** (for grounding predicates in raw RGB or proprioception data), and

- **Symbolic reasoning via programmatic abstraction** (using code-based Boolean logic, recursion, typing, and compositional rules).

Formally, the abstract world model learns a transition function over **abstract states** $S$ and **high-level actions (HLAs)**, rather than pixel space transitions.

This directly addresses two limitations of standard action-conditioned world models:

- **Semantic entanglement** — Visual or proprioceptive embeddings may entangle unrelated factors; NSPs selectively expose task-relevant, interpretable features.

- **Causal compositionality** — By representing world dynamics through logical programs, NSPs allow explicit causal reasoning over predicates (e.g., “If a balance plate is uneven → machine-off”) rather than relying on learned latent correlations.

### 2. Contribution to OOD Generalization

#### a. Task-Specific Abstraction Learning

The system learns to **invent predicates online** that selectively encode *task-relevant relational structure*.  
This improves OOD robustness because the model learns *what* to represent (predicate structure) rather than memorizing *perceptual configurations*.

Example:  
In the Coffee domain, instead of memorizing spatial jug-pose distributions, the learned predicate `JugInMachine(jug, machine)` defines a reusable abstract relation that transfers to *novel jugs or machines* unseen in training.

For a world model, this suggests an interpretable latent abstraction layer, grounded in learned symbolic structure, that can generalize across unseen object instances, dynamics, and novel combinations.

#### b. Separation of Perception and Logic

By decoupling *low-level sensory grounding* (through robust VLM-perception APIs) and *high-level logical reasoning* (through symbolic code), the model avoids overfitting to pixel statistics — a core failure mode in OOD world modeling (e.g., domain shifts in lighting, object textures, or dexterous configurations).

#### c. Derived Predicates Enable Relational Compositionality

Derived NSPs (e.g., `OnPlate(x,y)` computed recursively from `DirectlyOn`) enable zero-shot reasoning over relational hierarchies without direct visual supervision.  
This compositional generalization allows extrapolating logical combinations in unseen configurations — an essential ingredient for open-ended environments and long-horizon predictions.

### 3. Contribution to Long-Horizon Future Prediction

#### a. Hierarchical Structure via HLAs

The paper learns **High-Level Actions (HLAs)** that encode preconditions and effects over NSPs:

$$F(s, \omega) = s \cup EFF^+ \setminus EFF^- \quad \text{if } PRE \subseteq s$$

This abstract state transition model operates at a **symbolic temporal abstraction level**, allowing efficient reasoning over **long-horizon plans** that would require hundreds of primitive time steps at the pixel-action level.  

For an action-conditioned world model, this provides a **hierarchical backbone**:

- NSP-level transitions form *macro-transitions* measurable over long horizons.

- The world model can predict sequences of HLAs to forecast extended futures with much lower combinatorial explosion.

#### b. Optimistic Operator Learning

Their extended **cluster-and-intersect** operator learning algorithm prefers *optimistic preconditions* — enabling exploration and avoiding over-restrictive models.  
For predictive models, this enables better **forward coverage of hypothetical futures**, essential for planning or model-based forecasting under uncertainty.

#### c. Planning-Driven Data Collection

Data acquisition is actively coupled with the abstract planner, ensuring the world model samples transitions where abstraction errors matter — a form of **goal-conditioned exploration** that reduces compounding error in long-horizon predictions.

### 4. Integration Potential into a 2026 Action-Conditioned World Model

For a world model like *2026, DOI: 10.48550/ARXIV.2510.24161*, which likely focuses on **predicting future sensory states given action sequences**, integration points include:

#### a. Abstract Conditioning Layer

Use NSPs as a **predicate-level latent space** on top of the continuous latent dynamics model.  
Prediction can occur both in latent feature space (for fine-grained sensory rollout) and in **predicate space** (for abstract event prediction), improving semantic stability across long time horizons.

#### b. Neuro-Symbolic Regularization

Incorporate NSP consistency constraints during training:

$$\mathcal{L}_{NSP} = \sum_{\psi \in \Psi} \text{BCE}(\psi(x_t), \psi(\hat{x}_t))$$

This ensures the predicted world evolution preserves logical consistency across predicates, making the latent dynamics more interpretable and aligned with causal task structure.

#### c. Multi-Scale Planning Interface

Embed symbolic HLAs into the policy/planning head of the world model — allowing the system to roll out macro-steps (“Pick”, “Pour”, “Balance”) internally, while the lower-level dynamics handles continuous execution.

### 5. Summary Table

 | Challenge in Action-Conditioned World Models | VISUALPREDICATOR Contribution

 | Poor OOD generalization | Learns compositional NSPs and derived predicates grounded in perceptual data

 | Entangled latent representations | Explicit neuro-symbolic factorization of perception and logic

 | Fragile long-horizon predictions | Abstract world model with high-level actions enables stable macro-transition prediction

 | Compounding model error | Planning-guided exploration and optimistic operator learning improve long-term consistency

 | Lack of interpretability | Symbolic NSPs make latent causal mechanisms explicit and inspectable

#### **In short:**

This paper provides a **neuro-symbolic abstraction framework** that can be layered atop or within an action-conditioned world model to:

- **Structure latent space** around compositional, interpretable predicates rather than raw pixels,

- **Support symbolic future prediction** over long action horizons, and

- **Improve robustness and generalization** across environments and object types by learning transferable logical world models.

If you want, I can sketch a **possible hybrid architecture diagram** showing how NSP-based symbolic abstractions could be integrated into a modern transformer-based world model for 2026 predictive control — would you like that?

Written by AIdea plugin

**06/08/2026, 14:52:32**

**gpt-5-chat-latest:**

Here’s a synthesis of how *VISUALPREDICATOR: Learning Abstract World Models with Neuro-Symbolic Predicates for Robot Planning* (ICLR 2025) could contribute to **enhancing out-of-distribution (OOD) generalization** and **long-horizon future action prediction** in the context of an **action-conditioned world model** like the one proposed in *DOI: 10.48550/ARXIV.2510.24161* (presumably a next-generation world model, 2026):

### 1. Core Idea: Abstract, Neuro-Symbolic World Modeling

The paper introduces **Neuro-Symbolic Predicates (NSPs)** — compositional, interpretable abstractions that bridge perception and logic.  
They combine:

- **Neural perception via VLM calls** (for grounding predicates in raw RGB or proprioception data), and

- **Symbolic reasoning via programmatic abstraction** (using code-based Boolean logic, recursion, typing, and compositional rules).

Formally, the abstract world model learns a transition function over **abstract states** $S$ and **high-level actions (HLAs)**, rather than pixel space transitions.

This directly addresses two limitations of standard action-conditioned world models:

- **Semantic entanglement** — Visual or proprioceptive embeddings may entangle unrelated factors; NSPs selectively expose task-relevant, interpretable features.

- **Causal compositionality** — By representing world dynamics through logical programs, NSPs allow explicit causal reasoning over predicates (e.g., “If a balance plate is uneven → machine-off”) rather than relying on learned latent correlations.

### 2. Contribution to OOD Generalization

#### a. Task-Specific Abstraction Learning

The system learns to **invent predicates online** that selectively encode *task-relevant relational structure*.  
This improves OOD robustness because the model learns *what* to represent (predicate structure) rather than memorizing *perceptual configurations*.

Example:  
In the Coffee domain, instead of memorizing spatial jug-pose distributions, the learned predicate `JugInMachine(jug, machine)` defines a reusable abstract relation that transfers to *novel jugs or machines* unseen in training.

For a world model, this suggests an interpretable latent abstraction layer, grounded in learned symbolic structure, that can generalize across unseen object instances, dynamics, and novel combinations.

#### b. Separation of Perception and Logic

By decoupling *low-level sensory grounding* (through robust VLM-perception APIs) and *high-level logical reasoning* (through symbolic code), the model avoids overfitting to pixel statistics — a core failure mode in OOD world modeling (e.g., domain shifts in lighting, object textures, or dexterous configurations).

#### c. Derived Predicates Enable Relational Compositionality

Derived NSPs (e.g., `OnPlate(x,y)` computed recursively from `DirectlyOn`) enable zero-shot reasoning over relational hierarchies without direct visual supervision.  
This compositional generalization allows extrapolating logical combinations in unseen configurations — an essential ingredient for open-ended environments and long-horizon predictions.

### 3. Contribution to Long-Horizon Future Prediction

#### a. Hierarchical Structure via HLAs

The paper learns **High-Level Actions (HLAs)** that encode preconditions and effects over NSPs:

$$F(s, \omega) = s \cup EFF^+ \setminus EFF^- \quad \text{if } PRE \subseteq s$$

This abstract state transition model operates at a **symbolic temporal abstraction level**, allowing efficient reasoning over **long-horizon plans** that would require hundreds of primitive time steps at the pixel-action level.  

For an action-conditioned world model, this provides a **hierarchical backbone**:

- NSP-level transitions form *macro-transitions* measurable over long horizons.

- The world model can predict sequences of HLAs to forecast extended futures with much lower combinatorial explosion.

#### b. Optimistic Operator Learning

Their extended **cluster-and-intersect** operator learning algorithm prefers *optimistic preconditions* — enabling exploration and avoiding over-restrictive models.  
For predictive models, this enables better **forward coverage of hypothetical futures**, essential for planning or model-based forecasting under uncertainty.

#### c. Planning-Driven Data Collection

Data acquisition is actively coupled with the abstract planner, ensuring the world model samples transitions where abstraction errors matter — a form of **goal-conditioned exploration** that reduces compounding error in long-horizon predictions.

### 4. Integration Potential into a 2026 Action-Conditioned World Model

For a world model like *2026, DOI: 10.48550/ARXIV.2510.24161*, which likely focuses on **predicting future sensory states given action sequences**, integration points include:

#### a. Abstract Conditioning Layer

Use NSPs as a **predicate-level latent space** on top of the continuous latent dynamics model.  
Prediction can occur both in latent feature space (for fine-grained sensory rollout) and in **predicate space** (for abstract event prediction), improving semantic stability across long time horizons.

#### b. Neuro-Symbolic Regularization

Incorporate NSP consistency constraints during training:

$$\mathcal{L}_{NSP} = \sum_{\psi \in \Psi} \text{BCE}(\psi(x_t), \psi(\hat{x}_t))$$

This ensures the predicted world evolution preserves logical consistency across predicates, making the latent dynamics more interpretable and aligned with causal task structure.

#### c. Multi-Scale Planning Interface

Embed symbolic HLAs into the policy/planning head of the world model — allowing the system to roll out macro-steps (“Pick”, “Pour”, “Balance”) internally, while the lower-level dynamics handles continuous execution.

### 5. Summary Table

 | Challenge in Action-Conditioned World Models | VISUALPREDICATOR Contribution

 | Poor OOD generalization | Learns compositional NSPs and derived predicates grounded in perceptual data

 | Entangled latent representations | Explicit neuro-symbolic factorization of perception and logic

 | Fragile long-horizon predictions | Abstract world model with high-level actions enables stable macro-transition prediction

 | Compounding model error | Planning-guided exploration and optimistic operator learning improve long-term consistency

 | Lack of interpretability | Symbolic NSPs make latent causal mechanisms explicit and inspectable

#### **In short:**

This paper provides a **neuro-symbolic abstraction framework** that can be layered atop or within an action-conditioned world model to:

- **Structure latent space** around compositional, interpretable predicates rather than raw pixels,

- **Support symbolic future prediction** over long action horizons, and

- **Improve robustness and generalization** across environments and object types by learning transferable logical world models.

If you want, I can sketch a **possible hybrid architecture diagram** showing how NSP-based symbolic abstractions could be integrated into a modern transformer-based world model for 2026 predictive control — would you like that?

Written by AIdea plugin

### Comment: ICLR 2025 (Spotlight)

[在 Zotero 查看](zotero://select/library/items/P5XLBRBQ)

Comment: ICLR 2025 (Spotlight)

Here’s a synthesis of how VISUALPREDICATOR: Learning Abstract World Models with Neuro-Symbolic Predicates for Robot Planning (ICLR 2025) could contribute to enhancing out-of-distribution (OOD) generalization and long-horizon future action prediction in the context of an action-conditioned world model like the one proposed in DOI: 10.48550/ARXIV.2510.24161 (presumably a next-generation world model, 2026):

- 
Core Idea: Abstract, Neuro-Symbolic World Modeling

The paper introduces Neuro-Symbolic Predicates (NSPs) — compositional, interpretable abstractions that bridge perception and logic. They combine:

Neural perception via VLM calls (for grounding predicates in raw RGB or proprioception data), and
Symbolic reasoning via programmatic abstraction (using code-based Boolean logic, recursion, typing, and compositional rules).

Formally, the abstract world model learns a transition function over abstract states SS and high-level actions (HLAs), rather than pixel space transitions.

This directly addresses two limitations of standard action-conditioned world models:

Semantic entanglement — Visual or proprioceptive embeddings may entangle unrelated factors; NSPs selectively expose task-relevant, interpretable features.
Causal compositionality — By representing world dynamics through logical programs, NSPs allow explicit causal reasoning over predicates (e.g., “If a balance plate is uneven → machine-off”) rather than relying on learned latent correlations.

- 
Contribution to OOD Generalization a. Task-Specific Abstraction Learning

The system learns to invent predicates online that selectively encode task-relevant relational structure. This improves OOD robustness because the model learns what to represent (predicate structure) rather than memorizing perceptual configurations.

Example: In the Coffee domain, instead of memorizing spatial jug-pose distributions, the learned predicate JugInMachine(jug, machine) defines a reusable abstract relation that transfers to novel jugs or machines unseen in training.

For a world model, this suggests an interpretable latent abstraction layer, grounded in learned symbolic structure, that can generalize across unseen object instances, dynamics, and novel combinations.

b. Separation of Perception and Logic

By decoupling low-level sensory grounding (through robust VLM-perception APIs) and high-level logical reasoning (through symbolic code), the model avoids overfitting to pixel statistics — a core failure mode in OOD world modeling (e.g., domain shifts in lighting, object textures, or dexterous configurations). c. Derived Predicates Enable Relational Compositionality

Derived NSPs (e.g., OnPlate(x,y) computed recursively from DirectlyOn) enable zero-shot reasoning over relational hierarchies without direct visual supervision. This compositional generalization allows extrapolating logical combinations in unseen configurations — an essential ingredient for open-ended environments and long-horizon predictions. 3. Contribution to Long-Horizon Future Prediction a. Hierarchical Structure via HLAs

The paper learns High-Level Actions (HLAs) that encode preconditions and effects over NSPs: F(s,ω)=s∪EFF+∖EFF−if PRE⊆s F(s,ω)=s∪EFF+∖EFF−if PRE⊆s

This abstract state transition model operates at a symbolic temporal abstraction level, allowing efficient reasoning over long-horizon plans that would require hundreds of primitive time steps at the pixel-action level.

For an action-conditioned world model, this provides a hierarchical backbone:

NSP-level transitions form macro-transitions measurable over long horizons.
The world model can predict sequences of HLAs to forecast extended futures with much lower combinatorial explosion.

b. Optimistic Operator Learning

Their extended cluster-and-intersect operator learning algorithm prefers optimistic preconditions — enabling exploration and avoiding over-restrictive models. For predictive models, this enables better forward coverage of hypothetical futures, essential for planning or model-based forecasting under uncertainty. c. Planning-Driven Data Collection

Data acquisition is actively coupled with the abstract planner, ensuring the world model samples transitions where abstraction errors matter — a form of goal-conditioned exploration that reduces compounding error in long-horizon predictions. 4. Integration Potential into a 2026 Action-Conditioned World Model

For a world model like 2026, DOI: 10.48550/ARXIV.2510.24161, which likely focuses on predicting future sensory states given action sequences, integration points include: a. Abstract Conditioning Layer

Use NSPs as a predicate-level latent space on top of the continuous latent dynamics model. Prediction can occur both in latent feature space (for fine-grained sensory rollout) and in predicate space (for abstract event prediction), improving semantic stability across long time horizons. b. Neuro-Symbolic Regularization

Incorporate NSP consistency constraints during training: LNSP=∑ψ∈ΨBCE(ψ(xt),ψ(x^t)) LNSP​=ψ∈Ψ∑​BCE(ψ(xt​),ψ(x^t​))

This ensures the predicted world evolution preserves logical consistency across predicates, making the latent dynamics more interpretable and aligned with causal task structure. c. Multi-Scale Planning Interface

Embed symbolic HLAs into the policy/planning head of the world model — allowing the system to roll out macro-steps (“Pick”, “Pour”, “Balance”) internally, while the lower-level dynamics handles continuous execution. 5. Summary Table Challenge in Action-Conditioned World Models	VISUALPREDICATOR Contribution Poor OOD generalization	Learns compositional NSPs and derived predicates grounded in perceptual data Entangled latent representations	Explicit neuro-symbolic factorization of perception and logic Fragile long-horizon predictions	Abstract world model with high-level actions enables stable macro-transition prediction Compounding model error	Planning-guided exploration and optimistic operator learning improve long-term consistency Lack of interpretability	Symbolic NSPs make latent causal mechanisms explicit and inspectable In short:

This paper provides a neuro-symbolic abstraction framework that can be layered atop or within an action-conditioned world model to:

Structure latent space around compositional, interpretable predicates rather than raw pixels,
Support symbolic future prediction over long action horizons, and
Improve robustness and generalization across environments and object types by learning transferable logical world models.

If you want, I can sketch a possible hybrid architecture diagram showing how NSP-based symbolic abstractions could be integrated into a modern transformer-based world model for 2026 predictive control — would you like that? 17:15 05/29/26

## 附件与批注

### PDF

[打开 PDF](zotero://open-pdf/library/items/3X94NCTZ)

[批注 29L56GS3 · 第 2 页](zotero://open-pdf/library/items/3X94NCTZ?annotation=29L56GS3&page=2)

> challenges

[批注 J9YWPDPT · 第 2 页](zotero://open-pdf/library/items/3X94NCTZ?annotation=J9YWPDPT&page=2)

> Neuro-Symbolic Predicates

[批注 A7ISD7FM · 第 2 页](zotero://open-pdf/library/items/3X94NCTZ?annotation=A7ISD7FM&page=2)

> the predicates must be learned from input pixel data,

[批注 DJADRWPH · 第 2 页](zotero://open-pdf/library/items/3X94NCTZ?annotation=DJADRWPH&page=2)

> they should not overfit to the situations encountered during training,

[批注 UECHHDMB · 第 2 页](zotero://open-pdf/library/items/3X94NCTZ?annotation=UECHHDMB&page=2)

> zero-shot generalize

[批注 AG8FN4LJ · 第 2 页](zotero://open-pdf/library/items/3X94NCTZ?annotation=AG8FN4LJ&page=2)

> need an efficient way of exploring different possible plans to collect the data needed to learn good predicates

[批注 86LLX4SE · 第 2 页](zotero://open-pdf/library/items/3X94NCTZ?annotation=86LLX4SE&page=2)

> a new robot learning approach that interleaves proposing new predicates (using VLMs), predicate scoring/validation (adapting the modern predicate-learning algorithm by Silver et al. (2022)), and goal-driven exploration with a planner in the loop

[批注 254RLV5D · 第 2 页](zotero://open-pdf/library/items/3X94NCTZ?annotation=254RLV5D&page=2)

> NSPs

[批注 SQSLUI7V · 第 2 页](zotero://open-pdf/library/items/3X94NCTZ?annotation=SQSLUI7V&page=2)

> An algorithm for inventing NSPs

[批注 LKBBFQEB · 第 2 页](zotero://open-pdf/library/items/3X94NCTZ?annotation=LKBBFQEB&page=2)

> an extension to a new operator learning algorithm

[批注 DWMINSGY · 第 2 页](zotero://open-pdf/library/items/3X94NCTZ?annotation=DWMINSGY&page=2)

> continuous state/action spaces

[批注 V55GUXDH · 第 2 页](zotero://open-pdf/library/items/3X94NCTZ?annotation=V55GUXDH&page=2)

> online interaction with the environment

[批注 QTTJPFQA · 第 2 页](zotero://open-pdf/library/items/3X94NCTZ?annotation=QTTJPFQA&page=2)

> learn state abstractions from training tasks that generalize to held-out test tasks

[批注 C8EM3NFR · 第 2 页](zotero://open-pdf/library/items/3X94NCTZ?annotation=C8EM3NFR&page=2)

> minimal planning budget.

[批注 NQUPEXCK · 第 3 页](zotero://open-pdf/library/items/3X94NCTZ?annotation=NQUPEXCK&page=3)

> Skills, tasks, and environments are the primary inputs

[批注 3NTTPP4I · 第 3 页](zotero://open-pdf/library/items/3X94NCTZ?annotation=3NTTPP4I&page=3)

> higher-level abstractions over these basic states and actions

[批注 CZFZ53J3 · 第 3 页](zotero://open-pdf/library/items/3X94NCTZ?annotation=CZFZ53J3&page=3)

> A predicate ψ is a Boolean feature of a state

[批注 6NWK4GLG · 第 3 页](zotero://open-pdf/library/items/3X94NCTZ?annotation=6NWK4GLG&page=3)

> A set of predicates Ψ induces an abstract state

[批注 NQTBBBI4 · 第 3 页](zotero://open-pdf/library/items/3X94NCTZ?annotation=NQTBBBI4&page=3)

> High-Level Actions (HLAs) augment skills with preconditions

[批注 NMSURFFS · 第 3 页](zotero://open-pdf/library/items/3X94NCTZ?annotation=NMSURFFS&page=3)

> and postconditions

[批注 ZAFB8NCC · 第 3 页](zotero://open-pdf/library/items/3X94NCTZ?annotation=ZAFB8NCC&page=3)

> HLA ω is a function from a tuple  of objects in Om to a tuple ⟨π, PRE, EFF+, EFF−⟩ where π ∈ AO is a skill

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
