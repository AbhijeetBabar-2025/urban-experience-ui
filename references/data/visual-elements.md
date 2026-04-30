# Visual Elements Library

> 40 CSS-ready visual element patterns to enrich the visual hierarchy of the web. All elements use CSS variables and can adapt to any city and cultural palette.

---

## A. Floating Cards & Badges

### #1 Floating Price Card
Category: A — Floating Cards
Urban Flow Fit: General (adapt colors/radius to director)

> Small UI card showing price or feature summary, floating next to the hero content

```html
<div class="float-card" style="--float-x:65%;--float-y:20%;">
  <span class="float-card-icon">💎</span>
  <strong>Pro Plan</strong>
  <span class="float-card-detail">From $29/mo</span>
</div>
```

```css
.float-card {
  position: absolute;
  left: var(--float-x); top: var(--float-y);
  padding: 0.75rem 1.2rem;
  background: var(--bg-surface);
  border: 1px solid var(--border);
  border-radius: var(--radius-card);
  backdrop-filter: blur(12px);
  display: flex; align-items: center; gap: 0.6rem;
  font-size: 0.8rem;
  animation: float-gentle 6s ease-in-out infinite;
}
@keyframes float-gentle {
  0%,100%{transform:translateY(0)} 50%{transform:translateY(-8px)}
}
```

---

### #2 Notification Badge
Category: A — Floating Cards
Urban Flow Fit: Tarantino, Guy Ritchie, Edgar Wright

> Attention-grabbing small badge for "NEW", "HOT", "BETA" labels

```html
<div class="notif-badge" style="--badge-x:80%;--badge-y:10%;">
  <span class="notif-pulse"></span>
  NEW
</div>
```

```css
.notif-badge {
  position: absolute;
  left: var(--badge-x); top: var(--badge-y);
  padding: 0.3rem 0.8rem;
  background: var(--accent);
  color: var(--bg);
  font-size: 0.65rem; font-weight: 700; letter-spacing: 0.1em;
  border-radius: 999px;
}
.notif-pulse {
  position: absolute; inset: -3px;
  border-radius: inherit;
  border: 2px solid var(--accent);
  animation: pulse-ring 2s ease-out infinite;
}
@keyframes pulse-ring {
  to { transform:scale(1.4); opacity:0 }
}
```

---

### #3 Testimonial Mini Card
Category: A — Floating Cards
Urban Flow Fit: Wong Kar-wai, Sofia Coppola, Wes Anderson

> Floating small testimonial card with avatar and quote

```html
<div class="mini-testimonial" style="--mt-x:70%;--mt-y:60%;">
  <img src="avatar.jpg" alt="" class="mt-avatar">
  <p class="mt-quote">"Changed everything."</p>
  <span class="mt-name">— Sarah K.</span>
</div>
```

```css
.mini-testimonial {
  position: absolute;
  left: var(--mt-x); top: var(--mt-y);
  max-width: 200px; padding: 1rem;
  background: var(--bg-surface);
  border: 1px solid var(--border);
  border-radius: var(--radius-card);
  backdrop-filter: blur(16px);
  font-size: 0.75rem;
}
.mt-avatar {
  width: 28px; height: 28px; border-radius: 50%;
  object-fit: cover; margin-bottom: 0.5rem;
}
.mt-quote { font-style: italic; color: var(--text-muted); }
```

---

### #4 Feature Chip Stack
Category: A — Floating Cards
Urban Flow Fit: Documentary, Ridley Scott

> A set of small feature chips arranged next to the hero content to express product characteristics

```html
<div class="chip-stack" style="--cs-x:5%;--cs-y:40%;">
  <span class="chip">AI Powered</span>
  <span class="chip">99.9% Uptime</span>
  <span class="chip">SOC2</span>
</div>
```

```css
.chip-stack {
  position: absolute;
  left: var(--cs-x); top: var(--cs-y);
  display: flex; flex-direction: column; gap: 0.4rem;
}
.chip {
  padding: 0.35rem 0.75rem;
  background: var(--bg-surface);
  border: 1px solid var(--border);
  border-radius: 999px;
  font-size: 0.7rem; font-weight: 500;
  backdrop-filter: blur(8px);
  white-space: nowrap;
}
```

---

### #5 Floating Metric Card
Category: A — Floating Cards
Urban Flow Fit: Nolan, Fincher, Documentary

> Card showing a single data metric, such as "2M+ Users" or "<50ms Latency"

```html
<div class="metric-float" style="--mf-x:72%;--mf-y:45%;">
  <span class="mf-value">2M+</span>
  <span class="mf-label">Active Users</span>
</div>
```

