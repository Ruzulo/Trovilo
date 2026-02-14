# Trovilo - KI-gestützte Local SEO Automation

> Effiziente Google Business Profile Optimierung für KMUs in Bayern

## 🎯 Über dieses Projekt

Dieses Repository dokumentiert die technische Infrastruktur und Workflows für **Trovilo** - ein Local-SEO-Service-Business, das KMUs in der Region Penzberg/München hilft, ihre Online-Sichtbarkeit durch KI-gestützte Automatisierung zu verbessern.

### Business-Modell
- **Zielgruppe:** Kleine und mittlere Unternehmen (Handwerk, Gastronomie, Gesundheit, Einzelhandel)
- **Kernservice:** Google Business Profile Optimierung + laufende Betreuung
- **Technologie:** n8n Workflows + Claude API für Content-Generierung
- **Region:** Penzberg, Bad Tölz, Wolfratshausen, Geretsried (50km Radius)

## 📁 Repository-Struktur

```
Trovilo/
├── workflows/          # n8n Workflow JSON-Exports
├── prompts/           # Claude API Prompt-Templates
├── docs/              # Setup-Guides & SOPs
├── website/           # Trovilo Website (index.html, style.css, script.js)
├── scripts/           # Hilfsskripte
├── BETA-PITCH-BIBLE.md # Sales & Pitch-Skripte
└── README.md          # Diese Datei
```

## 🚀 Services & Preise

### Einmalige Pakete

#### Optimierung (€299)
Für bestehende Profile, die optimiert werden müssen
- ✓ Profil-Check & Kategorien fixen
- ✓ Beschreibung optimieren
- ✓ 5 Google Posts erstellen
- ✓ Bewertungs-System aufsetzen
- ✓ 10-15 FAQs erstellen

#### Kickstart (€599) - Empfohlen
Für neue Profile oder größere Lücken
- ✓ Alles aus "Optimierung"
- ✓ Komplette Profil-Verifikation
- ✓ NAP-Check (5-10 Verzeichnisse)
- ✓ Schema Markup für Website
- ✓ 20-30 FAQs + Services-Liste
- ✓ 2x Follow-up nach 2+4 Wochen

#### Premium (€999)
Für ambitionierte Businesses + Multi-Location
- ✓ Alles aus "Kickstart"
- ✓ **3 Monate Content-Betreuung inklusive**
- ✓ Wöchentliche Google Posts
- ✓ Monatliche Performance-Reports
- ✓ Bewertungs-Management
- ✓ Multi-Location Setup möglich

### Laufende Betreuung (optional, monatlich kündbar)

#### Betreuung Basis (€75/Monat)
"Set & Forget" - Autopilot-Modus
- ✓ Review Monitoring & Antworten
- ✓ Monatlicher Report
- ✓ Spam-Meldung

#### Betreuung Aktiv (€149/Monat) - Beliebt
Aktive Optimierung + Wachstum
- ✓ Alles aus "Basis"
- ✓ 4 Google Posts pro Monat
- ✓ 2 FAQ Updates monatlich
- ✓ Foto-Management (1x/Monat)

## 🛠️ Tech Stack

- **Automation:** n8n (Cloud + VPS)
- **AI Content:** Anthropic Claude (Sonnet 4.5)
- **Google APIs:** Business Profile API, Sheets, Docs, Drive
- **Design:** Canva Pro (via MCP)
- **Analytics:** Google Search Console
- **Website:** GitHub Pages (trovilo.de)

## 📊 Workflows

### ✅ Google Posts Generator
Automatisierte Erstellung von 4 Google Business Profile Posts in verschiedenen Kategorien:
- TIPP/WISSEN
- ANGEBOT
- BEHIND-THE-SCENES
- FAQ

**Status:** Produktiv  
**Details:** [workflows/google-posts-generator.json](workflows/google-posts-generator.json)

### 🔜 Geplante Workflows
- Review Response Generator
- Keyword Research Automation
- GBP Performance Reporting
- Automated Audit Report Generator

## 🎓 Setup-Guides

- [n8n Cloud Setup](docs/n8n-setup.md)
- Claude API Integration (coming soon)
- Client Onboarding Process (coming soon)

## 📝 Prompts

Alle Prompts sind als wiederverwendbare Templates in `/prompts/` verfügbar:
- [Google Posts Template](prompts/google-posts-template.md)
- GBP Description Generator (coming soon)
- FAQ Generator (coming soon)
- Review Response Templates (coming soon)

## 🎯 Sales & Outreach

- **BETA-PITCH-BIBLE.md:** Komplette Sammlung von Cold-Call-Skripten, WhatsApp-Pitches, Audit-Templates, Einwandbehandlung
- **Zielgruppe:** Handwerker (Elektriker, Sanitär, Maler) in Penzberg, Bad Tölz, Wolfratshausen
- **Strategie:** Kostenloses Video-Audit (3-5 Min.) als Lead-Magnet

## 🔒 Sicherheit

- **Keine API-Keys im Repo!** Alle Credentials in n8n-Credentials oder Environment Variables
- `.gitignore` verhindert versehentliches Pushen von Secrets
- Workflow-JSONs enthalten nur Struktur, keine Credentials

## 📈 Aktueller Status

- ✅ Website live auf trovilo.de
- ✅ Pricing finalisiert (€299/€599/€999 + €75/€149)
- ✅ Sales-Materialien fertig (BETA-PITCH-BIBLE.md)
- 🔄 Erste Beta-Kunden werden akquiriert
- 🔜 n8n Workflows werden produktiv gestellt

## 📄 Lizenz

Dieses Projekt ist privat und für eigene Business-Zwecke.  
© 2026 Trovilo

## 🤝 Kontakt

Bei Fragen zum Setup oder den Workflows:  
**Email:** servus@trovilo.de  
**Website:** https://trovilo.de  
**WhatsApp:** +49 160 9790 9740

---

**Status:** 🟢 In aktiver Entwicklung (Sabbatical-Phase bis 28.02.2026)
