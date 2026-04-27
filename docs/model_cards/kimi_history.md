# Kimi 家族发展史

## 家族主线

Kimi 的路线起点是“长上下文可用性”，后期逐渐演进到“多模态 + thinking + agent”的综合工作模型。

| 时间 | 节点 | 提升 | 创新 |
|---|---|---|---|
| 2024 | Kimi 长上下文阶段 | 在中文产品中把长文本读取与处理做成强标签 | 以长上下文为中心的产品定位。[S061] |
| 2025 | Kimi K2 | 从长文本助手升级为 agent 任务模型 | 原生多模态与工具导向工作流。[S018] |
| 2026 | Kimi K2.6 | 推理模式、上下文、模态与结构继续强化 | thinking/non-thinking、256k context、MoE、多模态配置。[S017][S027] |

## 架构创新摘要

- `Kimi K2.6` 不是只有长上下文，它还公开了 MoE、vision tower、patch 结构和 DeepSeekV3-style text config 字段。[S027]
- 和 DeepSeek 相比，Kimi 把多模态结构公开得更完整；和 Qwen 相比，它更强调 agent 任务入口和 thinking/non-thinking 产品化。[S017][S027]

## 每代的核心创新

- `早期 Kimi`：让长上下文成为产品入口，而不是论文能力展示。[S061]
- `K2`：开始明显朝 agent 工作流靠拢，而非只做长文阅读助手。[S018]
- `K2.6`：把多模态、MoE、thinking/non-thinking、长上下文整合成前沿 open-weight/API 家族。[S017][S027]

## 当前最新节点

- `Kimi K2.6` 是当前公开主线推荐型号之一，官方强调 native multimodal、256k context、thinking/non-thinking modes。[S017]

## 仍未披露的信息

Kimi K2.6 的 active params、训练 token、完整后训练配方与 agent 数据细节未完整公开。[S017][S027]
