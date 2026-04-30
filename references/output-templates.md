# Output Templates

Use these files as working artifacts inside the target project directory.

## decisions.md

```markdown
# Design Decisions

- Entry mode:
- Region:
- City:
- Vibe/Era:
- Niche:
- Pages:
- Major page roles:
- Image placeholders:
- Sub-agent delegation plan (optional):

## Demo Uniqueness Audit

- Previous-work audit:
- Recurring traits to avoid:
- Shell-ban list:
- Primary composition family:
- Why this family differs from the most recent output:
- Wireframe-level uniqueness test:

## Research Notes

### Research Boundary
- City research is observational input, not a spec:
- What is being translated into web language:
- What must not be flattened into product-template logic:

### Research Sources
- Local Food / Vibe:
- Local Soundscape / Artist:
- Vibrant Culture:
- Secondary analysis:
- Niche source 1:
- Niche source 2:

### City Palette
- Primary:
- Secondary:
- Accent:
- Shadow:
- Text:

### City Signatures
1.
2.
3.

### Urban Translation Notes
- Framing (Architecture):
- Rhythm (Music/Soundscape):
- Texture (Food/Material):
- Lighting (Atmosphere):
- Space:
- What should stay ambiguous or restrained:

### Niche References
- URL:
- URL:

### Reference Decomposition
- Reference A contributes:
- Reference B contributes:
- Reference C contributes:
- What will not be copied:

### Optional Reference Site Analysis
- Section map:
- Interaction inventory:
- Background techniques:
- Color and type cues:
```

## storyboard.md

```markdown
# Urban Treatment

## Urban Brief
- Visual thesis:
- Signature technique 1:
- Signature technique 2:
- Signature technique 3:
- Motion rules:
- Typography rules:

## Site Urban Grammar
- Page-shell logic:
- Navigation posture:
- Framing discipline:
- Density cadence:
- Recurring material layers:
- Allowed composition families:
- What may repeat:
- What must vary page to page:
- Demo uniqueness guardrail:

## District Arc

### Page: Home
- Page-role district:
- Page district thesis:
- One big idea:
- Hero dominance statement:
- Restraint statement:
- Material thesis:
- Typography thesis:
- Narrative arc:
- Hero archetype:
- Signature composition:
- Grid fallback test:
- Shared system holdback:
- UI exposure guardrail:
- What this page must not inherit from previous demos:
- Section sequence:

### District 1
- Beat:
- Function:
- Archetype:
- Composition ref:
- Flow ref:
- Interaction ref:
- Visual elements:
- Why this exists:
```

## compiled-spec.md

```markdown
# Compiled Spec

## Page: Home
- Page district thesis:
- Signature composition:
- Signature composition source id:
- Why this cannot collapse into a default grid:
- One big idea:
- Heavy interaction:
- Heavy interaction source id:
- Showy reveals:
- Showy reveal source id(s):
- Restraint notes:
- Typography source id(s):
- Atmosphere/background source id(s):

## Entrance Map
- District 1:
- District 2:
- District 3:
- District 4:

### District 1
- Beat:
- Function:
- Archetype:
- Entrance:
- Flow source id:
- Interaction:
- Interaction source id:
- Composition source id:
- Visual element source id(s):
- Typography source id(s):
- Background/texture source id(s):

```css
/* layout */
/* entrance */
/* interaction */
```

```html
<!-- structure hint -->
```

```js
// include only if the chosen interaction requires JS
```

## External Library Decision

### Q1: What is the core motion experience of this page?
- 

### Q2: Can the native library entries do it?
- 

### Q3: If an external library is used, why this one and how will it be redirected through the chosen urban language?
- 

### Decision
- 

## Shared System
- Navigation:
- Footer:
- Spacing rhythm:
- Typography system:
- Utility primitives:
- Repeated motifs allowed only after page compositions are locked:
- Uniqueness check against previous demos:

## Phase 3 Quality Check
- [ ] Every section has complete layout CSS
- [ ] Every section has complete entrance behavior
- [ ] Every section has complete interaction behavior or intentional `none`
- [ ] JS-required effects include complete JS
- [ ] Entrance variety rules pass
- [ ] `fadeUp` appears at most 2 times on the page
- [ ] External Library Decision block is complete
- [ ] Library source ids are present for all major visual moves

## Derived Global Tokens
```css
:root {
  --bg: #000000;
  --text: #f3f3f3;
  --accent: #d4a35f;
  --radius-card: 8px;
  --transition-fast: 0.35s;
  --transition-slow: 1s;
  --ease: cubic-bezier(0.22, 1, 0.36, 1);
}
```
```
