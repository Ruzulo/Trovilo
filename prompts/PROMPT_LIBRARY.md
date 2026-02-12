# Claude Prompt Library
**Trovilo Local SEO Services**

Wiederverwendbare Prompts für Google Business Profile Optimierung

---

## Verwendung

**Variablen:**
- `[FIRMENNAME]` - Name des Unternehmens
- `[BRANCHE]` - Branche (z.B. Handwerk, Gastro, Gesundheit)
- `[STADT]` - Hauptstadt/Ort
- `[BESONDERHEIT]` - Alleinstellungsmerkmal/USP
- `[SERVICES]` - Angebotene Leistungen
- `[ÖFFNUNGSZEITEN]` - Geschäftszeiten

---

## 1. GBP Description (Google Business Profile Beschreibung)

### Prompt 1.1: Standard GBP Description
```
Schreibe eine professionelle Google Business Profile Beschreibung für:

Firmenname: [FIRMENNAME]
Branche: [BRANCHE]
Stadt: [STADT]
Besonderheit: [BESONDERHEIT]
Services: [SERVICES]

Anforderungen:
- Max 750 Zeichen
- Beginne mit stärkstem USP
- Lokaler Bezug zu [STADT]
- Natürliche Keyword-Integration (Branche + Stadt)
- Call-to-Action am Ende
- Keine übertriebenen Marketing-Floskeln
- Authentisch und vertrauenswürdig
```

### Prompt 1.2: GBP Description - Handwerk
```
Erstelle eine Google Business Beschreibung für einen Handwerksbetrieb:

[FIRMENNAME] - [BRANCHE] in [STADT]
Besonderheit: [BESONDERHEIT]

Fokus:
- Handwerksqualität und Erfahrung betonen
- Schnelle Reaktionszeit/Notdienst erwähnen (falls zutreffend)
- Zertifikate oder Meistertitel einbinden
- Lokale Verankerung (Familienunternehmen, seit X Jahren)
- Konkrete Services auflisten
- Max 600 Zeichen, bodenständiger Ton
```

### Prompt 1.3: GBP Description - Gastronomie
```
Schreibe eine einladende GBP-Beschreibung für Gastronomie:

Restaurant/Café: [FIRMENNAME]
Ort: [STADT]
Besonderheit: [BESONDERHEIT] (z.B. "hausgemachte Pasta", "vegane Optionen")

Anforderungen:
- Atmosphäre und Ambiente beschreiben
- Kulinarische Highlights nennen
- Lokale Zutaten/Lieferanten erwähnen (wenn zutreffend)
- Öffnungszeiten-Hinweis (z.B. "täglich geöffnet")
- Reservierungsmöglichkeit erwähnen
- Warm und einladend, max 700 Zeichen
```

### Prompt 1.4: GBP Description - Gesundheit
```
Verfasse eine vertrauenswürdige GBP-Beschreibung für Gesundheitsdienstleister:

Praxis: [FIRMENNAME]
Fachgebiet: [BRANCHE] (z.B. Zahnarzt, Physiotherapie)
Standort: [STADT]
Besonderheit: [BESONDERHEIT]

Wichtig:
- Expertise und Qualifikationen betonen
- Behandlungsschwerpunkte auflisten
- Moderne Ausstattung/Technologie erwähnen
- Patienten-Komfort (z.B. "angstfreie Behandlung", "barrierefreier Zugang")
- Terminbuchung erwähnen
- Seriös und professionell, max 750 Zeichen
```

---

## 2. Google Posts

### Prompt 2.1: 4 Google Posts (Multi-Category)
```
Erstelle 4 verschiedene Google Posts für:

Firmenname: [FIRMENNAME]
Branche: [BRANCHE]
Stadt: [STADT]
Besonderheit: [BESONDERHEIT]

Kategorien:
1. TIPP/WISSEN: Nützlicher Branchen-Tipp für Kunden
2. ANGEBOT: Verlockende Aktion oder Rabatt
3. BEHIND-THE-SCENES: Einblick ins Team oder Prozess
4. FAQ: Beantworte häufige Kundenfrage

Jeder Post:
- Max 1500 Zeichen
- Beginnt mit passendem Emoji
- Endet mit Call-to-Action
- Lokalen Bezug zu [STADT] einbauen
- Natürlich & authentisch schreiben
- Keine Hashtags

JSON Format:
{
  "posts": [
    {"kategorie": "TIPP", "text": "...", "cta": "..."},
    {"kategorie": "ANGEBOT", "text": "...", "cta": "..."},
    {"kategorie": "BEHIND-THE-SCENES", "text": "...", "cta": "..."},
    {"kategorie": "FAQ", "text": "...", "cta": "..."}
  ]
}
```

