# Prompt für Codex / OpenCode

Kopiere diesen Prompt in Codex CLI oder OpenCode um die Website zu bauen.

---

## Prompt

Baue eine Single Page HTML Website als Proposal für das Startup AIDVANCE.

**Lies zuerst diese beiden Dateien im Projektordner:**
1. `SPEC.md` — Technische Spezifikation (HTML-Struktur, CSS-Design-System, Komponenten)
2. Der Content-Plan unten

**Output:** Eine einzelne `index.html` Datei. Self-contained, keine externen Dependencies.

**Content-Plan:**

### HEADER
- h1: "Proposal für AIDVANCE"
- Subtitle: "Agentische Workflows verbessern — systematisch, messbar, sicher"
- Kontext-Zeile: "Ergebnis des Gesprächs vom 26. März 2026 · Von Samuel Fleig"

### SEKTION 1: Claude Code Coaching (Stufe 1 — sofort lieferbar)
Hands-on Training wie man Claude Code produktiv nutzt. Basierend auf Anthropic Academy Curriculum.

5 Coaching-Domänen als Icon-Karten:
1. 🏗️ Agentic Architecture & Orchestration (27%) — Multi-Agent-Systeme, Task-Dekomposition, Hub-and-Spoke Patterns
2. ⚙️ Tool Design & MCP Integration (18%) — Model Context Protocol Server, Tool-Boundary Management
3. 💻 Claude Code Configuration & Workflows (20%) — Setup, Hooks, Modes, Custom Skills
4. ✍️ Prompt Engineering & Structured Output (20%) — Effektive Prompts, JSON-Output, Chain-of-Thought
5. 🧠 Context Management & Reliability (15%) — Kontext-Fenster optimieren, Fehlerbehandlung, Recovery

Credentials-Block:
- "2 Monate intensives Arbeiten mit Claude Code"
- "44 Projekte mit Git-Versionierung, 800+ Commits"
- "Eigenes Eval-Framework für messbare Qualitätsverbesserung"
- Empfehlung: "Für non-native-IT Nutzer empfehlen wir Claude CoWork (GUI) als Einstieg"

### SEKTION 2: Evolve-Pipeline MVP (Stufe 2 — der eigentliche Wert)
Ein System das agentische Workflows nach jedem Run evaluiert und gezielt verbessert.

Flowchart (vertikal, CSS-Boxes mit Verbindungslinien):
1. 🔄 Agentischer Workflow — "Euer bestehendes Setup läuft wie gewohnt"
2. 👁️ Observer — "Beobachtet den Workflow automatisch"
3. 💡 Improvement-Vorschläge — "Generiert Liste möglicher Verbesserungen"
4. ☝️ Pick ONE — "Eine Verbesserung auswählen, isoliert testbar"
5. ⚖️ A/B Run — "Workflow MIT vs OHNE Verbesserung" (split in zwei Boxen: A | B)
6. 👤 Human Eval — "Mensch bewertet: Ist B signifikant besser als A?"
7. ✅ Accept / ❌ Reject — "Verbesserung übernehmen oder verwerfen" (zwei Buttons grün/rot)
8. 🔁 Loop — "Zurück zum Observer → kontinuierliche Verbesserung"

4 Prinzipien (als kleine Liste):
- Qualität > Geschwindigkeit — besonders bei therapeutischen Daten
- Human-in-the-Loop ist Pflicht — kein blinder Auto-Accept
- Eine Verbesserung pro Zyklus — isoliert testbar und nachvollziehbar
- Erst wenn der Prozess gut ist, dann automatisieren

2 Referenz-Cards:
- 🔬 Karpathy AutoResearch (März 2026): "AI-Agent der autonom Experimente durchführt, ~12 pro Stunde. Behält was funktioniert, verwirft was nicht hilft." Link: github.com/karpathy/autoresearch
- 📄 Google Hyperagents (arXiv 2603.19461): "Meta-Agent der nicht nur Tasks verbessert, sondern seinen eigenen Verbesserungsprozess optimiert." Link: arxiv.org/abs/2603.19461

Samuels relevante Erfahrung (3 Punkte):
- Sidecar-NG: Von 45.000 auf 1.200 Zeilen Code durch eval-driven Feature-Selektion
- AgentArena: 8 Experiments, 140+ Benchmark-Runs, pass@k Statistik
- Safety Gates: Prompt-Injection-Schutz für sensitive Daten (direkt relevant für AIDVANCE)

### SEKTION 3: Autonomous Self-Improvement (Stufe 3 — Ausblick)
Visuell ausgegraut (opacity 0.5, dashed border). Nur 3 Sätze:
- "Vollautonome Verbesserung ohne Human-in-the-Loop — die langfristige Vision."
- "Aktuell ein offenes Forschungsproblem. Karpathy, Google und viele andere Labs arbeiten daran."
- "Ich kann es versuchen, aber ich kann es nicht garantieren — nobody has solved this yet."

### FOOTER
- "Nächster Schritt: Beispiel-Workflows von AIDVANCE teilen (non-confidential)"
- 3 offene Fragen an Jannis:
  1. Wie funktioniert euer Produkt technisch — ist Karl auch ein agentisches System?
  2. Welche Tasks bearbeitet ihr aktuell mit agentischen Workflows?
  3. Könnt ihr non-confidential Beispieldaten teilen?
- Kontakt: Samuel Fleig

**Design-Regeln (aus SPEC.md):**
- Dark theme: BG #0F1117, Cards #1A1D27, Accent #2563EB
- System-font-stack, keine externen Fonts
- Mobile-first, Breakpoint 768px
- Subtle fade-in Animationen via IntersectionObserver
- KEIN generischer AI-Look (keine Neon-Gradients, keine Matrix-Ästhetik)
