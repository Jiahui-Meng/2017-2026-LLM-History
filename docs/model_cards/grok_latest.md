# xAI 最新模型卡：Grok 4.20

## 基本信息

- 最新公开模型：xAI API 表列出 Grok 4.20 reasoning 与 non-reasoning 变体。[S024: API table]
- 开放程度：闭源；通过 xAI API 提供。[S024: API table]

## 模型结构（官方披露）

| field | Grok 4.20 官方结构信息 |
|---|---|
| architecture family | Grok API model；底层 transformer/MoE 结构官方未披露。[S024: API table] |
| dense/MoE | 官方未披露。[S024: API table] |
| total params | 官方未披露。[S024: API table] |
| active params | 官方未披露。[S024: API table] |
| layers | 官方未披露。[S024: API table] |
| hidden size | 官方未披露。[S024: API table] |
| attention mechanism | 官方未披露。[S024: API table] |
| positional encoding | 官方未披露。[S024: API table] |
| experts/router | 官方未披露。[S024: API table] |
| context window | API 表列出 2M context。[S024: API table] |
| tokenizer/vocab | 官方未披露。[S024: API table] |
| modal encoder | API pricing 中出现 image token 项；底层视觉编码器官方未披露。[S024: API table] |
| output heads/modalities | 文本输出；其他产品能力不作为内部 head 结构记录。[S024: API table] |
| reasoning/test-time structure | 公开 reasoning 与 non-reasoning 变体；内部 reasoning 结构官方未披露。[S024: API table] |
| deployment formats | xAI API。[S024: API table] |
| officially undisclosed | 参数、层数、hidden size、attention、positional encoding、experts/router、tokenizer/vocab、训练和后训练配方。[S024: API table] |

## 推理/产品系统结构

Grok 4.20 的公开差异主要是 reasoning/non-reasoning 变体和 2M context API 规格，不能据此推导内部网络结构。[S024: API table]

## LMArena 最新表现

见 `data/lmarena_latest.csv`；LMArena 不提供 Grok 4.20 的内部结构字段。[S050: schema]

## 核心优势

官方公开的显著能力是超长 2M context 与 reasoning/non-reasoning API 变体。[S024: API table]

## 核心短板

除接口规格外，底层结构几乎全部官方未披露。[S024: API table]

## 与其他模型的关键区别

Grok 以 API 长上下文规格突出；开放权重模型则可在官方 config 或 model card 中审计专家、层数、hidden size 等字段。[S027: config.json][S032: config.json]

## 未公开信息

底层模型结构、参数、active params、层数、hidden size、attention、positional encoding、experts/router、tokenizer/vocab、训练与后训练配方均官方未披露。[S024: API table]

## claim-to-source map

- C012 -> S024
