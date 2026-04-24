# OpenAI 最新模型卡：GPT-5.5 / GPT-5.4

## 基本信息

- 最新公开模型：GPT-5.5 是 ChatGPT/Codex 侧最新发布模型；OpenAI 在发布页说明源时点未向 API 开放。[S001: release][S004: rollout]
- 可用相关结构接口：GPT-5.4 在 API/Codex 中公开 1M context、computer use、vision 与 reasoning effort。[S003: capability and availability]
- 开放程度：闭源；底层权重、参数规模和模型配置未公开。[S001: release][S003: overview]

## 模型结构（官方披露）

| field | GPT-5.5 / GPT-5.4 官方结构信息 |
|---|---|
| architecture family | GPT frontier reasoning/product family；官方未披露底层 transformer 结构。[S001: release][S003: overview] |
| dense/MoE | 官方未披露。[S001: release] |
| total params | 官方未披露。[S001: release][S002: system card] |
| active params | 官方未披露。[S001: release][S002: system card] |
| layers | 官方未披露。[S002: system card] |
| hidden size | 官方未披露。[S002: system card] |
| attention mechanism | 官方未披露。[S002: system card] |
| positional encoding | 官方未披露。[S002: system card] |
| experts/router | 官方未披露。[S002: system card] |
| context window | GPT-5.4 API/Codex 公开 1M context；GPT-5.5 的 API 上下文在源时点官方未披露。[S003: availability][S004: rollout] |
| tokenizer/vocab | 官方未披露。[S003: overview] |
| modal encoder | GPT-5.4 公开图像输入与 computer-use 视觉能力；底层视觉编码器官方未披露。[S003: computer use and vision] |
| output heads/modalities | 文本输出；computer use 是 API/产品动作输出接口，不等同于 base model 内部 head 结构。[S003: computer use] |
| reasoning/test-time structure | GPT-5.5 系统卡提到 Pro 场景的 parallel test-time compute；GPT-5.4 API 暴露 reasoning effort：none/low/medium/high/xhigh。[S002: system card][S003: reasoning effort] |
| deployment formats | ChatGPT、Codex；GPT-5.4 另有 API。GPT-5.5 源时点未向 API 开放。[S001: availability][S003: availability][S004: rollout] |
| officially undisclosed | 参数、层数、hidden size、attention、MoE/dense、tokenizer/vocab、训练数据规模、优化器、完整后训练配方。[S001: release][S002: system card] |

## 推理/产品系统结构

OpenAI 公开的是产品与 API 层结构：reasoning effort、computer use、Codex、ChatGPT model picker 与 test-time compute。它们应记录为推理/产品系统能力，不写成 base model 内部结构。[S002: system card][S003: computer use]

## LMArena 最新表现

见 `data/lmarena_latest.csv` 与 `docs/lmarena_results.md`。LMArena 是人类偏好评测，不提供模型内部结构证据。[S050: schema]

## 核心优势

强项来自推理时计算、工具/电脑使用接口、Codex 产品集成与多模态输入接口；这些优势目前无法从官方资料归因到参数规模或 MoE/dense 结构。[S002: system card][S003: computer use]

## 核心短板

结构透明度低：底层模型尺寸、层数、attention、tokenizer、训练和后训练配方均官方未披露。[S001: release][S002: system card]

## 与其他模型的关键区别

OpenAI 最新模型的公开信息更偏产品化推理接口，而 DeepSeek、Qwen、Kimi、MiniMax、GLM 等开放权重模型可从 config.json 读取具体层数、hidden size、专家数和上下文长度。[S027: config.json][S028: config.json][S030: config.json]

## 未公开信息

底层模型结构、参数规模、active params、层数、hidden size、attention、positional encoding、experts/router、tokenizer/vocab、完整训练数据、优化器和后训练配方均官方未披露。[S001: release][S002: system card]

## claim-to-source map

- C001 -> S001, S004
- C002 -> S003
- C015/C016/C018/C019 -> 用于与开放权重结构透明度对照
