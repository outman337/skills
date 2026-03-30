# Asymmetric Investing Skills

美股不对称投资 Skills 共享仓库 | Asymmetric Stock Investing Skills for Claude

两个配套 Skill，专为**不对称投资框架**设计——低估值地板、高增速、热门赛道的三条腿逻辑。

---

## 📦 Skills 列表

### 1. `asymmetric-screener` — 不对称机会猎手

**主动扫描美股市场，发现被错误定价的高不对称性投资机会。**

无需提供 ticker，Skill 自己去网上搜索候选，按"三条腿的凳子"框架筛选，生成带可视化评分卡的候选报告。

**触发方式：**
> "找机会" / "扫一下" / "有什么新机会" / "find asymmetric setups" / "最近有什么好票"

**输出包括：**
- 市场环境速写（哪些板块热、资金流向）
- 5-8 个候选的可视化 card（P/S 同行对比条、均值回归数学、不对称评分）
- 最值得 Deep Dive 的优先级建议

**安装：**
```
/install-skill https://github.com/outman337/asymmetric-investing-skills/raw/main/asymmetric-screener.skill
```

---

### 2. `asymmetric-validator` — 不对称验证器

**输入一个 ticker，快速判定是否符合不对称投资框架，给出 PASS / BORDERLINE / FAIL。**

不做完整投研报告——只做框架验证，速度优先。

**触发方式：**
> "验证 XXXX" / "XXXX 不对称吗" / "screen XXXX" / "跑一下 XXXX" / "XXXX passes?"

**输出包括：**
- 三条腿逐条验证（收入加速 / 估值地板 / 热门赛道）
- EBITDA 转正催化检查
- 同行估值对比表（可视化）
- 最终判定卡片（PASS / BORDERLINE / FAIL）
- 反向不对称检查（是否 priced for perfection）

**安装：**
```
/install-skill https://github.com/outman337/asymmetric-investing-skills/raw/main/asymmetric-validator.skill
```

---

## 🔧 安装方法

### 方法一：URL 安装（推荐）

在 Claude 对话中输入安装命令即可，两个 Skill 分别安装：

```
/install-skill https://github.com/outman337/asymmetric-investing-skills/raw/main/asymmetric-screener.skill
```

```
/install-skill https://github.com/outman337/asymmetric-investing-skills/raw/main/asymmetric-validator.skill
```

### 方法二：手动下载安装

1. 从本仓库下载对应的 `.skill` 文件
2. 在 Claude 对话中使用 `/install-skill` 命令并上传文件

---

## 📐 核心框架：三条腿的凳子

每个候选必须同时满足三个条件：

| 条件 | 标准 |
|------|------|
| **Leg 1 — 低估值地板** | P/S 低于同行中位数 40%+，提供下行保护 |
| **Leg 2 — 收入加速** | 最近 1-2 季度 YoY ≥25%，TTM ≥$20M |
| **Leg 3 — 热门赛道** | 近 3 个月板块资金净流入，市场关注度高 |

**硬性排除：** Pre-revenue、现金跑道 <6 个月、市值 >$50B、P/S 高于同行

**加分项：** 距首次 EBITDA 转正 ≤2 个季度、内部人净买入、具体可量化催化剂

---

## 🔗 与其他 Skill 的衔接

| Skill | 协同方式 |
|-------|---------|
| `asymmetric-screener` | 发现候选 → 传给 validator 快速过筛 |
| `asymmetric-validator` | 验证通过 → 进入 equity-research 做完整 Deep Dive |

典型工作流：**screener 扫描** → **validator 确认** → **equity-research 深研** → 决策

---

## ⚠️ 免责声明

本 Skill 生成的分析基于公开信息和模型推算，仅供研究参考，不构成投资建议。投资有风险，决策需谨慎。

---

## License

MIT