```css
.metric-float {
  position: absolute;
  left: var(--mf-x); top: var(--mf-y);
  padding: 0.8rem 1.2rem;
  background: var(--bg-surface);
  border: 1px solid var(--border);
  border-radius: var(--radius-card);
  backdrop-filter: blur(12px);
  text-align: center;
}
.mf-value {
  display: block;
  font-size: 1.5rem; font-weight: 800;
  color: var(--accent);
  line-height: 1;
}
.mf-label { font-size: 0.65rem; color: var(--text-muted); }
```

---

### #6 Status Indicator Card
Category: A — Floating Cards
Urban Flow Fit: Fincher, Nolan, Ridley Scott

> Small card showing system status with a pulsing green dot

```html
<div class="status-card" style="--sc-x:8%;--sc-y:15%;">
  <span class="status-dot"></span>
  <span>All Systems Operational</span>
</div>
```

```css
.status-card {
  position: absolute;
  left: var(--sc-x); top: var(--sc-y);
  padding: 0.5rem 1rem;
  background: var(--bg-surface);
  border: 1px solid var(--border);
  border-radius: var(--radius-card);
  backdrop-filter: blur(12px);
  display: flex; align-items: center; gap: 0.5rem;
  font-size: 0.72rem;
}
.status-dot {
  width: 8px; height: 8px;
  background: #22c55e; border-radius: 50%;
  animation: blink 2s ease-in-out infinite;
}
@keyframes blink { 50%{opacity:.4} }
```

---

## B. Geometric Shapes & Accents

### #7 Overlapping Rectangles
Category: B — Geometric Shapes
Urban Flow Fit: Tarantino, Guy Ritchie, Edgar Wright

> Two to three overlapping color blocks behind content for BRUTAL visual impact

```html
<div class="geo-overlap">
  <div class="geo-rect geo-rect--1"></div>
  <div class="geo-rect geo-rect--2"></div>
  <div class="geo-rect geo-rect--3"></div>
</div>
```

```css
.geo-overlap { position: relative; }
.geo-rect {
  position: absolute;
  width: 300px; height: 200px;
  border: 3px solid var(--accent);
}
.geo-rect--1 { top: 0; left: 0; background: var(--accent); opacity: 0.15; }
.geo-rect--2 { top: 30px; left: 40px; background: var(--accent-alt); opacity: 0.1; }
.geo-rect--3 { top: 60px; left: 80px; border-style: dashed; }
```

---

### #8 Corner Brackets
Category: B — Geometric Shapes
Urban Flow Fit: Nolan, Villeneuve, Park Chan-wook

> Delicate L-shaped decorative lines at container corners for a cinematic framing effect

```html
<div class="bracket-frame">
  <div class="bracket-content">
    <!-- content here -->
  </div>
</div>
```

```css
.bracket-frame {
  position: relative; padding: 2rem;
}
.bracket-frame::before, .bracket-frame::after {
  content: '';
  position: absolute;
  width: 30px; height: 30px;
  border-color: var(--accent);
  border-style: solid;
}
.bracket-frame::before { top:0;left:0; border-width:2px 0 0 2px; }
.bracket-frame::after { bottom:0;right:0; border-width:0 2px 2px 0; }
```

---

### #9 Dot Grid Pattern
Category: B — Geometric Shapes
Urban Flow Fit: Wes Anderson, Documentary

> Background dot grid decoration for a layout design or engineering blueprint feel

```html
<div class="dot-grid" aria-hidden="true"></div>
```

```css
.dot-grid {
  position: absolute; inset: 0;
  background-image: radial-gradient(var(--border) 1px, transparent 1px);
  background-size: 24px 24px;
  opacity: 0.4;
  pointer-events: none;
}
```

---

### #10 Cross Marks
Category: B — Geometric Shapes
Urban Flow Fit: Fincher, Nolan, Villeneuve

> Scattered small cross marks to add a technical and precise feel

```html
<div class="cross-mark" style="--cx:20%;--cy:30%;"></div>
<div class="cross-mark" style="--cx:75%;--cy:65%;"></div>
```

```css
.cross-mark {
  position: absolute;
  left: var(--cx); top: var(--cy);
  width: 12px; height: 12px;
}
.cross-mark::before, .cross-mark::after {
  content: ''; position: absolute;
  background: var(--accent); opacity: 0.5;
}
.cross-mark::before { width:100%;height:1px;top:50%; }
.cross-mark::after { height:100%;width:1px;left:50%; }
```

---

### #11 Diagonal Accent Line
Category: B — Geometric Shapes
Urban Flow Fit: Park Chan-wook, Ridley Scott

> A diagonal line across the screen to break the monotony of horizontal composition

```html
<div class="diag-line" aria-hidden="true"></div>
```

