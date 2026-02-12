# Google Posts Generator - Prompt Template

## Verwendung in n8n Code Node

```javascript
const apiBody = {
  model: 'claude-sonnet-4-20250514',
  max_tokens: 2000,
  messages: [{
    role: 'user',
    content: `Du bist ein Google Business Profile Experte. Erstelle 4 verschiedene Google Posts für folgendes Business:

Firmenname: ${inputData.firmenname}
Branche: ${inputData.branche}
Stadt: ${inputData.stadt}
Besonderheit: ${inputData.besonderheit}

Erstelle 4 Posts in verschiedenen Kategorien:
1. TIPP/WISSEN: Nützlicher Branchen-Tipp für Kunden
2. ANGEBOT: Verlockende Aktion oder Rabatt
3. BEHIND-THE-SCENES: Einblick ins Team oder Prozess
4. FAQ: Beantworte häufige Kundenfrage

Jeder Post:
- Max 1500 Zeichen
- Beginnt mit passendem Emoji
- Endet mit Call-to-Action
- Lokalen Bezug zu ${inputData.stadt} einbauen
- Natürlich & authentisch schreiben
- Keine Hashtags (wirken spammy)

ANTWORTE NUR mit diesem JSON-Format, NICHTS ANDERES:
{
  "posts": [
    {"kategorie": "TIPP", "text": "...", "cta": "..."},
    {"kategorie": "ANGEBOT", "text": "...", "cta": "..."},
    {"kategorie": "BEHIND-THE-SCENES", "text": "...", "cta": "..."},
    {"kategorie": "FAQ", "text": "...", "cta": "..."}
  ]
}`
  }]
};
```

## Variablen

- `firmenname`: Name des Unternehmens
- `branche`: Branche/Kategorie (z.B. Gastronomie, Handwerk)
- `stadt`: Standort für lokalen Bezug
- `besonderheit`: USP oder Besonderheit des Business

## Output-Format

Das Prompt erzwingt ein strukturiertes JSON-Format:

```json
{
  "posts": [
    {
      "kategorie": "TIPP",
      "text": "☕ Wussten Sie, dass...",
      "cta": "Besuchen Sie uns in Penzberg!"
    },
    ...
  ]
}
```

## Best Practices

1. **Emoji-Auswahl:** Passend zur Kategorie (💡 für Tipps, 🎁 für Angebote, 👥 für Behind-the-Scenes, ❓ für FAQs)
2. **Lokaler Bezug:** Immer Stadt/Region erwähnen für Local SEO
3. **Call-to-Action:** Konkret und handlungsorientiert
4. **Keine Hashtags:** Wirken auf GBP spammy und unprofessionell
5. **Authentizität:** Natürliche Sprache, keine Marketing-Floskeln

## Beispiel-Output

**TIPP (Gastronomie):**
```
☕ Wussten Sie, dass frisch gemahlener Kaffee nur 30 Minuten sein volles Aroma behält? 

Deshalb mahlen wir bei Test Café in Penzberg jede Bohne erst auf Bestellung. So schmecken Sie den Unterschied - versprochen!

Unser Tipp: Lagern Sie Kaffeebohnen zuhause immer luftdicht und dunkel. Niemals im Kühlschrank - das zerstört die Aromen.

➡️ Kommen Sie vorbei und probieren Sie den Unterschied selbst!
```

## Integration in n8n

1. **Set Node:** Definiert Input-Daten (firmenname, branche, etc.)
2. **Code Node:** Baut API-Body mit diesem Prompt
3. **HTTP Request:** Sendet an Claude API
4. **Code Node:** Parst JSON-Response und formatiert für Output