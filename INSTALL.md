# 妈妈.skill 安装说明

---

## 选择你的平台

### A. Claude Code（推荐）

本项目遵循官方 [AgentSkills](https://agentskills.io) 标准，整个 repo 就是 skill 目录。克隆到 Claude skills 目录即可：

```bash
# ⚠️ 必须在 git 仓库根目录执行！
cd $(git rev-parse --show-toplevel)

# 方式 1：安装到当前项目
mkdir -p .claude/skills
git clone https://github.com/yahao333/mama.skill .claude/skills/mama

# 方式 2：安装到全局（所有项目都能用）
git clone https://github.com/yahao333/mama.skill ~/.claude/skills/mama
```

---

### 依赖安装

```bash
# 基础（Python 3.9+）
pip3 install pypinyin        # 中文姓名转拼音 slug（可选但推荐）

# 图片 OCR（手写笔记、照片）
pip3 install playwright
playwright install chromium

# 语音转文字（需要 ffmpeg）
# macOS: brew install ffmpeg
# Ubuntu: sudo apt install ffmpeg

# 微信解析
pip3 install python-docx openpyxl
```

---

## 快速开始

### 1. 导出微信聊天记录

**Windows 用户**：
推荐使用 [WeChatMsg](https://github.com/LC044/WeChatMsg) 导出聊天记录。

**macOS 用户**：
推荐使用 [留痕](https://github.com/greyovo/留痕) 导出聊天记录。

### 2. 收集其他材料

- 妈妈发在家庭群里的消息
- 短信、邮件记录
- 语音录音（微信语音条可长按导出）
- 照片（含手写文字、菜谱）
- PDF 文档（扫描件）

### 3. 创建妈妈 Skill

在 Claude Code 中输入：

```
/mama
```

按提示操作即可。

---

## 目录结构说明

```
mama.skill/        ← clone 到 .claude/skills/mama/
├── SKILL.md            # skill 入口
├── prompts/            # Prompt 模板
├── tools/              # Python 工具脚本
├── moms/               # 生成的妈妈 Skill（gitignored）
│   └── {slug}/
│       ├── SKILL.md
│       ├── warmth.md   # 温暖风格
│       ├── wisdom.md   # 人生智慧
│       └── recipes.md  # 食谱
└── docs/
```