```css
.diag-line {
  position: absolute; inset: 0;
  overflow: hidden; pointer-events: none;
}
.diag-line::after {
  content: '';
  position: absolute;
  width: 150%; height: 1px;
  background: linear-gradient(90deg, transparent, var(--accent), transparent);
  top: 50%; left: -25%;
  transform: rotate(-15deg);
  opacity: 0.3;
}
```

---

### #12 Circle Accent
Category: B — Geometric Shapes
Urban Flow Fit: Miyazaki, Shinkai, Wes Anderson

> Large translucent circle decoration to soften the layout and create a focal point

```html
<div class="circle-accent" style="--ca-x:80%;--ca-y:20%;--ca-size:200px;"></div>
```

```css
.circle-accent {
  position: absolute;
  left: var(--ca-x); top: var(--ca-y);
  width: var(--ca-size); height: var(--ca-size);
  border: 2px solid var(--accent);
  border-radius: 50%;
  opacity: 0.2;
  transform: translate(-50%,-50%);
  pointer-events: none;
}
```

---

### #13 Stacked Triangles
Category: B — Geometric Shapes
Urban Flow Fit: Tarantino, Edgar Wright, Guy Ritchie

> Overlapping triangular decorations to add a sense of dynamic energy

```html
<div class="tri-stack" aria-hidden="true">
  <div class="tri tri--1"></div>
  <div class="tri tri--2"></div>
</div>
```

```css
.tri-stack { position: absolute; right: 10%; top: 15%; }
.tri {
  width: 0; height: 0;
  border-left: 40px solid transparent;
  border-right: 40px solid transparent;
  border-bottom: 70px solid var(--accent);
  position: absolute;
}
.tri--1 { opacity: 0.15; }
.tri--2 { opacity: 0.08; transform: translate(20px,10px) rotate(15deg); }
```

---

## C. Gradient Blobs & Atmospheric

### #14 Soft Gradient Blob
Category: C — Gradient Blobs
Urban Flow Fit: Miyazaki, Shinkai, Wong Kar-wai

> Large blurred color sphere to create a warm atmosphere in the background

```html
<div class="grad-blob" style="--gb-x:30%;--gb-y:40%;--gb-c1:var(--accent);--gb-c2:var(--accent-alt);"></div>
```

```css
.grad-blob {
  position: absolute;
  left: var(--gb-x); top: var(--gb-y);
  width: 500px; height: 500px;
  background: radial-gradient(circle, var(--gb-c1), var(--gb-c2), transparent 70%);
  filter: blur(80px);
  opacity: 0.3;
  transform: translate(-50%,-50%);
  pointer-events: none;
}
```

---

### #15 Glass Morphism Panel
Category: C — Gradient Blobs
Urban Flow Fit: General (especially Villeneuve, Nolan)

> Frosted glass effect panel for carrying content while showing background layers

```html
<div class="glass-panel">
  <h3>Feature Title</h3>
  <p>Description text here.</p>
</div>
```

```css
.glass-panel {
  padding: 2rem;
  background: color-mix(in srgb, var(--bg-surface) 60%, transparent);
  backdrop-filter: blur(20px) saturate(1.2);
  border: 1px solid color-mix(in srgb, var(--border) 50%, transparent);
  border-radius: var(--radius-card);
  box-shadow: 0 8px 32px rgba(0,0,0,0.08);
}
```

---

### #16 Aurora Gradient
Category: C — Gradient Blobs
Urban Flow Fit: Shinkai, Miyazaki, Sofia Coppola

> Horizontal aurora effect to create a dreamlike feel at the top or in the background of the page

```html
<div class="aurora" aria-hidden="true"></div>
```

```css
.aurora {
  position: absolute; top: 0; left: 0; right: 0;
  height: 60vh;
  background: linear-gradient(
    135deg,
    color-mix(in srgb, var(--accent) 20%, transparent),
    color-mix(in srgb, var(--accent-alt) 15%, transparent),
    transparent 60%
  );
  filter: blur(60px);
  pointer-events: none;
  animation: aurora-shift 12s ease-in-out infinite alternate;
}
@keyframes aurora-shift {
  to { transform:translateX(5%) scaleY(1.1); opacity:0.7; }
}
```

---

### #17 Light Leak Overlay
Category: C — Gradient Blobs
Urban Flow Fit: Wong Kar-wai, Sofia Coppola

> Simulated film light leak for a vintage and romantic feel

```html
<div class="light-leak" aria-hidden="true"></div>
```

```css
.light-leak {
  position: absolute; inset: 0;
  background: linear-gradient(
    120deg,
    transparent 30%,
    color-mix(in srgb, var(--accent) 12%, transparent) 50%,
    color-mix(in srgb, var(--accent-warm, #ff6b35) 8%, transparent) 70%,
    transparent 90%
  );
  mix-blend-mode: screen;
  pointer-events: none;
  opacity: 0.6;
}
```

