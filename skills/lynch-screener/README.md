# lynch-screener — 彼得林奇十倍股猎手

[中文](#中文) | [English](#english)

---

## 中文

### 这个 Skill 是干什么的？

主动扫描美股市场，发现符合彼得林奇 (One Up on Wall Street) 风格的成长股候选——专注 **Fast Grower** 和 **Stalwart** 两类十倍股温床。**你不需要提供 ticker**——Skill 自己去网上搜无聊行业、被忽视的角落、内部人买入信号，按林奇六分类输出评分卡。

### 触发方式

以下说法都会触发此 Skill：

> "找十倍股" / "林奇风格扫一下" / "找成长股" / "找下一个十倍股" / "找无聊好公司" / "找被忽视的成长股" / "lynch screen" / "tenbagger"

### 林奇心法

1. **十倍股藏在无聊的角落**——名字越无聊、行业越讨人厌、卖方覆盖越少越好
2. **Buy what you know**——二分钟独白讲不清楚的故事不要碰
3. **Fast Grower 是十倍股的主要来源**——但必须便宜（PEG < 1）
4. **小盘 > 大盘**——大象不会跑
5. **避开热门股、避开"下一个 XXX"、避开多元恶化 (diworsification)**

### 林奇六分类

| 类别 | EPS 增速 | 十倍股可能性 |
|------|---------|------------|
| Slow Grower | <5% | 极低（直接剔除） |
| Stalwart | 10-12% | 低 |
| **Fast Grower** | **20-25%+** | **极高（主猎物）** |
| Cyclical | 看周期 | 中（周期底） |
| Turnaround | N/A | 中 |
| Asset Play | N/A | 低-中 |

### 输出内容

- 本轮狩猎心得（哪些角落最林奇友好、林奇会反向看哪里）
- 5-8 个候选评分卡（六分类标签、二分钟独白、PEG 标尺、林奇式叙事）
- 每个候选的"散户优势"建议（去哪里能先看到产品）

### 评分维度（满分 10）

| 维度 | 权重 |
|------|------|
| Fast Grower 含金量 | 2.5 分 |
| PEG 折扣度 | 2.0 分 |
| 业务无聊度 / 被忽视度 | 1.5 分 |
| 资产负债表健康度 | 1.5 分 |
| 内部人 + 回购信号 | 1.0 分 |
| 二分钟独白清晰度 | 1.5 分 |

**市值软扣分**：<$2B +0.5 / $2-10B 0 / $10-50B -0.5 / >$50B -1.0

### 与其他 Skill 的衔接

- 通常跟在 `lynch-screener` 之后用 `lynch-validator`：screener 发现候选 → validator 完整框架打分
- 跟 `asymmetric-screener` 互补：一个找成长股，一个找均值回归

### 安装

```
npx skills add outman337/skills --skill lynch-screener
```

或 URL 安装：

```
/install-skill https://github.com/outman337/skills/raw/main/skills/lynch-screener/SKILL.md
```

---

## English

### What does this Skill do?

Actively scans the US stock market for growth stock candidates matching Peter Lynch's style (*One Up on Wall Street*) — focused on **Fast Growers** and **Stalwarts**, the two main tenbagger breeding grounds. **No ticker needed** — the Skill searches boring industries, neglected corners, and insider buying signals on its own, then outputs scored cards organized by Lynch's six categories.

### Trigger phrases

> "find tenbaggers" / "lynch screen" / "find growth stocks" / "find boring winners" / "scan for next tenbagger"

### Lynch's Core Beliefs

1. **Tenbaggers hide in boring corners** — the more boring the name, the more disliked the industry, the fewer analysts covering it, the better
2. **Buy what you know** — if you can't explain it in a two-minute monologue, skip it
3. **Fast Growers are the main source of tenbaggers** — but they must be cheap (PEG < 1)
4. **Small caps > large caps** — elephants don't gallop
5. **Avoid hot stocks, avoid "the next XXX", avoid diworsification**

### Lynch's Six Categories

| Category | EPS Growth | Tenbagger Potential |
|----------|-----------|---------------------|
| Slow Grower | <5% | Very low (excluded) |
| Stalwart | 10-12% | Low |
| **Fast Grower** | **20-25%+** | **Very high (main hunt)** |
| Cyclical | Cyclical | Medium (at trough) |
| Turnaround | N/A | Medium |
| Asset Play | N/A | Low-medium |

### Output

- Hunting notes (which corners are most Lynch-friendly, where to look contrarian)
- 5-8 candidate scorecards (category tag, two-minute monologue, PEG ruler, Lynch-style narrative)
- Per-candidate "retail edge" suggestion (where you can see the product first)

### Scoring (out of 10)

| Dimension | Weight |
|-----------|--------|
| Fast Grower quality | 2.5 |
| PEG discount | 2.0 |
| Boringness / neglect | 1.5 |
| Balance sheet health | 1.5 |
| Insider buying + buybacks | 1.0 |
| Two-minute monologue clarity | 1.5 |

**Market cap soft penalty**: <$2B +0.5 / $2-10B 0 / $10-50B -0.5 / >$50B -1.0

### Works best with

- Use `lynch-validator` after this skill to score each candidate against the full framework
- Complements `asymmetric-screener`: one hunts growth, the other hunts mean reversion

### Installation

```
npx skills add outman337/skills --skill lynch-screener
```

Or via URL:

```
/install-skill https://github.com/outman337/skills/raw/main/skills/lynch-screener/SKILL.md
```
