# Apify Google Maps Scraper - Setup Guide
**Trovilo Local SEO Lead Generation**

---

## BUDGET: $5 = ~100-250 Businesses

**Actor:** Google Maps Scraper by Compass
**Link:** https://apify.com/compass/crawler-google-places
**Cost:** ~$0.02-0.05 pro Business

---

## SCHRITT 1: Actor öffnen

1. Gehe zu: https://apify.com/compass/crawler-google-places
2. Klicke **"Try for free"** oder **"Run"**
3. Du siehst die Konfiguration-Oberfläche

---

## SCHRITT 2: Konfiguration einfügen

Kopiere diese **optimierte Konfiguration** in die entsprechenden Felder:

### **Search Queries (searchStrings):**

```json
[
  "Café Penzberg",
  "Restaurant Penzberg",
  "Bäckerei Penzberg",
  "Elektriker Penzberg",
  "Klempner Penzberg",
  "Maler Penzberg",
  "Zahnarzt Penzberg",
  "Physiotherapie Penzberg",
  "Friseur Penzberg",
  "Blumenladen Penzberg",
  
  "Café Weilheim",
  "Restaurant Weilheim",
  "Elektriker Weilheim",
  "Klempner Weilheim",
  "Zahnarzt Weilheim",
  "Physiotherapie Weilheim",
  "Friseur Weilheim",
  
  "Café Peiting",
  "Restaurant Peiting",
  "Elektriker Peiting",
  "Zahnarzt Peiting",
  
  "Café Murnau",
  "Restaurant Murnau",
  "Elektriker Murnau",
  "Zahnarzt Murnau"
]
```

**25 Suchbegriffe** × ~8-12 Results = **~200-300 Businesses**
**Erwartete Kosten:** ~$4-5 (perfekt für Budget!)

---

### **Weitere wichtige Settings:**

**Im Apify Actor Input-Feld:**

```json
{
  "searchStrings": [SEE ABOVE],
  "maxCrawledPlaces": 12,
  "language": "de",
  "includeWebsite": true,
  "includeReviews": true,
  "includeImages": true,
  "includeOpeningHours": true,
  "includePeopleAlsoSearch": false,
  "exportPlaceUrls": false,
  "maxReviews": 0,
  "maxImages": 0,
  "scrapeDirectionUrl": false,
  "scrapeReviewerName": false,
  "scrapeReviewId": false,
  "scrapeReviewUrl": false,
  "scrapeResponseFromOwnerText": false
}
```

**Wichtige Parameter erklärt:**

- `maxCrawledPlaces: 12` = Max 12 Ergebnisse pro Suchbegriff (spart Kosten)
- `language: "de"` = Deutsche Ergebnisse
- `includeWebsite: true` = Website-URL (wichtig für Outreach)
- `includeReviews: true` = Review Count & Rating
- `includeImages: true` = Fotos Count (für SEO Score)
- `includeOpeningHours: true` = Öffnungszeiten
- `maxReviews: 0` = KEINE einzelnen Reviews scrapen (spart MASSIV Kosten!)
- `maxImages: 0` = KEINE einzelnen Bilder-URLs (nur Count)

**Warum maxReviews=0?**
- Einzelne Reviews = teuer ($0.001 pro Review)
- Du brauchst nur COUNT + RATING für SEO Score
- Spart ~70% der Kosten!

---

## SCHRITT 3: Run starten

1. **Scrolle nach unten** im Actor
2. Klicke **"Start"** oder **"Run"**
3. **Warte 10-20 Minuten** (je nach Anzahl)
4. Du siehst Live-Progress in der Console

---

## SCHRITT 4: Export

**Nach Completion:**

1. Klicke auf **"Export"** Button
2. Wähle **"CSV"** Format
3. Download die Datei → `apify-google-maps-results.csv`

---

## SCHRITT 5: Import in Google Sheets

1. **Neue Google Sheets** erstellen: "Trovilo Leads"
2. **File → Import → Upload**
3. Wähle `apify-google-maps-results.csv`
4. Import-Settings:
   - Separator: **Comma**
   - Convert text to numbers/dates: **Yes**
5. **Import**

---

## SCHRITT 6: Spalten aufräumen

**Apify gibt dir VIELE Spalten. Wichtigste:**

- `title` = Business Name
- `address` = Adresse
- `phoneNumber` = Telefon
- `website` = Website
- `totalScore` = Rating (z.B. 4.5)
- `reviewsCount` = Anzahl Reviews
- `imageCount` = Anzahl Fotos
- `categoryName` = Branche
- `location.lat` / `location.lng` = Koordinaten

**Lösche unwichtige Spalten:**
- `placeId`, `url`, `additionalInfo`, `description` etc.

**Behalte nur:**
```
A: ID (selbst hinzufügen)
B: title → Name
C: address → Adresse  
D: phoneNumber → Telefon
E: website → Website
F: totalScore → Rating
G: reviewsCount → Reviews
H: imageCount → Fotos
I: categoryName → Branche
J: (NEU) GBP_Vollständigkeit
K: (NEU) Letzte_Aktivität
L: (NEU) SEO_Score
M: (NEU) Notizen
N: (NEU) Status
O: (NEU) Datum
```