---

### #18 Radial Vignette
Category: C — Gradient Blobs
Urban Flow Fit: Fincher, Park Chan-wook, Nolan

> Radial gradient vignette effect on the edges of the frame to focus the viewer's attention

```html
<div class="vignette" aria-hidden="true"></div>
```

```css
.vignette {
  position: absolute; inset: 0;
  background: radial-gradient(
    ellipse at center,
    transparent 50%,
    color-mix(in srgb, var(--bg) 80%, black) 100%
  );
  pointer-events: none;
}
```

---

### #19 Dual Orb Glow
Category: C — Gradient Blobs
Urban Flow Fit: Villeneuve, Ridley Scott

> Two color-intertwined light spheres to create a sci-fi atmosphere

```html
<div class="dual-orb">
  <div class="orb orb--1"></div>
  <div class="orb orb--2"></div>
</div>
```

```css
.dual-orb { position: absolute; inset: 0; pointer-events: none; overflow: hidden; }
.orb {
  position: absolute;
  width: 400px; height: 400px;
  border-radius: 50%;
  filter: blur(100px);
  opacity: 0.25;
}
.orb--1 { background: var(--accent); top: -10%; left: 60%; }
.orb--2 { background: var(--accent-alt); bottom: -10%; left: 20%; }
```

---

### #20 Noise Texture Overlay
Category: C — Gradient Blobs
Urban Flow Fit: Ridley Scott, Fincher, Wong Kar-wai

> SVG noise texture overlay to add film grain or industrial texture

```html
<div class="noise-overlay" aria-hidden="true"></div>
```

```css
.noise-overlay {
  position: absolute; inset: 0;
  background: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence baseFrequency='0.75'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)'/%3E%3C/svg%3E");
  background-size: 128px;
  opacity: 0.04;
  mix-blend-mode: overlay;
  pointer-events: none;
}
```

---

## D. Stats & Data Displays

### #21 Hero Stats Bar
Category: D — Stats & Data
Urban Flow Fit: Documentary, Nolan, Fincher

> Horizontally arranged groups of data, placed at the bottom or below the Hero section

```html
<div class="stats-bar">
  <div class="stat"><span class="stat-val">99.9%</span><span class="stat-lbl">Uptime</span></div>
  <div class="stat"><span class="stat-val">2M+</span><span class="stat-lbl">Users</span></div>
  <div class="stat"><span class="stat-val">&lt;50ms</span><span class="stat-lbl">Latency</span></div>
</div>
```

```css
.stats-bar {
  display: flex; gap: 3rem;
  padding: 1.5rem 0;
  border-top: 1px solid var(--border);
}
.stat-val {
  display: block;
  font-size: 1.8rem; font-weight: 800;
  color: var(--text);
  font-variant-numeric: tabular-nums;
}
.stat-lbl {
  font-size: 0.7rem; color: var(--text-muted);
  text-transform: uppercase; letter-spacing: 0.08em;
}
```

---

### #22 Giant Number
Category: D — Stats & Data
Urban Flow Fit: Tarantino, Edgar Wright, Wes Anderson

> Oversized single number paired with a small label to create a visual anchor

```html
<div class="giant-num">
  <span class="gn-number">47</span>
  <span class="gn-unit">countries served</span>
</div>
```

```css
.giant-num { text-align: center; }
.gn-number {
  display: block;
  font-size: clamp(5rem, 12vw, 10rem);
  font-weight: 900;
  line-height: 0.9;
  color: var(--accent);
  opacity: 0.15;
}
.gn-unit {
  font-size: 0.8rem;
  text-transform: uppercase;
  letter-spacing: 0.15em;
  color: var(--text-muted);
}
```

---

### #23 Progress Ring
Category: D — Stats & Data
Urban Flow Fit: Nolan, Villeneuve, Documentary

> SVG circular progress display to express achievement rate or rating

```html
<div class="progress-ring">
  <svg viewBox="0 0 100 100" class="pr-svg">
    <circle cx="50" cy="50" r="42" class="pr-track"/>
    <circle cx="50" cy="50" r="42" class="pr-fill" style="--progress:75;"/>
  </svg>
  <span class="pr-label">75%</span>
</div>
```

```css
.progress-ring { position: relative; width: 100px; height: 100px; }
.pr-svg { transform: rotate(-90deg); }
.pr-track { fill:none; stroke:var(--border); stroke-width:6; }
.pr-fill {
  fill: none; stroke: var(--accent); stroke-width: 6;
  stroke-linecap: round;
  stroke-dasharray: 264;
  stroke-dashoffset: calc(264 - (264 * var(--progress) / 100));
  transition: stroke-dashoffset 1s ease;
}
.pr-label {
  position: absolute; inset: 0;
  display: grid; place-items: center;
  font-size: 1.2rem; font-weight: 700;
}
```

