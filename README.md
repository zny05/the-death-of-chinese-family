# the-death-of-chinese-family

**the-death-of-chinese-family** is a manga adaptation project based on the Zhihu article **"婚姻制度在年轻人眼中为何失去吸引力？" (Why has the marriage system lost its appeal to young people?)** by MC鲁迅, a marriage-field practice author.

## 📖 Story Source

- **Original Article**: [婚姻制度在年轻人眼中为何失去吸引力？](https://www.zhihu.com/question/2064210525970608692/answer/2078428412390139392)
- **Author**: MC鲁迅 (婚恋从业纪实作者)
- **Theme**: The erosion of marriage's appeal to young people, explored through quiet, detailed domestic moments rather than dramatic conflict
- **Adaptation Style**: Realistic comic journalism — using the "comic journal" format to transform real-life marital observations into a visual narrative

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

## 🛠️ Technical Details

- **Art Style**: 国漫·现代都市 (Chinese modern comic style)
- **Color Temperature**: 偏冷 (cool bias — 卧室偏蓝灰, 客厅偏暖白, 夜场偏青黑)
- **Nano Banana 2 Format**: JSON with `text watermark 'P01-PN01' in the corner`
- **Page Count**: 19 pages (18 content + 1 cover spread)
- **Characters**: 李斌 (husband, 30s, fatigued silence), 妻子 (wife, strong, control-oriented), MC鲁迅 (author/narrator, appears later)

## 📜 License

This project is licensed under the MIT License - see the `LICENSE` file for details.

## 🙏 Acknowledgments

- Original article author: MC鲁迅
- All character observations drawn from real marital dynamics
- Inspired by the "slice-of-life" manga journalism tradition