# GLM / Z.ai 最新模型卡

- 最新模型名称：GLM-5.1。[S022: Overview]
- 发布时间：Z.ai release notes 显示 2026-04-07。[S022: release notes]
- 开放程度：Z.ai 文档/API；开源/MIT 状态需以 Hugging Face/GitHub model card 核对，本项目将 docs 页明确内容作为事实。[S022: Overview]
- 架构：Z.ai GLM-5.1 docs 未披露参数/专家/attention；描述为 long-horizon flagship foundation model。[S022: Overview]
- 预训练：官方 docs 摘录未披露训练数据、硬件、优化器。
- 后训练：release notes 称 built with multi-turn SFT, RL, process-quality evaluation framework。[S022: release notes]
- 推理方式：200K context、128K output、thinking mode、streaming、function call、context caching、structured output、MCP。[S022: Capability]
- 微调/部署：Z.ai API；本地/open-weight 细节需 model card 更新。
- LMArena 最新表现：GLM-4.7 在 WebDev rank 6；GLM-4.6 在 text_style_control rank 56。GLM-5.1 出现在 LMArena viewer older snapshot但本 CSV未完整抓取。[S052: webdev latest][S051: rows]
- 核心优势：长程工程任务、自主迭代、工具与 MCP 集成。
- 核心短板：官方 docs 页未披露架构参数；需区分 GLM-5.1 与 GLM-4.7/5 榜单条目。
- 与其他模型关键区别：Z.ai 明确把评估重心从单轮能力转向 8 小时 sustained execution。[S022: Long-Horizon]
- 未公开信息：参数、激活参数、专家、attention、训练 token。
- claim-to-source map：C011->S022。

