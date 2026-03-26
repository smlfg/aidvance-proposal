# AIDVANCE Proposal — Pipeline Plan

## Context
Samuel hatte heute (26.03.2026) ein tolles Gespräch mit Jannis Pasoglou, CEO von AIDVANCE.
AIDVANCE baut "Karl" — einen therapeutischen AI Listener für emotionales Wohlbefinden.
Team: <10 Leute, FDA-Zulassungsprozess, Confidential Data.

**Jannis will:** Jeden Mitarbeiter zum "10X Engineer" machen durch selbstverbessernde agentische Workflows.
**Samuel bietet:** Drei Stufen — Coaching, Eval-Pipeline MVP, Autonome Self-Improvement (Moonshot).
**Deliverable:** Single Page HTML als Proposal-Website + Showcase von Samuels Agent-Pipeline-Skills.

## Projekt-Setup

**Ordner:** `/home/smlflg/Projekte/Jobs_Selbständigkeit_Geldverdienen/aidvance-proposal/`
**Output:** `index.html` (Single Page, self-contained)

## Pipeline: Claude Code → Codex → OpenCode

### Schritt 1: Content-Briefing (Claude Code — DIESER PLAN)

Die Website hat 3 Sektionen + Header/Footer:

---

### HEADER
- "Proposal für AIDVANCE" — Von Samuel Fleig
- Subtitle: "Agentische Workflows verbessern — systematisch, messbar, sicher"
- Kurzer Kontext: Ergebnis des Gesprächs vom 26.03.2026

---

### SEKTION 1: Claude Code Coaching (Stufe 1 — sofort lieferbar)

**Kernaussage:** Hands-on Training wie man Claude Code produktiv nutzt.

**Inhalt:**
- Basierend auf Anthropic Academy Curriculum (13 kostenlose Kurse, anthropic.skilljar.com)
- 5 Coaching-Domänen (aus der Claude Certified Architect Zertifizierung):
  1. **Agentic Architecture & Orchestration** (27%) — Multi-Agent-Systeme, Task-Dekomposition
  2. **Tool Design & MCP Integration** (18%) — Model Context Protocol, Tool-Boundaries
  3. **Claude Code Configuration & Workflows** (20%) — Setup, Hooks, Modes
  4. **Prompt Engineering & Structured Output** (20%) — Effektive Prompts, JSON-Output
  5. **Context Management & Reliability** (15%) — Kontext-Fenster, Fehlerbehandlung
- Samuels Erfahrung: 2 Monate intensives Arbeiten, 44 Projekte, 800+ Commits
- Für non-native-IT: Claude CoWork (GUI) statt CLI empfohlen
- **Ziel:** Jeder im Team nutzt AI-Tools bewusst und effektiv, nicht trial-and-error

**Visuell:** Icon-Karten für die 5 Domänen

---

### SEKTION 2: Evolve-Pipeline MVP (Stufe 2 — der eigentliche Wert)

**Kernaussage:** Ein System das agentische Workflows nach jedem Run evaluiert und gezielt verbessert.

**Schematisches Flowchart (CSS/SVG):**
```
[Agentischer Workflow]
    ↓
[Observer 👁️] — beobachtet den Workflow
    ↓
[Improvement-Vorschläge] — Liste möglicher Verbesserungen
    ↓
[Pick ONE] — eine Verbesserung auswählen
    ↓
[A/B Run] — Workflow MIT vs OHNE Verbesserung
    ↓
[Human Eval] — Mensch bewertet: Ist B signifikant besser als A?
    ↓
[Accept ✓ / Reject ✗] — Verbesserung übernehmen oder verwerfen
    ↓
[Loop] → zurück zum Observer
```

**Wichtige Prinzipien:**
- Qualität > Geschwindigkeit (besonders bei therapeutischen Daten)
- Human-in-the-Loop ist Pflicht — kein blinder Auto-Accept
- Eine Verbesserung pro Zyklus — isoliert testbar
- Erst wenn der Prozess gut ist, dann automatisieren

**Referenzen (als Sidebar/Gedankenstrich):**
- **Karpathy AutoResearch** (März 2026): AI-Agent der autonom Experimente läuft, ~12/Stunde, behält was besser ist. GitHub: github.com/karpathy/autoresearch
- **Google Hyperagents** (arXiv 2603.19461, März 2026): Meta-Agent der nicht nur Tasks verbessert, sondern seinen eigenen Verbesserungsprozess optimiert.
- Beide zeigen: Self-Improving Agents sind kein Sci-Fi mehr, aber noch Forschung.

**Samuels Erfahrung dazu:**
- Sidecar-NG: 45K LOC → 1.2K LOC durch eval-driven Feature-Selektion
- AgentArena: 8 Experiments, 140+ Runs, pass@k Statistik
- Safety Gates: Prompt-Injection-Schutz für Confidential Data (direkt relevant!)

**Visuell:** Flowchart als CSS-Diagramm, Referenz-Papers als kleine Cards

---

### SEKTION 3: Autonomous Self-Improvement (Stufe 3 — Ausblick)

**Kernaussage:** Kurzgehalten. "Das ist die Vision, aber noch nicht reif."

**Inhalt (max 3 Sätze):**
- Vollautonome Verbesserung ohne Human-in-the-Loop
- Aktuell ein offenes Forschungsproblem (Karpathy, Google, viele Labs arbeiten dran)
- Samuel: "Ich kann es versuchen, aber ich kann es nicht garantieren — nobody has solved this yet."

**Visuell:** Ausgegraut/dezenter als Stufe 1+2, zeigt Ehrlichkeit

---

### FOOTER
- Kontakt: Samuel Fleig
- "Nächster Schritt: Beispiel-Workflows von AIDVANCE teilen (non-confidential)"
- Die 3 offenen Fragen an Jannis:
  1. Wie funktioniert euer Produkt technisch — ist Karl auch ein agentisches System?
  2. Welche Tasks bearbeitet ihr aktuell mit agentischen Workflows?
  3. Könnt ihr non-confidential Beispieldaten teilen?

---

### Schritt 2: Technische Spec (Codex)

Codex bekommt diesen Content-Plan und spezifiziert:
- HTML-Struktur (Sections, IDs, semantic markup)
- CSS-Design (Dark theme passend zu Samuels anderen Seiten, professionell aber nicht generisch)
- Flowchart-Implementierung (CSS Grid/Flexbox + SVG Pfeile)
- Responsive Breakpoints
- Keine externen Dependencies (self-contained HTML)

### Schritt 3: Build (OpenCode)

OpenCode bekommt Content-Plan + Codex-Spec und baut `index.html`.

## Verification
- [ ] Ordner existiert: `Jobs_Selbständigkeit_Geldverdienen/aidvance-proposal/`
- [ ] `index.html` öffnet sich im Browser
- [ ] Alle 3 Stufen sichtbar
- [ ] Flowchart in Stufe 2 ist lesbar und verständlich
- [ ] Referenzen (Karpathy, Hyperagents) sind korrekt verlinkt
- [ ] Footer enthält die 3 Fragen an Jannis
- [ ] Seite sieht professionell aus (kein generischer AI-Look)
- [ ] Mobile-responsive
