# 未公开信息与置信度

## 判定规则

- 只有官方发布页、官方文档、官方 GitHub/Hugging Face model card、官方 config.json 中出现的字段，才写入事实表。
- 没有官方字段时统一写“官方未披露”。
- LMArena 分数只用于人类偏好观察，不用于补全结构字段。[S050: schema]

## 闭源模型未公开结构

| 模型 | 已公开接口结构 | 官方未披露字段 | 置信度 |
|---|---|---|---|
| GPT-5.5 / GPT-5.4 | GPT-5.4 1M context、reasoning effort、computer use；GPT-5.5 ChatGPT/Codex 发布。[S001][S003][S004] | dense/MoE、参数、active params、layers、hidden size、attention、positional encoding、experts/router、tokenizer/vocab、训练与后训练配方。 | 高 |
| Claude Opus 4.7 | 1M context、xhigh effort、task budgets、图像输入、API/云平台部署。[S005][S006] | 参数、active params、layers、hidden size、attention、experts/router、tokenizer/vocab、训练与后训练配方。 | 高 |
| Gemini 3.1 Pro / 3 Pro | 1,048,576 input / 65,536 output tokens、多模态输入、thinking、function calling、search grounding、code execution。[S008][S009] | dense/MoE、参数、layers、hidden size、attention、experts/router、tokenizer/vocab、训练与后训练配方。 | 高 |
| Grok 4.20 | 2M context、reasoning/non-reasoning API 变体、image token pricing。[S024] | dense/MoE、参数、layers、hidden size、attention、experts/router、tokenizer/vocab、训练与后训练配方。 | 高 |

## 开放权重但仍缺失的结构字段

| 模型 | 官方已公开结构 | 官方未披露字段 | 置信度 |
|---|---|---|---|
| Llama 4 Scout/Maverick | MoE、image-text-to-text、total/active naming、experts 数、context。[S012][S033][S034] | layers、hidden size、attention、positional encoding、tokenizer/vocab、vision encoder 细节、router/top-k、完整训练/后训练配方。 | 高 |
| Kimi K2.6 | 61 text layers、7168 hidden、384 routed experts、vision 27 layers、262144 context、vocab 163840。[S027] | active params、训练数据、优化器、完整后训练配方。 | 高 |
| DeepSeek-V3.2 | 61 layers、7168 hidden、256 routed experts、DSA/MLA 字段、163840 context、vocab 129280。[S028] | V3.2 active params、训练数据差异、完整后训练配方。 | 高 |
| Qwen3.5/Qwen3.6 | MoE、layers、hidden size、alternating attention、mRoPE、vision tower、context、vocab。[S030][S031] | 完整训练数据、优化器、完整后训练配方、reasoning 内部结构。 | 高 |
| MiniMax-M2.1 | 62 layers、3072 hidden、256 local experts、MTP、196608 context、vocab 200064。[S029] | 完整训练数据、优化器、训练基础设施、完整后训练配方。 | 高 |
| GLM-5.1 | 78 layers、6144 hidden、256 routed experts、DSA/index 字段、202752 context、vocab 154880。[S032] | active params、训练数据、优化器、完整后训练配方、reasoning 内部结构。 | 高 |
| Mistral Large 3 | sparse MoE、675B total、41B active、256k context、Apache 2.0 open-weight。[S025][S026][S035] | layers、hidden size、attention、positional encoding、tokenizer/vocab、专家数量、router/top-k、vision encoder 细节、完整训练/后训练配方。 | 高 |

## 产品系统能力与模型结构的分界

tool calling、computer use、search grounding、MCP、subagents、Claude Code、Codex、Gemini code execution、xAI reasoning/non-reasoning route 都是公开接口或产品系统能力。除非官方明确把它们写入模型 config 或技术报告中的内部层结构，本项目不把它们记为 base model architecture。[S003][S005][S008][S011][S022][S024]
