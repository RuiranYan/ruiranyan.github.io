---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Education
======
* **硕士**, 大数据技术与工程, 中国科学技术大学人工智能与数据科学学院 (在读)
* **学士**, 中科大少年班学院, 中国科学技术大学

Projects & Open Source
======
* **OmniGen / OmniGen2 — 通用图像生成与主体驱动数据**
  * 在北京智源研究院参与 OmniGen 系列项目，目标是构建统一的图像生成模型，支持文本到图像生成、图像编辑以及多种视觉任务，并通过统一框架实现跨任务的知识迁移。负责从零搭建主体驱动多模态数据工作流（GroundingDINO + SAM / SAM2 + Outpaint），构建大规模主体驱动数据集 X2I / X2I2，并基于此训练 OmniGen V1 / V2，大幅提升主体一致性与生成自然度。
  * *Tags: Multimodal, Image Generation, BAAI*

* **Agent-R1 — 面向 Agent 系统的强化学习框架**
  * 作为开源项目 Agent-R1 的核心贡献者之一，参与设计用于 agentic system 的端到端强化学习训练框架，支持多轮对话、多工具调用等复杂场景，并在 PPO / GRPO 等主流算法上做了适配和修正，推动大模型在真实任务上的强化学习训练实践。
  * *Tags: Agent, RL, Open Source*

* **O1Embedder — 让检索模型先“想一想”**
  * 面对复杂多步推理任务，传统表征模型难以直接利用推理型大模型的能力。O1Embedder 通过构造长思维链数据，将大模型“思考过程”转化为监督信号，并用多任务学习统一推理与表征能力，使检索模型在复杂推理和 zero-shot 场景下具备更强的理解与泛化能力。
  * *Tags: Representation, Reasoning*

Engineering & Internship experience
======

* **字节跳动 · 抖音搜索 — 个性化预训练大模型 / LLM4Rec**
  * 在抖音搜索多模态预训练方向，围绕“个性化预训练大模型”展开工作：通过多模态表征构建、RQ-VAE / RQKmeans 量化分词以及表征回写方案，构建适配抖音域内的视频表征模型，并将其应用于精排与长序列检索，在严点 QAUC、主动点 QAUC 等指标上取得线上收益。
  * *Tags: LLM4Rec, Multimodal*

* **OPPO · 应用商城 - 多任务推荐**
  * 在 OPPO 围绕多任务推荐模型与工业级系统迭代进行了多轮优化：在信息流及应用商店分发搜索主场景下，对公司多任务模型 PLE 引入表征解耦与辅助蒸馏机制，缓解任务间负迁移问题，并通过优化 Gate 网络结构，在控制模型复杂度的同时取得可观的 AUC 提升和线上收益。
  * *Tags: Recommender Systems, Multitask*

Competitions & Awards
======

* **Meta KDD Cup 2024 · CRAG: Comprehensive RAG Benchmark**
  * 在 Meta KDD Cup 2024 CRAG 赛道中，围绕复杂现实场景的检索增强生成系统设计方案：通过 query 域分类与实体抽取、结合知识图谱的数据重写，以及大模型自验证机制，提升 RAG 系统在复杂问题与噪声环境下的鲁棒性与可信度，最终取得全球第四与复杂问题特别奖。
  * *Tags: RAG, Competition*

Skills
======
* Multitask Learning
* Multimodal Models
* Representation & Reasoning
