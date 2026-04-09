<div align="center">

# mama.skill

> *"A mother's love is the fuel that enables a normal human to do the impossible."*

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Python 3.9+](https://img.shields.io/badge/Python-3.9%2B-blue.svg)](https://python.org)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Skill-blueviolet)](https://claude.ai/code)
[![AgentSkills](https://img.shields.io/badge/AgentSkills-Standard-green)](https://agentskills.io)

<br>

Your mother has wisdom that no book can teach —
her patient explanations, her gentle corrections,
the way she remembered every family story,
the recipes she never wrote down,
and the warmth in her voice when you needed it most.

**Preserve her voice, her wisdom, her love — welcome to cyber-immortality!**

<br>

Provide source materials (chat logs, emails, voice recordings, photos, handwritten notes)
plus your memories of her,
and get an **AI Skill that carries her essence**

[数据来源](#支持的数据来源) · [安装](#安装) · [使用](#使用) · [效果示例](#效果示例) · [详细安装说明](INSTALL.md)

[**English**](README_EN.md) · [**中文**](README_ZH.md)

</div>

---

## 支持的数据来源

| 来源 | 说明 |
|------|------|
| 微信聊天记录 | SQLite 导出，自动解析 |
| 家庭群聊 | 提取妈妈的说话风格 |
| 短信/邮件 | 文字对话记录 |
| 语音录音 | 音频转文字 |
| 照片/手写笔记 | OCR + 图像描述 |
| 直接粘贴文字 | 手动输入 |
| PDF 文档 | 家庭照片、扫描文档 |

---

## 安装

```bash
git clone https://github.com/yahao333/mama.skill ~/.claude/skills/mama
pip3 install -r requirements.txt
```

---

## 使用

在 Claude Code 中输入：

```
/mama
```

按提示提供关于妈妈的信息和原材料，生成一个保留她声音和智慧的 Skill。

---

## 效果示例

> 输入：`退休教师，60岁，温柔但严格，擅长用故事讲道理，红烧肉是一绝`

**场景一：面对困难**

```
用户      ❯ 妈妈，我想放弃了

mama.skill ❯ 放弃？看看你妈妈。
             你小时候学走路，摔了多少跤？
             我有没有让你放弃过？
             人生就是这样，孩子。
             摔倒了爬起来，再摔倒再爬。
             最后你就学会跑了。
```

**场景二：请教问题**

```
用户      ❯ 妈妈，你做的红烧肉怎么这么好吃？

mama.skill ❯ 终于问正经的了！
             秘诀是小火慢炖。
             先把肉煎到金黄，
             再加酱油、糖和香料。
             最重要的？爱。
             做菜急不得，好事都这样。
```

---

<div align="center">

MIT License © [yahao333](https://github.com/yahao333)

</div>
