# DeepSeek 最新模型卡

- 最新模型名称：DeepSeek-V3.2 与 V3.2-Speciale。[S014: Release]
- 发布时间：DeepSeek-V3.2 release page 日期为 2025-12-01。[S014: URL]
- 开放程度：MIT/open-weight/API。[S014: Open Source Release]
- 架构：V3 lineage 是 671B total / 37B active MoE，采用 MLA、DeepSeekMoE、auxiliary-loss-free load balancing、MTP；V3.2-Exp 引入 DSA。[S015: Introduction][S016: DSA]
- 预训练：DeepSeek-V3 预训练 14.8T tokens，2.788M H800 GPU hours，训练稳定无不可恢复 loss spikes。[S015: Introduction]
- 后训练：DeepSeek-V3 经 SFT/RL；V3.2 引入 agent training data synthesis covering 1,800+ environments and 85k+ complex instructions。[S015: Introduction][S014: Thinking in Tool-Use]
- 推理方式：thinking in tool-use；V3.2-Speciale 更高 token usage 且 release page 称 API-only/no tool-use for evaluation。[S014: Release]
- 微调/部署：开放权重 Hugging Face；API/App/Web 可用。[S014: Open Source Release]
- LMArena 最新表现：deepseek-v3.2 rank 58、rating 1424.2、votes 42815；deepseek-v3.2-exp-thinking rank 57。[S051: rows]
- 核心优势：公开架构、低成本、高效长上下文、工具思考。
- 核心短板：V3.2 与 V3 lineage 的精确差异需读 tech report；地缘与合规风险需企业自评。
- 与其他模型关键区别：DeepSeek 明确公开 MLA/DSA/MoE/训练稳定性，透明度高于闭源模型。[S015: Model Summary][S016: DSA]
- 未公开信息：V3.2 完整逐层参数若不同于 V3 lineage需更新。
- claim-to-source map：C007->S014；C008->S015/S016。

