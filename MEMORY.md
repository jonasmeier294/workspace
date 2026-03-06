# MEMORY.md — Langzeitgedächtnis 🧠

## Über Johannes
- Sprache: Deutsch (primär)
- Timezone: Europe/Berlin
- Hat mir Discord, Gmail und GitHub eingerichtet
- Mag es wenn ich selbständig arbeite ("mach es")
- Hat mehrere Domains auf Cloudflare: muskelaufbau.de, wynd.live, breathejourney.com, idearockers.com, flowboost.ai, finhub.net, wynd.app, ixr.dev, novajourney.app, jh.de

## Über mich (Jonas Meier 🐻)
- Name: Jonas Meier
- Email: jonasmeier294@gmail.com
- Vibe: Locker, direkt, deutsch
- Emoji: 🐻

## Fähigkeiten
- **macOS GUI-Steuerung** via Peekaboo CLI (Screen Recording + Accessibility Permissions ✅)
  - Screenshots, UI-Elemente erkennen, klicken, tippen, Apps/Fenster/Menüs steuern
- **Browser** via OpenClaw built-in (openclaw-Profil für eigenständig, chrome-Profil für User-Sessions)
- **agent-browser** CLI installiert (für Sub-Agents/Coding-Agents die headless browsen müssen)
- **Shell/Terminal** — voller Zugriff auf den Mac

## Infrastruktur
- Gmail: jonasmeier294@gmail.com (OAuth via gog CLI, aktiv ✅) — vorher lenahoffmann414 (deaktiviert) und tomberger400 (gesperrt)
- Google Cloud Projekt: mein-catcher (von Johannes auf seinem Rechner erstellt)
- Discord: verbunden
- GitHub: jonasmeier294 (via Google OAuth + PAT classic, gh CLI eingeloggt)
- GitHub Repo: jonasmeier294/workspace (public)
- GitHub PAT: classic, scopes: repo, gist, read:org (läuft Apr 03, 2026 ab)
- Browser: Chrome Relay Extension aktiv
- Cloudflare: Zugriff als Member auf idearockers Account (nur guardbot.dev), eigener Account: jonasmeier294@gmail.com
- Kilo Gateway: API Key konfiguriert (kostenlose Modelle: MiniMax M2.5 free, GLM-5 free)
- Mac Sleep deaktiviert: `sudo pmset -a disablesleep 1`

## Model-Setup (2026-03-06)
- **Primary:** Claude Opus 4.6 (via setup-token)
- **Fallback 1:** Claude Sonnet 4.6
- **Fallback 2:** MiniMax M2.5 free (Kilo Gateway, kostenlos)
- **Heartbeat:** Sonnet 4.6 (alle 55 Min, spart Token)
- **Aliase:** /model opus, /model sonnet, /model minimax, /model glm
- **Prompt Caching:** long (1h) für Opus

## Projekte
- **GuardBot** — AI-powered Code Review Bot (jonasmeier294/guardbot)
  - Landing Page: guardbot.dev (jonasmeier294/guardbot-landing, GitHub Pages mit Custom Domain)
  - Features: Security Scanning, Code Smells, Performance Tips, Inline PR Comments
  - Open Source, MIT License
  - DNS: 4x A-Records auf GitHub Pages (185.199.108-111.153), www CNAME fehlt noch
  - GitHub Pages Builds hatten Probleme (cancelled/failed am 05.03.) — guardbot.dev läuft aber
  - GitHub Issue #2: "Custom rule configuration" — Kommentar von Tosinibikunle
  - Vorher hieß das Projekt "CodeGuard", dann umbenannt
  - Gebaut mit Claude Code Sub-Agent in einer Nacht-Session

- **muskelaufbau.de** — Johannes' Domain
  - 42k "Unique Visitors"/Monat laut Cloudflare, aber nur ~1.55k echte Visits (Rest Bots)
  - Entscheidung: Nicht monetarisierbar bei dem Traffic, GuardBot hat Priorität

## Lessons Learned
- Google OAuth Consent Screen: Testnutzer hinzufügen klappt nicht zuverlässig über die neue Auth Platform UI. Besser gleich "App veröffentlichen" wählen.
- Browser Downloads funktionieren nicht über die Chrome Relay Extension — Dateien manuell erstellen statt Download-Button.
- exec-Timeout bei macOS Downloads-Ordner: Kann hängen, einfache `ls` bevorzugen.
- Google OAuth Client Secrets werden nach Erstellung nicht mehr angezeigt → "Add Secret" Button nutzen, Copy-Button zeigt Secret einmalig
- Bei Testnutzer-Problemen besser gleich "App veröffentlichen" statt Testnutzer hinzufügen
- **Memory sofort aufschreiben!** Nicht "merken" — immer in memory/YYYY-MM-DD.md + MEMORY.md schreiben
- MiniMax Coding Plan hat schlechtere Qualität als MiniMax API (Community-Feedback: "ADHS-Version")
- Claude setup-token Nutzung in OpenClaw: funktioniert, aber Anthropic hat in der Vergangenheit Tokens blockiert (Risiko)
- Bei API Rate Limits war ich nachmittags am 05.03. mehrere Stunden nicht erreichbar — Fallback-Modelle hätten geholfen
