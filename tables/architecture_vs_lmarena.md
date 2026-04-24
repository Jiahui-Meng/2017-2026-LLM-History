# Architecture vs LMArena

| 观察 | 解释 | 证据 |
|---|---|---|
| MoE 开放模型进入高分区 | MoE 提供高总容量低激活成本，但榜单高分还依赖后训练和产品系统。 | [S051: rows][S052: webdev latest] |
| 闭源模型高分不可归因到参数 | 参数/专家官方未披露，不能建立参数-分数关系。 | [S001: Intro][S005: Intro][S009: Model table][S024: API table] |
| WebDev 与工具/后训练强相关 | GLM/MiniMax 的公开材料都强调 agentic coding、工具调用和 long-horizon planning。 | [S020: Overview][S023: Agentic Coding] |
| 多模态榜单不是单一架构榜 | vision/text-to-image 受视觉 encoder、图像模型、审美后训练和产品安全策略影响。 | [S053: text_to_image latest][S054: vision latest] |

