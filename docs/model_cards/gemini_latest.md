# Gemini 最新模型卡

- 最新模型名称：Gemini 3.1 Pro；Gemini 3 Pro Preview/Flash/Image 是 3 系列核心公开 API 族。[S010: launch][S009: Meet Gemini 3]
- 发布时间：Gemini 3.1 Pro 博客发布于 2026-02-19；Gemini 3 Pro docs latest update 为 2025-11。[S010: header][S008: Gemini 3 Pro]
- 开放程度：闭源 API/Vertex/Gemini app/NotebookLM。[S010: launch]
- 架构：官方未披露参数、专家、attention；公开定位为 multimodal reasoning / agentic workflows。[S009: intro]
- 预训练：训练数据规模、硬件、优化器官方未披露；knowledge cutoff Jan 2025。[S009: Model table]
- 后训练：官方未披露完整 SFT/RL 配方。
- 推理方式：Thinking、function calling、search grounding、code execution、file search、URL context、structured outputs。[S009: Model table]
- 微调/部署：闭源 API 与 Google Cloud/Vertex；无开放权重。[S010: launch]
- LMArena 最新表现：text_style_control 中 gemini-3.1-pro-preview rank 6、rating 1492.2、votes 22905；vision 榜 Gemini 3 Pro rank 1。[S051: rows][S054: vision latest]
- 核心优势：多模态长上下文、搜索 grounding、视觉/文档/视频输入。[S009: Model table]
- 核心短板：闭源参数和训练细节未知；preview 版本可能变动。[S009: Model version patterns]
- 与其他模型关键区别：Google 把 native multimodal、Search grounding 与 1M context 集成进 API 作为差异。[S009: Model table]
- 未公开信息：参数、激活参数、专家、训练 token、完整 tokenizer。
- claim-to-source map：C004->S008/S009/S010；C014->S050。

