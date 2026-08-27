# Prior Art Research: qiaomu-syc

**Date:** 2026-08-27
**Queries:** "writing style skill", "chinese prose style", "personal writing style", "iceberg narrative"

## Candidates Found

| Skill | Installs | Relevance |
|---|---|---|
| `sugarforever/01coder-agent-skills@personal-chinese-writing-style` | 350 | 中文个人写作风格，但无具体文学技法规则 |
| `different-ai/agent-bank@writing-style` | 370 | 通用写作风格，非中文散文专项 |
| `haowjy/creative-writing-skills@style-analysis` | 289 | 风格分析，非风格模拟 |
| `haowjy/creative-writing-skills@cw-prose-writing` | 259 | 散文写作，无数字锚点/冰山叙事机制 |
| `dongbeixiaohuo/writing-agent@style-modeler` | 118 | 风格建模，通用 |

## Synthesis

**Keep:** 触发词设计参考 `personal-chinese-writing-style` 的中文触发模式。

**Adapt:** 无现有 skill 实现"数字锚点密集 + 冰山叙事 + 哲学收束句"三位一体的中文散文风格模拟。

**Reject:** 所有候选均为通用写作风格，缺乏具体文学技法的量化规则（如"每500字3个数字锚点"、"禁止感叹号"等）。

**Invent:** 基于《我的女友景甜》原文深度分析，提炼8条量化风格规则，建立禁止清单，设计冰山情感载体映射表。

## Missing Evidence

- 未能获取 `sugarforever/01coder-agent-skills` 的完整 SKILL.md 内容
- 未进行人工对比测试

## Conclusion

无现有 skill 覆盖 SYC 风格的核心机制，需要原创设计。