---

### #24 Comparison Metric
Category: D — Stats & Data
Urban Flow Fit: Documentary, Fincher

> Before-and-after data display to visualize improvement effects

```html
<div class="compare-metric">
  <div class="cm-before"><span class="cm-val">3.2s</span><span class="cm-lbl">Before</span></div>
  <div class="cm-arrow">&rarr;</div>
  <div class="cm-after"><span class="cm-val">0.4s</span><span class="cm-lbl">After</span></div>
</div>
```

```css
.compare-metric {
  display: flex; align-items: center; gap: 1.5rem;
  padding: 1rem 1.5rem;
  background: var(--bg-surface);
  border: 1px solid var(--border);
  border-radius: var(--radius-card);
}
.cm-val { display:block; font-size:1.5rem; font-weight:800; }
.cm-before .cm-val { color: var(--text-muted); text-decoration: line-through; }
.cm-after .cm-val { color: var(--accent); }
.cm-lbl { font-size:0.6rem; text-transform:uppercase; letter-spacing:0.1em; color:var(--text-muted); }
.cm-arrow { font-size:1.5rem; color:var(--accent); }
```

---

### #25 Horizontal Data Strip
Category: D — Stats & Data
Urban Flow Fit: Ridley Scott, Nolan

> Full-width data strip, showing key metrics in a ticker or static style

```html
<div class="data-strip">
  <div class="ds-item">Users: 2.4M</div>
  <div class="ds-sep">|</div>
  <div class="ds-item">Revenue: $48M ARR</div>
  <div class="ds-sep">|</div>
  <div class="ds-item">NPS: 72</div>
</div>
```

```css
.data-strip {
  display: flex; justify-content: center; gap: 1.5rem;
  padding: 0.8rem 0;
  border-top: 1px solid var(--border);
  border-bottom: 1px solid var(--border);
  font-size: 0.75rem; font-weight: 500;
  font-variant-numeric: tabular-nums;
  letter-spacing: 0.05em;
  text-transform: uppercase;
}
.ds-sep { color: var(--border); }
```

---

### #26 Rating Badge
Category: D — Stats & Data
Urban Flow Fit: Wes Anderson, General

> Rating display badge with stars or scores

```html
<div class="rating-badge">
  <span class="rb-stars">★★★★★</span>
  <span class="rb-score">4.9</span>
  <span class="rb-count">2,847 reviews</span>
</div>
```

```css
.rating-badge {
  display: inline-flex; align-items: center; gap: 0.5rem;
  padding: 0.5rem 1rem;
  background: var(--bg-surface);
  border: 1px solid var(--border);
  border-radius: var(--radius-card);
  font-size: 0.75rem;
}
.rb-stars { color: var(--accent); letter-spacing: 2px; }
.rb-score { font-weight: 800; }
.rb-count { color: var(--text-muted); }
```

---

## E. Decorative Lines & Dividers

### #27 Animated Underline
Category: E — Decorative Lines
Urban Flow Fit: General

> Gradient dynamic underline below a title to add a refined feel

```html
<h2 class="anim-underline">Section Title</h2>
```

```css
.anim-underline {
  position: relative; display: inline-block;
  padding-bottom: 0.5rem;
}
.anim-underline::after {
  content: '';
  position: absolute; bottom: 0; left: 0;
  width: 100%; height: 2px;
  background: linear-gradient(90deg, var(--accent), var(--accent-alt, var(--accent)));
  transform: scaleX(0); transform-origin: left;
  transition: transform 0.6s cubic-bezier(0.16,1,0.3,1);
}
.anim-underline:hover::after,
.anim-underline.is-visible::after { transform: scaleX(1); }
```

---

### #28 Vertical Accent Line
Category: E — Decorative Lines
Urban Flow Fit: Nolan, Villeneuve, Park Chan-wook

> Vertical line next to content blocks, suggesting film strips or a timeline

```html
<div class="v-accent-line">
  <div class="val-content">
    <p>Content alongside the accent line.</p>
  </div>
</div>
```

```css
.v-accent-line {
  position: relative;
  padding-left: 1.5rem;
}
.v-accent-line::before {
  content: '';
  position: absolute; left: 0; top: 0; bottom: 0;
  width: 2px;
  background: linear-gradient(to bottom, var(--accent), transparent);
}
```

---

### #29 Grid Overlay
Category: E — Decorative Lines
Urban Flow Fit: Fincher, Nolan, Wes Anderson

> Thin line grid overlaying the entire section to add a sense of structure

