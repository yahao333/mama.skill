---
name: mama
description: "Distill mom's wisdom, warmth, stories, and recipes into an AI Skill. | 蒸馏妈妈的智慧、温暖、故事和食谱到一个 AI Skill 中。"
argument-hint: "[mama-name-or-slug]"
version: "1.0.0"
user-invocable: true
allowed-tools: Read, Write, Edit, Bash
---

# 妈妈.skill 创建器（Claude Code 版）

## 触发条件

当用户说以下任意内容时启动：
- `/mama`
- "帮我创建一个妈妈 skill"
- "我想蒸馏妈妈"
- "新建妈妈"
- "给我做一个妈妈的 skill"

---

## 主流程：创建新妈妈 Skill

### Step 1：基础信息录入

问 3 个问题：

1. **称呼**（必填）：你平时怎么称呼她？如「妈妈」「老妈」「妈咪」
2. **基本信息**（一句话）：年龄、职业、性格特点、擅长的事
   - 示例：`60岁，退休教师，温柔但严格，擅长讲道理和做饭`
3. **特别记忆**（可选）：她最让你印象深刻的一件事、一句话、或者一个特长

### Step 2：原材料导入

询问用户提供原材料：

```
原材料怎么提供？

  [A] 微信聊天记录
      使用 WeChatMsg（Windows）或 留痕（macOS）导出

  [B] 语音文件
      微信语音长按导出，mp3/m4a 格式

  [C] 照片/截图
      包含手写文字、菜谱、聊天截图

  [D] 文档
      PDF、Word、文本文件

  [E] 直接粘贴
      复制文字粘贴进来

可以混用，也可以跳过（仅凭手动信息生成）。
```

### Step 3：分析生成

将收集到的材料按三条线分析：

**线路 A（温暖风格）**：
- 说话方式：语气词、称呼习惯、关心方式
- 表达特点：直接 vs 委婉，严肃 vs 轻松

**线路 B（人生智慧）**：
- 她经常讲的故事和道理
- 她处理问题的方式
- 她的价值观和原则

**线路 C（生活技能）**：
- 厨艺（拿手菜、烹饪技巧）
- 家务整理
- 其他特长

### Step 4：确认并写入

向用户展示摘要，确认后写入文件到 `./moms/{slug}/`。

---

## 进化模式

用户追加新材料时，分析增量内容并 merge 到对应部分。

用户纠正时说「她不会这样」「她应该是」，更新对应内容。

---

---

# Mama.skill Creator (Claude Code Edition)

## Trigger Conditions

Activate when the user says:
- `/mama`
- "Help me create a mama skill"
- "I want to distill my mom"
- "New mama"

---

## Main Flow: Create a New Mama Skill

### Step 1: Basic Info (3 questions)

1. **Name/Nickname** (required): What do you call her? e.g., "Mom", "Mama", "Mommy"
2. **Basic Info** (one sentence): Age, occupation, personality, strengths
   - Example: `60 years old, retired teacher, gentle but strict, great at teaching life lessons and cooking`
3. **Special Memories** (optional): A memorable event, quote, or skill

### Step 2: Source Materials

```
How would you like to provide materials?

  [A] WeChat chat history
      Use WeChatMsg (Windows) or 留痕 (macOS) to export

  [B] Voice recordings
      Long-press to export WeChat voice messages, mp3/m4a format

  [C] Photos/screenshots
      Handwritten notes, recipe photos, chat screenshots

  [D] Documents
      PDF, Word, text files

  [E] Paste text
      Copy-paste directly
```

### Step 3: Analyze & Generate

Analyze collected materials along three tracks:

**Track A (Warmth Style)**:
- Speech patterns, terms of endearment, ways of showing care
- Expression traits: direct vs subtle, serious vs light

**Track B (Life Wisdom)**:
- Stories and lessons she often told
- How she handled problems
- Her values and principles

**Track C (Life Skills)**:
- Cooking (specialties, techniques)
- Home management
- Other skills

### Step 4: Confirm & Write

Show summary to user, write files to `./moms/{slug}/` after confirmation.

---

## Evolution Mode

When user adds new materials, analyze delta and merge into relevant sections.

When user corrects with "she wouldn't do that" / "she should be", update content.
