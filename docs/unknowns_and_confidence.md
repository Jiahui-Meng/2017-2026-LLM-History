# 未公开信息与置信度

## 判定规则

- 只记录官方发布页、官方文档、官方 GitHub/Hugging Face model card、官方论文或官方 config 中明确出现的事实。
- 闭源模型未公开的结构、参数、专家数、训练 token、后训练细节，统一写“官方未披露”。
- 产品系统能力和 base model 内部结构强制分开；不能因为 ChatGPT、Muse Spark、Claude Code 很强，就反推底层模型结构。

## 历史叙事里的高风险误区

| 误区 | 正确处理 |
|---|---|
| 把“产品节点”写成“模型架构节点” | 例如 ChatGPT、Muse Spark、Claude Code 需要标记为 product/system node。 |
| 把早期技术报告数字直接套到后续未披露版本 | 例如 DeepSeek-V3 的公开数字不能直接当作 V3.2 未披露字段。 |
| 用排行榜结果补全架构事实 | LMArena 只能说明人类偏好结果，不能证明参数、专家、注意力机制。 |
| 把同样叫 MoE 的家族写成同一种创新 | Mixtral、DeepSeek、Qwen、Kimi、Llama 4、Mistral Large 3 的 MoE 路线和公开粒度并不相同。 |

## 闭源家族的主要未知项

| 家族 | 已知 | 官方未披露 |
|---|---|---|
| OpenAI GPT-4 / GPT-5.x | context、工具、推理预算、产品能力。[S001][S003][S044] | dense/MoE、参数、层数、专家数、完整训练与后训练配方。 |
| Claude 3 / 4.x | Constitutional AI 路线、长上下文、effort、task budget、agentic coding。[S005][S045][S047] | 参数、层数、专家路由、训练 token 与完整奖励设计。 |
| Gemini 1.5 / 3 | 1M 级 context、多模态、Thinking、grounding、tooling。[S008][S009][S048] | 参数、专家结构、完整训练/后训练配方。 |
| Grok 4.20 | 2M context、reasoning/non-reasoning 变体。[S024] | 内部结构、训练细节、专家路由。 |
| Muse Spark | 产品能力和子代理工作流定位。[S011] | 底层模型结构与训练细节。 |

## 开放权重家族的主要未知项

开放权重模型通常更透明，但也未必披露完整训练与后训练配方。DeepSeek、Qwen、Kimi、MiniMax、GLM、Llama 4、Mistral Large 3 虽然公开了大量结构事实，但在 active params、训练 token、奖励细节和完整 agent 数据配方上仍经常保留空白。[S015][S027][S028][S029][S030][S031][S032][S033][S035]
