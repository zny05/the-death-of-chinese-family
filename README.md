# the-death-of-chinese-family

**the-death-of-chinese-family** is a manga adaptation project based on the Zhihu article **"婚姻制度在年轻人眼中为何失去吸引力？" (Why has the marriage system lost its appeal to young people?)** by MC鲁迅, a marriage-field practice author.

## 📖 Story Source

- **Original Article**: [婚姻制度在年轻人眼中为何失去吸引力？](https://www.zhihu.com/question/2064210525970608692/answer/2078428412390139392)
- **Author**: MC鲁迅 (婚恋从业纪实作者)
- **Theme**: The erosion of marriage's appeal to young people, explored through quiet, detailed domestic moments rather than dramatic conflict
- **Adaptation Style**: Realistic comic journalism — using the "comic journal" format to transform real-life marital observations into a visual narrative

### 项目来源

- **原文链接**：[婚姻制度在年轻人眼中为何失去吸引力？](https://www.zhihu.com/question/2064210525970608692/answer/2078428412390139392)
- **作者**：MC鲁迅（婚恋从业纪实作者）
- **主题**：通过细腻的 domestic 细节探讨婚姻对年轻人的吸引力如何流失，不依靠戏剧冲突，只展现“婚姻平淡日子里的暗流”

## 🎨 Project Overview

This project adapts MC鲁迅's marriage observations into a **19-page manga** (including cover) that explores marital dynamics through:

- **Quiet, observant storytelling** — no shouting matches, no violence, only the "small, terrifying刺" of spiritual friction
- **Domestic space as character** — the home itself becomes a character, with repeated spatial elements creating atmosphere
- **Time as structural device** — a single day (7:45 AM to 8:15 PM) structured into 5 narrative acts
- **Minimalist visual style** — international comic style with soft cinematic lighting, muted warm-cool palette

The adaptation follows a complete 6-step workflow:

1. **Architecture & Pacing** — Narrative structure, page count, visual rhythm
2. **Character Consistency** — JSON-based character anchors for 李斌 and 妻子 (expressions, emotions, traits)
3. **Page-level Breakdown** — 22 pages with panel composition and visual重心
4. **Panel-level Detailing** — 58 panels with composition, character performance, and text elements
5. **Nano Banana 2 Prompt Engineering** — 37 generation prompts with watermarks, style keywords, and composition rules
6. **Visual Style Guide** — Consistent aesthetics across all pages

### 项目概览

本项目将 MC鲁迅的婚姻观察改编为 **19页漫画**（含封面），通过以下方式叙事：

- **安静的观察叙事** — 无高 volume争吵，无暴力，只有“精神折磨的细小而可怕的刺”
- **家庭空间作为角色** — 家 itself 成为一个角色，通过重复的空间元素营造氛围
- **时间作为结构装置** — 单日（7:45 AM 至 8:15 PM）划分为 5 个叙事 Act
- **极简视觉风格** — 国际漫画风格，柔和电影光影，调和的暖冷色调

本项目遵循完整的 6 步工作流：

1. **架构与铺排** — 叙事结构、页数、视觉节奏（`story_pacing_plan.md`）
2. **人物一致性** — 基于 JSON 的人物锚点，用于 李斌 和 妻子（表情、情绪、特质）
3. **逐页拆解分镜** — 22 页带有面板 composition 和 visual重心
4. **每格细节处理** — 58 个面板带有 composition、人物表现和 text 元素
5. **Nano Banana 2 提示词工程** — 37 个 generation 提示词带有 watermarks、style keywords 和 composition rules
6. **视觉风格指南** — 全页一致的美学
   
## 📁 Repository Structure

```
.
├── .gitignore           # Git ignore rules
├── CLAUDE.md            # Standardized SOP for comic script creation
├── CLAUDE.TXT           # Mirror of CLAUDE.md
├── LICENSE              # Project license
├── Prompt_Note.md       # User workflow notes
├── story/
│   └── MC鲁迅的《李斿之死》剧情 - 原文.md  # Original story text
├── story_pacing_plan.md # 19-page narrative architecture (Step 1 output)
├── characters/          # 13 JSON character consistency anchors
│   ├── character_李斌.json
│   ├── character_李斌_无语.json
│   ├── character_李斌_疲惫闭眼.json
│   ├── character_李斌_腰带变身的笑.json
│   └── ... (wife character + expressions)
├── pages/               # 22 page scripts (pages 00-21)
│   ├── page_00.md       # Cover spread
│   ├── page_01.md - page_04.md  # Act I: "唤醒"
│   ├── page_05.md - page_07.md  # Act II: "出门"
│   ├── page_08.md - page_09.md  # Act III: "独处"
│   ├── page_10.md - page_15.md  # Act IV: "夜归"
│   ├── page_16.md - page_19.md  # Act V: "命名"
│   └── page_20.md - page_21.md  # Supplemental pages
├── panels/              # 58 panel-level detail scripts
│   ├── p00_cover.md     # Cover page
│   ├── p01_panel01.md - p01_panel06.md  # Panel details
│   └── ... (p02-p18 panels)
└── prompts/             # 37 Nano Banana 2 generation prompts
    ├── prompt_p00_cover.json    # Cover prompt
    ├── prompt_p01_panel01.json - prompt_p01_panel06.json  # Panel prompts
    └── ... (p02-p18 prompts)
```
### 📁 仓库结构

```markdown
.
├── .gitignore           # Git 忽略规则
├── CLAUDE.md            # 漫画脚本生成的标准化 SOP
├── CLAUDE.TXT           # CLAUDE.md 的镜像
├── LICENSE              # 项目许可证
├── Prompt_Note.md       # 用户工作流笔记
├── story/
│   └── MC鲁迅的《李斿之死》剧情 - 原文.md  # 原始故事文本
├── story_pacing_plan.md # 19页叙事架构（Step 1 输出）
├── characters/          # 13 个 JSON 人物一致性锚点
│   ├── character_李斌.json
│   ├── character_李斌_无语.json
│   ├── character_李斌_疲惫闭眼.json
│   ├── character_李斌_腰带变身的笑.json
│   └── ... (妻子角色 + 表情)
├── pages/               # 22 个页脚本（pages 00-21）
│   ├── page_00.md       # 封面跨页
│   ├── page_01.md - page_04.md  # Act I: "唤醒"
│   ├── page_05.md - page_07.md  # Act II: "出门"
│   ├── page_08.md - page_09.md  # Act III: "独处"
│   ├── page_10.md - page_15.md  # Act IV: "夜归"
│   ├── page_16.md - page_19.md  # Act V: "命名"
│   └── page_20.md - page_21.md  # Supplemental pages
├── panels/              # 58 个面板级细节脚本
│   ├── p00_cover.md     # 封面页
│   ├── p01_panel01.md - p01_panel06.md  # 面板细节
│   └── ... (p02-p18 panels)
└── prompts/             # 37 个 Nano Banana 2 generation 提示词
    ├── prompt_p00_cover.json    # 封面提示词
    ├── prompt_p01_panel01.json - prompt_p01_panel06.json  # 面板提示词
    └── ... (p02-p18 prompts)
```

## ⚙️ Workflow

The project follows a standardized 6-step SOP documented in `CLAUDE.md`:

1. **Step 1** — Architecture & pacing plan (`story_pacing_plan.md`)
2. **Step 2** — Character consistency JSON anchors
3. **Step 3** — Stage-by-stage implementation
4. **Step 4** — Page-level breakdown (`pages/page_NN.md`)
5. **Step 5** — Panel-level detailing (`panels/p[页码]_panel[分格号].md`)
6. **Step 6** — Nano Banana 2 prompt generation (`prompts/prompt_p[页码]_panel[分格号].json`)

**Key constraints**:
- No `--ar` ratio specifications (Nano Banana 2 unified)
- Fixed watermark: `生成页码-分格序号` in corner
- All prompt content references Step 2 JSON (no filename/link references)
- Page pacing: 18 pages + 1 cover spread = 19 page units

### ⚙️ 工作流

项目遵循 `CLAUDE.md` 中规定的标准化 6 步 SOP：

1. **Step 1** — 架构与铺排计划 (`story_pacing_plan.md`)
2. **Step 2** — 人物一致性 JSON 锚点
3. **Step 3** — 分批分阶段实施
4. **Step 4** — 逐页拆解分镜 (`pages/page_NN.md`)
5. **Step 5** — 面板级细节处理 (`panels/p[页码]_panel[分格号].md`)
6. **Step 6** — Nano Banana 2 提示词生成 (`prompts/prompt_p[页码]_panel[分格号].json`)

**关键约束**：
- 无 `--ar` 规格说明（Nano Banana 2 统一指定）
- 固定 watermark：`生成页码-分格序号` 在角落
- 所有提示词内容引用 Step 2 JSON（不使用"文件名"或"文件链接"引用）
- 页铺排：18 页 + 1 封面跨页 = 19 页单位

## 🛠️ Technical Details

- **Art Style**: 国漫·现代都市 (Chinese modern comic style)
- **Color Temperature**: 偏冷 (cool bias — 卧室偏蓝灰, 客厅偏暖白, 夜场偏青黑)
- **Nano Banana 2 Format**: JSON with `text watermark 'P01-PN01' in the corner`
- **Page Count**: 19 pages (18 content + 1 cover spread)
- **Characters**: 李斌 (husband, 30s, fatigued silence), 妻子 (wife, strong, control-oriented), MC鲁迅 (author/narrator, appears later)

### 🛠️ 技术细节

- **艺术风格**：国漫·现代都市 (Chinese modern comic style)
- **色温**：偏冷 (cool bias — 卧室偏蓝灰、客厅偏暖白、夜场偏青黑)
- **Nano Banana 2 格式**：JSON 含 `text watermark 'P01-PN01' in the corner`
- **页数**：19 页 (18 content + 1 封面跨页)
- **人物**： 李斌 (丈夫，30多岁，熬夜后疲惫沉默), 妻子 (妻子，强势，控制欲强，细节敏感), MC鲁迅 (作者/叙事者， Page 18 后出现)

## 📜 License

This project is licensed under the MIT License - see the `LICENSE` file for details.

### 📜 许可证

本项目采用 MIT License - 详见 `LICENSE` 文件。

## 🙏 Acknowledgments

- Original article author: MC鲁迅
- All character observations drawn from real marital dynamics
- Inspired by the "slice-of-life" manga journalism tradition

### 🙏 致谢

- 原文作者：MC鲁迅
- 所有人物观察均源自真实的婚姻动态
- 受 "slice-of-life" 漫画新闻传统启发