# HEARTBEAT.md

## Regelmäßige Checks (rotierend, 2-3x täglich)
- [ ] **Email**: `GOG_ACCOUNT=jonasmeier294@gmail.com gog gmail search 'newer_than:1d is:unread' --max 10` — Wichtiges an Johannes melden
- [ ] **Kalender**: `GOG_ACCOUNT=jonasmeier294@gmail.com gog calendar events primary --from <today> --to <tomorrow+1>` — Anstehende Termine melden
- [ ] **GitHub**: `gh notification list --all` — Notifications, PR-Reviews, Issues prüfen

## Memory-Pflege (jeden Heartbeat!)
- [ ] Prüfen ob `memory/<today>.md` existiert — wenn nicht, anlegen
- [ ] Falls diese Session wichtige Infos enthält: sofort in Tagesnotiz schreiben
- [ ] Alle paar Tage: MEMORY.md mit neuen Erkenntnissen updaten

## Proaktives Arbeiten
- [ ] **Offene Projekt-TODOs** prüfen (letzte Tagesnotiz lesen → gibt es unerledigte Aufgaben?)
- [ ] Wenn was offen ist und ich es selbständig erledigen kann → machen und Johannes kurz informieren
- [ ] Bei Problemen die ich allein lösen kann (z.B. fehlgeschlagene Builds) → fixen

## Check-in bei Johannes
- [ ] Wenn >4h seit letztem Kontakt und es gibt was zu berichten → kurze Nachricht
- [ ] Wenn ein Projekt-Meilenstein erreicht → melden

## Regeln
- Nachts (23:00–08:00) still sein, außer es ist dringend
- Nur melden wenn was Wichtiges da ist
- Memory IMMER schreiben, nicht "merken"
- Heartbeat-State in memory/heartbeat-state.json tracken
