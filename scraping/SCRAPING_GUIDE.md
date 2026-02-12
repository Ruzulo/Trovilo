# Google Maps Scraping Guide
**Trovilo Local SEO - Manuelle Lead-Generierung**

---

## Warum Manuell?

✅ **Vorteile:**
- €0 Kosten (vs. €49/Monat Apify)
- Perfekt für kleine Regionen wie Penzberg
- Volle Kontrolle über Datenqualität
- Direkt qualifizieren während Scraping

❌ **Nachteile:**
- Zeit-Investment (2-3h pro Branche/Stadt)
- Nicht skalierbar für >500 Businesses
- Manuelle Updates nötig

**Upgrade zu Apify später wenn:** Du expandierst zu München oder willst 1000+ Leads automatisch

---

## Google Sheet Template

**Kopiere dieses Template:**
```
ID | Name | Adresse | Telefon | Website | Rating | Reviews | Fotos | GBP Vollständigkeit | Letzte Aktivität | SEO Score | Notizen | Kontaktiert | Status | Datum
```

### Spalten-Erklärung:

| Spalte | Was eintragen | Warum wichtig |
|--------|---------------|---------------|
| **ID** | Fortlaufende Nummer (1, 2, 3...) | Eindeutige Referenz |
| **Name** | Firmenname aus Google Maps | Identifikation |
| **Adresse** | Vollständige Adresse | Lokal-Bezug prüfen |
| **Telefon** | Telefonnummer | Outreach-Kanal |
| **Website** | URL (wenn vorhanden) | SEO-Analyse möglich |
| **Rating** | Sterne-Bewertung (z.B. 4.5) | Qualitäts-Indikator |
| **Reviews** | Anzahl Bewertungen | Engagement-Level |
| **Fotos** | Anzahl Fotos im GBP | Content-Aktivität |
| **GBP Vollständigkeit** | Skala 1-10 oder Niedrig/Mittel/Hoch | Lead-Qualität |
| **Letzte Aktivität** | Datum letzter Google Post | Aktiv vs. Inaktiv |
| **SEO Score** | Eigene Bewertung 1-10 | Verbesserungspotential |
| **Notizen** | Auffälligkeiten | Kontext für Outreach |
| **Kontaktiert** | Datum Erstkontakt | CRM-Funktion |
| **Status** | Lead/Kontaktiert/Interessiert/Kunde | Pipeline-Tracking |
| **Datum** | Wann gescraped | Aktualität |

---

## Schritt-für-Schritt Anleitung

### **Schritt 1: Google Maps öffnen**

