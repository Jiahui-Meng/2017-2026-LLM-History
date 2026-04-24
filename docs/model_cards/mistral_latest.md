# Mistral 最新模型卡

- 最新模型名称：Mistral Large 3 / Mistral 3 family。[S025: header]
- 发布时间：Mistral docs 标注 v25.12，博客发布 Mistral 3。[S026: docs][S025: header]
- 开放程度：Apache 2.0/open-weight。[S025: Mistral Large 3]
- 架构：Sparse MoE，675B total / 41B active；Mistral Large 3 是 multimodal multilingual model。[S025: Mistral Large 3][S026: docs]
- 预训练：从零训练于 3000 NVIDIA H200 GPUs；完整数据配比未披露。[S025: Mistral Large 3]
- 后训练：instruction fine-tuned versions released；reasoning version coming soon。[S025: Mistral Large 3]
- 推理方式：256k context；vLLM/Red Hat/NVIDIA optimized NVFP4, Blackwell attention and MoE kernels, speculative decoding。[S025: NVIDIA collaboration][S026: docs]
- 微调/部署：base/instruct weights、Mistral AI Studio、Bedrock、Azure Foundry、HF、OpenRouter、Fireworks、Together 等。[S025: Available Today]
- LMArena 最新表现：mistral-large-3 在 text_style_control rank 76、rating 1415.4、votes 40077。[S051: rows]
- 核心优势：Apache 2.0、欧洲/企业部署、开放权重 frontier MoE。
- 核心短板：非 reasoning 版在复杂推理上未必领先；训练数据配比未披露。
- 与其他模型关键区别：Mistral 用 permissive open weights 和企业部署生态形成差异。[S025: Why Mistral 3]
- 未公开信息：训练数据配比、完整后训练配方。
- claim-to-source map：C013->S025/S026。

