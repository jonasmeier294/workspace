# OpenClaw Use Cases & Anwendungsfälle

> Recherche-Report, Stand: 18. Februar 2026
> Quellen: docs.openclaw.ai, github.com/openclaw/openclaw, Showcase-Seite, ClawHub

---

## Was ist OpenClaw?

OpenClaw ist ein **selbst-gehosteter, persönlicher AI-Assistent** (MIT-Lizenz), der als Gateway zwischen deinen Messaging-Apps und AI-Coding-Agents fungiert. Du läufst einen einzigen Gateway-Prozess auf deinem Rechner und erreichst deinen Assistenten über WhatsApp, Telegram, Discord, Slack, Signal, iMessage, Google Chat, Microsoft Teams, Matrix, IRC, WebChat und mehr — gleichzeitig.

**Kernarchitektur:** Chat-Apps → Gateway (Node.js) → Pi Agent (RPC) → Tools (Browser, Exec, Canvas, Nodes, Cron, Web, Messaging)

---

## Was unterscheidet OpenClaw von ChatGPT, Siri & Co.?

| Merkmal | OpenClaw | ChatGPT / Gemini / Siri |
|---|---|---|
| **Self-hosted** | Läuft auf deiner Hardware, deine Daten | Cloud-only |
| **Multi-Channel** | Ein Agent, alle Messenger gleichzeitig | Eigene App oder Web |
| **Tool-Use / Code-Agent** | Shell, Browser, Dateien, Canvas — echte Aktionen | Eingeschränkt (Plugins) |
| **Cron & Heartbeat** | Proaktiver Agent mit Scheduler | Nur reaktiv |
| **Skills-System** | Erweiterbar via ClawHub + eigene Skills | Geschlossenes Plugin-System |
| **Mobile Nodes** | iOS/Android als Kamera, Mikrofon, Canvas | Nicht möglich |
| **Multi-Agent Routing** | Mehrere Agents mit isolierten Sessions | Ein Agent |
| **Voice Wake / Talk Mode** | Always-on Sprache auf macOS/iOS/Android | Siri-artig, aber eingeschränkter |
| **Open Source** | MIT-Lizenz, Community-driven | Proprietär |

---

## Use Cases nach Kategorien

### 🖥️ Coding & Entwicklung

| Use Case | Beschreibung | Nützlichkeit |
|---|---|---|
| **PR Review via Chat** | OpenClaw reviewed GitHub-PRs und liefert Feedback direkt in Telegram/WhatsApp | ⭐⭐⭐⭐⭐ |
| **iOS App via Telegram** | Komplette iOS-App mit Maps + Voice Recording, deployed auf TestFlight — alles per Telegram-Chat gesteuert | ⭐⭐⭐⭐ |
| **CodexMonitor** | CLI + VS Code Tool zum Überwachen lokaler Codex-Sessions | ⭐⭐⭐ |
| **SNAG Screenshot→Markdown** | Hotkey → Screenshot-Region → Gemini Vision → Markdown im Clipboard | ⭐⭐⭐⭐⭐ |
| **Code-Aufgaben per WhatsApp** | "Ship checklist" per Nachricht → Agent arbeitet im Repo | ⭐⭐⭐⭐⭐ |
| **Agents UI** | Desktop-App zum Verwalten von Skills/Commands über mehrere AI-Tools | ⭐⭐⭐⭐ |

### 🛒 Browser-Automation & Shopping

| Use Case | Beschreibung | Nützlichkeit |
|---|---|---|
| **Tesco Shop Autopilot** | Wöchentlicher Einkauf: Meal Plan → Produkte → Lieferslot buchen → Bestellen. Kein API nötig, rein Browser-gesteuert | ⭐⭐⭐⭐⭐ |
| **ParentPay Schulessen** | Automatisierte UK-Schulessen-Buchung via Browser-Steuerung | ⭐⭐⭐⭐ |
| **Web-Recherche** | Agent surft eigenständig, extrahiert Infos, fasst zusammen | ⭐⭐⭐⭐⭐ |

### 📅 Produktivität & Automatisierung

| Use Case | Beschreibung | Nützlichkeit |
|---|---|---|
| **Morning Briefing (Cron)** | Täglicher Cron-Job: "Fasse Overnight-Updates zusammen" → Ergebnis in Slack/WhatsApp | ⭐⭐⭐⭐⭐ |
| **E-Mail Monitoring** | Heartbeat checkt Gmail, meldet wichtige Mails proaktiv | ⭐⭐⭐⭐⭐ |
| **Kalender-Erinnerungen** | Agent erinnert an Termine, prüft regelmäßig Google Calendar | ⭐⭐⭐⭐⭐ |
| **Webhook-Integration** | Externe Events (GitHub, CI/CD, Monitoring) triggern Agent-Aktionen | ⭐⭐⭐⭐ |
| **R2 Upload / File Sharing** | Dateien auf Cloudflare R2 hochladen, Presigned URLs generieren | ⭐⭐⭐⭐ |

### 🏠 Smart Home & Hardware