1. Gehe zu [Google Maps](https://www.google.com/maps)
2. Suche nach: `Café Penzberg`
   - Für andere Branchen: `[BRANCHE] [STADT]` (z.B. "Zahnarzt Penzberg", "Elektriker Weilheim")

### **Schritt 2: Ergebnisliste durchgehen**

**Was du siehst:**
- Liste von Businesses auf der linken Seite
- Meist 20-30 Ergebnisse für kleine Städte wie Penzberg

**Für jedes Business:**

1. **Klicke auf den Business-Namen** → öffnet Details-Panel

2. **Kopiere folgende Daten:**
   - **Name:** Direkt unter Profilbild
   - **Rating:** Sterne + Anzahl (z.B. "4.5 ⭐ (120)")
   - **Adresse:** Unter "Adresse"
   - **Telefon:** Unter "Telefon" (falls vorhanden)
   - **Website:** Button "Website" (falls vorhanden)

3. **Scrolle im Detail-Panel runter:**
   - **Fotos:** Klicke auf "Fotos" Tab → zähle ungefähr (z.B. "50+")
   - **Letzte Aktivität:** Scrolle zu "Updates" → siehst du Google Posts? Wenn ja, notiere letztes Datum

4. **Bewerte GBP Vollständigkeit (1-10):**
   - **10/10:** Alle Felder ausgefüllt, 10+ Fotos, regelmäßige Posts, 4+ Sterne, 50+ Reviews
   - **7/10:** Meiste Felder ausgefüllt, einige Fotos, keine Posts
   - **4/10:** Nur Name/Adresse/Telefon, wenige Fotos, keine Reviews
   - **1/10:** Minimal-Profil, keine Website, keine Fotos

5. **Bewerte SEO Score (1-10):**
   - **1-3:** Sehr schlecht (unvollständig, keine Website, keine Reviews)
   - **4-6:** Mittelmäßig (Basics vorhanden, aber kaum Aktivität)
   - **7-10:** Gut (vollständig, aktiv) → **NICHT dein Zielkunde!**

6. **Notizen:**
   - Auffälligkeiten: "Keine Website", "Nur 2 Fotos", "Letzte Aktivität 2023", "Viele negative Reviews"

### **Schritt 3: In Google Sheet eintragen**

**Tipp:** Nutze Tastaturkürzel
- Strg+C / Strg+V für Copy/Paste
- Tab-Taste um zur nächsten Spalte zu springen

**Beispiel-Eintrag:**
```
1 | Café Glück | Bahnhofstraße 12, 82377 Penzberg | 08856 1234 | www.cafe-glueck.de | 4.5 | 85 | 30+ | 7/10 | Keine Posts | 6/10 | Keine Google Posts, Website veraltet | | Lead | 12.02.26
```

### **Schritt 4: Qualifizierung**

**BESTE LEADS (SEO Score 3-6):**
- Haben Potenzial, aber vernachlässigen Digital Marketing
- Brauchen Hilfe, können sich Service leisten
- **Priorisiere diese!**

**SCHLECHTE LEADS (SEO Score 1-2):**
- Zu wenig aktiv, evtl. kein Budget
- Oder: Geschäft existiert nicht mehr

**KEINE LEADS (SEO Score 7-10):**
- Machen schon alles richtig
- Haben wahrscheinlich bereits Agentur

---

## Test: "Café Penzberg"

**Ziel:** Scrape die ersten 10 Cafés in Penzberg

**Erwartete Zeit:** 30-45 Minuten

**Vorgehen:**
1. Google Maps → "Café Penzberg"
2. Durchgehe Liste von oben nach unten
3. Stoppe nach 10 Einträgen
4. Sortiere Sheet nach "SEO Score" (niedrigste zuerst)
5. Die Top 3-5 mit schlechtestem Score = deine ersten Outreach-Targets

**Nach dem Test:**
- Du hast Gefühl für Qualität entwickelt
- Weißt, wie lange 50 Businesses dauern (~2-3h)
- Kannst Prozess optimieren

---

## Export-Struktur für n8n/Outreach

### Format: CSV Export

**Spalten für Outreach-Workflow:**
```
Name, Telefon, Website, Rating, SEO_Score, Notizen
```

**Nutze diese für:**
- Cold Call Liste (sortiert nach SEO Score)
- Email Outreach (nur mit Website)
- Priorisierung (SEO Score 3-6)

### n8n Integration (später)

Wenn du willst, können wir später einen Workflow bauen:
1. Google Sheet → Read Data
2. Filter: SEO Score 3-6
3. Für jeden Lead:
   - Generiere personalisierte Email (Claude API)
   - Sende Email via Gmail
   - Markiere als "Kontaktiert" im Sheet

---

## Branchen-Prioritäten für Penzberg

**Starte mit:**
1. ✅ **Cafés/Restaurants** (10-15 in Penzberg)
2. ✅ **Handwerk** (Elektriker, Klempner, Maler) (20-30)
3. ✅ **Gesundheit** (Zahnarzt, Physio, Apotheken) (10-15)
4. **Einzelhandel** (Blumen, Boutiquen) (15-20)
5. **Business Services** (Steuerberater, IT) (10-15)

**Total:** ~100-150 Businesses → 5-8 Stunden Scraping-Zeit

---

## Quality Checks

**STOP und überprüfe nach jeweils 20 Einträgen:**

❓ **Sind die Daten vollständig?**
- Fehlt oft Telefon oder Website? → Notiere "nicht vorhanden"

❓ **Ist die Bewertung konsistent?**
- SEO Score 6 für Business mit 4.8 Rating & 200 Reviews? → Zu hoch!
- SEO Score 3 für Business ohne Reviews? → Richtig!

❓ **Sind die Notizen hilfreich für Outreach?**
- "Schlecht" → ❌ Zu vage
- "Keine Google Posts seit 2023, nur 3 Fotos, Website veraltet" → ✅ Konkret!

---

## Next Steps nach Scraping

**Mit deiner Lead-Liste kannst du:**

1. **Priorisieren:** Sortiere nach SEO Score (3-6 = beste Targets)
2. **Cold Outreach starten:**
   - Nutze Prompts aus Prompt Library
   - Personalisiere mit Notizen aus Sheet
3. **Tracking:** Markiere Status (Kontaktiert → Interessiert → Kunde)
4. **n8n Automation bauen:** (Quest 4.x)
   - Auto-Email Generator
   - Follow-Up Sequences

---

## Alternative: Apify (für später)

**Wenn du skalieren willst:**

### Apify Setup (Quick Guide)

1. **Account:** [Apify.com](https://apify.com) → Sign Up
2. **Free Trial:** $5 credit (reicht für ~500 Businesses)
3. **Actor:** "Google Maps Scraper" by [Apify Maps Scraper](https://apify.com/compass/crawler-google-places)

**Kosten nach Trial:**
- ~$49/month für 1000 Scrapes/Monat
- Pay-as-you-go: $0.05 pro Business

**Setup:**
```json
{
  "searchStrings": ["Café Penzberg", "Restaurant Weilheim"],
  "maxCrawledPlaces": 100,
  "includeWebsite": true,
  "includeReviews": true,
  "language": "de"
}
```

**Output:** JSON/CSV → direkt in Google Sheets oder n8n

**Wann Apify nutzen:**
- München (1000+ Restaurants)
- Regelmäßige Updates (monatlich)
- Multi-Stadt Expansion

---

**Version:** 1.0  
**Datum:** 12.02.2026  
**Autor:** Trovilo Team