---

## SCHRITT 7: SEO Score berechnen (Formel)

**Füge diese Formel in Spalte L (SEO_Score) ein:**

**Zeile 2 (erste Datenzeile):**

```
=MIN(10, MAX(1, 
  10 
  - IF(G2>50, 2, IF(G2>20, 1, 0))
  - IF(F2>4.5, 2, IF(F2>4.0, 1, 0))
  - IF(H2>30, 2, IF(H2>10, 1, 0))
  - IF(E2<>"", 1, 0)
))
```

**Was macht die Formel?**
- Startet bei 10
- **-2 Punkte** wenn >50 Reviews (zu etabliert)
- **-2 Punkte** wenn Rating >4.5 (zu gut)
- **-2 Punkte** wenn >30 Fotos (zu aktiv)
- **-1 Punkt** wenn Website vorhanden (aber nicht zu viel Abzug)
- **Ergebnis:** 1-10 Score

**Beste Leads = Score 3-6** 🎯

**Kopiere Formel** in alle Zeilen nach unten!

---

## SCHRITT 8: Manuelle Felder ergänzen

**Für jede Zeile (oder Top 50):**

1. **Spalte J (GBP_Vollständigkeit):**
   - Öffne Google Maps → Business suchen
   - Bewerte 1-10 (siehe Scraping Guide)
   - Oder schreibe: "Nicht geprüft"

2. **Spalte K (Letzte_Aktivität):**
   - Google Maps → "Updates" Tab checken
   - Schreibe: "Keine Posts" oder "Feb 2026" oder "Nicht geprüft"

3. **Spalte M (Notizen):**
   - Auffälligkeiten notieren
   - Z.B. "Keine Website", "Viele negative Reviews", "Keine Posts - gute Chance!"

4. **Spalte N (Status):**
   - Erstmal leer lassen oder "Lead" eintragen
   - Später: "Kontaktiert", "Interessiert", "Kunde"

---

## SCHRITT 9: Filtern & Priorisieren

**Google Sheets Filter setzen:**

1. Markiere Header-Zeile (Zeile 1)
2. **Data → Create a filter**
3. **Sortiere nach SEO_Score** (niedrigste zuerst)
4. **Filter:** SEO_Score = 3-6

**Top 20-30 Leads markieren:**
- Spalte A: Färbe Zelle **GRÜN** = Top Priority
- Spalte A: Färbe Zelle **GELB** = Medium Priority

---

## SCHRITT 10: Duplicate Removal (wichtig!)

**Apify kann Duplicates haben** (Business in mehreren Städten):

1. **Data → Data cleanup → Remove duplicates**
2. Wähle Spalte **B (Name)** + **C (Adresse)**
3. **Remove duplicates**

**Erwartetes Ergebnis:**
- ~200-300 raw results
- ~150-200 unique businesses nach Deduplication
- ~50-80 Top Leads (Score 3-6)

---

## KOSTEN-TRACKING

**Nach dem Run:**

1. Apify Console → **Usage & Billing**
2. Checke **Costs für diesen Run**
3. Sollte **$3-5** sein

**Wenn >$5:**
- STOP den Run vorher! (du kannst partial results nutzen)
- Reduziere `maxCrawledPlaces` auf 8-10

---

## TROUBLESHOOTING

**Problem: "Zu viele Ergebnisse, >$5"**
→ Lösung: Stoppe Run nach $4, nutze partial results

**Problem: "Duplicate Businesses"**
→ Lösung: Google Sheets → Remove duplicates (siehe Step 10)

**Problem: "Keine Website-Daten"**
→ Lösung: Actor-Settings → `includeWebsite: true` prüfen

**Problem: "Run dauert >30 Min"**
→ Normal! Bei 25 Suchbegriffen kann es 20-30 Min dauern

---

## ERWARTETE ERGEBNISSE

**Nach diesem Setup hast du:**

✅ **~150-200 Unique Businesses** in Penzberg + Umgebung
✅ **Alle relevanten Branchen** (Gastro, Handwerk, Gesundheit, Einzelhandel)
✅ **Vollständige Daten** (Tel, Website, Rating, Reviews, Fotos)
✅ **SEO Score** automatisch berechnet
✅ **Top 50-80 Leads** identifiziert (Score 3-6)
✅ **Budget:** $4-5 (unter $5 Limit!)

---

## NEXT STEPS

**Nach Import:**

1. **Manuelle Qualifizierung** der Top 50 (2-3h)
   - Letzte Aktivität checken
   - GBP Vollständigkeit bewerten
   - Notizen hinzufügen

2. **Erste Outreach-Liste** erstellen (Top 20)
   - Sortiert nach SEO Score
   - Mit personalisierten Notizen

3. **Demo-Audits** vorbereiten (siehe Quest 10.3)

---

**Version:** 1.0  
**Datum:** 12.02.2026  
**Budget:** $5  
**Expected Leads:** 50-80 Top Quality
