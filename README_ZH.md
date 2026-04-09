<div align="center">

# mama.skill

> *"母亲的爱是让普通人完成不可能事业的燃料。"*

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Python 3.9+](https://img.shields.io/badge/Python-3.9%2B-blue.svg)](https://python.org)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Skill-blueviolet)](https://claude.ai/code)
[![AgentSkills](https://img.shields.io/badge/AgentSkills-Standard-green)](https://agentskills.io)

<br>

妈妈有智慧，那些没有任何书能教的东西 ——
她耐心的解释，她温柔的纠正，
她记得的每一个家庭故事，
她从不写下来的食谱，
还有当你最需要时，她声音里的温暖。

**保留她的声音，她的智慧，她的爱 —— 欢迎加入赛博永生！**

<br>

提供原材料（聊天记录、邮件、语音、照片、手写笔记）
加上你对她的记忆，
生成一个**承载她灵魂的 AI Skill**

[支持的数据来源](#支持的数据来源) · [安装](#安装) · [使用](#使用) · [效果示例](#效果示例) · [详细安装说明](INSTALL.md)

[**English**](README_EN.md) · [**中文**](README_ZH.md)

</div>

---

## 支持的数据来源

| 来源 | 说明 |
|------|------|
| 微信聊天记录 | SQLite 格式导出，自动解析 |
| 家庭群聊记录 | 提取妈妈的发言风格 |
| 短信 / 邮件 | 文字对话记录 |
| 语音转文字 | 录音文件转文本 |
| 照片 / 手写笔记 | OCR 识别 + 图像描述 |
| 直接粘贴文字 | 手动输入 |
| PDF 文档 | 家庭照片、扫描件 |

---

## 安装

```bash
git clone https://github.com/yahao333/mama.skill ~/.claude/skills/mama
```

### 依赖

```bash
pip3 install -r requirements.txt
```

---

## 使用

在 Claude Code 中输入：

```
/mama
```

按提示提供关于妈妈的信息和原材料，生成一个保留她声音和智慧的 Skill。

### 管理命令

| 命令 | 说明 |
|------|------|
| `/mama` | 调用妈妈 Skill 创建器 |
| `/list-mamas` | 列出所有已创建的妈妈 Skill |
| `/delete-mama {slug}` | 删除指定妈妈 Skill |

---

## 效果示例

> 输入：`退休教师，60岁，温柔但严格，特别擅长讲人生道理，喜欢用故事教育人，做的红烧肉是一绝`

**场景一：遇到困难**

```
用户      ❯ 我工作好累，感觉坚持不下去了

mama.skill ❯ 累了就休息一下嘛，身体是革命的本钱。
             你还记得你小时候学骑车吗？摔了多少次，
             但你就是不肯放弃，最后不也学会了吗？
             慢慢来，妈妈相信你。
```

**场景二：请教做饭**

```
用户      ❯ 红烧肉怎么做才软烂入味？

mama.skill ❯ 选五花肉，要带皮的。
             先焯水去腥，然后小火慢炒，
             加冰糖上色，生抽老抽各适量，
             最重要的是——要有耐心，小火炖至少一个小时。
             对了，炒糖色的时候别急，别糊了。
```

---

## 项目结构

```
mama.skill/
├── SKILL.md              # Skill 入口
├── prompts/              # Prompt 模板
├── tools/                # Python 工具
├── moms/                 # 生成的妈妈 Skill（gitignored）
│   └── {slug}/
│       └── SKILL.md     # 生成的子技能
└── LICENSE
```

---

<div align="center">

MIT License © [yahao333](https://github.com/yahao333)

</div>
