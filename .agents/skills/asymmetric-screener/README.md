# asymmetric-screener — 不对称机会猎手

[中文](#中文) | [English](#english)

---

## 中文

### 这个 Skill 是干什么的？

主动扫描美股市场，发现被错误定价的高不对称性投资机会。**你不需要提供 ticker**——Skill 自己去网上搜索候选，按"三条腿的凳子"框架筛选，生成带可视化评分卡的候选报告。

### 触发方式

以下说法都会触发此 Skill：

> "找机会" / "扫一下" / "有什么新机会" / "搜一下潜在标的" / "最近有什么好票" / "帮我筛一下" / "scan opportunities" / "find asymmetric setups"

### 核心框架：三条腿的凳子

每个候选必须同时满足三个条件：

| 条件 | 标准 |
|------|------|
| **Leg 1 — 低估值地板** | P/S 低于同行中位数 40%+，提供下行保护 |
| **Leg 2 — 收入加速** | 最近 1-2 季度 YoY ≥25%，TTM ≥$20M |
| **Leg 3 — 热门赛道** | 近 3 个月板块资金净流入，市场关注度高 |

### 输出内容

- 市场环境速写（板块热度、资金流向）
- 5-8 个候选的可视化评分卡（P/S 同行对比条、均值回归数学、不对称评分）
- 优先 Deep Dive 建议

### 安装

```
npx skills add outman337/skills --skill asymmetric-screener
```

或 URL 安装：

```
/install-skill https://github.com/outman337/skills/raw/main/skills/asymmetric-screener/SKILL.md
```

---

## English

### What does this Skill do?

Actively scans the US stock market to discover high-asymmetry investment opportunities that are mispriced by the market. **No ticker needed** — the Skill searches for candidates on its own, filters them through the "three-legged stool" framework, and generates a visual scored report.

### Trigger phrases

> "找机会" / "find asymmetric setups" / "scan opportunities" / "what's mispriced right now" / "find me some good tickers"

### Core Framework: The Three-Legged Stool

Every candidate must pass all three legs simultaneously:

| Leg | Standard |
|-----|----------|
| **Leg 1 — Valuation Floor** | P/S at least 40% below peer median — provides downside protection |
| **Leg 2 — Revenue Acceleration** | YoY growth ≥25% in last 1-2 quarters, TTM revenue ≥$20M |
| **Leg 3 — Hot Sector** | Net capital inflows into sector over last 3 months |

### Output

- Market environment snapshot (sector heat, fund flows)
- 5-8 candidate visual cards (P/S peer comparison bars, mean-reversion math, asymmetry score)
- Priority Deep Dive recommendations

### Installation

```
npx skills add outman337/skills --skill asymmetric-screener
```

Or via URL:

```
/install-skill https://github.com/outman337/skills/raw/main/skills/asymmetric-screener/SKILL.md
```
