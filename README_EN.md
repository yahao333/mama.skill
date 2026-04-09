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
the stories she remembered about every family member,
the recipes she never wrote down,
and the warmth in her voice when you needed it most.

**Preserve her voice, her wisdom, her love — welcome to cyber-immortality!**

<br>

Provide source materials (chat logs, emails, voice recordings, photos, handwritten notes)
plus your memories of her,
and get an **AI Skill that carries her essence**

[Supported Sources](#supported-data-sources) · [Install](#install) · [Usage](#usage) · [Demo](#demo) · [Detailed Install](INSTALL.md)

[**English**](README_EN.md) · [**中文**](README_ZH.md)

</div>

---

## Supported Data Sources

| Source | Description |
|--------|-------------|
| WeChat chat history | SQLite export, auto-parsed |
| Family group chats | Extract mom's speaking style |
| SMS / Emails | Text conversation records |
| Voice recordings | Audio to text transcription |
| Photos / Handwritten notes | OCR + image description |
| Paste text directly | Manual input |
| PDF documents | Family photos, scanned documents |

---

## Install

### Claude Code

```bash
# Run at git repo root
mkdir -p .claude/skills
git clone https://github.com/yahao333/mama.skill .claude/skills/mama

# Or install globally
git clone https://github.com/yahao333/mama.skill ~/.claude/skills/mama
```

### Dependencies

```bash
pip3 install -r requirements.txt
```

---

## Usage

In Claude Code, type:

```
/mama
```

Follow the prompts to provide information and materials about your mother.
Generate a Skill that preserves her voice and wisdom.

### Commands

| Command | Description |
|---------|-------------|
| `/mama` | Invoke full Skill |
| `/mama-warmth` | Warmth and encouragement mode |
| `/mama-wisdom` | Life wisdom mode |
| `/mama-recipe` | Cooking Q&A mode |

---

## Demo

> Input: `Retired teacher, 60 years old, gentle but strict, great at teaching life lessons through stories, her braised pork is legendary`

**Scenario 1: Facing Difficulties**

```
User         ❯ I'm so tired from work, I feel like I can't go on

mama.skill   ❯ Tired? Then rest. Health comes first.
              Do you remember learning to ride a bike as a child?
              You fell so many times, but you never gave up.
              And you learned in the end, didn't you?
              Take your time. Mom believes in you.
```

**Scenario 2: Asking About Cooking**

```
User         ❯ How do you make braised pork that's tender and flavorful?

mama.skill   ❯ Use pork belly with the skin on.
              First blanch to remove impurities, then sauté on low heat.
              Add rock sugar for color, light and dark soy sauce as needed.
              Most importantly — be patient. Simmer on low for at least an hour.
              Oh, and don't rush the sugar — don't let it burn.
```

---

## Project Structure

```
mama.skill/
├── SKILL.md              # Skill entry point
├── prompts/              # Prompt templates
│   ├── intake.md        #   Info collection
│   ├── wisdom_analyzer.md # Wisdom extraction
│   ├── warmth_analyzer.md # Warmth style extraction
│   ├── story_builder.md #   Story generation
│   ├── recipe_analyzer.md # Recipe extraction
│   └── warmth_builder.md # Warm response generation
├── tools/               # Python tools
│   ├── wechat_parser.py      # WeChat parser
│   ├── voice_transcriber.py  # Voice transcription
│   ├── ocr_reader.py         # OCR recognition
│   └── recipe_extractor.py   # Recipe extraction
├── moms/                # Generated mama Skills
├── docs/
├── requirements.txt
└── LICENSE
```

---

## Notes

- **Source quality determines Skill quality**: Voice + handwritten notes > Chat logs > Description only
- Prioritize: Stories **she told** > Experience **she shared in groups** > Daily chat
- WeChat export tools: [WeChatMsg](https://github.com/LC044/WeChatMsg) (Windows)

---

<div align="center">

MIT License © [yahao333](https://github.com/yahao333)

</div>
