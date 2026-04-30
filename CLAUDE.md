# CLAUDE.md

Project memory for Claude Code.

## Purpose

This repository ships a reusable Skill named `urban-experience-layout`.

Its purpose is to help AI agents create websites with:

- stronger premium design direction
- better rhythm, spatial composition, and lighting logic
- less repetition across multiple demos
- a city + vibe based research-and-translation workflow rather than generic luxury prompting

## Read First

- [README.md](./README.md)
- [SKILL.md](./SKILL.md)

## Installation

**Windows:**
```powershell
git clone https://github.com/AbhijeetBabar-2025/urban-experience-ui "$env:USERPROFILE\.claude\skills\urban-experience-layout"
```

**macOS / Linux:**
```bash
git clone https://github.com/AbhijeetBabar-2025/urban-experience-ui ~/.claude/skills/urban-experience-ui
```

Then invoke with `/urban-experience-ui` inside Claude Code.

## Claude Notes

- Treat this repo as a skill package, not as a normal app repo.
- If editing skill logic, keep `SKILL.md` concise and push details into `references/`.
- If changing workflow rules, sync the templates and guardrails in:
  - `references/output-templates.md`
  - `references/premium-calibration.md`
  - `references/anti-garbage.md`
- Preserve `Demo Uniqueness Protocol`.
- Every invocation must complete the start questionnaire before Phase 1.
- When web access is available, research the chosen city, local food, and local soundscape (artist/genre) before locking Phase 1.
- Treat the city as urban research, not as a spec sheet. Formalize only the web translation artifacts.
- Do not collapse this project into a generic “high-end website prompt”.

## Design Intent

The core pain point this project addresses:

AI website outputs often fail at:

- pacing
- space
- light
- hierarchy
- premium restraint
- cross-demo uniqueness

This skill solves those through a structured, artifact-based workflow.

Important boundary:

The city is not the computer workflow. The city is the source material. The computer-operable workflow starts when the agent turns that research into `decisions.md`, `storyboard.md`, `compiled-spec.md`, and implementation.
