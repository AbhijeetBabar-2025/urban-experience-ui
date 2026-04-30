# Anti-Convergence System

## Soundscape Selection — Reasoning Requirement

The failure mode is not picking the wrong music. The failure mode is **picking an artist through association instead of analysis**.

Association: niche is "tech startup" → Daft Punk comes to mind → recommend it.
Analysis: what specific sonic texture, tempo, rhythmic layering, and frequency range does this niche need? Which album or track in this artist's catalog contains those qualities most precisely?

**Before committing to any artist or track, answer these three questions:**

1. **What specific visual problem does this artist or track solve for this niche?**
   Name a concrete sonic or rhythmic trait — not "it feels premium" or "it has a cool vibe." Something like: "Steve Reich's *Music for 18 Musicians* uses interlocking repetitive phases and slow harmonic shifts that match this financial data platform's need for precision and patient complexity."

2. **Would this same music work equally well for three unrelated niches?**
   If yes, the selection is too generic. An artist that "works for any premium brand" is not a creative choice — it is a mood board. Pick music that fits this niche specifically because of its internal structure, not because of its genre.

3. **Are you picking the artist or picking the artist's reputation?**
   Artists that are heavily discussed in high-fashion or tech culture carry a reputation bias. If your reasoning relies on that reputation ("everyone knows Kraftwerk has a mechanical, clean aesthetic") rather than on specific rhythmic patterns, sound design, or structural decisions — that is association, not analysis. Rebuild the justification from the music itself.

If any answer is unsatisfactory, choose a different artist or soundscape before proceeding to decisions.md.

Use this during Phase 2 when choosing hero archetypes, narrative arcs, and section archetypes.

The goal is to stop the agent from drifting toward the same shell, the same rhythm, or the same section logic across repeated projects or across multiple pages in the same site.

## Hash-Based Selection

When a library offers multiple soundscape-compatible options, do not always pick the first or most obvious one.

- Build a music-compatible pool first.
- Use a stable site-name hash as the starting position.
- Walk the pool from that position, skipping entries that violate page-role or uniqueness constraints.

## Minimum Rules

- Hero archetype: choose from Tier 1 and Tier 2 city-fit pools, then select via site-name hash.
- Narrative arc: select the city's default or variant arc via hash, not personal agent preference.
- Section archetype: choose via city pool plus hash, then apply page-role constraints.

## Cross-Page Anti-Convergence

For multi-page sites:

- The same function type should prefer a different archetype on different pages.
- The same archetype id may appear at most 2 times across the whole site, excluding footer-like repeats.
- Add page index offset to the site hash so each page starts at a different pool position.
- If two pages still converge, the lower-priority page must re-roll within the same city-compatible pool.

## Required Checks

Before Phase 2 is complete, confirm:

- Beat sequence matches the city's template instead of generic marketing flow.
- Beat count fits the city's typical range.
- Every section has a camera reference and an interaction reference, or an intentional `none`.
- At least 2 sections per page are structurally different from default marketing layouts.
- The homepage and interior pages do not reuse the same shell with only superficial changes.
