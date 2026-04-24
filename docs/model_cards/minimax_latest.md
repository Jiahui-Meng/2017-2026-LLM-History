# MiniMax 最新模型卡

- 最新模型名称：MiniMax-M2.1。[S020: model card]
- 发布时间：MiniMax 官方新闻为 2025-12-23，后训练经验文为 2026-01-22。[S021: header]
- 开放程度：Modified MIT/open-weight/API。[S020: model card]
- 架构：MoE，约 230B total / ~10B active。[S020: Overview][S021: Model Overview]
- 预训练：完整预训练数据/优化器/硬件官方未披露。
- 后训练：Agentic Data Synthesis 包括 real-data-driven SWE Scaling、expert-driven AppDev、virtual long-horizon WebExplorer。[S021: Agentic Data Synthesis]
- 推理方式：面向 coding、tool use、instruction following、long-horizon planning；推荐 SGLang/vLLM/Transformers/KTransformers/MLX-LM。[S020: Local Deployment]
- 微调/部署：Hugging Face weights，API，local deployment。[S020: How to Use]
- LMArena 最新表现：WebDev rank 7、rating 1422、votes 6387；text_style_control 中 MiniMax-M2.5 另见数据集快照。[S052: webdev latest]
- 核心优势：低激活参数、高 agent/coding 性价比、开放权重。
- 核心短板：通用多模态能力不是主要公开卖点；完整训练细节较少。
- 与其他模型关键区别：相比 Mistral/DeepSeek/Kimi，MiniMax 更明确聚焦“可部署 coding agent”。
- 未公开信息：专家数量、训练 token、数据配比。
- claim-to-source map：C010->S020/S021。

