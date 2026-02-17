# Trovilo – Status für nächste Chat-Session

> Letzte Aktualisierung: 17.02.2026

## Über Mario (Inhaber)
- **Mario Grüttner** (nicht Marco Riedl!)
- Wohnt in Penzberg, südlich von München
- Aktuell im Sabbatical bis 28.02.2026
- Hauptjob wartet danach → Trovilo als Nebengeschäft
- Ziel: >15.000€/Monat Gewinn → dann Hauptjob kündigen
- Fokus: KMU in 50km Radius um Penzberg
- Kontakt: 0151 2983 2946 · servus@trovilo.de

## Wo stehen wir?

### Website ✅
- trovilo.de ist live bei Ionos (FTP-Deployment)
- GitHub: Ruzulo/Trovilo, branch: main, Ordner: /website
- **Website nicht mehr anfassen!**

### Lead Pipeline
- Google Sheet: https://docs.google.com/spreadsheets/d/1sa6Gx0cMYbqYWU6wVE1tJWdql9k-tkAKtVqQRbj2CoE

### Aktueller Lead-Status
| Lead | Status | Nächster Schritt |
|------|--------|-----------------|
| Nemanja | 🟡 Warten | Meldet sich |
| Elektro Kuhn (Antdorf) | 🟡 Warten | Follow-up ab ~20.02. mit Audit |
| Michael Demml | 🔴 Kein Interesse | - |
| Michael Gärtner | 🔴 Gescheitert | - |

### Outreach-Prozess (beschlossen!)
1. "Ich habe mir Ihr Google Profil angeschaut – da gibt es Potenzial"
2. "Darf ich Ihnen ein kostenloses Audit schicken?"
3. Audit zuschicken → Vertrauen aufbauen → dann Angebot

---

## Audit-Template ✅ (HTML-Format – finale Lösung)

**Format: HTML → PDF** (nicht Google Doc, nicht Canva)
- Pixel-perfektes Layout, immer gleich
- Teal-Tabellen-Header, Score-Box, Farben – alles korrekt
- n8n ersetzt {{VARIABLEN}} im HTML, dann PDF-Export

**Template-Dateien im GitHub:**
- Vorlage: `/audit/trovilo_audit_VORLAGE.html`
- Beispiel Elektro Kuhn: `/audit/audit_elektro_kuhn.html`

**Verwendung:**
1. Im Browser öffnen → Drucken → "Als PDF speichern"
2. Oder: n8n Workflow befüllt Variablen automatisch

**Alle Platzhalter ({{VARIABLE}}):**
- `{{FIRMENNAME}}`, `{{BRANCHE}}`, `{{DATUM}}`
- `{{GBP_SCREENSHOT}}` – Placeholder-Text, Bild manuell einfügen
- `{{SCORE_GESAMT}}` – Gesamtpunktzahl 0-100
- `{{SICHTBARKEIT}}`, `{{LETZTE_AKTIVITAET}}`, `{{ANZAHL_BEWERTUNGEN}}`, `{{BEWERTUNGS_SCHNITT}}`
- `{{BEFUND_VOLLSTAENDIGKEIT}}`, `{{SCORE_VOLLSTAENDIGKEIT}}`
- `{{BEFUND_BEWERTUNGEN}}`, `{{SCORE_BEWERTUNGEN}}`
- `{{BEFUND_LEISTUNGEN}}`, `{{SCORE_LEISTUNGEN}}`
- `{{BEFUND_FOTOS}}`, `{{SCORE_FOTOS}}`
- `{{BEFUND_AKTIVITAET}}`, `{{SCORE_AKTIVITAET}}`
- `{{WETTB_SICHTBARKEIT_SIE}}`, `{{WETTB_1_NAME}}`, `{{WETTB_1_SICHTBARKEIT}}`, `{{WETTB_1_BEWERTUNGEN}}`
- `{{WETTB_2_NAME}}`, `{{WETTB_2_SICHTBARKEIT}}`, `{{WETTB_2_BEWERTUNGEN}}`
- `{{MASSNAHME_1_BEREICH}}` bis `{{MASSNAHME_5_BEREICH}}` + `_TEXT`
- `{{EMPFOHLENES_PAKET}}`, `{{PAKET_BEGRUENDUNG}}`, `{{PAKET_LEISTUNGEN}}`, `{{PAKET_PREIS}}`

**Maßnahmen-Texte: immer so formulieren dass der Lead denkt "das brauche ich einen Profi für"**
- ✅ "Lokale Suchbegriffe analysieren und gezielt einbauen"
- ✅ "SEO-optimierten Text verfassen der Algorithmus + Kunden anspricht"
- ✅ "Richtige Kategorien einbauen – falsche Auswahl kostet Ranking"
- ❌ "Fotos hochladen" → macht er selbst

### n8n Audit-Workflow (als nächstes bauen!)
- Input: GBP-Link
- Claude analysiert GBP via Places API / Web-Scraping
- Claude füllt alle {{VARIABLEN}} aus (als JSON)
- n8n ersetzt Variablen im HTML-Template (Python/String-Replace Node)
- Output: PDF via HTML-to-PDF Service (z.B. Gotenberg, WeasyPrint, oder Browserless)
- Mario fügt Screenshot manuell ein → fertig zum Verschicken

---

## Nächste Schritte (Priorität)
1. 📄 HTML-Template-Dateien ins GitHub pushen (`/audit/` Ordner)
2. 📞 Elektro Kuhn Follow-up ab ~20.02. – Audit manuell befüllen + als PDF verschicken
3. 📞 Nemanja – warten auf Rückmeldung
4. 🤖 n8n Audit-Workflow bauen
5. 📋 10+ neue Leads identifizieren (Google Maps screenen)

## Wichtige Links
- Website: https://trovilo.de
- GitHub: https://github.com/Ruzulo/Trovilo
- Google Sheet Leads: https://docs.google.com/spreadsheets/d/1sa6Gx0cMYbqYWU6wVE1tJWdql9k-tkAKtVqQRbj2CoE
- Google Doc Template (alt, nicht mehr aktiv): https://docs.google.com/document/d/1Bpt9GbRgAQoc1LbtUpgw7Cn9rcDc8wtnRSmGcfABKHI/edit

## Preise
- Optimierung: €299 einmalig
- Kickstart: €599 einmalig
- Premium: €999 einmalig
- Betreuung Basis: €75/Monat
- Betreuung Aktiv: €149/Monat
