# Urban Experience UI


<p align="center">
  A cross-agent skill for designing websites using a city-and-vibe research workflow.
</p>


<p align="center">
  <a href="https://opensource.org/licenses/MIT"><img src="https://img.shields.io/badge/License-MIT-cb9b6b?style=for-the-badge&labelColor=17120f" alt="MIT License"></a>
  <a href="./CLAUDE.md"><img src="https://img.shields.io/badge/Claude%20Code-Supported-a9784b?style=for-the-badge&labelColor=17120f" alt="Claude Code"></a>
</p>

---

## What It Is

**Urban Experience UI** is an advanced, reasoning-first **Claude Code skill** designed to power **agentic web design** workflows. Instead of relying on generic templates, it empowers AI agents to think like an urban architect. It guides the AI through a structured workflow for generative UI and frontend development:

1. Pick a famous city and a specific vibe/era
2. Research that city's visual language (architecture, lighting, street rhythm, material)
3. Translate the research into web artifacts: `decisions.md`, `storyboard.md`, `compiled-spec.md`
4. Implement HTML / CSS / JS from the spec

The city is research input, not a spec sheet. The agent's job is to extract structural patterns from urban environments and translate them into layout, composition, motion, and typography.

---

## Workflow

| Phase | Work | Output |
|-------|------|--------|
| Phase 1 | Start questionnaire, choose city + vibe, uniqueness audit, research | `decisions.md` |
| Phase 2 | Site-wide urban grammar, per-page district thesis, signature composition | `storyboard.md` |
| Phase 3 | Flow, interaction, composition, texture, typography per storyboard | `compiled-spec.md` |
| Phase 4 | Implement, add reduced-motion + responsive, run anti-garbage checks | HTML / CSS / JS |

Phase 2 internal order is fixed: site-wide grammar → per-page thesis → per-page composition → shared system.

---

## Installation

**Windows:**
```powershell
git clone https://github.com/AbhijeetBabar-2025/urban-experience-ui "$env:USERPROFILE\.claude\skills\urban-experience-ui"
```

**macOS / Linux:**
```bash
git clone https://github.com/AbhijeetBabar-2025/urban-experience-ui ~/.claude/skills/urban-experience-ui
```

Invoke with `/urban-experience-ui` inside Claude Code.


## Suggested Prompt

```text
Use urban-experience-ui to build a homepage.
Pick the city and vibe yourself.
Research the city and vibe first if web access is available.
Run the Demo Uniqueness Protocol.
Do not reuse shells from previous demos.
```

---

## References Library

All reference data lives in `references/`, organized by phase. Load only what the current phase needs.

### Core Rule Files

| File | Purpose |
|------|---------|
| [`references/library-index.md`](./references/library-index.md) | Which files to read per phase |
| [`references/premium-calibration.md`](./references/premium-calibration.md) | Self-check after urban brief |
| [`references/anti-garbage.md`](./references/anti-garbage.md) | Common AI design degradation patterns |
| [`references/anti-convergence.md`](./references/anti-convergence.md) | Hash-based selection to prevent repeated shells |
| [`references/implementation-guardrails.md`](./references/implementation-guardrails.md) | Phase 3–4 build rules |
| [`references/reference-protocol.md`](./references/reference-protocol.md) | How to decompose a reference site without copying |
| [`references/output-templates.md`](./references/output-templates.md) | Standard format templates per phase |

### Data Libraries

| File | Contents |
|------|---------|
| `references/data/cities.md` | Famous cities with architectural and visual style |
| `references/data/hero-archetypes.md` | 30 hero skeletons |
| `references/data/narrative-beats.md` | 25 narrative beats + 18 urban arc templates |
| `references/data/section-functions.md` | 50 functional section types |
| `references/data/section-archetypes.md` | 91+ section skeletons |
| `references/data/dna-index.tsv` | Design DNA index of 1,486 sites |
| `references/data/design-dna-db.txt` | Site-level DNA data |
| `references/data/urban-flow-50.md` | 55 entrance and reveal behaviors |
| `references/data/interaction-effects-50.md` | 55+ hover / click / scroll interactions |
| `references/data/compositions.md` | 80 layout compositions |
| `references/data/visual-elements.md` | 40 visual decoration elements |
| `references/data/background-techniques.md` | 50+ hero background techniques |
| `references/data/typography-urban.md` | 40+ text treatments |
| `references/data/color-grades.md` | 40+ city palette to UI token translations |
| `references/data/font-moods.md` | 30+ font pairings by tone |
| `references/data/textures.md` | 30+ surface techniques |

---

## Repository Structure

```text
urban-experience-ui/
├── SKILL.md                        ← main skill logic
├── skill.json                      ← universal skill manifest
├── CLAUDE.md                       ← Claude Code
├── docs/                           ← banner, demo assets
└── references/
    ├── library-index.md
    ├── premium-calibration.md
    ├── anti-garbage.md
    ├── anti-convergence.md
    ├── implementation-guardrails.md
    ├── reference-protocol.md
    ├── output-templates.md
    └── data/                       ← 18 design data libraries
```

---

## Contributing

See [CONTRIBUTING.md](./CONTRIBUTING.md).

## License

MIT. See [LICENSE](./LICENSE).

---

## Topics & Keywords

`claude-code` `claude-skill` `ai-agent` `agentic-workflow` `web-design` `generative-ui` `frontend-development` `city-inspired-design` `urban-experience` `design-system` `ui-framework` `layout-engine` `storyboard` `ux` `reasoning-skill` `anthropic` `mcp`
