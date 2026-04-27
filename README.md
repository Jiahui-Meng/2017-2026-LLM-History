# 2017-2026 LLM 发展时间线与创新图谱

本项目从“最新模型横向对比”重构为“LLM 发展史时间线”。核心问题不再是“现在谁最新”，而是“每一代关键模型出现时，它比上一代提升了什么、创新是什么、又留下了什么问题”。项目覆盖 OpenAI、Anthropic Claude、Google Gemini、Meta/Llama、Kimi、DeepSeek、Qwen，以及 MiniMax、GLM、xAI、Mistral 等主流路线；闭源模型继续坚持“官方未披露就明确写未披露”，不拿二手猜测补空白。[S036][S041][S045][S050]

## 五个阶段

1. `Transformer 基础期 (2017-2019)`：先解决“怎么更好地建模序列和通用文本表示”，代表节点是 Transformer、GPT-1、BERT、T5。[S036][S037][S038][S039]
2. `规模涌现期 (2020-2021)`：参数、数据和算力一起放大，GPT-3 证明 few-shot 能力会随规模出现；FLAN 则说明“会做任务”不只靠预训练，也靠指令化后训练。[S040][S041][S042]
3. `对齐与聊天期 (2022-2023)`：InstructGPT、ChatGPT、Claude 把“能生成”推进到“能听懂人类意图、连续对话、遵守约束”。[S043][S045][S046]
4. `开源竞赛期 (2023-2024)`：Llama 2、Mixtral、Gemini 1.5、Qwen2.5、DeepSeek-V3 让 open-weight、MoE、长上下文、多模态成为主线竞争点。[S048][S049][S056][S059][S015]
5. `推理与 Agent 期 (2025-2026)`：Claude 4.x、Gemini 3、Llama 4、Kimi K2.6、DeepSeek-R1/V3.2、Qwen3.x 把 reasoning、tool use、长程执行、MoE 工程化推到台前。[S005][S009][S014][S017][S033][S060]

## 全局时间线总览

