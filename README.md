# Trovilo - KI-gestützte Local SEO Automation

> Effiziente Google Business Profile Optimierung für KMUs in Bayern

## 🎯 Über dieses Projekt

Dieses Repository dokumentiert die technische Infrastruktur und Workflows für **Trovilo** - ein Local-SEO-Service-Business, das KMUs in der Region Penzberg/München hilft, ihre Online-Sichtbarkeit durch KI-gestützte Automatisierung zu verbessern.

### Business-Modell
- **Zielgruppe:** Kleine und mittlere Unternehmen (Gastronomie, Handwerk, Gesundheit)
- **Kernservice:** Google Business Profile Optimierung + laufende Betreuung
- **Technologie:** n8n Workflows + Claude API für Content-Generierung
- **Region:** Penzberg, Weilheim, München-Süd

## 📁 Repository-Struktur

```
trovilo-business/
├── workflows/          # n8n Workflow JSON-Exports
├── prompts/           # Claude API Prompt-Templates
├── docs/              # Setup-Guides & SOPs
├── scripts/           # Hilfsskripte
└── README.md          # Diese Datei
```

## 🚀 Services

### Kickstart-Paket (€699)
- Google Business Profile Komplett-Setup
- NAP-Optimierung, Kategorien, Description
- 10-15 professionelle Fotos
- 20 FAQs + 4 Google Posts
- Review-Management Templates
- **Danach:** €169/Monat laufende Betreuung

### Professional-Paket (€899)
- Alles aus Kickstart
- Erweiterte Keyword-Recherche
- Monatliche Content-Erstellung
- **Danach:** €229/Monat Premium-Betreuung

## 🛠️ Tech Stack

- **Automation:** n8n (Cloud + VPS)
- **AI Content:** Anthropic Claude (Sonnet 4)
- **Google APIs:** Sheets, Docs, Drive
- **Design:** Canva Pro
- **Analytics:** Google Search Console

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

## 🔒 Sicherheit

- **Keine API-Keys im Repo!** Alle Credentials in n8n-Credentials oder Environment Variables
- `.gitignore` verhindert versehentliches Pushen von Secrets
- Workflow-JSONs enthalten nur Struktur, keine Credentials

## 📄 Lizenz

Dieses Projekt ist privat und für eigene Business-Zwecke.  
© 2026 Trovilo

## 🤝 Kontakt

Bei Fragen zum Setup oder den Workflows:  
**Email:** [email protected]  
**Domain:** trovilo.de

---

**Status:** 🟢 In aktiver Entwicklung (Sabbatical-Phase bis 28.02.2026)