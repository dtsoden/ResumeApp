# Resume Tailor

**A free desktop app that tailors your résumé for any job, locally on your machine.**

[![Latest Release](https://img.shields.io/github/v/release/dtsoden/ResumeApp?label=Latest&color=blue)](https://github.com/dtsoden/ResumeApp/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/dtsoden/ResumeApp/total?label=Total%20Downloads&color=success)](https://github.com/dtsoden/ResumeApp/releases)
[![License](https://img.shields.io/badge/License-PolyForm%20Noncommercial%201.0.0-blue.svg)](#license)
[![Platforms](https://img.shields.io/badge/Windows-supported-success)](#download)
[![Mac](https://img.shields.io/badge/macOS-supported-success)](#download)

---

## Download

| Platform | File | Status |
|---|---|---|
| **Windows** (x64) | [⬇ Resume Tailor Setup.exe](https://github.com/dtsoden/ResumeApp/releases/latest/download/Resume.Tailor.Setup.exe) | Available |
| **macOS** (Apple Silicon) | [⬇ Resume Tailor-arm64.dmg](https://github.com/dtsoden/ResumeApp/releases/latest/download/Resume.Tailor-arm64.dmg) | Available |
| **macOS** (Intel) | [⬇ Resume Tailor-x64.dmg](https://github.com/dtsoden/ResumeApp/releases/latest/download/Resume.Tailor-x64.dmg) | Available |

> **Always grab the [latest release](https://github.com/dtsoden/ResumeApp/releases/latest)** for new features and fixes.

---

## What it does

You feed Resume Tailor everything about your career, past résumés, LinkedIn excerpts, public profile URLs, Q&A answers about gaps. For each job you apply to, paste the JD and Resume Tailor builds a custom-tailored résumé that matches that job's vocabulary, surfaces the most relevant experience, and scores how well you fit.

Every résumé you generate gets tracked under an Application chain so you can compare drafts, refine them, and keep iterating.

## Why use it

### Your career stays on your machine
- All data lives locally in SQLite. Your résumés, history, applications, AI provider keys.
- No accounts. No telemetry. No analytics. No proxy.
- The app makes calls directly from your machine to whichever AI provider you configure.

### Bring your own AI
- **OpenAI**: GPT-5, GPT-5 Mini, GPT-5 Nano (cheap, fast, ideal default)
- **Anthropic**: Claude Opus, Sonnet, Haiku
- **Google**: Gemini 2.0 / 2.5 Flash + Pro
- **Local**: Ollama or LM Studio for fully offline use

Pay your provider directly. No middleman markup, no monthly subscription.

### Stretch level dial
Choose how aggressively the writer should reframe your background in the JD's vocabulary:

- 🟡 **Conservative**: corpus phrasing as-is. Most defensible at interview.
- 🟢 **Balanced**: JD-vocabulary reframing where defensibly equivalent. Inferred capabilities surfaced with corpus backing.
- 🔴 **Aggressive**: maximum JD keyword density. Liberal alias bridging. Inferred capabilities promoted to Skills.

Fabrication is forbidden at every level. The slider only changes which honest interpretations get surfaced, never invents tools, domains, degrees, certifications, or metrics you don't have.

### Deterministic scoring
Same JD, same résumé text, same score. No more wild swings between regenerations. The app caches the AI's rubric per JD so subsequent generations score against a fixed, transparent rubric.

### Three-tier match classification
Every JD requirement is classified honestly:
- **Literal**: the exact phrase is in your résumé
- **Semantic equivalent**: corpus has the same activity in different vocabulary (DR ↔ Disaster Recovery)
- **Defensible inference**: corpus implies the capability via career trajectory (Director title → ownership; multi-year tenure → strategic vision)
- **Real gap**: genuinely missing, no factual basis

You see the classification for every requirement. The score is auditable: you can read why each item was credited.

### Per-application version chains
Every résumé you generate against a job lands in an Application chain. Refine it. Edit the markdown. Regenerate at a different stretch. Compare versions side-by-side. Prune older drafts to keep the list clean.

### Eligibility-aware
Set your work authorization, W2 eligibility, security clearance, and relocation preference once. The writer only mentions them on a generated résumé when the JD explicitly asks for that category, so you don't volunteer information unnecessarily, but you also don't get filtered out by an ATS looking for "US Citizen".

---

## Key features at a glance

- AI-tailored résumés grounded in your actual career history
- Multi-format ingestion: PDF, DOCX, plain text, URLs, OCR for image-PDFs
- Editable, exportable .docx output
- Conversational refinement ("ask the AI what's missing")
- Surgical, additive bullet insertion (chat-to-refine)
- Profile builder with auto-rebuild
- Application tracker with status, notes, deadlines
- Markdown editor for hands-on tweaks
- Light + dark theme, custom accent color, custom app name
- Bundled OCR (Tesseract) for image-only PDFs
- 100% offline once installed (with local AI provider)

---

## System requirements

| | Minimum |
|---|---|
| OS | Windows 10 or later (x64), or macOS 11 Big Sur or later (Intel or Apple Silicon) |
| RAM | 4 GB |
| Disk | 600 MB for app + your data |
| Internet | Only for cloud AI providers; not required with Ollama / LM Studio |

---

## Privacy

Your data lives at:
- **Windows**: `%APPDATA%\Roaming\Resume Tailor\`
- **macOS**: `~/Library/Application Support/Resume Tailor/`

Inside that folder:
- `sqlite/app.db`: your career data, applications, settings
- `storage/`: your uploaded files and generated résumés
- `logs/`: local app logs

**Nothing is ever sent anywhere except to the AI provider you configure**, and that connection goes from your machine directly to the provider. Resume Tailor does not proxy or log your AI traffic.

Your data is preserved across uninstall and reinstall. To completely remove it, delete the data folder above.

---

## License

**PolyForm Noncommercial 1.0.0**, free for personal, hobby, research, education, and other noncommercial use.

Companies may not repackage, resell, or use Resume Tailor for any commercial purpose.

This is a *source-available* license. Commercial licensing is available on request, open a GitHub issue or contact the maintainer.

---

## Support & feedback

Found a bug? Have a feature request? [Open an issue](https://github.com/dtsoden/ResumeApp/issues).

---

Copyright (c) 2026 David Soden.
