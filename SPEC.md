# SPEC.md — AIDVANCE Proposal Website

## Output

Single file: `index.html` (self-contained, no external dependencies)

---

## HTML Structure

```html
<!DOCTYPE html>
<html lang="de">
<head> meta, title, embedded <style>, embedded <script> </head>
<body>
  <header id="hero">
    <h1>Proposal für AIDVANCE</h1>
    <p class="subtitle">Agentische Workflows verbessern — systematisch, messbar, sicher</p>
    <p class="context">Ergebnis des Gesprächs vom 26. März 2026</p>
  </header>

  <main>
    <section id="coaching" class="tier tier-1">
      <h2>Stufe 1: Claude Code Coaching</h2>
      <p class="tier-tagline">Sofort lieferbar</p>
      <!-- 5 domain cards in a CSS grid -->
      <div class="domain-grid"> 5x .domain-card </div>
      <div class="credentials">Samuel's experience block</div>
    </section>

    <section id="evolve-pipeline" class="tier tier-2">
      <h2>Stufe 2: Evolve-Pipeline MVP</h2>
      <p class="tier-tagline">Der eigentliche Wert</p>
      <div class="pipeline-flow"> 8 steps as connected boxes </div>
      <div class="principles"> 4 principle items </div>
      <div class="references"> 2 reference cards (Karpathy, Hyperagents) </div>
      <div class="experience"> Samuel's relevant experience </div>
    </section>

    <section id="autonomous" class="tier tier-3 muted">
      <h2>Stufe 3: Autonomous Self-Improvement</h2>
      <p>3 sentences only, visually muted</p>
    </section>
  </main>

  <footer id="next-steps">
    <h2>Nächste Schritte</h2>
    <div class="questions"> 3 questions for Jannis </div>
    <div class="contact">Samuel Fleig</div>
  </footer>
</body>
</html>
```

---

## CSS Design System

### Colors

```css
--bg-primary:    #0F1117   /* page background */
--bg-card:       #1A1D27   /* card/section background */
--bg-card-hover: #22263A
--accent:        #2563EB   /* primary blue */
--accent-light:  #3B82F6
--text-primary:  #E2E8F0
--text-secondary:#94A3B8
--text-muted:    #64748B
--border:        #2D3348
--success:       #22C55E   /* Accept button */
--danger:        #EF4444   /* Reject button */
```

### Typography

- Font stack: `system-ui, -apple-system, sans-serif`
- `h1`: 2.5rem, font-weight 700
- `h2`: 1.75rem, font-weight 600
- Body: 1rem, line-height 1.6
- `.tier-tagline`: 0.875rem, uppercase, letter-spacing 0.1em, color `var(--accent)`

### Layout

- `max-width: 900px`, `margin: 0 auto`
- Section padding: `4rem 1.5rem`
- Card padding: `1.5rem`
- Card border-radius: `12px`
- Card border: `1px solid var(--border)`

### Responsive

- Mobile-first
- Breakpoint: `768px`
- `domain-grid`: 1 column mobile → 3 columns desktop (rows: 3+2 or 2+3)
- `pipeline-flow`: vertical stack on all sizes, wider boxes at desktop
- Reference cards: 1 column mobile → 2 columns desktop

---

## Content

### Header

- Title: "Proposal für AIDVANCE"
- Subtitle: "Agentische Workflows verbessern — systematisch, messbar, sicher"
- Context line: "Ergebnis des Gesprächs vom 26. März 2026"

---

### Section 1: Claude Code Coaching

**Tier tagline:** "Sofort lieferbar"

**Intro text:** Hands-on Training für produktive Claude Code Nutzung — basierend auf dem Anthropic Academy Curriculum (13 Kurse, anthropic.skilljar.com) und der Claude Certified Architect Zertifizierung.

**5 Domain Cards:**

| Icon | Title | Percentage | Description |
|------|-------|-----------|-------------|
| 🏗️ | Agentic Architecture & Orchestration | 27% | Multi-Agent-Systeme, Task-Dekomposition, Orchestrierung |
| ⚙️ | Tool Design & MCP Integration | 18% | Model Context Protocol, saubere Tool-Boundaries |
| 💻 | Claude Code Configuration & Workflows | 20% | Setup, Hooks, Modes, CI-Integration |
| ✍️ | Prompt Engineering & Structured Output | 20% | Effektive Prompts, JSON-Output, Reliabilität |
| 🧠 | Context Management & Reliability | 15% | Kontext-Fenster optimieren, Fehlerbehandlung |

**Credentials block:**
- 2 Monate intensives Arbeiten mit Claude Code
- 44 Projekte, 800+ Commits
- Hinweis: Für non-native-IT Claude CoWork (GUI) statt CLI empfohlen
- Ziel: Jeder im Team nutzt AI-Tools bewusst und effektiv — kein Trial-and-Error

