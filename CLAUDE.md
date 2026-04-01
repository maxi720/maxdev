# maxdev — CLAUDE.md

## Projekt

Private persönliche Website für **maxdev** (GitHub: maxi720).
Remote: `https://github.com/maxi720/maxdev.git`

## Website

Liegt in `website/` — 100 % statisch, kein Build-Tool, kein Framework.

| Datei | Zweck |
|---|---|
| `website/index.html` | Startseite mit Projektkarten-Übersicht (VPS, Quizapp, Skills) |
| `website/vps.html` | VPS-Sicherheits-Guide mit Copy-to-Clipboard-Befehlen |
| `website/quizapp.html` | Quizapp-Seite (QR-Codes App Store / Play Store + Beschreibung) |
| `website/skills.html` | Skills-Seite (Download der Datenschutz-Skills) |
| `website/downloads/` | Downloadbare Dateien (`.skill`-Files) |
| `website/impressum.html` | Deutsches Impressum + Datenschutzerklärung |
| `website/style.css` | Gemeinsames Design-System |

## Design

- Ästhetik: Dark Terminal / Cyberpunk (neon-grün `#39ff83`, cyan `#00e5cc`, fast schwarzer Hintergrund)
- Schriften: ausschließlich System-Font-Stacks (kein CDN) → DSGVO-konform
- Responsive, mobile-first

## DSGVO / GDPR

- Keine Cookies, kein Tracking, keine externen Ressourcen
- Kein Consent-Banner erforderlich
- Impressum verlinkt im Footer jeder Seite
- Server-Logs in Datenschutzerklärung nach Art. 6 Abs. 1 lit. b DSGVO abgedeckt

## Neue Projekte hinzufügen

1. Neue `projektname.html` erstellen (Nav + Footer von bestehender Seite kopieren)
2. `aria-current="page"` auf den passenden Nav-Link setzen
3. Projektkarte in `index.html` ergänzen
4. Nav-Link in **allen** anderen Seiten ergänzen

## Lokal testen

Live Server Extension in VS Code (Port 5500) — Clipboard API funktioniert über `http://127.0.0.1`.

## Git

Branch: `main` — lokaler und Remote-Stand haben divergiert.
Zum Synchronisieren: `git pull origin main --rebase`, dann `git push`.

## Installierte Skills

| Skill | Ordner | Zweck |
|---|---|---|
| `frontend-design` | `.agents/skills/frontend-design` | Distinctive UI-Gestaltung |
| `ui-ux-pro-max` | `.agents/skills/ui-ux-pro-max` | Design-System, UX-Regeln |
| `datenschutz-oesterreich` | `.agents/skills/datenschutz-oesterreich` | DSGVO + DSG Österreich |
| `datenschutz-deutschland` | `.agents/skills/datenschutz-deutschland` | DSGVO + BDSG + TTDSG Deutschland |

> `gdpr-dsgvo-expert` wurde durch die obigen zwei Skills ersetzt und gelöscht.

Die Skill-Quelldateien liegen in `website/downloads/`.
