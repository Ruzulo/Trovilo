# Google Sheets SEO Score Formeln
**Automatische Lead-Qualifizierung**

---

## HAUPTFORMEL: SEO Score (1-10)

**Diese Formel identifiziert automatisch Businesses mit schlechten Profilen!**

**Spalte L, Zeile 2:**

```excel
=MIN(10, MAX(1, 10 - IF(G2>50, 2, IF(G2>20, 1, 0)) - IF(F2>4.5, 2, IF(F2>4.0, 1, 0)) - IF(H2>30, 2, IF(H2>10, 1, 0)) - IF(E2<>"", 1, 0)))
```

**Dann: Formel nach unten kopieren für alle 129 Zeilen!**

---

## WIE FUNKTIONIERT ES?

**Start-Wert:** 10 Punkte (maximal schlecht = bester Lead für dich!)

**Abzüge:**

1. **Reviews (Spalte G):**
   - >50 Reviews: -2 Punkte (zu etabliert)
   - 20-50 Reviews: -1 Punkt (mittel)
   - <20 Reviews: -0 Punkte (gut für uns!)

2. **Rating (Spalte F):**
   - >4.5 Sterne: -2 Punkte (zu gut, brauchen wenig Hilfe)
   - 4.0-4.5 Sterne: -1 Punkt (okay)
   - <4.0 Sterne: -0 Punkte (Verbesserungspotential!)

3. **Fotos (Spalte H):**
   - >30 Fotos: -2 Punkte (sehr aktiv)
   - 10-30 Fotos: -1 Punkt (mittel aktiv)
   - <10 Fotos: -0 Punkte (wenig Content!)

4. **Website (Spalte E):**
   - Hat Website: -1 Punkt
   - Keine Website: -0 Punkte (großes Defizit!)

**Ergebnis:**
- **1-2:** Sehr schwach (evtl. kein Budget)
- **3-6:** ✅ **BESTE LEADS** (Potenzial + Budget)
- **7-10:** Zu gut optimiert (kein Bedarf)

---

## WICHTIGSTE SPALTEN AUS APIFY CSV:

Apify gibt dir viele Spalten. Behalte diese:

- `title` → **Name** (Spalte B)
- `address` → **Adresse** (Spalte C)
- `phoneNumber` → **Telefon** (Spalte D)
- `website` → **Website** (Spalte E)
- `totalScore` → **Rating** (Spalte F)
- `reviewsCount` → **Reviews** (Spalte G)
- `imageCount` → **Fotos** (Spalte H)
- `categoryName` → **Branche** (Spalte I)

---

## BONUS-FORMELN

### Priority Flag (automatisch)

**Spalte P, Zeile 2:**

```excel
=IF(AND(L2>=3, L2<=6, G2<30), "🟢 TOP LEAD", IF(AND(L2>=4, L2<=7), "🟡 MEDIUM", "⚪ LOW"))
```

**Was es tut:**
- 🟢 **TOP LEAD:** Score 3-6 UND <30 Reviews
- 🟡 **MEDIUM:** Score 4-7
- ⚪ **LOW:** Alles andere

---

## FILTER SETZEN

**Nach Formeln einfügen:**

1. Markiere Header-Zeile (Zeile 1)
2. **Data → Create a filter**
3. **Sortiere nach SEO_Score** (Spalte L) - niedrigste zuerst
4. **Filter:** SEO_Score zwischen 3 und 6

**Das sind deine Top Leads!**

---

**Version:** 1.0  
**Datum:** 13.02.2026