---

### Section 2: Evolve-Pipeline MVP

**Tier tagline:** "Der eigentliche Wert"

**Intro text:** Ein System, das agentische Workflows nach jedem Run evaluiert und gezielt verbessert. Qualität > Geschwindigkeit — besonders bei therapeutischen Daten.

**Pipeline Flowchart (8 steps):**

```
Step 1: 🔄 Agentischer Workflow
        ↓ (vertical connector line)
Step 2: 👁️ Observer
        "Beobachtet Ablauf, Entscheidungen, Output-Qualität"
        ↓
Step 3: 💡 Improvement-Vorschläge
        "Generiert Liste möglicher Verbesserungen"
        ↓
Step 4: ☝️ Pick ONE
        "Eine Hypothese auswählen — isoliert testbar"
        ↓
Step 5: ⚖️ A/B Run          [split: two boxes side by side]
        [ A: Ohne Änderung ] [ B: Mit Verbesserung ]
        ↓
Step 6: 👤 Human Eval
        "Ist B signifikant besser als A?"
        ↓
Step 7: ✅ Accept / ❌ Reject   [two buttons side by side]
        [green button: Accept ✓] [red button: Reject ✗]
        ↓
Step 8: 🔁 Loop
        "Zurück zum Observer" [arrow pointing back up to Step 2]
```

Connector implementation: CSS `::after` pseudo-elements on each step box draw a 2px vertical line in `var(--accent)`. The A/B split in Step 5 forks into two lines that converge back before Step 6.

**4 Principles (as a clean list with icon + text):**

1. ✅ Qualität > Geschwindigkeit — besonders bei therapeutischen Daten
2. 👤 Human-in-the-Loop ist Pflicht — kein blinder Auto-Accept
3. 🎯 Eine Verbesserung pro Zyklus — isoliert testbar, keine Interferenzen
4. 🔬 Erst wenn der Prozess gut ist, dann automatisieren

**2 Reference Cards (side by side at ≥768px):**

