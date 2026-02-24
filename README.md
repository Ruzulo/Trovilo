# Trovilo – KI-gestützter Local SEO Service

> **Status: ⏹️ Experiment beendet (Februar 2026)**

## Was ist Trovilo?

Trovilo war ein Experiment: Kann eine Einzelperson mit modernen KI-Tools in wenigen Tagen einen funktionsfähigen Local-SEO-Service aufbauen – von der Website über automatisierte Audits bis zur Kundenakquise?

**Die Antwort: Technisch ja. Kommerziell – nicht ohne Product-Market-Fit.**

Dieses Repository dokumentiert den gesamten Aufbau als Portfolio-Showcase und ehrlichen Erfahrungsbericht.

## 🔗 Live Demo

- **Website:** [trovilo.de](https://trovilo.de) (Showcase-Modus)
- **Beispiel-Audit:** [trovilo.de/audit-beispiel.html](https://trovilo.de/audit-beispiel.html)

## Was wurde gebaut (in wenigen Tagen)

### Website & Audit-System
- Responsive Landing Page mit Pricing, FAQ, Case Study
- Automatisiertes GBP-Audit-System (Claude API generiert komplette Reports aus einem Google-Maps-Link)
- Anonymisierter Beispiel-Audit als Demo

### Automation & Workflows (n8n)
- Google Posts Generator (4 Kategorien: Tipp, Angebot, Behind-the-Scenes, FAQ)
- Keyword Research Generator
- Review Response Generator
- Lead-Scraping-Pipeline (Google Maps → Google Sheets)

### KI-Prompts & Templates
- Wiederverwendbare Prompt-Library für Local SEO Tasks
- Google Posts Template mit strukturiertem Output
- Audit-Generierung via Claude API

### Lead-Generierung
- Google Maps Scraping Guide (manuell + Apify)
- Scoring-System für Lead-Qualifizierung (SEO Score 1-10)
- Tracking-Templates für Pipeline-Management

## Tech Stack

| Komponente | Tool |
|---|---|
| KI-Content | Claude API (Anthropic) |
| Automation | n8n (Cloud + VPS) |
| Website | HTML/CSS/JS, gehostet bei IONOS |
| Lead-Scraping | Google Maps, Apify |
| Versionierung | GitHub |
| Design | Canva |

## Marktvalidierung & Learnings

### Was passiert ist
- 15 Kaltakquise-Anrufe bei lokalen Handwerkern (Elektriker, Spengler, Maler)
- **Ergebnis: 0 Conversions**
- Häufigste Antwort: *"Ich kann mich vor Aufträgen kaum retten"*

### Zentrale Erkenntnisse

**1. Zielgruppe falsch gewählt**
Handwerker in der Region sind chronisch überlastet – sie haben kein Kundenproblem. Bessere Zielgruppen wären Restaurants, Friseure, Fahrschulen oder Reinigungsfirmen gewesen.

**2. Build vs. Validate**
~90% der Zeit floss in Technik, ~10% in Verkaufen. Die Reihenfolge hätte umgekehrt sein müssen: erst validieren, dann bauen.

**3. Etablierte Konkurrenz**
Regionale SEO-Agenturen bedienen den Markt bereits. Der Preisvorteil durch KI-Effizienz reicht allein nicht als Differenzierung.

**4. Regulatorische Hürden (DSGVO)**
Automatisierte Massen-Outreach per E-Mail ist in Deutschland rechtlich problematisch. Kaltakquise per Telefon bleibt der einzige skalierbare Kanal – aber der skaliert schlecht als Solo-Unternehmer.

**5. Twitter/X ≠ Realität**
Die "AI + Local SEO = goldmine"-Posts auf X beschreiben ein US-Markt-Szenario. Der deutsche KMU-Markt funktioniert anders.

## Repository-Struktur

```
Trovilo/
├── website/           # Live-Website (trovilo.de) + Beispiel-Audit
├── workflows/         # n8n Workflow JSON-Exports
├── prompts/           # Claude API Prompt-Templates
├── scraping/          # Google Maps Lead-Gen (Guides, Config, Templates)
├── docs/              # Setup-Dokumentation (n8n, APIs)
└── README.md          # Diese Datei
```

## Für wen ist dieses Repo interessant?

- **Gründer**, die mit KI-Tools ein Service-Business aufbauen wollen (und aus meinen Fehlern lernen möchten)
- **Entwickler**, die sehen wollen, wie man Claude API, n8n und Web-Scraping zu einem funktionierenden Produkt verbindet
- **Local-SEO-Interessierte**, die Prompt-Templates und Workflow-Vorlagen suchen

## Über den Autor

Gebaut während eines 3-monatigen Sabbaticals (Dez 2025 – Feb 2026) als Experiment, ob man mit KI-Tools als Solo-Unternehmer ein profitables Service-Business aufbauen kann.

**Fazit:** Die Technik war das Einfache. Product-Market-Fit bleibt die eigentliche Herausforderung – egal wie gut die Tools sind.

## Lizenz

Dieses Repository ist öffentlich zugänglich als Portfolio und Lernressource.

© 2026 Mario Grüttner
