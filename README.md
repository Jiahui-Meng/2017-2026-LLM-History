# 2025-2026 最新大语言模型架构与能力图谱

本项目是一个中文研究库，聚焦 2025-2026 公开可核验的主流大语言模型：OpenAI GPT/ChatGPT/o 系列、Anthropic Claude、Google Gemini、Meta Muse/Llama、Moonshot Kimi、DeepSeek、Qwen、MiniMax、Z.ai/GLM、xAI Grok、Mistral。所有关键事实按 claim-level citation 标注；闭源模型未披露的参数、专家数、训练数据规模等均写为“官方未披露”，不做猜测。[S001: GPT-5.5 release][S050: dataset card]

## 最新模型清单

| 机构 | 最新公开模型/路线 | 开放程度 | 关键定位 |
|---|---|---:|---|
| OpenAI | GPT-5.5；API 侧最新稳定主线仍需区分 GPT-5.4 | 闭源 | 复杂真实工作、工具使用、代码、研究；GPT-5.5 暂未同步 API 发布。[S001: Intro][S004: ChatGPT rollout] |
| Anthropic | Claude Opus 4.7 | 闭源 | 混合推理、长程编码代理、1M context、xhigh effort。[S005: Also launching today][S006: product page] |
| Google | Gemini 3.1 Pro / Gemini 3 Pro family | 闭源 | 多模态、长上下文、grounding、工具与 coding。[S010: launch][S009: Meet Gemini 3] |
| Meta | Muse Spark；开放权重路线为 Llama 4 Scout/Maverick | Muse 闭源/私测 API；Llama 开放权重 | 消费级 Meta AI 与多代理产品系统；Llama 4 是 MoE 多模态开放权重。[S011: Takeaways][S013: Llama specs] |
| Moonshot/Kimi | kimi-k2.6 | Modified MIT/open-weight + 托管 API | 原生多模态 agentic、thinking/non-thinking、256k context。[S017: Model List] |
| DeepSeek | DeepSeek-V3.2 / V3.2-Speciale | MIT/open-weight | MoE + MLA/DSA、reasoning-first、thinking in tool-use。[S014: Release] |
| Qwen | Qwen3.6-35B-A3B；旗舰仍含 Qwen3.5-397B-A17B | Apache 2.0/open-weight | 高效 MoE、混合注意力、长上下文、多语言。[S019: News] |
| MiniMax | MiniMax-M2.1 | Modified MIT/open-weight | 230B/10B active MoE，面向 coding、tool use、long-horizon agent。[S020: Overview] |
| Z.ai/GLM | GLM-5.1 | MIT/open-weight/API | 长程 8 小时自主工程任务、200k context、工具使用。[S022: Overview] |
| xAI | Grok 4.20 reasoning/non-reasoning | 闭源 | 2M context、低幻觉、prompt adherence、工具调用。[S024: API table] |
| Mistral | Mistral Large 3 / Mistral 3 family | Apache 2.0/open-weight | 675B/41B active sparse MoE，多模态、多语言、企业自部署。[S025: Mistral Large 3] |

## 十大最新技术趋势

1. Frontier 模型从“单次问答”转向 long-horizon agent：GPT-5.5、Claude Opus 4.7、GLM-5.1、Kimi K2.6 都强调计划、工具、验证和持续执行。[S001: Intro][S005: Testing][S022: Overview][S017: Model List]
2. MoE 成为开放权重 frontier 主流：DeepSeek、Llama 4、Kimi、Qwen、MiniMax、GLM、Mistral Large 3 均公开采用稀疏专家路线。[S014: Release][S013: Llama specs][S020: Overview][S025: Mistral Large 3]
3. 闭源 frontier 不再披露参数规模：OpenAI、Anthropic、Google、xAI 的最新模型官方材料未公开总参数、激活参数和专家数。[S001: Intro][S005: Intro][S009: Meet Gemini 3][S024: API table]
4. 推理时计算产品化：OpenAI Pro/Thinking、Claude effort、Gemini Thinking、Kimi thinking/non-thinking、GLM thinking mode 都把“思考预算”作为接口或产品能力。[S003: GPT-5.4][S005: Also launching today][S009: Meet Gemini 3][S017: Model List][S022: Capability]
5. 多模态从“视觉插件”变为原生能力：Gemini 3、Muse Spark、Kimi K2.6、Mistral Large 3、Llama 4 都强调文本+图像/视频/PDF 的统一处理。[S009: Model table][S011: Ask Meta AI][S017: Model List][S025: Mistral Large 3][S013: Llama specs]
6. 长上下文进入 1M+ 时代，但实现路径不同：Gemini 3 为 1M 输入，OpenAI GPT-5.4 API 为 1M，Claude Opus 4.7 产品页称 1M，Grok 4.20 为 2M，Llama 4 Scout 为 10M。[S009: Model table][S003: Computer use][S006: product page][S024: API table][S013: Llama specs]
7. Attention/KV cache 优化公开化：DeepSeek MLA/DSA、Llama iRoPE/NoPE、Qwen hybrid attention、Mistral sparse MoE serving 都直接服务于长上下文与低成本部署。[S015: Model Summary][S016: DSA][S012: iRoPE][S019: News][S025: NVIDIA collaboration]
8. 开放权重模型更强调可部署性：Mistral NVFP4、MiniMax FP8/BF16、Kimi INT4、Llama int4 单 H100、GLM/MIT 都在降低企业自托管门槛。[S025: vLLM/NVFP4][S020: model card][S018: K2 overview][S013: Llama specs][S022: Overview]
9. LMArena 从 Overall 走向多维拆分：text_style_control、webdev、vision、document、search、text_to_image、image_edit 等拆分更能暴露产品系统能力差异。[S050: Subsets]
10. “架构能力”和“产品系统能力”边界更模糊：搜索 grounding、computer use、file search、tool search、agent swarm、subagents 往往不是裸模型能力，而是模型+工具+路由+安全策略的系统结果。[S003: Tools][S011: subagents][S024: API table]

