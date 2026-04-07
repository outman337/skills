# Skills

[中文](#中文) | [English](#english)

---

## 中文

> ⚠️ **免责声明**：本项目仅供教育和学习使用，不构成任何投资建议。投资有风险，请在做出任何投资决策前自行研究并咨询专业顾问。

为 Claude 打造的投资分析 Skills 集合，专注**不对称投资框架**和**彼得林奇成长股框架**——用系统化方法发现和验证被市场错误定价的机会，以及寻找下一个十倍股。

### 可用 Skills

#### 📈 投资分析

| Skill | 描述 |
|-------|------|
| [asymmetric-screener](./skills/asymmetric-screener) | 主动扫描美股市场，发现被错误定价的高不对称性投资机会。无需提供 ticker，自动搜索候选并生成可视化评分报告。 |
| [asymmetric-validator](./skills/asymmetric-validator) | 输入一个 ticker，按"三条腿的凳子"框架快速验证，给出 PASS / BORDERLINE / FAIL 判定。 |
| [lynch-screener](./skills/lynch-screener) | 彼得林奇十倍股猎手——主动扫描美股市场，按林奇风格发现 Fast Grower 和 Stalwart 候选。专注无聊行业、被忽视的角落、低 PEG，按林奇六分类输出评分卡。 |
| [lynch-validator](./skills/lynch-validator) | 彼得林奇验证器——输入一个 ticker，按林奇完整框架验证：六分类、二分钟独白、十三买入信号、十一红灯、PEG 估值、林奇式财务健康度，给出 PASS / WATCH / FAIL 判定。 |

### 安装方式

#### 方式一：npx 安装（推荐）

安装全部 Skills：
```
npx skills add outman337/skills
```

安装单个 Skill：
```
npx skills add outman337/skills --skill asymmetric-screener
npx skills add outman337/skills --skill asymmetric-validator
npx skills add outman337/skills --skill lynch-screener
npx skills add outman337/skills --skill lynch-validator
```

#### 方式二：Claude.ai 网页端

1. 打开 **设置 > 功能** 并启用**代码执行与文件创建**
2. 进入对应 skill 文件夹，下载 `SKILL.md`
3. 在 Claude 中进入 **自定义 > Skills**
4. 点击 **+** 上传文件即可

#### 方式三：URL 直接安装

```
/install-skill https://github.com/outman337/skills/raw/main/skills/asymmetric-screener/SKILL.md
```

```
/install-skill https://github.com/outman337/skills/raw/main/skills/asymmetric-validator/SKILL.md
```

```
/install-skill https://github.com/outman337/skills/raw/main/skills/lynch-screener/SKILL.md
```

```
/install-skill https://github.com/outman337/skills/raw/main/skills/lynch-validator/SKILL.md
```

---

## English

> ⚠️ **Disclaimer**: This project is for educational and informational purposes only. Nothing here constitutes financial advice. Always do your own research and consult a qualified financial advisor before making investment decisions.

A collection of Claude Skills for investment analysis, built around the **asymmetric investing framework** and the **Peter Lynch growth-stock framework** — systematic approaches to finding and validating mispriced opportunities and hunting for the next tenbagger.

### Available Skills

#### 📈 Investment Analysis

| Skill | Description |
|-------|-------------|
| [asymmetric-screener](./skills/asymmetric-screener) | Actively scans the US stock market to discover high-asymmetry investment opportunities. No ticker needed — the skill searches on its own and generates a scored visual report. |
| [asymmetric-validator](./skills/asymmetric-validator) | Input a ticker and get a rapid PASS / BORDERLINE / FAIL verdict based on the "three-legged stool" asymmetric framework. |
| [lynch-screener](./skills/lynch-screener) | Peter Lynch tenbagger hunter — scans the US market for Fast Grower and Stalwart candidates in Lynch's style. Focused on boring industries, neglected corners, and low PEG, with scorecards organized by Lynch's six categories. |
| [lynch-validator](./skills/lynch-validator) | Peter Lynch validator — input a ticker and run the full Lynch framework: six categories, two-minute monologue, thirteen buy signals, eleven red flags, PEG valuation, Lynch-style balance sheet check. Returns PASS / WATCH / FAIL. |

### Installation

#### Option A — npx (recommended)

Install all skills:
```
npx skills add outman337/skills
```

Install a specific skill:
```
npx skills add outman337/skills --skill asymmetric-screener
npx skills add outman337/skills --skill asymmetric-validator
npx skills add outman337/skills --skill lynch-screener
npx skills add outman337/skills --skill lynch-validator
```

#### Option B — Claude.ai Web / Desktop

1. Go to **Settings > Capabilities** and enable **Code execution and file creation**
2. Download the `SKILL.md` from the skill folder you want
3. In Claude, go to **Customize > Skills**
4. Click **+** and upload the file

#### Option C — Direct URL install

```
/install-skill https://github.com/outman337/skills/raw/main/skills/asymmetric-screener/SKILL.md
```

```
/install-skill https://github.com/outman337/skills/raw/main/skills/asymmetric-validator/SKILL.md
```

```
/install-skill https://github.com/outman337/skills/raw/main/skills/lynch-screener/SKILL.md
```

```
/install-skill https://github.com/outman337/skills/raw/main/skills/lynch-validator/SKILL.md
```

---

## License

MIT
