# Grok 最新模型卡

- 最新模型名称：Grok 4.20 reasoning / non-reasoning。[S024: API table]
- 发布时间：xAI API 页列为 latest/new；具体发布时间需 xAI release notes 更新。[S024: API table]
- 开放程度：闭源 API。
- 架构：官方未披露参数、专家、attention、tokenizer；第三方关于 multi-agent 的说法不作为官方架构事实。
- 预训练：官方未披露。
- 后训练：官方 API 页强调 lowest hallucination rate、strict prompt adherence；训练方法未披露。[S024: API table]
- 推理方式：reasoning/non-reasoning variants、2M context、agentic tool calling。[S024: API table]
- 微调/部署：xAI API；无开放权重。[S024: API table]
- LMArena 最新表现：grok-4.20-beta1 rank 8、rating 1485.0；grok-4.20-beta-0309-reasoning rank 10；grok-4.20-multi-agent-beta-0309 出现在 2026-04-02 snapshot。[S051: rows][S050: viewer rows]
- 核心优势：2M context、实时/工具产品生态、偏低价格。
- 核心短板：闭源架构与安全细节有限；LMArena 4.20 条目部分可能 preliminary。
- 与其他模型关键区别：xAI 把大上下文与低幻觉/prompt adherence 作为 API 卖点。[S024: API table]
- 未公开信息：参数、训练数据、专家、具体 multi-agent 是否底层架构。
- claim-to-source map：C012->S024。

