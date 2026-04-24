# 架构比较

| 模型 | Dense/MoE | 多模态 | attention/context 关键点 | 未公开 |
|---|---|---|---|---|
| GPT-5.5 | 官方未披露 | 产品支持复杂工具工作；底层结构未披露 | GPT-5.5 官方强调工具、规划、检查工作；参数/attention 未披露。[S001: Intro] | 参数、专家、attention、tokenizer、训练规模 |
| Claude Opus 4.7 | 官方未披露；官方称 hybrid reasoning | 图像输入增强 | 1M context，higher-res image long edge 2576 px；effort 新增 xhigh。[S005: Improved multimodal][S006: product page] | 参数、专家、attention、tokenizer |
| Gemini 3.1/3 | 官方未披露 | 文本、图像、视频、音频、PDF 输入 | Gemini 3 Pro Preview 1M/64k，支持 thinking/search grounding/function calling/code execution。[S009: Model table] | 参数、专家、tokenizer、训练数据 |
| Muse Spark | 官方未披露 | 文本+图像产品能力 | Meta 官方强调 multimodal perception 与并行 subagents 产品体验。[S011: Ask Meta AI] | 参数、context、attention、训练规模 |
| Llama 4 Maverick | MoE | 文本+图像 | 400B total/17B active/128 experts/1M context；Scout 109B/17B/16 experts/10M context。[S013: Llama specs] | 完整训练数据配比 |
| DeepSeek-V3.2 | MoE | 文本 | V3 lineage: MLA、DeepSeekMoE、671B total/37B active；V3.2-Exp 引入 DSA。[S015: Model Summary][S016: DSA] | V3.2 完整参数若与 V3 lineage 差异需以 tech report 更新 |
| Kimi K2.6 | MoE lineage | native multimodal | K2.6 model list: 256k context、visual+text、thinking/non-thinking；K2 quickstart 披露 1T/32B active lineage。[S017: Model List][S018: Overview] | K2.6 完整技术报告细节 |
| Qwen3.5/3.6 | MoE/hybrid | family supports multimodal | GitHub release notes披露 Qwen3.5-397B-A17B、Qwen3.6-35B-A3B 等模型。[S019: News] | 逐模型完整 attention/数据配比需 model card 补齐 |
| MiniMax-M2.1 | MoE | 文本 | 约 230B total/~10B active，面向 coding/tool use/long-horizon planning。[S020: Overview][S021: Model Overview] | 完整专家数、训练数据规模 |
| GLM-5.1 | 官方 docs 未披露 | 文本 | 200K context、128K output、thinking/function/MCP/context cache。[S022: Overview] | 参数、专家、attention、训练数据 |
| Grok 4.20 | 官方未披露 | API pricing includes text/image tokens | 2M context，reasoning/non-reasoning variants。[S024: API table] | 参数、专家、attention、训练数据 |
| Mistral Large 3 | Sparse MoE | 文本+图像 | 675B total/41B active，256k context，Apache 2.0。[S025: Mistral Large 3][S026: docs] | 训练数据配比 |