```html
<div class="grid-overlay" aria-hidden="true"></div>
```

```css
.grid-overlay {
  position: absolute; inset: 0;
  background-image:
    linear-gradient(var(--border) 1px, transparent 1px),
    linear-gradient(90deg, var(--border) 1px, transparent 1px);
  background-size: 60px 60px;
  opacity: 0.08;
  pointer-events: none;
}
```

---

### #30 Crosshair Target
Category: E — Decorative Lines
Urban Flow Fit: Fincher, Villeneuve, Ridley Scott

> Crosshair decoration suggesting precision targeting or a technical feel

```html
<div class="crosshair" style="--ch-x:50%;--ch-y:50%;">
  <div class="ch-ring"></div>
</div>
```

```css
.crosshair {
  position: absolute;
  left: var(--ch-x); top: var(--ch-y);
  width: 60px; height: 60px;
  transform: translate(-50%,-50%);
}
.crosshair::before, .crosshair::after {
  content:''; position:absolute; background:var(--accent); opacity:0.3;
}
.crosshair::before { width:100%;height:1px;top:50%; }
.crosshair::after { height:100%;width:1px;left:50%; }
.ch-ring {
  position:absolute; inset:10px;
  border:1px solid var(--accent);
  border-radius:50%; opacity:0.3;
}
```

---

### #31 Frame Border
Category: E — Decorative Lines
Urban Flow Fit: Park Chan-wook, Wong Kar-wai

> Thin border around the entire section, like a movie frame boundary

```html
<div class="frame-border">
  <!-- section content -->
</div>
```

```css
.frame-border {
  position: relative;
  margin: 2rem;
  padding: 3rem;
}
.frame-border::before {
  content: '';
  position: absolute; inset: 0;
  border: 1px solid var(--border);
  pointer-events: none;
}
```

---

### #32 Gradient Divider
Category: E — Decorative Lines
Urban Flow Fit: Shinkai, Miyazaki, Sofia Coppola

> Gradient fade-out divider, more sophisticated than a solid color line

```html
<hr class="grad-divider">
```

```css
.grad-divider {
  border: none;
  height: 1px;
  background: linear-gradient(
    90deg,
    transparent,
    var(--border) 20%,
    var(--accent) 50%,
    var(--border) 80%,
    transparent
  );
  margin: 3rem 0;
  opacity: 0.5;
}
```

---

## F. Interactive Micro-Elements

### #33 Scroll Indicator
Category: F — Interactive Micro-Elements
Urban Flow Fit: General

> Down arrow or wheel animation at the bottom of the page, guiding the user to scroll down

```html
<div class="scroll-hint">
  <div class="sh-mouse">
    <div class="sh-wheel"></div>
  </div>
  <span class="sh-text">Scroll</span>
</div>
```

```css
.scroll-hint {
  display:flex; flex-direction:column; align-items:center; gap:0.5rem;
  position:absolute; bottom:2rem; left:50%; transform:translateX(-50%);
}
.sh-mouse {
  width:22px; height:34px;
  border:2px solid var(--text-muted);
  border-radius:11px;
  display:grid; place-items:start center; padding-top:6px;
}
.sh-wheel {
  width:3px; height:6px;
  background:var(--text-muted); border-radius:2px;
  animation:scroll-bob 2s ease-in-out infinite;
}
.sh-text { font-size:0.6rem; text-transform:uppercase; letter-spacing:0.15em; color:var(--text-muted); }
@keyframes scroll-bob { 0%,100%{opacity:1;transform:translateY(0)} 50%{opacity:0.3;transform:translateY(6px)} }
```

---

### #34 Magnetic Hover Button
Category: F — Interactive Micro-Elements
Urban Flow Fit: Nolan, Villeneuve, General

> Button slightly offsets to track the cursor when it gets close, creating a magnetic interaction effect

```html
<button class="mag-btn" data-magnetic>
  <span class="mag-btn-text">Get Started</span>
</button>
```

```css
.mag-btn {
  position: relative;
  padding: 0.8rem 2rem;
  background: var(--accent);
  color: var(--bg);
  border: none; border-radius: var(--radius-card);
  font-weight: 600; cursor: pointer;
  transition: transform 0.3s cubic-bezier(0.16,1,0.3,1);
}
.mag-btn-text {
  display: inline-block;
  transition: transform 0.3s cubic-bezier(0.16,1,0.3,1);
}
/* JS sets --mx, --my on mousemove */
.mag-btn:hover {
  transform: translate(var(--mx,0), var(--my,0));
}
```

---

### #35 Rotating Seal Badge
Category: F — Interactive Micro-Elements
Urban Flow Fit: Wes Anderson, Tarantino

> Circular text badge that slowly rotates continuously, adding personality and a handcrafted feel

