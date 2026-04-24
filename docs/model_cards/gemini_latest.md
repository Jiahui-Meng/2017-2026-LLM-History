# Google 最新模型卡：Gemini 3.1 Pro / Gemini 3 Pro

## 基本信息

- 最新公开模型：Gemini 3.1 Pro 与 Gemini 3 Pro Preview 相关官方资料覆盖 API、Vertex AI 和 Gemini 产品渠道。[S008: models][S009: developer guide][S010: announcement]
- 开放程度：闭源；Google 公开接口能力，不公开权重或底层 config。[S008: models]

## 模型结构（官方披露）

| field | Gemini 官方结构信息 |
|---|---|
| architecture family | Gemini multimodal reasoning family；底层 transformer/MoE 结构官方未披露。[S008: models][S010: announcement] |
| dense/MoE | 官方未披露。[S008: models] |
| total params | 官方未披露。[S008: models][S010: announcement] |
| active params | 官方未披露。[S008: models] |
| layers | 官方未披露。[S008: models] |
| hidden size | 官方未披露。[S008: models] |
| attention mechanism | 官方未披露。[S008: models] |
| positional encoding | 官方未披露。[S008: models] |
| experts/router | 官方未披露。[S008: models] |
| context window | Gemini 3 Pro Preview 模型表列出 1,048,576 input tokens 和 65,536 output tokens。[S008: model table][S009: guide] |
| tokenizer/vocab | 官方未披露。[S008: models] |
| modal encoder | 公开文本、图像、视频、音频、PDF 输入能力；底层各模态编码器官方未披露。[S008: model table][S009: guide] |
| output heads/modalities | 文本输出；函数调用、search grounding 和 code execution 是 API 工具结构。[S008: tools][S009: guide] |
| reasoning/test-time structure | 官方公开 thinking 支持；具体内部 reasoning head/latent structure 官方未披露。[S008: model table][S009: thinking] |
| deployment formats | Gemini API、Vertex AI、Gemini app、NotebookLM 等产品/平台渠道。[S008: models][S010: announcement] |
| officially undisclosed | 参数、层数、hidden size、attention、MoE/dense、tokenizer/vocab、训练数据规模、优化器、后训练配方。[S008: models] |

## 推理/产品系统结构

Google 公开的是 thinking、function calling、search grounding、code execution、long-context 输入等接口结构；这些不等同于内部模型层结构。[S008: tools][S009: guide]

## LMArena 最新表现

见 `data/lmarena_latest.csv`。榜单可反映人类偏好，不构成 Gemini 内部结构证据。[S050: schema]

## 核心优势

长上下文、多模态输入、搜索 grounding、函数调用和代码执行是官方强调的系统能力。[S008: model table][S009: guide]

## 核心短板

结构透明度低，无法与开放权重 MoE 模型在层数、专家数、hidden size 层面对齐比较。[S008: models]

## 与其他模型的关键区别

Gemini 更像完整多模态产品栈；Qwen3.5/Kimi K2.6 则在官方 config 中直接披露 vision tower 层数、hidden size、patch size 等字段。[S027: config.json][S030: config.json]

## 未公开信息

底层模型结构、参数、active params、层数、hidden size、attention、positional encoding、experts/router、tokenizer/vocab、训练与后训练配方均官方未披露。[S008: models]

## claim-to-source map

- C004 -> S008, S009
- C014 -> S050
