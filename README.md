# qiaomu-syc

> AI 写情绪，最容易犯的错是把情绪写出来。
>
> **qiaomu-syc 用短句、精确数字、行为细节和留白，让读者自己感受到它。**

[中文](#中文) · [English](#english)

[![GitHub stars](https://img.shields.io/github/stars/joeseesun/qiaomu-syc?style=flat-square)](https://github.com/joeseesun/qiaomu-syc/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/joeseesun/qiaomu-syc?style=flat-square)](https://github.com/joeseesun/qiaomu-syc/forks)
[![GitHub issues](https://img.shields.io/github/issues/joeseesun/qiaomu-syc?style=flat-square)](https://github.com/joeseesun/qiaomu-syc/issues)
[![Last commit](https://img.shields.io/github/last-commit/joeseesun/qiaomu-syc?style=flat-square)](https://github.com/joeseesun/qiaomu-syc/commits/main)
[![License: MIT](https://img.shields.io/badge/license-MIT-yellow?style=flat-square)](LICENSE)

<a name="中文"></a>
## 中文

`qiaomu-syc` 是一个中文写作 Agent Skill。它把孙宇晨公开长文中呈现出的克制散文技法，拆解成一套可复用的写作流程：

- 情绪高峰反而用最短的句子
- 用精确数字代替抽象感受
- 把情绪藏进行为、物件和身体反应
- 用并置制造落差，不替读者下结论
- 每一节用一句克制的判断收住

它适合情感叙事、第一人称回忆、人物故事和已有文本改写。它不复制原文，也不冒充原作者。

## 先看效果

**你说：**

```text
用 SYC 风格写：一个人在机场等一个不会来的人
```

**Agent 会这样写：**

```text
航班落地的时间是下午两点四十七分。
我提前一个小时到了。

两点四十七分，出口的门开了。
三点零五分，门关上了。

我数了一下出来的人。一百三十二个。
她不在里面。

后来我买了一杯咖啡。
三十八块。

我喝了一口，放在旁边的台子上，没有再喝。
```

没有“失落”“难过”或“遗憾”。但东西还在。

## 一行安装

```bash
npx skills add joeseesun/qiaomu-syc
```

安装后重启你的 Agent，然后直接用自然语言触发。

## 你可以直接这样说

```text
用 SYC 风格写：一个人在空房间里等电话
```

```text
孙宇晨文风，写一段关于钱和爱情的散文
```

```text
把下面这段话改成冰山叙事：不要直接写情绪，多用数字和动作
```

```text
qiaomu-syc 改写这段文字，去掉感叹号、排比句和 AI 味
```

## 它具体改变什么

| 普通 AI 写法 | qiaomu-syc 的处理 |
|---|---|
| “我感到非常失落” | 写他又数了一遍航班出口的人数 |
| “我们相隔很远” | 写两个地点的温度和九千五百公里 |
| “那一刻我意识到……” | 删除解释，只留下动作和物件 |
| 用形容词制造情绪 | 用两个数字并置制造落差 |
| 结尾总结人生意义 | 用一句不超过十五字的判断收住 |

## 核心机制

| 机制 | 怎么写 | 刻意避免 |
|---|---|---|
| 短句节奏 | 情绪越重，句子越短 | 长句解释感受 |
| 数字锚点 | 时间、金额、重量、距离都写具体 | “大约”“差不多” |
| 冰山叙事 | 用动作、物件、身体反应承载情感 | 直接写爱、痛、失落 |
| 对比结构 | 两个事实并置，写完就停 | 加一句替读者总结 |
| 哲学收束 | 每节末尾用短判断留余韵 | 感叹号和煽情金句 |

完整规则见 [SKILL.md](SKILL.md)，更细的节奏和结构分析见 [references/style-dna.md](references/style-dna.md)。

## 安装前确认

- [ ] 已安装 [Node.js](https://nodejs.org/)；运行 `node --version` 能看到版本号
- [ ] 终端中可使用 `npx`；运行 `npx --version` 能看到版本号
- [ ] 使用支持 Agent Skills / `SKILL.md` 的 AI Agent
- [ ] 安装完成后会重启或重新加载 Agent，让新 Skill 生效

### 发现但不安装

先检查仓库里能识别到哪些 Skill：

```bash
npx skills add joeseesun/qiaomu-syc --list
```

预期结果中应出现：

```text
qiaomu-syc
```

### 安装指定 Skill

```bash
npx skills add joeseesun/qiaomu-syc --skill qiaomu-syc
```

## 适合与不适合

**适合：**

- 第一人称情感叙事
- 人物回忆和关系故事
- 克制风格的公众号文章
- 把直白、煽情或 AI 味明显的文字重新收紧
- 需要数字、动作、物件承担叙事的短篇散文

**不适合：**

- 新闻、技术文档或学术论文
- 需要明确转化目标的营销文案
- 要求事实准确但没有提供可靠素材的真实人物叙事
- 冒充孙宇晨本人发布，或让读者误以为内容出自本人

## 目录结构

```text
qiaomu-syc/
├── SKILL.md                 # Agent 执行规则
├── agents/interface.yaml    # Agent 界面与兼容信息
├── evals/trigger_cases.json # 触发与不触发测试样例
├── references/style-dna.md  # 风格结构分析
├── reports/                 # 设计研究与评测证据
├── manifest.json            # 版本与发布元数据
└── LICENSE
```

## 常见问题

| 问题 | 处理方法 |
|---|---|
| 安装时提示 `No valid skills found` | 更新到最新 Node.js 与 `skills` CLI，再运行 `npx skills add joeseesun/qiaomu-syc --list` |
| 安装成功但没有触发 | 重启 Agent，并明确说 `SYC 风格`、`孙宇晨文风`、`冰山叙事` 或 `qiaomu-syc` |
| 输出仍然很像普通 AI | 加一句：`不要感叹号，不要排比，不要直接写情绪，用动作和数字替代` |
| 数字太多，像流水账 | 要求 `只保留 3 个最有反差的数字锚点，其余改成动作细节` |
| 风格太像原文 | 要求保留叙事机制，但更换人物关系、场景、物件和数字，不复用原句 |

## 来源、致谢与边界

这个 Skill 的风格研究起点是孙宇晨（Justin Sun）于 2026 年 8 月 27 日公开发布的长文《我的女友景甜》，并参考了海明威冰山理论、新新闻主义和罗兰·巴特的零度写作。

本项目是独立的写作技法研究与 Agent Skill，和孙宇晨本人及其团队没有隶属、授权或代言关系。请把它用于学习、创作和文本实验；不要复制原文，不要冒充真实人物，也不要用生成内容制造关于真实人物的虚假陈述。

---

<!-- qiaomu-profile:start -->
## 关于向阳乔木

向阳乔木（乔向阳 / Joe）是一位实践型 AI 产品与内容创作者，长期把前沿 AI 变化转译成可复用的工作流、产品判断、AI 编程实践、AI 搜索实践和 GEO/AI 营销方法。

- 个人网站: https://qiaomu.ai
- 博客: https://blog.qiaomu.ai
- X: https://x.com/vista8
- GitHub: https://github.com/joeseesun/
- 微信公众号: 向阳乔木推荐看

### 支持与关注

| 打赏支持 | 微信公众号 |
|---|---|
| <img src="assets/qiaomu-profile/qiaomu_reward_qr.png" alt="向阳乔木打赏二维码" width="180" /> | <img src="assets/qiaomu-profile/qiaomu_wechat_public_account_qr.jpg" alt="向阳乔木推荐看公众号二维码" width="180" /> |
| 感谢支持乔木持续分享 AI 实践 | 扫码关注「向阳乔木推荐看」 |

<!-- qiaomu-profile:end -->

---

<a name="english"></a>
## English

AI often overexplains emotion. **qiaomu-syc** does the opposite: it uses short sentences, precise numbers, physical actions, objects, contrast, and silence to make the reader feel what the narrator never says.

It is a Chinese writing Agent Skill derived from a structural study of the restrained prose techniques found in Justin Sun's public essay *My Girlfriend Jing Tian*.

### Install

```bash
npx skills add joeseesun/qiaomu-syc
```

Discover the Skill before installing:

```bash
npx skills add joeseesun/qiaomu-syc --list
```

### Try it

```text
Use qiaomu-syc to write about someone waiting at an airport for a person who will not arrive.
```

```text
Rewrite this passage as an iceberg narrative. Do not name the emotion; carry it through numbers, actions, and objects.
```

### What it controls

- short sentences at emotional peaks
- precise numeric anchors instead of abstract feelings
- emotions hidden in behavior, objects, and physical reactions
- contrast through juxtaposed facts, without commentary
- restrained closing lines that leave room for the reader

### Scope and disclaimer

This is an independent writing-technique study and Agent Skill. It is not affiliated with, authorized by, or endorsed by Justin Sun or his team. Do not use it to impersonate a real person, reproduce the source essay, or fabricate claims about real people.

## License

[MIT](LICENSE) © 向阳乔木
