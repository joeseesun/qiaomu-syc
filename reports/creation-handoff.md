# Creation Handoff: qiaomu-syc

**Date:** 2026-08-27
**Version:** 1.0.0
**Mode:** Production
**Author:** 向阳乔木

## Reference Skills Studied

| Skill | Lesson |
|---|---|
| `sugarforever/01coder-agent-skills@personal-chinese-writing-style` | 中文触发词设计模式 |
| `haowjy/creative-writing-skills@cw-prose-writing` | 散文写作的输出规范结构 |
| `qiaomu-kazike-writer` | 乔木风格 skill 的整体架构参考 |

## Deliberate Rejections

- **不使用通用"文学风格"框架**：SYC风格有极强的量化特征（数字密度、句长分布），需要具体规则而非模糊描述
- **不模拟作者人格**：skill 模拟文风技法，不模拟孙宇晨的价值观或个人立场
- **不设置"情感强度"参数**：SYC风格的克制是绝对的，不应有"更感性"的变体

## Original Contributions

1. **8条量化风格规则**：从原文统计分析提炼，每条有原文示例和量化标准
2. **禁止清单**：12条明确禁止的AI味表达，可直接用于输出检查
3. **冰山情感载体映射表**：情感→物件/行为的具体映射，可复用
4. **Style DNA 参考文档**：句长分布、数字密度、段落结构的量化统计

## Design Advantages

- **hypothesis**: 量化规则比模糊描述更能稳定复现特定文风
- **validated advantage**: 禁止清单可有效过滤AI味输出（基于原文分析）
- **design advantage**: 冰山情感载体映射表提供可操作的写作路径

## Highlights

- 全文零感叹号规则是最强的去AI味信号
- "数字用中文写"（三点五，不是3.5）是细节但关键
- 收束句≤15字的硬性限制防止过度解释
