# CET-6 Writing Coach · A Claude Skill

> A Claude Skill that coaches Chinese college students on the **CET-6 essay** —
> built to push scores past **130/710** (essay band 13+/15).
> Drop the platitudes ("read more, write more"), get line-level edits on **your** essay.

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Skill](https://img.shields.io/badge/Claude-Skill-orange.svg)](#-install)
[![中文](https://img.shields.io/badge/lang-中文-red.svg)](README.md)

> Note: this Skill is **Chinese-facing by design** — its dialogue, triggers and
> rubrics are written for Chinese learners. The references and edits are in
> English, but the coaching voice is Chinese. This README is provided so
> non-Chinese readers can understand the project.

---

## What it is

A prompt Skill for **College English Test Band 6 (CET-6) writing** in mainland
China. Once installed in Claude (Cowork or Claude Code), it auto-activates on
Chinese keywords like *六级作文 / 批改 / 升级 / 虚拟语气 / 论证不深 / 思辨* and
runs as a virtual examiner-coach.

**Assumed user**: a Chinese undergrad who can write ~150–200 words but is
stuck around band 8–10/15, with symptoms like opening "Nowadays...", overusing
*important / good / many*, flat argumentation, Chinglish phrases.

## What it does

| Mode | Triggered by | Output |
|---|---|---|
| **Grade & revise** | Pasted essay | Band score + 4-color annotations + minor-fix version + score-pushing rewrite + ONE top weakness |
| **Brief & outline** | Prompt only | Prompt analysis → 3 thesis angles (safety/mainstream/standout) → 3-paragraph skeleton |
| **Sentence upgrade** | A flat sentence | Low/mid/high three-tier rewrite |
| **Diction swap** | "What's a better word for X" | Register + collocation + scenario (not synonyms) |
| **Write from scratch** | "Write one for me" | Pushes back first, then writes annotated model |

**Precision-strike six tactics** (v1.1): verb upgrade, adjective stripping,
noun collocation, long-sentence info packing, short-sentence punch, depersonalised
(物称) subjects.

**Reference arsenal**: subjunctive, inversion, absolute constructions, noun
clauses, relative clauses, PEEL→PEEAL-CR, Toulmin triangle, 12 logical
fallacies, steel-manning, critical-thinking toolkit.

## Install

### Cowork (drag-and-drop)
1. Download `cet6-writing-coach.skill` from [Releases](../../releases)
2. Drop it into Claude Cowork chat
3. Click "Save skill"

### Claude Code (manual)
```bash
git clone https://github.com/<YOUR_USERNAME>/cet6-writing-coach.git
cp -r cet6-writing-coach ~/.claude/skills/
```

## Repo layout
```
SKILL.md                  Main entry (5 modes + 6 precision tactics + tier-gated grammar)
references/               Detailed arsenals (11 files, loaded on demand)
examples/                 Real coaching transcripts
```

## Contributing
PRs welcome — see [CONTRIBUTING.md](CONTRIBUTING.md). New collocations, fresh
real-exam topics, and bug reports are especially appreciated.

## License
[MIT](LICENSE) © 2026 Herry