### Prompt 2.2: Saisonaler Google Post - Handwerk
```
Schreibe einen saisonalen Google Post für Handwerksbetrieb:

[FIRMENNAME] - [BRANCHE] in [STADT]
Aktuelle Saison: [SAISON] (z.B. "Winter", "Frühling")

Inhalt:
- Saisonspezifische Tipps (z.B. Winterfest machen, Frühjahrs-Check)
- Lokaler Bezug zu [STADT] (Wetter, typische Probleme)
- Hinweis auf Verfügbarkeit/Terminbuchung
- Max 1200 Zeichen
- Emoji am Anfang
- CTA: "Jetzt Termin vereinbaren"
```

### Prompt 2.3: Angebots-Post - Gastro
```
Erstelle einen verlockenden Angebots-Post für Restaurant/Café:

[FIRMENNAME] in [STADT]
Angebot: [ANGEBOT] (z.B. "Mittagsmenü", "Happy Hour", "Sonntagsbrunch")

Anforderungen:
- Angebot appetitlich beschreiben
- Preis und Zeitraum nennen
- Besondere Highlights (z.B. "inkl. Getränk", "hausgemacht")
- Buchungs-/Reservierungshinweis
- Max 1000 Zeichen
- Emoji 🍽️ oder ähnliches
- Dringlichkeit erzeugen (z.B. "Nur noch diese Woche")
```

### Prompt 2.4: Tipp-Post - Gesundheit
```
Verfasse einen hilfreichen Gesundheits-Tipp als Google Post:

Praxis: [FIRMENNAME]
Fachgebiet: [BRANCHE]
Stadt: [STADT]

Tipp-Thema: [THEMA] (z.B. "Rückenschmerzen vermeiden", "Zahnpflege-Routine")

Struktur:
- Beginne mit Problem-Frage (z.B. "Leiden Sie oft unter...?")
- 3-5 praktische Tipps
- Hinweis auf professionelle Hilfe bei [FIRMENNAME]
- Max 1400 Zeichen
- Emoji 💡 oder 🩺
- Seriös und vertrauenswürdig
```

---

## 3. Review Responses (Bewertungsantworten)

### Prompt 3.1: Review Response Generator (Multi-Sentiment)
```
Schreibe professionelle Antworten für diese Google Reviews:

Review 1:
- Bewertung: [BEWERTUNG]/5 Sterne
- Reviewer: [NAME]
- Text: "[REVIEW_TEXT]"

Review 2:
- Bewertung: [BEWERTUNG]/5 Sterne
- Reviewer: [NAME]
- Text: "[REVIEW_TEXT]"

Review 3:
- Bewertung: [BEWERTUNG]/5 Sterne
- Reviewer: [NAME]
- Text: "[REVIEW_TEXT]"

Richtlinien:
- Bedanke dich IMMER für die Bewertung
- Bei 4-5 Sterne: Freundlich, einladend, persönlich
- Bei 1-2 Sterne: Professionell, lösungsorientiert, Kontaktaufnahme anbieten
- Bei 3 Sterne: Wertschätzend, Verbesserungsbereitschaft zeigen
- Namen des Reviewers verwenden
- Max 100 Wörter pro Antwort
- Natürliche Sprache, keine Marketing-Floskeln

JSON Format:
{
  "antworten": [
    {"antwort": "...", "ton": "freundlich/professionell/entschuldigend"},
    {"antwort": "...", "ton": "..."},
    {"antwort": "...", "ton": "..."}
  ]
}
```

### Prompt 3.2: Positive Review Response
```
Schreibe eine herzliche Antwort auf diese positive Bewertung:

Firma: [FIRMENNAME]
Reviewer: [NAME]
Bewertung: 5 Sterne
Text: "[REVIEW_TEXT]"

Anforderungen:
- Bedanke dich aufrichtig
- Gehe auf spezifische Punkte aus der Bewertung ein
- Lade zum Wiederkommen ein
- Persönlich und warm, nicht zu förmlich
- Max 80 Wörter
- Nutze den Namen des Reviewers
```

