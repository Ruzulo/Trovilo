# Scraping Resources

Manuelle Google Maps Lead-Generierung für Local SEO Kundenakquise.

## 📁 Files

### `SCRAPING_GUIDE.md`
Vollständige Anleitung für manuelle Google Maps Scraping:
- Schritt-für-Schritt Prozess
- Qualifizierungs-Kriterien (SEO Score 1-10)
- Best Practices & Quality Checks
- Apify Alternative für später

### `APIFY_SETUP_GUIDE.md` ✨ NEU
Automatisiertes Scraping mit Apify ($5 Budget):
- 25 Suchbegriffe (Penzberg, Weilheim, Peiting, Murnau)
- Optimiert für 150-200 Businesses
- CSV Export → Google Sheets Import
- Duplicate Removal & Scoring

### `GOOGLE_SHEETS_FORMULAS.md`
Auto-Scoring & Priorisierung:
- SEO Score Formel (1-10)
- Bedingte Formatierung
- Priority Flags (🟢 TOP / 🟡 MEDIUM / ⚪ LOW)
- Conversion Estimates
- Package Recommendations

### `N8N_APIFY_WORKFLOW.md`
n8n Integration für vollautomatische Lead-Gen:
- Apify → Google Sheets Pipeline
- Auto-Scoring via JavaScript
- Email Notifications
- Monatliche Scheduling

### `templates/lead-tracking-template.csv`
Google Sheets Import-Template mit allen Spalten

### `examples/example-cafe-penzberg.csv`
10 Beispiel-Cafés aus Penzberg mit realistischem Scoring

## 🎯 Quick Start

### Option A: Apify (Empfohlen für $5 Budget)

1. **Setup Apify:** Folge `APIFY_SETUP_GUIDE.md`
2. **Run Actor:** 25 Suchbegriffe, 10-20 Min
3. **Import CSV:** → Google Sheets
4. **Apply Formulas:** `GOOGLE_SHEETS_FORMULAS.md`
5. **Qualify Top 50:** Manuelle Checks (2-3h)
6. **Result:** 150-200 Businesses, 50-80 Top Leads

**Zeit:** 30 Min Setup + 2-3h Qualifizierung = ~3h total
**Kosten:** $4-5

### Option B: Manuell (Für Learning / Kleine Tests)

1. **Import Template:** `lead-tracking-template.csv` → Google Sheets
2. **Lies Guide:** `SCRAPING_GUIDE.md`
3. **Test:** Scrape erste 10 Cafés in Penzberg (~30-45min)
4. **Priorisiere:** Sortiere nach SEO Score (3-6 = beste Leads)
5. **Outreach:** Nutze Prompts aus `/prompts/PROMPT_LIBRARY.md`

**Zeit:** 30-45 Min für 10, 2-3h für 50
**Kosten:** €0

## 💡 SEO Score Guide

- **1-2:** Zu schwach, kein Bedarf oder Budget
- **3-6:** ✅ BESTE LEADS - Potenzial + Budget
- **7-10:** Bereits gut optimiert, kein Bedarf

## ⏱️ Zeit-Investment

- 10 Businesses: 30-45min
- 50 Businesses: 2-3h
- 100 Businesses: 5-8h

## 🚀 Upgrade Path

**Wann zu Apify wechseln:**
- Expansion nach München (>500 Businesses)
- Regelmäßige monatliche Updates
- Multi-Stadt Skalierung

---

**Version:** 1.0  
**Datum:** 12.02.2026