Card 1: Karpathy AutoResearch
- Icon: 🔬
- Title: "AutoResearch"
- Author/Date: "Andrej Karpathy, März 2026"
- Description: AI-Agent der autonom Experimente läuft (~12/Stunde) und behält, was messbar besser ist.
- Link: [github.com/karpathy/autoresearch](https://github.com/karpathy/autoresearch)

Card 2: Google Hyperagents
- Icon: 📄
- Title: "Hyperagents"
- Author/Date: "Google, März 2026 — arXiv 2603.19461"
- Description: Meta-Agent der nicht nur Tasks verbessert, sondern seinen eigenen Verbesserungsprozess optimiert.
- Link: [arxiv.org/abs/2603.19461](https://arxiv.org/abs/2603.19461)

Both cards note: "Beide zeigen: Self-Improving Agents sind kein Sci-Fi mehr — aber noch Forschung."

**Experience block:**

- Sidecar-NG: 45.000 LOC → 1.200 LOC durch eval-driven Feature-Selektion
- AgentArena: 8 Experimente, 140+ Runs, pass@k Statistik
- Safety Gates: Prompt-Injection-Schutz für vertrauliche Daten (direkt relevant für AIDVANCE)

---

### Section 3: Autonomous Self-Improvement (Muted)

**Tier tagline:** "Ausblick"

**3 sentences only (italic, muted styling):**

"Vollautonome Verbesserung ohne Human-in-the-Loop ist die nächste Stufe. Aktuell ein offenes Forschungsproblem — Karpathy, Google und viele Labs arbeiten daran. Samuel: Ich kann es versuchen, aber ich kann es nicht garantieren — nobody has solved this yet."

---

### Footer

**Heading:** "Nächste Schritte"

**3 Questions for Jannis (numbered list):**

1. Wie funktioniert Karl technisch — ist Karl auch ein agentisches System?
2. Welche Tasks bearbeitet ihr aktuell mit agentischen Workflows?
3. Könnt ihr non-confidential Beispieldaten oder Workflows teilen?

**Contact / CTA:**

- Name: Samuel Fleig
- CTA: "Nächster Schritt: Beispiel-Workflows von AIDVANCE teilen (non-confidential)"

---

## Component Specs

### Domain Cards

Each `.domain-card`:
- Unicode icon, `font-size: 2rem`, centered above title
- `h3` title
- Percentage badge: small pill, `background: var(--accent)`, `color: white`, `border-radius: 999px`, `padding: 2px 8px`, `font-size: 0.75rem`
- One-line description in `var(--text-secondary)`
- Hover: `transform: translateY(-2px)`, `background: var(--bg-card-hover)`, `box-shadow: 0 4px 16px rgba(0,0,0,0.3)`

Layout: CSS Grid, `grid-template-columns: repeat(3, 1fr)` at desktop, `repeat(1, 1fr)` mobile. The 4th and 5th cards center in the second row at desktop (use `grid-column` or `justify-content: center` on the grid).

### Pipeline Flowchart

`.pipeline-flow` is a flex column, `align-items: center`.

Each `.pipeline-step` is a box:
- `min-width: 280px` (desktop), full width on mobile
- `background: var(--bg-card)`, `border: 1px solid var(--border)`, `border-radius: 12px`
- `padding: 1rem 1.5rem`
- Icon + title in a flex row
- Optional subtitle in `var(--text-secondary)`, `font-size: 0.875rem`

Connectors between steps: `.pipeline-step::after` pseudo-element, `width: 2px`, `height: 32px`, `background: var(--accent)`, centered below each box.

Step 5 (A/B) is a special layout:
- A `.ab-split` container with two `.pipeline-step` boxes side by side (`display: flex; gap: 1rem`)
- The fork lines: CSS-only, two `::before` lines diverging left/right from the connector above
- The merge lines: two `::after` lines converging back to center below

Step 7 (Accept/Reject):
- Two `<button>` elements in a flex row, `gap: 0.75rem`
- Accept: `background: var(--success)`, `color: white`, `border: none`, `padding: 0.5rem 1.25rem`, `border-radius: 8px`
- Reject: `background: var(--danger)`, same sizing
- Buttons are visual only (no onclick logic needed)

Step 8 (Loop):
- Has a curved arrow pointing back upward to Step 2
- Implementation: SVG inline arrow or CSS border trick on the right side of the flow container
- Label: "Nächster Zyklus"

### Reference Cards

`.references` uses CSS Grid: `grid-template-columns: 1fr` mobile, `1fr 1fr` at ≥768px.

Each `.reference-card`:
- Large icon (2rem)
- Title + author/date line
- 2-line description
- External link styled as `color: var(--accent-light)`, no underline default, underline on hover

### Muted Section (Section 3)

```css
.tier.muted {
  opacity: 0.5;
  border: 1px dashed var(--border);
  border-radius: 12px;
}
.tier.muted p {
  font-style: italic;
  color: var(--text-muted);
}
```

No hover effects on any child elements.

### Footer

```css
footer#next-steps {
  background: var(--bg-card);
  border-top: 1px solid var(--border);
  padding: 4rem 1.5rem;
}
```

Questions as an `<ol>` with custom counter styling: number in `var(--accent)`, bold, followed by question text in `var(--text-primary)`.

Contact block: plain text, `var(--text-secondary)`, with CTA in `var(--text-primary)`.

---

## Animations

### Scroll Fade-in

All `<section>` and `<footer>` elements start hidden:

```css
.fade-in {
  opacity: 0;
  transform: translateY(20px);
  transition: opacity 0.6s ease, transform 0.6s ease;
}
.fade-in.visible {
  opacity: 1;
  transform: translateY(0);
}
```

JavaScript: `IntersectionObserver` with `threshold: 0.1` adds `.visible` class when element enters viewport.

### Card Hover

```css
.domain-card {
  transition: transform 0.2s ease, background 0.2s ease, box-shadow 0.2s ease;
}
```

### Pipeline Stagger

Each `.pipeline-step` gets a staggered animation delay on first appearance:

```css
.pipeline-step:nth-child(1) { transition-delay: 0.0s; }
.pipeline-step:nth-child(2) { transition-delay: 0.1s; }
/* ...and so on up to 0.7s */
```

Applied via the same `IntersectionObserver` fade-in mechanism when the pipeline section becomes visible.

### Prohibited Animations

- No parallax
- No particle effects
- No gradient backgrounds
- No typing/typewriter animations
- No neon glow effects

---

## Anti-Patterns (DO NOT)

- No gradient backgrounds — flat `var(--bg-primary)` only
- No neon colors — only the defined palette above
- No "AI-generated" look — not a grid of identical icon-cards with generic descriptions
- No external fonts — system-ui stack only, no Google Fonts `<link>`
- No JavaScript frameworks — vanilla JS only
- No lorem ipsum — all text is real content from the content plan
- No CDN links for CSS frameworks (Bootstrap, Tailwind, etc.)
- No `<canvas>` animations
- No `@keyframes` that loop indefinitely

---

## File Delivery

Single file `index.html`, approximately 400–600 lines. All CSS in `<style>` tag in `<head>`. All JS in `<script>` tag before `</body>`. No external requests at load time.