## 核心模型差异总结

闭源模型的最大差异已转向推理时计算、工具集成和产品路由，而不是可见参数规模；开放权重模型的最大差异则在 MoE 稀疏度、attention/KV 优化、上下文长度、许可约束和部署格式。DeepSeek 与 Kimi 倾向“巨大 MoE + 低激活 + 长程 agent”；Qwen 与 GLM 强调中文/多语言和工程代理；Mistral 强调 Apache 2.0 与欧洲企业部署；MiniMax 聚焦低激活 coding agent；Meta 同时走 Muse 闭源产品化和 Llama 开放权重路线。[S014: Release][S017: Model List][S019: News][S022: Overview][S025: Mistral Large 3][S020: Overview][S011: Takeaways][S013: Llama specs]

## LMArena 最新观察

LMArena 是人类偏好盲测，不是绝对智能测验；rating、置信区间和 vote_count 必须一起读，preliminary/低票数模型不能只按 rank 下结论。[S050: Notes][S050: Schema] 在 text_style_control/latest 的公开数据中，Claude Opus 4.7 thinking、Claude Opus 4.6 thinking、Gemini 3.1 Pro preview、Grok 4.20、GPT-5.4-high 等模型处于前列，但不同日期快照会变动。[S051: text_style_control latest rows] WebDev 榜单对工具化编码更敏感，Claude Opus thinking、GPT-5.2-high、Gemini 3 Pro、GLM-4.7、MiniMax-M2.1 均靠前。[S052: webdev latest]

## 架构 vs LMArena 分析

LMArena 高分和架构没有单因果关系。MoE 开放模型可以上榜，但 text_style_control 前列仍有大量闭源、参数未知模型；WebDev 高分更可能来自后训练、工具调用稳定性、测试时计算和产品脚手架；Vision/Text-to-Image 榜单受视觉 encoder、图像生成模型和安全/审美后训练影响更大。[S050: Subsets][S052: webdev latest][S053: text_to_image latest][S054: vision latest]

## 未公开信息清单

OpenAI GPT-5.5/GPT-5.4、Claude Opus 4.7、Gemini 3.1/3、Grok 4.20、Muse Spark 的参数规模、专家数、训练 token 数、优化器和完整数据配比官方未披露。[S001: Intro][S005: Intro][S010: launch][S024: API table][S011: A New Model] 这些项目在表格中均写为“官方未披露”，只把官方公开的 context、modalities、接口能力和安全/系统卡信息列为事实。

## Citation Audit 摘要

本库共建立 50+ 条 claim 记录，关键事实映射到 `data/claims.yaml`；高风险项包括闭源参数、LMArena 快照日期、第三方 benchmark 和“agentic/multi-agent”系统边界，详见 `citation_audit.md`。

## 后续更新方法

1. 先更新 `data/sources.yaml` 的 `accessed_at` 与新来源。
2. 用 Hugging Face `lmarena-ai/leaderboard-dataset` 的 `latest` split 重建 `data/lmarena_latest.csv`。[S050: Usage]
3. 只替换有来源支撑的 claim；闭源参数继续写“官方未披露”。
4. 重新同步 `tables/` 与 `docs/model_cards/` 中的 claim-to-source map。

## 目录

见各章节：

- `docs/latest_model_landscape.md`
- `docs/architecture_comparison.md`
- `docs/lmarena_results.md`
- `docs/model_cards/`
- `data/models.yaml`
- `data/sources.yaml`
- `data/claims.yaml`

