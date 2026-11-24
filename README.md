# ppt-architect

一套面向 AI Agent 的**高质量可编辑 PPT 策划、图形化版式架构与交付质检 Skill**。

它定位为 PPT 制作的**“总设计师与质量总监（大脑层）”**，让任意 AI 在结合底层执行 Skill（如 `pptx` / `python-pptx` / `pptxgenjs` / SVG 生成、AI 生图、数据可视化、网页检索、渲染看图）后，都能稳定产出**逻辑严密、版式多样、视觉统一、100% 原生可编辑**的高质量演示文稿，或将图片型海报高还原重构为原生 PowerPoint 页面。

---

## 核心特性

- **固定设计顺序（防套模板）**：强制遵循 `信息关系 → 主导版式 → 视觉资产 → 文字`，绝不为了套用漂亮图形而虚构因果/时间/循环关系。
- **整套叙事闭环**：反对把系统处理流程直接当成答辩大纲；强调“每页四问”、术语统一、严格区分“事实 / 设计 / 展望”以及首尾呼应。
- **连续五页零重复 + 19 种模板库**：内置 16 类信息关系映射与 19 种可复现图形模板（成果全景 / 时间流程 / 结构分析 / 对照聚焦），制作前必填《五页版式分配表》。
- **多 Skill 协同契约**：清晰定义本 Skill 与检索、AI 生图、数据图表、PPTX 落盘、渲染目检等外部 Skill 之间的交付边界；硬性要求 AI 生图**绝不含文字、数字与伪 UI**，文字全部原生可编辑。
- **海报转可编辑 PPT 专项 SOP**：提供“极少量独立可替换位图 + 大部分原生矢量对象”的三层重构架构与六步高还原实操法。
- **迭代修改纪律与四维质检**：多轮修订严格区分“锁定项 / 修改项 / 关联检查项”，交付前通过渲染预览逐页执行内容、视觉、细节、文件四维全量质检。

---

## 目录结构

本仓库采用通用 Agent Skill 标准布局（渐进式按需加载），克隆后即可直接作为一个 Skill 文件夹使用：

```text
.
├── README.md                                  # 仓库说明与安装指引
├── SKILL.md                                   # 核心总控指令：角色心智、六条铁律、多Skill协同协议、8步工作流
└── references/
    ├── layout-and-templates.md                # 16类信息关系映射、19种图形模板库、五页版式分配表与视觉节奏规则
    ├── visual-assets-and-copywriting.md       # 视觉系统基准、色彩语义、AI生图无文字规范、品牌资产、文案与图表标准
    ├── poster-to-editable-ppt.md              # 专项SOP：图片型PPT/海报高还原转真实可编辑原生PPT
    └── review-and-qa-checklist.md             # 迭代修改管理协议（锁定/修改/关联项）与交付前四维逐页质检清单
```

---

## 快速安装与使用

### 方式 1：直接克隆到 AI Agent 的 Skills 目录

- **Antigravity（当前项目）**
  ```bash
  git clone https://github.com/yhthub/PPT.git .agents/skills/ppt-architect
  ```
- **Antigravity（全局生效）**
  ```bash
  git clone https://github.com/yhthub/PPT.git ~/.gemini/config/skills/ppt-architect
  ```
- **Claude Code（全局 / 项目）**
  ```bash
  git clone https://github.com/yhthub/PPT.git ~/.claude/skills/ppt-architect
  ```
- **Cursor / Codex 等其他兼容 Agent Skills 标准的工具**
  ```bash
  git clone https://github.com/yhthub/PPT.git .cursor/skills/ppt-architect
  ```

### 方式 2：使用 Agent Skills CLI 安装

```bash
npx skills add yhthub/PPT
```

---

## 推荐搭配的执行层 Skill

`ppt-architect` 负责方法论、结构规划、版式分配与质量把关，建议与以下任意执行能力搭配使用：

1. **PPTX / SVG 落盘工具**：`pptx`、`python-pptx`、`pptxgenjs`、`html2pptx` 或矢量 SVG 生成 Skill。
2. **图像生成工具**：Imagen / Nano Banana / DALL-E 等（严格遵循本 Skill 的无文字风格锁输出独立主体插画）。
3. **事实与资产检索工具**：网页搜索 / 浏览器 Skill（核验官方最新数据，获取可核验的官方产品 Logo 与图标）。
4. **渲染与视觉审查工具**：LibreOffice / PowerPoint 转 PNG + 多模态视觉看图（执行交付前逐页目检）。
