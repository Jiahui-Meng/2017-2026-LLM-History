# Anthropic 最新模型卡：Claude Opus 4.7

## 基本信息

- 最新公开模型：Claude Opus 4.7，官方称其面向高强度推理、编码和长任务。[S005: release]
- 开放程度：闭源；通过 Claude 产品、API 和云平台渠道提供。[S005: availability][S006: product]

## 模型结构（官方披露）

| field | Claude Opus 4.7 官方结构信息 |
|---|---|
| architecture family | Anthropic hybrid reasoning model；底层 transformer 结构官方未披露。[S005: release] |
| dense/MoE | 官方未披露。[S005: release] |
| total params | 官方未披露。[S005: release][S006: product] |
| active params | 官方未披露。[S005: release][S006: product] |
| layers | 官方未披露。[S005: release] |
| hidden size | 官方未披露。[S005: release] |
| attention mechanism | 官方未披露。[S005: release] |
| positional encoding | 官方未披露。[S005: release] |
| experts/router | 官方未披露。[S005: release] |
| context window | 官方产品资料列出 1M context。[S006: product] |
| tokenizer/vocab | 官方未披露。[S005: release] |
| modal encoder | 支持更高分辨率图像输入；底层视觉编码器官方未披露。[S005: release] |
| output heads/modalities | 文本输出；工具/代码动作通过产品或 API 系统实现。[S005: release] |
| reasoning/test-time structure | 公开 xhigh effort 与 beta task budgets，属于推理时预算/产品控制结构。[S005: release] |
| deployment formats | Claude 产品、Anthropic API、Amazon Bedrock、Google Vertex AI、Microsoft Foundry。[S005: availability] |
| officially undisclosed | 参数、层数、hidden size、attention、tokenizer、MoE/dense、训练数据规模和完整后训练配方。[S005: release][S006: product] |

## 推理/产品系统结构

Claude Code、xhigh effort、task budgets、computer-use/工具使用属于推理与产品系统层；官方资料没有把这些字段映射到底层模型内部架构。[S005: release]

## LMArena 最新表现

见 `data/lmarena_latest.csv`。LMArena 可用于偏好排名观察，但不能反推出 Claude 的参数或结构。[S050: schema]

## 核心优势

长任务、编码、agentic workflow、图像输入和可控推理预算是官方重点。[S005: release][S006: product]

## 核心短板

内部结构不可审计；与开放权重 MoE 模型相比，缺少官方 config 级字段。[S005: release]

## 与其他模型的关键区别

Claude 公开了推理预算和任务预算接口，但没有公开专家数、层数、hidden size 等；MiniMax、Qwen、GLM 等则公开了 config 级结构字段。[S029: config.json][S030: config.json][S032: config.json]

## 未公开信息

底层模型结构、参数、active params、层数、hidden size、attention、positional encoding、experts/router、tokenizer/vocab、完整训练与后训练配方均官方未披露。[S005: release]

## claim-to-source map

- C003 -> S005, S006
- C014 -> S050
