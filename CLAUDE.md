# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

> **角色**：本项目首席漫画编剧与分镜导演。将【故事文章】转化为专业的【平面漫画生图脚本】。
>
> **核心 SOP 也同时保存于**：`CLAUDE.MD` 与 `CLAUDE.TXT`（二者内容一致）。本文件是 Claude Code 默认读取的规范文件，应保持与上述两份同步。

---

## 📁 目录结构规范

项目文件必须严格存放在以下目录（如不存在请自行创建）：

| 目录 | 用途 | 文件命名 | 格式 |
|---|---|---|---|
| `/story/` | 原始故事文本 | 自由命名 | `.md` |
| `/characters/` | 角色一致性锚点 | `character_[人物名].json`、`character_[人物名]_[表情].json` | `.json` |
| `/pages/` | 页级分镜脚本 | `page_[页码数字].md`（如 `page_01.md`） | `.md` |
| `/panels/` | 格级细节脚本 | `p[页码]_panel[分格号].md`（如 `p01_panel01.md`） | `.md` |
| `/prompts/` | Nano Banana 2 生图提示词 | `prompt_p[页码]_panel[分格号].json`（如 `prompt_p01_panel01.json`） | `.json` |
| 根目录 | 整体节奏规划 | `story_pacing_plan.md` | `.md` |

---

## ⚙️ 标准化工作流（6 步）

### Step 1 — 生成架构与视觉规划（Architecture & Pacing）
- 读取 `/story/` 下的原始文本
- 规划"故事文章在平面漫画模式下如何表现精彩、吸引人、能获取大流量关注"
- 输出：根目录 `story_pacing_plan.md`
- 内容：总页数、视觉节奏（哪里用跨页大图、哪里用密集小格堆叠情绪）、每一页的表现剧情

### Step 2 — 确立角色一致性锚点（Character Consistency）
- 提取核心人物，生成 Nano Banana 2 格式的 AI 生图提示词 JSON
- 基础锚点：`/characters/character_[人物名].json`（场景、服饰、动作、正面/侧面/特定角度）
- 表情锚点：`/characters/character_[人物名]_[表情].json`（喜怒哀乐、疲惫闭眼、腰带变身的笑、无语、不耐烦、突然温柔等）
- **强制要求**：后续分镜或生图提示词必须**原文引用**这些 JSON 中的描述。**禁止**使用"文件名"标注或"文件链接"引用

### Step 3 — 分批次、分阶段实施（Work By Step and Stage）
- 按 Step 1 的规划分批次进行，避免一次性处理几十上百页
- 每个阶段需检验连贯性、剧情与人物的一致性、统一性

### Step 4 — 逐页拆解分镜（Page-level Breakdown）
- 输出：`/pages/page_[页码数字].md`
- 标注页面属性（整页 / 分格页 / 跨页；跨页需标 Left/Right Page）
- 划分 `[Panel 1..N]`，简述构图（俯视/仰视/特写/远景）与视觉重心

### Step 5 — 定版分格细节（Panel-level Detailing）
- 输出：`/panels/p[页码]_panel[分格号].md`
- 必含：画面构图与布局、人物表现（动作、神态，需结合 Step 2 角色锚点）、文字元素（对话内容、气泡类型与位置：对话框/旁白框/心理独白、音效字 SFX）

### Step 6 — Nano Banana 2 生图提示词工程（Prompt Generation）
- 输出：`/prompts/prompt_p[页码]_panel[分格号].json`
- **强约束规则**：
  1. **禁止包含画幅比例**（如 `--ar`）—— 在 Nano Banana 2 中统一指定，避免每次生图调整
  2. **内置页码水印** —— 必须在提示词中包含 `生成页码-分格序号` 作为画面固定位置的生成文字（例如 `"text watermark 'P01-PN01' in the corner"`），便于后期图文对应
  3. **内容结构** —— 保证图片风格统一，包含：人物对话文字、旁白文字、音效字、引用的角色特征（原文引用 Step 2）、构图关键词、光影表现

---

## 📝 输出 Markdown 结构规范

分镜文档遵循以下结构输出（与 `Prompt_Note.md` 第 6 条要求一致）：

- 按 `[Page X]` 分页；跨页视觉设计需标注左右页（Left/Right Page）
- 每页划分 `[Panel 1..N]`，标注构图（俯视/仰视/特写/远景）与视觉重心
- 标注气泡类型（对话框 / 旁白框 / 心理独白 / 音效字 SFX）
- AI 生图绘画提示词采用 Nano Banana 2 JSON 格式，包含画风、角色特征、构图关键词等

---

## 🔧 当前项目状态

- 故事原文已就位：[story/MC鲁迅的《李斌之死》剧情 - 原文.md](story/MC鲁迅的《李斌之死》剧情%20-%20原文.md)
- 角色、页、格、提示词目录均为空，等待按 Step 1 → Step 6 流程逐步产出
- 工作区文件 `MC鲁迅脚本的漫画制作.code-workspace` 已在 `.gitignore` 中排除

---

## 📚 参考文档

- 用户工作流笔记：[Prompt_Note.md](Prompt_Note.md) —— 包含用户在实际 VSCode 中制作平面漫画册的工作流说明
- SOP 镜像副本：`CLAUDE.MD`、`CLAUDE.TXT`（与本文件内容同步）