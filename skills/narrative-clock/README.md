# narrative-clock — Druckenmiller 36 个月叙事时钟

[中文](#中文) | [English](#english)

---

## 中文

### 这个 Skill 是干什么的？

输入一个**叙事**（不是 ticker——是一个主题/趋势/故事），按 Druckenmiller "从不信到信需要 18-36 个月" 的框架，定位这个叙事处于"下注窗口 → 定性期 → 顺水期 → 过期" 周期中的哪一刻。生成可视化时钟图 + 六维度交叉验证 + 行动含义。

### 触发方式

> "XX 这个故事在哪个阶段" / "XX 叙事走到哪了" / "XX 现在算几个月" / "定位一下 XX" / "XX 处于 36 个月的什么位置" / "narrative clock XX" / "XX 是早期还是晚期" / "现在该不该入场 XX 主题"

### 核心框架：四阶段时钟

| 阶段 | 月份 | 别名 | 共识状态 | Druckenmiller 动作 |
|------|------|------|---------|-------------------|
| 🟢 **下注窗口** | 0-18 | 孤独期 | 极少数人信，多数人嘲笑 | 2% 侦察 → 信号集中后重仓 |
| 🟡 **定性期** | 18-24 | 切换期 | 共识快速形成，sell-side 切换 framework | 在车上的继续 hold；最后上车窗口 |
| 🔴 **顺水期** | 24-36 | 拥挤期 | 多数机构都信，零售跟进 | 不下车但不追高，开始想退出路径 |
| ⚫ **过期** | >36 | 教科书期 | 出租车司机都知道 | 默认不参与，除非新催化重置时钟 |

### 执行流程

**Step 1 — 识别"变化"**：把用户输入的主题/趋势转化为可定位起点的具体叙事

**Step 2 — 定位起点事件**：找到那个"ChatGPT 时刻"——36 个月时钟的 0 刻度。例如 AI = ChatGPT 发布 (2022/11)、核电复兴 = MSFT-Three Mile Island 协议 (2024/9)

**Step 3 — 四阶段时间定位**：计算从起点到今天的月数，落入哪一阶段

**Step 4 — 六维度交叉验证**：卖方覆盖度 / 媒体曝光度 / 机构持仓变化 / 价格行为 / 估值 framework 切换 / 反对者声量

**Step 5 — 综合定位 + 冲突分析**：六维度一致 → 直接定位；不一致 → 这本身是重要信息（"叙事走得比时间快"或"sell-side 滞后的最后不信"等模式）

**Step 6 — 生成时钟报告**：可视化 widget 输出，包含时钟条 + marker 位置 + 六维度网格 + 综合结论

**Step 7 — 行动含义**：根据定位给出框架性建议（不是投资建议）

### 输出内容

- 叙事名称 + 起点事件 + 已过月数
- 可视化时钟条（🟢 0-18M / 🟡 18-24M / 🔴 24-36M），marker 标注当前位置
- 六维度交叉验证表格（每个维度独立判断阶段）
- 综合定位结论
- 阶段对应的 Druckenmiller 式行动框架

### 与其他 Skill 的衔接

- **定位完成后想找具体标的** → 引导到 `asymmetric-screener` 或 `lynch-screener`
- **已有候选要做不对称验证** → 引导到 `asymmetric-validator`
- **已持有想检查信念** → 引导到 `belief-check`
- 这个 skill 定位**叙事**而不是个股，互补关系而非替代

### Druckenmiller 精神

> 定位的目的不是预测未来，是知道自己现在站在哪里，从而决定该做什么样的动作。

### 安装

```
npx skills add outman337/skills --skill narrative-clock
```

或 URL 安装：

```
/install-skill https://github.com/outman337/skills/raw/main/skills/narrative-clock/SKILL.md
```

---

## English

### What does this Skill do?

Input a **narrative** (not a ticker — a theme, trend, or story) and the skill locates where it sits in Druckenmiller's "18-36 months from disbelief to belief" cycle: Betting Window → Definition → Tailwind → Expired. Generates a visual clock + six-dimension cross-validation + action implications.

### Trigger phrases

> "where is the XX narrative now" / "narrative clock for XX" / "is XX early or late" / "should I enter XX theme now" / "how many months into XX"

### The Four-Stage Clock

| Stage | Months | Alias | Consensus | Druckenmiller's Move |
|-------|--------|-------|-----------|---------------------|
| 🟢 **Betting Window** | 0-18 | Lonely phase | Very few believe, most mock | 2% scout → load up when signals converge |
| 🟡 **Definition** | 18-24 | Switching phase | Consensus forms fast, sell-side reframes | Holders keep holding; last entry window |
| 🔴 **Tailwind** | 24-36 | Crowded phase | Most institutions believe, retail follows | Don't exit but don't chase, plan exit path |
| ⚫ **Expired** | >36 | Textbook phase | Even taxi drivers know it | Don't participate unless a new catalyst resets the clock |

### Workflow

**Step 1 — Identify the "change"**: Convert the user's theme/trend into a specific narrative with a locatable origin

**Step 2 — Locate the origin event**: Find the "ChatGPT moment" — the 0 mark of the 36-month clock. E.g., AI = ChatGPT launch (Nov 2022), nuclear revival = MSFT-Three Mile Island deal (Sep 2024)

**Step 3 — Four-stage time positioning**: Calculate months elapsed from origin to today

**Step 4 — Six-dimension cross-validation**: Sell-side coverage / media exposure / institutional holdings / price action / valuation framework shift / dissenter volume

**Step 5 — Composite positioning + conflict analysis**: Six dimensions aligned → direct positioning; misaligned → that itself is important info

**Step 6 — Generate clock report**: Visualize widget with clock bar + marker + six-dimension grid + verdict

**Step 7 — Action implications**: Framework guidance based on position (not investment advice)

### Output

- Narrative name + origin event + months elapsed
- Visual clock bar (🟢 0-18M / 🟡 18-24M / 🔴 24-36M), marker shows current position
- Six-dimension cross-validation table
- Composite verdict
- Stage-appropriate Druckenmiller-style action framework

### Works best with

- **After positioning, want specific tickers** → hand off to `asymmetric-screener` or `lynch-screener`
- **Have candidates, want asymmetric validation** → hand off to `asymmetric-validator`
- **Holding something, want to check conviction** → hand off to `belief-check`
- This skill positions **narratives**, not individual stocks — complementary, not a replacement

### The Druckenmiller Spirit

> The point of positioning isn't to predict the future — it's to know where you stand right now so you can decide what kind of move to make.

### Installation

```
npx skills add outman337/skills --skill narrative-clock
```

Or via URL:

```
/install-skill https://github.com/outman337/skills/raw/main/skills/narrative-clock/SKILL.md
```