| 时间 | 节点 | 提升 | 创新 | 行业影响 |
|---|---|---|---|---|
| 2017-06 | Transformer | 抛开 RNN 串行瓶颈，训练并行性和长程依赖处理显著提升 | self-attention + encoder-decoder attention | 成为后续 GPT、BERT、T5、Gemini、Claude、Llama 的共同底座。[S036] |
| 2018-06 | GPT-1 | 把“先大规模预训练，再任务微调”做成统一范式 | 生成式预训练 | 为 GPT 系列和“语言模型即基础模型”路线定型。[S037] |
| 2018-10 | BERT | 在理解任务上大幅提升表示质量 | 双向编码器 + MLM | 奠定了 encoder 路线和后续检索/理解型 NLP 基础。[S038] |
| 2019-10 | T5 | 把多任务统一到 text-to-text 接口 | 统一任务格式 | 影响了 FLAN、instruction tuning 和后来的通用 API 设计。[S039] |
| 2020-05 | GPT-3 | 少样本能力明显增强 | 通过 scaling 获得 in-context learning | 让“大模型涌现能力”成为行业共识。[S040] |
| 2021-10 | FLAN | 同等底座下更会按指令做事 | instruction tuning | 证明“后训练范式”能显著改变模型可用性。[S042] |
| 2022-03 | Chinchilla | 同算力下训练更高效 | compute-optimal scaling law | 改变了“只堆参数”的思路，转向参数与 token 配比优化。[S041] |
| 2022-12 | ChatGPT / InstructGPT | 更稳定地对话、遵循意图和拒答 | RLHF 产品化 | 把 LLM 从研究对象变成大众产品。[S043] |
| 2023-03 | GPT-4 | 更强泛化、可靠性和多模态能力 | 更大规模对齐和 system-level deployment | 推高闭源前沿模型的能力上限与安全讨论门槛。[S044] |
| 2023-03 | Claude / Constitutional AI | 在对齐中更强调规则化、自我批评和无害性 | Constitutional AI | 形成与 RLHF 并列的重要对齐路线。[S045][S046] |
| 2023-07 | Llama 2 | 高质量 open-weight 路线成型 | 开放权重基础模型 + chat 版 | 极大加速了开源生态和企业自部署。[S049] |
| 2023-12 | Mixtral 8x7B | 以较低激活成本换更高总容量 | 稀疏 MoE 开源化 | 把 MoE 从研究概念推进到开源主战场。[S056] |
| 2024-02 | Gemini 1.5 | 超长上下文和原生多模态显著前进 | 1M 级 context + multimodal family | 长上下文从实验能力变成前沿产品能力。[S048] |
| 2024 | Qwen2 / Qwen2.5 | 中文、多语言、代码与长上下文能力均衡提升 | 系列化 open-weight、工具和多模态布局 | 让 Qwen 成为开源中文与多语言主线之一。[S058][S059] |
| 2024-12 | DeepSeek-V3 | 以更透明的开源结构追求高能力低成本 | DeepSeekMoE + MLA + MTP | 强化了“开源 frontier 也能做结构创新”的预期。[S015] |
| 2025-01 | DeepSeek-R1 | 推理能力和过程监督进入新阶段 | reasoning-first RL 路线 | 让行业重新聚焦 test-time compute 与 reasoning 训练。[S057] |
| 2025-2026 | Claude 4.x | agentic coding、effort、task budget 更强 | 推理预算产品化 | 说明高端模型竞争已从回答质量转向长程执行质量。[S005][S047] |
| 2025-2026 | Kimi K2.x | 长上下文、多模态、agent 化继续增强 | thinking/non-thinking、原生多模态 agent | Kimi 从“长文本入口”升级为综合 agent 路线。[S017][S018][S061] |
| 2025-2026 | Qwen3.x | 在开源家族里继续推进 MoE、混合注意力和多模态 | hybrid attention + MoE frontier 化 | 证明开源家族也能持续迭代架构而非只追随闭源。[S019][S030][S031][S060] |
| 2025-2026 | Llama 4 / Muse Spark | Meta 同时推进开放权重模型和产品系统模型 | MoE 多模态 open-weight + 产品路由/子代理 | 体现“模型路线”和“产品系统路线”开始分叉发展。[S011][S033][S034] |
| 2025-2026 | Gemini 3 / GPT-5.x / Grok 4.20 / GLM-5.1 / MiniMax-M2.1 / Mistral Large 3 | reasoning、工具、长上下文、部署效率集体升级 | frontier 推理预算、agentic 工具链、稀疏化与部署优化 | 当前竞争焦点已从单次问答转向 long-horizon work。[S001][S005][S009][S020][S022][S024][S025] |

## 主线家族

- [OpenAI 历史页](docs/model_cards/openai_history.md)
- [Claude 历史页](docs/model_cards/claude_history.md)
- [Gemini 历史页](docs/model_cards/gemini_history.md)
- [Meta / Llama 历史页](docs/model_cards/meta_history.md)
- [Kimi 历史页](docs/model_cards/kimi_history.md)
- [DeepSeek 历史页](docs/model_cards/deepseek_history.md)
- [Qwen 历史页](docs/model_cards/qwen_history.md)

## 第二层家族页

- [MiniMax 历史页](docs/model_cards/minimax_history.md)
- [GLM 历史页](docs/model_cards/glm_history.md)
- [Grok 历史页](docs/model_cards/grok_history.md)
- [Mistral 历史页](docs/model_cards/mistral_history.md)

## 创新专题

- [全局时间线详解](docs/llm_timeline.md)
- [预训练路线演进](docs/pretraining.md)
- [后训练路线演进](docs/post_training.md)
- [推理模型演进](docs/reasoning_models.md)
- [多模态模型演进](docs/multimodal_models.md)
- [Agent 与工具使用演进](docs/agentic_tool_use.md)

## 表格与图表

- [时间线总表](tables/timeline_overview.md)
- [创新矩阵表](tables/innovation_matrix.md)
- [架构结构表（附录）](tables/architecture_comparison.md)
- [时间线与范式跃迁图](diagrams/llm_taxonomy.mmd)
- [家族分叉图](diagrams/family_branches.mmd)
- [Dense vs MoE 结构示意](diagrams/dense_vs_moe.mmd)

## 附录

- [当前格局快照](docs/latest_model_landscape.md)
- [LMArena 结果](docs/lmarena_results.md)
- [LMArena 方法论](docs/lmarena_methodology.md)
- [未公开信息与置信度](docs/unknowns_and_confidence.md)
- [Citation Audit](citation_audit.md)