| Use Case | Beschreibung | Nützlichkeit |
|---|---|---|
| **Bambu 3D-Drucker** | Status, Jobs, Kamera, AMS, Kalibrierung — alles per Chat steuern | ⭐⭐⭐⭐ |
| **IoT via Shell** | Beliebige CLI-Tools (z.B. Home Assistant CLI) per Chat triggern | ⭐⭐⭐ |

### 🗣️ Voice & Sprache

| Use Case | Beschreibung | Nützlichkeit |
|---|---|---|
| **Voice Wake + Talk Mode** | Always-on Sprachassistent auf macOS/iOS/Android (ElevenLabs TTS) | ⭐⭐⭐⭐⭐ |
| **Telegram Voice Notes** | TTS-Antworten als Telegram-Sprachnachrichten (papla.media) | ⭐⭐⭐⭐ |
| **Voice-Storytelling** | Agent erzählt Geschichten, Film-Zusammenfassungen mit verschiedenen Stimmen | ⭐⭐⭐ |

### 🚆 Mobilität & Reisen

| Use Case | Beschreibung | Nützlichkeit |
|---|---|---|
| **Wiener Linien** | Echtzeit-Abfahrten, Störungen, Aufzüge, Routing für Wien | ⭐⭐⭐⭐ |
| **Standort-Abfragen** | GPS-Position vom Handy-Node abfragen, ortsbezogene Infos liefern | ⭐⭐⭐ |

### 🍷 Persönliche Daten & Wissen

| Use Case | Beschreibung | Nützlichkeit |
|---|---|---|
| **Weinkeller-Skill** | CSV-Import → durchsuchbare Weinsammlung (962 Flaschen im Beispiel) | ⭐⭐⭐⭐ |
| **Persönliches Gedächtnis** | MEMORY.md + tägliche Notes → Agent merkt sich Kontext langfristig | ⭐⭐⭐⭐⭐ |
| **Workspace-Files** | Agent verwaltet Notizen, Projekte, Dokumentation eigenständig | ⭐⭐⭐⭐⭐ |

### 📱 Social Media & Messaging

| Use Case | Beschreibung | Nützlichkeit |
|---|---|---|
| **Discord Bot** | Agent als aktiver Teilnehmer in Discord-Servern (reagiert, antwortet, moderiert) | ⭐⭐⭐⭐ |
| **Multi-Channel Broadcast** | Eine Nachricht an mehrere Channels/Plattformen gleichzeitig | ⭐⭐⭐ |
| **Gruppen-Assistent** | In WhatsApp/Telegram-Gruppen bei @mention antworten | ⭐⭐⭐⭐ |

### 📊 Monitoring & Ops

| Use Case | Beschreibung | Nützlichkeit |
|---|---|---|
| **Auth Monitoring** | Überwacht OAuth-Token-Zustand, warnt bei Ablauf | ⭐⭐⭐⭐ |
| **Health Checks** | Gateway-Status, Session-Health, automatische Diagnose via `openclaw doctor` | ⭐⭐⭐⭐ |
| **Git Status Checks** | Agent prüft proaktiv Repo-Status, uncommitted changes | ⭐⭐⭐ |

### 🎨 Canvas & Visuelle Outputs

| Use Case | Beschreibung | Nützlichkeit |
|---|---|---|
| **Live Canvas (A2UI)** | Agent rendert interaktive UI-Elemente auf macOS/iOS/Android | ⭐⭐⭐⭐ |
| **Dashboards** | Agent baut visuelle Dashboards als Canvas-Inhalte | ⭐⭐⭐ |

---

## Top 10 für Power-User (Empfehlung)

1. **🏆 Morning Briefing + E-Mail/Kalender-Monitoring** — Set-and-forget Produktivität
2. **🏆 Code-Aufgaben per WhatsApp/Telegram** — Coding von unterwegs
3. **🏆 PR Review Pipeline** — Automatisches Code-Review ins Messaging
4. **🏆 Browser-Automatisierung (Shopping, Formulare)** — Spart echte Zeit
5. **🏆 SNAG Screenshot→Markdown** — Developer-Productivity-Boost
6. **🏆 Voice Wake / Talk Mode** — Freihändiger Assistent
7. **🏆 Persönliches Gedächtnis (MEMORY.md)** — Agent der dich kennt
8. **🏆 Cron-basierte Webhooks + Benachrichtigungen** — Eigene Automationen
9. **🏆 Custom Skills (Weinkeller, Transport, etc.)** — Persönliches Toolkit bauen
10. **🏆 Multi-Channel Gateway** — Ein Agent, überall erreichbar

---

## Ressourcen

- **Docs:** <https://docs.openclaw.ai>
- **GitHub:** <https://github.com/openclaw/openclaw>
- **Discord:** <https://discord.gg/clawd>
- **Showcase:** <https://docs.openclaw.ai/start/showcase>
- **ClawHub (Skills):** <https://clawhub.com>
- **YouTube Walkthrough:** <https://www.youtube.com/watch?v=SaWSPZoPX34>
