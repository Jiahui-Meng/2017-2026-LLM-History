# DeepSeek 家族发展史

## 家族主线

DeepSeek 的意义不只是“开源强模型”，而是把结构创新、推理训练和工具思维连续地做成主线。

| 时间 | 节点 | 提升 | 创新 |
|---|---|---|---|
| 2024 | DeepSeek-V3 | 高能力与低成本部署平衡更强 | DeepSeekMoE + MLA + MTP。[S015] |
| 2025 | DeepSeek-R1 | 推理能力与过程优化显著增强 | reasoning-first RL。[S057] |
| 2025-12 | DeepSeek-V3.2 | 工具环境中的推理能力更强 | thinking in tool-use + DSA/MLA 透明配置。[S014][S028] |

## 架构创新摘要

- `MoE`：用稀疏专家扩大总容量，但每个 token 只激活少量专家。[S015][S028]
- `MLA / DSA`：不是单纯换专家，而是在 attention / KV 路径上继续做效率优化。[S028]
- `MTP`：说明 DeepSeek 关注的不只是静态结构，还有推理阶段的效率与预测组织方式。[S015][S028]

## 不能被简化成一个词

- `MoE`：DeepSeek 用稀疏专家扩总容量、降激活成本，但这不是全部。[S015][S028]
- `MLA / DSA`：它还在 attention / KV 路径上追求更高的长上下文与推理效率。[S028]
- `reasoning RL`：R1 代表的是训练范式变化，而不是单纯结构变化。[S057]
- `tool-use thinking`：V3.2 说明它正在把推理过程和工具使用耦合起来。[S014]

## 当前最新节点

- `DeepSeek-V3.2` 是当前主线模型，`DeepSeek-R1` 是理解其 reasoning 路线的重要前置节点。[S014][S057]

## 仍未披露的信息

V3.2 的 active params、完整训练数据差异、完整后训练配方仍未在官方材料中完全披露。[S014][S028]
