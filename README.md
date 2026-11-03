# Daisy Fig Lookpack Skill

**论文 Fig.1 的「构图 × 观感」风格包 Skill** —— 维护并应用 Daisy pastel look-pack
系统，面向 Cursor / Claude Code / Codex。

仓库：**[`Daisy-fig-lookpack-skill`](https://github.com/Daisy-achun/Daisy-fig-lookpack-skill)**  
Skill 名：`fig-lookpack`（调用：`/fig-lookpack`）  
作者：**Daisy**（[@Daisy-achun](https://github.com/Daisy-achun)）

> 和 [`Daisy-paper-diagram-skill`](https://github.com/Daisy-achun/Daisy-paper-diagram-skill) 是**姊妹仓，不要混装同一用途**。  
> 本仓特色是 **Lookpack（风格包）**：设计语法 + 8 核心 look + 扩展写法。  
> 那边特色是 **Paper Diagram（画图发行版）**：多端 `install/sync`、一键装进项目。

---

## 和 Daisy-paper-diagram-skill 怎么区分？

| | **Daisy-fig-lookpack-skill**（本仓） | **Daisy-paper-diagram-skill** |
|--|--------------------------------------|-------------------------------|
| **一句话** | 风格包 / 设计系统源 | 画论文流程图的多端发行版 |
| **Skill 名** | `fig-lookpack` | `paper-framework-diagram` |
| **仓库形态** | **扁平单目录**（拷进 skills 即用） | `skills/` + 三端镜像 + install 脚本 |
| **你更该用谁** | 要改 look、加风格、抠设计语法 | 只想装好就画 Fig.1 |
| **视觉气质** | 同一套学术 pastel 方法图语法 | 同一套学术 pastel 方法图语法 |

两套 **出图质量门禁一致**（≥10pt、真下标、反白框套娃、同源 SVG/PPTX）；差别在**定位与安装方式**，不是两套互斥画风。

---

## 项目介绍

本 Skill 把论文方法图拆成两轴：

1. **Composition（怎么摆）**：`network-rail` / `dual-stream` / `agent-loop` / `two-stage-train`  
2. **Look（长什么样）**：8 个核心 pastel 观感包（色带、模块堆栈、双塔、Agent 壳…）

Agent 读 Method 结构后 **锁定 1 套** `composition × look`，再按 `DESIGN_GRAMMAR.md` + 对应 `LOOK.md` 绘制。你也可以单独用它来：**新增 look、改色板、写 Style keywords、做风格 QA**。

### 生成什么风格的论文流程图

**学术 pastel 方法图**：白底、低饱和分区、大圆角、细箭头、大字号。

| Look | 画面 |
|------|------|
| `stage-band-pastel` | 多 Stage 彩色虚线色带 |
| `modular-pastel-stack` | 功能色模块 + Nx 壳 + 残差弯箭 |
| `dual-modality-gradient` | 双塔汇合 + ❄/🔥 |
| `agent-panel` | 奶油控制壳 + Tools + 轨迹 |
| `rl-grpo-chain` | 组采样卡 + 奖励公式 inset |
| `paradigm-compare` | 左右范式对比 |
| `benchmark-dense` | 构建 & 评测双面板 |
| `method-overview-flat` | 中央骨干兜底 |

---

## 快速安装（扁平直装）

```bash
git clone https://github.com/Daisy-achun/Daisy-fig-lookpack-skill.git
# Cursor 项目内
mkdir -p /path/to/project/.cursor/skills
cp -R Daisy-fig-lookpack-skill /path/to/project/.cursor/skills/fig-lookpack
```

或用户级：

```bash
mkdir -p ~/.cursor/skills
cp -R Daisy-fig-lookpack-skill ~/.cursor/skills/fig-lookpack
```

对话触发：`lookpack` / `风格包` / `论文流程图`，或显式 `/fig-lookpack`。

若你要 **Claude + Codex + Cursor 一键安装**，请改用  
[`Daisy-paper-diagram-skill`](https://github.com/Daisy-achun/Daisy-paper-diagram-skill)（Skill 名 `paper-framework-diagram`）。

---

## 仓库结构

```text
SKILL.md                 ← fig-lookpack 主指令
styles/
  DESIGN_GRAMMAR.md      ← 共享语法
  compositions/          ← 怎么摆
  looks/                 ← 8 核心观感 + 别名
  router.md · CATALOG.md
references/              ← 抠图 / PPT / QA
agents/openai.yaml
scripts/smoke_test_skill.py
```

扩展风格：复制 `styles/looks/_template`，写清 Design thinking、Style keywords、色板与禁止项。

---

## GitHub About（可粘贴）

- **简介：**  
  `论文 Fig.1 风格包 Skill（fig-lookpack）：pastel 构图×观感 packs；扁平目录，便于维护 look。姊妹仓：Daisy-paper-diagram-skill。`
- **Topics：** `agent-skills` · `cursor` · `paper-figures` · `lookpack` · `scientific-visualization` · `svg` · `pptx`

---

## 作者

**Daisy**（[@Daisy-achun](https://github.com/Daisy-achun)）

## License

MIT
