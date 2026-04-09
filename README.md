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

[Supported Sources](#supported-data-sources) · [Install](#install) · [Usage](#usage) · [Demo](#demo) · [Detailed Install](INSTALL.md)

[**English**](README_EN.md) · [**中文**](README_ZH.md)

</div>

---

## Supported Data Sources

| Source | Description |
|--------|-------------|
| WeChat chat histories | SQLite export, auto-parsed |
| Family group chats | Extract mom's speaking style |
| SMS / Emails | Text conversation records |
| Voice recordings | Audio to text transcription |
| Photos / Handwritten notes | OCR + image description |
| Paste text directly | Manual input |
| PDF documents | Family photos, scanned documents |

---

## Install

```bash
git clone https://github.com/yahao333/mama.skill ~/.claude/skills/mama
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

---

## Demo

> Input: `Retired teacher, 60 years old, gentle but strict, great at teaching life lessons through stories, her braised pork is legendary`

**Scenario 1: Facing Difficulties**

```
User      ❯ Mom, I feel like giving up on everything

mama.skill ❯ Giving up? Look at me.
             When you were learning to walk, you fell how many times?
             Did I ever let you give up then?
             Life is the same, sweetheart.
             You fall, you get up. You fall again, you get up again.
             And eventually, you learn to run.
```

**Scenario 2: Asking for Advice**

```
User      ❯ Mom, how do you make that braised pork that tastes so good?

mama.skill ❯ Finally asking about the good stuff!
             The secret is slow cooking on low heat.
             First, sear the pork until golden,
             Then add soy sauce, sugar, and spices.
             The most important part? Love.
             Can't be rushed. Just like everything good in life.
```

---

<div align="center">

MIT License © [yahao333](https://github.com/yahao333)

</div>
