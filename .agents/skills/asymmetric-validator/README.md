# asymmetric-validator — 不对称验证器

[中文](#中文) | [English](#english)

---

## 中文

### 这个 Skill 是干什么的？

输入一个 ticker，按照不对称投资框架逐条验证是否满足"三条腿的凳子"，快速给出 **PASS / BORDERLINE / FAIL** 判定。不做完整投研报告——只做框架验证，速度优先。

### 触发方式

> "验证 XXXX" / "XXXX 不对称吗" / "screen XXXX" / "过一下 XXXX" / "跑一下 XXXX" / "XXXX passes?" / "check XXXX"

### 验证流程

**Leg 1 — 收入加速**：TTM 收入、YoY 增速、环比趋势、Backlog 可见度

**Leg 2 — 估值地板**：P/S vs 同行中位数、毛利率、现金跑道、稀释风险

**Leg 3 — 热门赛道**：板块近 3 个月表现、资金流向、市场叙事

**Bonus — EBITDA 转正**：已转正 / 即将转正（≤2Q）/ 仍亏损

### 判定规则

| 结果 | 条件 |
|------|------|
| **PASS ✓** | 三条腿全部 PASS |
| **BORDERLINE ~** | 两条 PASS + 一条 BORDERLINE |
| **FAIL ✗** | 任意一条 FAIL，或触发硬性排除条件 |

### 输出内容

- 三条腿逐条验证（文字 + 数据）
- 同行估值对比表（可视化）
- 最终判定卡片（PASS / BORDERLINE / FAIL）
- 反向不对称检查（是否 priced for perfection）

### 与其他 Skill 的衔接

- 通常跟在 `asymmetric-screener` 之后使用：screener 发现候选 → validator 快速过筛
- PASS 或 BORDERLINE 的标的，下一步进入 `equity-research` 做完整 Deep Dive

### 安装

```
npx skills add outman337/skills --skill asymmetric-validator
```

或 URL 安装：

```
/install-skill https://github.com/outman337/skills/raw/main/skills/asymmetric-validator/SKILL.md
```

---

## English

### What does this Skill do?

Input a ticker and get a rapid **PASS / BORDERLINE / FAIL** verdict based on the asymmetric investing framework. No full research report — framework validation only, speed first.

### Trigger phrases

> "验证 XXXX" / "screen XXXX" / "does XXXX pass?" / "check XXXX" / "is XXXX asymmetric?"

### Validation Steps

**Leg 1 — Revenue Acceleration**: TTM revenue, YoY growth, QoQ trend, backlog visibility

**Leg 2 — Valuation Floor**: P/S vs peer median, gross margin, cash runway, dilution risk

**Leg 3 — Hot Sector**: Sector 3-month performance, fund flows, market narrative

**Bonus — EBITDA Turn**: Already positive / Turning positive (≤2Q) / Still burning

### Verdict Rules

| Result | Condition |
|--------|-----------|
| **PASS ✓** | All three legs pass |
| **BORDERLINE ~** | Two legs pass + one borderline |
| **FAIL ✗** | Any leg fails, or hard exclusion triggered |

### Output

- Three-leg validation (text + data)
- Peer valuation comparison table (visual)
- Final verdict card (PASS / BORDERLINE / FAIL)
- Reverse asymmetry check (priced for perfection?)

### Works best with

- Use after `asymmetric-screener`: screener finds candidates → validator quickly filters
- PASS/BORDERLINE results → hand off to `equity-research` for full Deep Dive

### Installation

```
npx skills add outman337/skills --skill asymmetric-validator
```

Or via URL:

```
/install-skill https://github.com/outman337/skills/raw/main/skills/asymmetric-validator/SKILL.md
```