### Prompt 3.3: Negative Review Response - Handwerk
```
Verfasse eine professionelle, lösungsorientierte Antwort auf negative Bewertung:

Betrieb: [FIRMENNAME] - [BRANCHE]
Reviewer: [NAME]
Bewertung: 1-2 Sterne
Kritik: "[KRITIKPUNKT]"

Struktur:
- Bedanke dich für Feedback
- Zeige Verständnis für Unzufriedenheit
- Erkläre (falls berechtigt) Situation kurz OHNE Ausreden
- Biete konkrete Lösung oder Wiedergutmachung an
- Gib Kontaktdaten (Telefon/Email) für direkte Klärung
- Max 120 Wörter
- Professionell, nie defensiv
```

---

## 4. FAQs (Häufige Fragen)

### Prompt 4.1: 20 FAQs für GBP
```
Erstelle 20 häufige Fragen und Antworten für Google Business Profile:

Firma: [FIRMENNAME]
Branche: [BRANCHE]
Stadt: [STADT]
Services: [SERVICES]

Kategorien (je 4-5 FAQs):
1. Öffnungszeiten & Erreichbarkeit
2. Preise & Kosten
3. Services & Leistungen
4. Buchung & Termine
5. Besonderheiten & Unterschiede

Anforderungen:
- Fragen so formulieren, wie Kunden wirklich fragen
- Antworten kurz (2-4 Sätze), klar, konkret
- Lokale Keywords einbauen (z.B. "[BRANCHE] [STADT]")
- Professionell aber zugänglich
- Keine Preise nennen, sondern auf Beratung verweisen (bei individuellen Leistungen)

JSON Format:
{
  "faqs": [
    {"frage": "...", "antwort": "..."},
    ...
  ]
}
```

### Prompt 4.2: FAQ - Handwerk (Notdienst & Kosten)
```
Erstelle 5 FAQs speziell für Handwerksbetrieb mit Fokus auf Notdienst & Kosten:

Betrieb: [FIRMENNAME]
Service: [BRANCHE]
Region: [STADT]

Themen:
- Notdienst-Verfügbarkeit
- Kostenvoranschlag
- Anfahrtskosten
- Zahlungsoptionen
- Garantie/Gewährleistung

Pro FAQ:
- Frage präzise
- Antwort max 50 Wörter
- Transparenz bei Kosten ohne konkrete Preise
- Vertrauen schaffen
```

### Prompt 4.3: FAQ - Gastro (Reservierung & Speisen)
```
Schreibe 5 FAQs für Restaurant/Café:

Name: [FIRMENNAME]
Ort: [STADT]
Besonderheit: [BESONDERHEIT]

Fragen zu:
- Reservierung (online/telefonisch)
- Speisekarte (vegetarisch/vegan/glutenfrei)
- Gruppenbuchungen
- Mitnahme/Lieferung
- Parkmöglichkeiten

Stil:
- Einladend und hilfsbereit
- Kurze, klare Antworten
- Hinweis auf Website/Speisekarte
```

---

## 5. Services (Leistungsbeschreibungen)

### Prompt 5.1: Service-Liste für GBP
```
Erstelle eine strukturierte Liste aller Services für Google Business Profile:

Firma: [FIRMENNAME]
Branche: [BRANCHE]
Hauptservices: [SERVICES]

Format für jeden Service:
- Service-Name (prägnant, max 3 Wörter)
- Kurzbeschreibung (1 Satz, 10-20 Wörter)
- Nutzen für Kunden betonen

Kategorien:
- Hauptleistungen (3-5 Services)
- Zusatzleistungen (2-3 Services)
- Notfall/Express-Services (falls zutreffend)

Hinweis: Keine Preise angeben in GBP

JSON Format:
{
  "services": [
    {"name": "...", "beschreibung": "..."},
    ...
  ]
}
```

### Prompt 5.2: Service-Description - Handwerk
```
Schreibe detaillierte Service-Beschreibungen für Handwerksbetrieb:

Betrieb: [FIRMENNAME]
Service: [SERVICE_NAME]
Stadt: [STADT]

Pro Service:
- Was ist enthalten?
- Wie läuft es ab? (Prozess in 3-4 Schritten)
- Wie lange dauert es?
- Was macht euch besonders? ([BESONDERHEIT])
- Warum [FIRMENNAME] in [STADT]?

Länge: 150-200 Wörter pro Service
Ton: Professionell, vertrauenswürdig, bodenständig
```

