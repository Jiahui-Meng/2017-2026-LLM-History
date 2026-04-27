# Gemini 家族发展史

## 家族主线

Google 的路线不是单纯复制 GPT，而是把 Transformer、T5/FLAN 的研究传统延续到原生多模态、长上下文和工具 grounding。

| 时间 | 节点 | 提升 | 创新 |
|---|---|---|---|
| 2017-2021 | Transformer / T5 / FLAN | 奠定统一架构、统一接口和 instruction tuning 基础 | self-attention、text-to-text、instruction tuning。[S036][S039][S042] |
| 2024 | Gemini 1.5 | 长上下文与原生多模态显著推进 | 1M 级 context + multimodal family。[S048] |
| 2025-2026 | Gemini 3 / 3.1 Pro | 工具、thinking、grounding、代码执行进一步融合 | multimodal reasoning + search grounding + code execution。[S008][S009][S010] |

## 架构创新摘要

- Google 的最大结构贡献首先是 Transformer 本身，然后是 T5/FLAN 这类统一接口与后训练方法论。[S036][S039][S042]
- 到 Gemini 阶段，官方更强调长上下文、多模态和工具能力，但底层 dense/MoE 与 attention 路径并未公开。[S008][S009][S048]

## 每代的核心创新

- `Transformer/T5/FLAN`：Google 在 LLM 主线上的最大贡献之一，是把底层架构、统一接口和 instruction tuning 都提前做成方法论。[S036][S039][S042]
- `Gemini 1.5`：让超长上下文成为主流前沿能力。[S048]
- `Gemini 3`：把多模态、Thinking、grounding、工具调用做成更统一的开发者/产品接口。[S008][S009]

## 当前最新节点

- `Gemini 3.1 Pro / Gemini 3 Pro Preview` 是当前可公开核验的主线节点，官方公开 1,048,576 input tokens、65,536 output tokens，并强调多模态输入、search grounding、code execution 与 Thinking。[S008][S009][S010]

## 仍未披露的信息

Gemini 家族的参数、专家路由、层数、完整训练与后训练配方官方未披露。[S008][S009]