```html
<div class="seal-badge">
  <svg viewBox="0 0 100 100" class="seal-text">
    <path id="seal-path" d="M50,50m-38,0a38,38 0 1,1 76,0a38,38 0 1,1 -76,0" fill="none"/>
    <text><textPath href="#seal-path">PREMIUM QUALITY ★ SINCE 2024 ★ </textPath></text>
  </svg>
</div>
```

```css
.seal-badge {
  width: 100px; height: 100px;
  animation: spin-slow 20s linear infinite;
}
.seal-text text {
  font-size: 9px;
  fill: var(--text-muted);
  letter-spacing: 0.15em;
  text-transform: uppercase;
}
@keyframes spin-slow { to{transform:rotate(360deg)} }
```

---

### #36 Cursor Follower Dot
Category: F — Interactive Micro-Elements
Urban Flow Fit: Nolan, Park Chan-wook, Villeneuve

> Decorative small dot that follows the cursor, adding a refined interaction feel

```html
<div class="cursor-dot" id="cursorDot"></div>
```

```css
.cursor-dot {
  position: fixed;
  width: 8px; height: 8px;
  background: var(--accent);
  border-radius: 50%;
  pointer-events: none;
  z-index: 9999;
  transition: transform 0.15s ease-out;
  mix-blend-mode: difference;
}
/* JS: document.addEventListener('mousemove', e => {
  dot.style.left = e.clientX+'px'; dot.style.top = e.clientY+'px';
}); */
```

---

### #37 Typing Cursor
Category: F — Interactive Micro-Elements
Urban Flow Fit: Fincher, Documentary

> Pulsing text cursor effect, simulating real-time input or a terminal feel

```html
<span class="type-cursor">Build faster_</span>
```

```css
.type-cursor::after {
  content: '|';
  color: var(--accent);
  font-weight: 300;
  animation: cursor-blink 1s step-end infinite;
  margin-left: 1px;
}
@keyframes cursor-blink { 0%,100%{opacity:1} 50%{opacity:0} }
```

---

## G. Content Blocks & Panels

### #38 Code Snippet Box
Category: G — Content Blocks
Urban Flow Fit: Fincher, Nolan, Documentary

> Decorative panel for displaying code snippets, with language labels and terminal-style title bars

```html
<div class="code-box">
  <div class="cb-header">
    <span class="cb-dots"><i></i><i></i><i></i></span>
    <span class="cb-lang">TypeScript</span>
  </div>
  <pre class="cb-code"><code>const result = await ai.generate(prompt);</code></pre>
</div>
```

```css
.code-box {
  background: color-mix(in srgb, var(--bg) 95%, white);
  border: 1px solid var(--border);
  border-radius: var(--radius-card);
  overflow: hidden; font-size: 0.8rem;
}
.cb-header {
  display:flex; align-items:center; gap:0.8rem;
  padding:0.6rem 1rem;
  border-bottom:1px solid var(--border);
}
.cb-dots i {
  display:inline-block; width:8px; height:8px;
  border-radius:50%; background:var(--border);
  margin-right:4px;
}
.cb-lang { font-size:0.65rem; color:var(--text-muted); margin-left:auto; }
.cb-code { padding:1rem; margin:0; overflow-x:auto; }
```

---

### #39 Quote Card
Category: G — Content Blocks
Urban Flow Fit: Wong Kar-wai, Sofia Coppola, Park Chan-wook

> Quote panel with large decorative quotes for testimonials or famous sayings

```html
<blockquote class="quote-card">
  <span class="qc-mark">&ldquo;</span>
  <p class="qc-text">This completely transformed our workflow.</p>
  <cite class="qc-cite">— Alex Chen, CTO</cite>
</blockquote>
```

```css
.quote-card {
  position: relative;
  padding: 2rem 2rem 1.5rem 3rem;
  background: var(--bg-surface);
  border-left: 3px solid var(--accent);
  border-radius: 0 var(--radius-card) var(--radius-card) 0;
}
.qc-mark {
  position: absolute; top: 0.5rem; left: 0.8rem;
  font-size: 3rem; line-height: 1;
  color: var(--accent); opacity: 0.3;
}
.qc-text { font-size: 1rem; line-height: 1.6; font-style: italic; }
.qc-cite { display:block; margin-top:0.8rem; font-size:0.75rem; color:var(--text-muted); font-style:normal; }
```

---

### #40 Video Thumbnail
Category: G — Content Blocks
Urban Flow Fit: General (especially Tarantino, Guy Ritchie)

> Video or image thumbnail with a play button overlay, for demo videos or promotional clips