### Prompt 5.3: Service-Description - Gastro
```
Erstelle ansprechende Menü-/Service-Beschreibungen:

Restaurant: [FIRMENNAME]
Angebot: [SERVICE_NAME] (z.B. "Mittagsmenü", "Catering", "Private Dining")

Beschreibe:
- Was wird geboten?
- Für wen geeignet? (Anlässe, Gruppengröße)
- Besondere Highlights ([BESONDERHEIT])
- Buchungsinfo
- Preishinweis (Bereich, z.B. "ab 25€")

Stil: Appetitlich, einladend, nicht übertrieben
Länge: 100-150 Wörter
```

---

## 6. Keyword Research

### Prompt 6.1: Local SEO Keywords Generator
```
Erstelle eine umfassende Keyword-Liste für Local SEO:

Branche: [BRANCHE]
Hauptstadt: [STADT]
Umkreis-Städte: [STÄDTE]

Kategorien (insgesamt 30 Keywords):
1. SERVICE + LOCATION (12 Keywords)
   - Format: "[BRANCHE] [STADT]", "[SERVICE] [STADT]"
   
2. NEAR ME INTENT (6 Keywords)
   - Format: "[BRANCHE] in der Nähe", "[SERVICE] near me"
   
3. NOTFALL/DRINGEND (4 Keywords)
   - Format: "[BRANCHE] jetzt geöffnet", "[BRANCHE] Notdienst"
   
4. VERGLEICH/QUALITÄT (4 Keywords)
   - Format: "bester [BRANCHE] [STADT]", "günstiger [SERVICE]"
   
5. LONG-TAIL (4 Keywords)
   - Spezifische Kombinationen (z.B. "[BRANCHE] mit [BESONDERHEIT] [STADT]")

Jedes Keyword:
- Suchvolumen-Schätzung (hoch/mittel/niedrig)
- Wettbewerb-Schätzung (hoch/mittel/niedrig)
- Priorität (1-5)

JSON Format:
{
  "keywords": [
    {
      "keyword": "...",
      "kategorie": "SERVICE_LOCATION/NEAR_ME/NOTFALL/VERGLEICH/LONG_TAIL",
      "suchvolumen": "hoch/mittel/niedrig",
      "wettbewerb": "hoch/mittel/niedrig",
      "prioritaet": 1-5
    }
  ]
}
```

---

## 7. Branchenspezifische Best Practices

### Handwerk
- **Tone:** Bodenständig, vertrauenswürdig, kompetent
- **Keywords:** Notdienst, schnell, zuverlässig, Meisterbetrieb
- **CTAs:** "Jetzt Termin vereinbaren", "Kostenlos Angebot anfragen"
- **USPs:** Erfahrung, Qualität, lokale Verankerung, Garantie

### Gastronomie
- **Tone:** Warm, einladend, appetitlich
- **Keywords:** frisch, hausgemacht, regional, gemütlich
- **CTAs:** "Jetzt reservieren", "Karte ansehen", "Bestellen"
- **USPs:** Atmosphäre, Zutaten-Qualität, besondere Gerichte

### Gesundheit
- **Tone:** Professionell, vertrauensvoll, empathisch
- **Keywords:** Expertise, modern, schonend, Termin verfügbar
- **CTAs:** "Termin buchen", "Beratung vereinbaren"
- **USPs:** Qualifikation, Ausstattung, Patientenkomfort

---

## 8. Verwendung in n8n Workflows

Diese Prompts sind optimiert für:
- **Code Nodes:** Template Literals mit `${variable}`
- **API Calls:** JSON-strukturierte Outputs
- **Batch Processing:** Mehrere Items gleichzeitig

Beispiel n8n Integration:
```javascript
const apiBody = {
  model: 'claude-sonnet-4-20250514',
  max_tokens: 2000,
  messages: [{
    role: 'user',
    content: `[PROMPT AUS LIBRARY]
    
    Firmenname: ${firmenname}
    Branche: ${branche}
    Stadt: ${stadt}
    Besonderheit: ${besonderheit}`
  }]
};
```

---

**Version:** 1.0
**Letzte Aktualisierung:** 12.02.2026
**Autor:** Trovilo Team
