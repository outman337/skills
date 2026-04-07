# lynch-validator — 彼得林奇验证器

[中文](#中文) | [English](#english)

---

## 中文

### 这个 Skill 是干什么的？

输入一个 ticker，按彼得林奇 (One Up on Wall Street) 的完整框架逐条验证：六分类归属、二分钟独白、十三条买入信号、十一条排除信号、PEG 估值、林奇式财务健康度，给出 **PASS / WATCH / FAIL** 判定和综合打分。不做完整投研报告——只做林奇框架验证。

### 触发方式

> "林奇验证 XXXX" / "XXXX 林奇风格" / "用林奇方法看 XXXX" / "lynch check XXXX" / "XXXX 是不是十倍股" / "XXXX 林奇喜欢吗" / "XXXX PEG 怎么样"

### 验证流程

**Step 1 — 六分类归属**：根据 EPS 增速归到 Slow Grower / Stalwart / Fast Grower / Cyclical / Turnaround / Asset Play

**Step 2 — 二分钟独白测试**：能否用小学生水平的语言在 2 分钟内讲清业务、增长引擎、风险

**Step 3 — 十三条买入信号**：无聊业务 / 机构低持仓 / 内部人买入 / 回购 / 重复消费 / niche / roll-out 等

**Step 4 — 十一条排除信号**：热门股 / "下一个 XXX" / 多元恶化 / 大客户依赖 / 高 P/E 低增速等

**Step 5 — PEG 估值**：林奇核心指标。原版 PEG + 股息调整 PEG，对照林奇标尺判定便宜/公允/贵

**Step 6 — 林奇式财务健康度**：净现金、长期债务/股本 <25%、库存增速 vs 销售增速、留存收益增速

**Step 7 — Fast Grower 专属**：roll-out 渗透率、SSS 持续性、5 年十倍股回报数学

### 判定规则

| 结果 | 条件 |
|------|------|
| **PASS ✓** | 得分 ≥7.5 + PEG <1 + 二分钟独白 PASS |
| **WATCH ~** | 得分 5.0-7.4，或 PEG 在 1-1.5 之间 |
| **FAIL ✗** | 得分 <5.0 / 二分钟独白 FAIL / 红灯 ≥3 条 / Slow Grower |

### 评分维度（满分 10）

| 维度 | 权重 |
|------|------|
| 类别质量 (Fast Grower 满分) | 2.0 分 |
| PEG 折扣度 | 2.0 分 |
| 二分钟独白清晰度 | 1.5 分 |
| 十三信号命中数 | 1.5 分 |
| 财务健康度 | 1.5 分 |
| 内部人 + 回购 | 0.8 分 |
| 被忽视度 | 0.7 分 |

**惩罚项**：每条红灯 -0.5；市值软扣分（<$2B +0.5 / $2-10B 0 / $10-50B -0.5 / >$50B -1.0）

### 输出内容

- 六分类归属 + 归类理由
- 二分钟独白（强制白话）
- 十三信号 + 十一红灯逐条 ✓/✗
- PEG ASCII 标尺定位
- 林奇式财务健康度快查
- Fast Grower 十倍股引擎检查（仅当归类为 Fast Grower）
- 综合打分表
- 最终判定卡片
- 林奇会追问的 5 个问题

### 与其他 Skill 的衔接

- 通常跟在 `lynch-screener` 之后使用：screener 发现候选 → validator 完整框架打分
- 跟 `asymmetric-validator` 互补：一个用林奇成长股框架，一个用不对称估值框架，可交叉验证

### 安装

```
npx skills add outman337/skills --skill lynch-validator
```

或 URL 安装：

```
/install-skill https://github.com/outman337/skills/raw/main/skills/lynch-validator/SKILL.md
```

---

## English

### What does this Skill do?

Input a ticker and the skill runs the full Peter Lynch framework: six-category assignment, two-minute monologue test, thirteen buy signals, eleven red flags, PEG valuation, Lynch-style balance sheet check. Returns **PASS / WATCH / FAIL** verdict with a composite score. No full research report — Lynch framework validation only.

### Trigger phrases

> "lynch check XXXX" / "is XXXX a tenbagger" / "would Lynch like XXXX" / "score XXXX using Lynch's framework"

### Validation Steps

**Step 1 — Six-category assignment**: Classify by EPS growth into Slow Grower / Stalwart / Fast Grower / Cyclical / Turnaround / Asset Play

**Step 2 — Two-minute monologue test**: Can you explain the business, growth engine, and risks in 2 minutes using middle-school language?

**Step 3 — Thirteen buy signals**: Boring name / low institutional ownership / insider buying / buybacks / repeat purchase / niche / roll-out, etc.

**Step 4 — Eleven red flags**: Hot stocks / "the next XXX" / diworsification / customer concentration / high P/E with low growth, etc.

**Step 5 — PEG valuation**: Lynch's signature metric. Both standard PEG and dividend-adjusted PEG, mapped against the Lynch ruler

**Step 6 — Lynch-style balance sheet**: Net cash, LT debt/equity <25%, inventory vs sales growth, retained earnings growth

**Step 7 — Fast Grower deep dive**: Roll-out penetration, SSS sustainability, 5-year tenbagger math

### Verdict Rules

| Result | Condition |
|--------|-----------|
| **PASS ✓** | Score ≥7.5 + PEG <1 + monologue PASS |
| **WATCH ~** | Score 5.0-7.4, or PEG between 1-1.5 |
| **FAIL ✗** | Score <5.0 / monologue FAIL / ≥3 red flags / Slow Grower |

### Scoring (out of 10)

| Dimension | Weight |
|-----------|--------|
| Category quality (Fast Grower = full marks) | 2.0 |
| PEG discount | 2.0 |
| Two-minute monologue clarity | 1.5 |
| Buy signal hits (out of 13) | 1.5 |
| Balance sheet health | 1.5 |
| Insider + buybacks | 0.8 |
| Neglect score | 0.7 |

**Penalties**: -0.5 per red flag; market cap soft penalty (<$2B +0.5 / $2-10B 0 / $10-50B -0.5 / >$50B -1.0)

### Output

- Six-category assignment + reasoning
- Two-minute monologue (forced plain language)
- Thirteen signals + eleven red flags checklist
- PEG ASCII ruler
- Lynch-style balance sheet quick check
- Fast Grower tenbagger engine check (Fast Growers only)
- Composite scoring table
- Final verdict card
- Five questions Lynch would ask

### Works best with

- Use after `lynch-screener`: screener finds candidates → validator scores them against the full framework
- Complements `asymmetric-validator`: one uses Lynch's growth framework, the other uses asymmetric valuation — cross-validate

### Installation

```
npx skills add outman337/skills --skill lynch-validator
```

Or via URL:

```
/install-skill https://github.com/outman337/skills/raw/main/skills/lynch-validator/SKILL.md
```