```html
<div class="vid-thumb">
  <img src="thumbnail.jpg" alt="Demo video" class="vt-img">
  <button class="vt-play" aria-label="Play video">
    <svg viewBox="0 0 24 24" class="vt-icon"><polygon points="8,5 19,12 8,19"/></svg>
  </button>
  <span class="vt-duration">2:34</span>
</div>
```

```css
.vid-thumb {
  position: relative; overflow: hidden;
  border-radius: var(--radius-card);
  aspect-ratio: 16/9;
}
.vt-img { width:100%; height:100%; object-fit:cover; }
.vt-play {
  position:absolute; inset:0;
  display:grid; place-items:center;
  background:rgba(0,0,0,0.3); border:none; cursor:pointer;
  transition:background 0.3s;
}
.vt-play:hover { background:rgba(0,0,0,0.5); }
.vt-icon { width:48px; height:48px; fill:white; }
.vt-duration {
  position:absolute; bottom:0.8rem; right:0.8rem;
  padding:0.2rem 0.5rem;
  background:rgba(0,0,0,0.7); color:white;
  font-size:0.7rem; border-radius:4px;
}
```

---

## Quick Reference Index

| # | Name | Cat | Director Fit |
|---|------|-----|-------------|
| 1 | Floating Price Card | A | General |
| 2 | Notification Badge | A | Tarantino/Ritchie/Wright |
| 3 | Testimonial Mini Card | A | Wong Kar-wai/Coppola/Anderson |
| 4 | Feature Chip Stack | A | Documentary/Ridley Scott |
| 5 | Floating Metric Card | A | Nolan/Fincher/Documentary |
| 6 | Status Indicator Card | A | Fincher/Nolan/Ridley Scott |
| 7 | Overlapping Rectangles | B | Tarantino/Ritchie/Wright |
| 8 | Corner Brackets | B | Nolan/Villeneuve/Park |
| 9 | Dot Grid Pattern | B | Anderson/Documentary |
| 10 | Cross Marks | B | Fincher/Nolan/Villeneuve |
| 11 | Diagonal Accent Line | B | Park/Ridley Scott |
| 12 | Circle Accent | B | Miyazaki/Shinkai/Anderson |
| 13 | Stacked Triangles | B | Tarantino/Wright/Ritchie |
| 14 | Soft Gradient Blob | C | Miyazaki/Shinkai/Wong Kar-wai |
| 15 | Glass Morphism Panel | C | General (Villeneuve/Nolan) |
| 16 | Aurora Gradient | C | Shinkai/Miyazaki/Coppola |
| 17 | Light Leak Overlay | C | Wong Kar-wai/Coppola |
| 18 | Radial Vignette | C | Fincher/Park/Nolan |
| 19 | Dual Orb Glow | C | Villeneuve/Ridley Scott |
| 20 | Noise Texture Overlay | C | Ridley Scott/Fincher/Wong Kar-wai |
| 21 | Hero Stats Bar | D | Documentary/Nolan/Fincher |
| 22 | Giant Number | D | Tarantino/Wright/Anderson |
| 23 | Progress Ring | D | Nolan/Villeneuve/Documentary |
| 24 | Comparison Metric | D | Documentary/Fincher |
| 25 | Horizontal Data Strip | D | Ridley Scott/Nolan |
| 26 | Rating Badge | D | Anderson/General |
| 27 | Animated Underline | E | General |
| 28 | Vertical Accent Line | E | Nolan/Villeneuve/Park |
| 29 | Grid Overlay | E | Fincher/Nolan/Anderson |
| 30 | Crosshair Target | E | Fincher/Villeneuve/Ridley Scott |
| 31 | Frame Border | E | Park/Wong Kar-wai |
| 32 | Gradient Divider | E | Shinkai/Miyazaki/Coppola |
| 33 | Scroll Indicator | F | General |
| 34 | Magnetic Hover Button | F | Nolan/Villeneuve/General |
| 35 | Rotating Seal Badge | F | Anderson/Tarantino |
| 36 | Cursor Follower Dot | F | Nolan/Park/Villeneuve |
| 37 | Typing Cursor | F | Fincher/Documentary |
| 38 | Code Snippet Box | G | Fincher/Nolan/Documentary |
| 39 | Quote Card | G | Wong Kar-wai/Coppola/Park |
| 40 | Video Thumbnail | G | General (Tarantino/Ritchie) |

### Category Distribution
- **A. Floating Cards:** #1-#6 (6 elements)
- **B. Geometric Shapes:** #7-#13 (7 elements)
- **C. Gradient Blobs:** #14-#20 (7 elements)
- **D. Stats & Data:** #21-#26 (6 elements)
- **E. Decorative Lines:** #27-#32 (6 elements)
- **F. Interactive Micro:** #33-#37 (5 elements)
- **G. Content Blocks:** #38-#40 (3 elements)
