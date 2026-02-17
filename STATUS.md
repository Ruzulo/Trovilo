# Trovilo – Status für nächste Chat-Session

> Letzte Aktualisierung: 17.02.2026

## Wo stehen wir?

### Website ✅
- trovilo.de ist live bei Ionos (FTP-Deployment)
- GitHub: Ruzulo/Trovilo, branch: main, Ordner: /website
- Text-Logo "📍 TROVILO" im Header (kein Bild-Logo)
- Alle Bugfixes erledigt (MwSt-Größe, Checklist, WhatsApp vereinfacht, "Check" statt "Audit")
- **Website nicht mehr anfassen!**

### Lead Pipeline
- Google Sheet: https://docs.google.com/spreadsheets/d/1sa6Gx0cMYbqYWU6wVE1tJWdql9k-tkAKtVqQRbj2CoE
- Details in LEADS.md

### Aktueller Lead-Status
| Lead | Status | Nächster Schritt |
|------|--------|-----------------|
| Nemanja | 🟡 Warten | Meldet sich |
| Elektro Kuhn | 🟡 Warten | 3 Tage (ab 17.02.) dann Follow-up |
| Michael Demml | 🔴 Kein Interesse | - |
| Michael Gärtner | 🔴 Gescheitert | - |

### Neuer Outreach-Prozess (beschlossen!)
**NICHT** mehr direkt Preis nennen. Stattdessen:
1. "Ich habe mir Ihr Google Profil angeschaut – da gibt es Potenzial"
2. "Darf ich Ihnen ein kostenloses Audit schicken?"
3. Audit zuschicken → Vertrauen aufbauen → dann Angebot

### Audit-Template ✅
- **Format: Google Doc** (nicht mehr Canva – besser für WhatsApp & Handy-Lesbarkeit)
- Google Doc Vorlage: https://docs.google.com/document/d/1Bpt9GbRgAQoc1LbtUpgw7Cn9rcDc8wtnRSmGcfABKHI/edit
- Canva Design (eingefroren, nicht mehr verwendet): https://www.canva.com/d/RZT2RR_zH2845aW

**Struktur:**
- Seite 1: Deckblatt + GBP Screenshot + Gesamtscore (teal) + Profil-Analyse Tabelle + Wettbewerber-Vergleich + CTA (rot)
- Seite 2: Maßnahmen-Tabelle + Paket-Empfehlung (gelb) + Warum Trovilo + Nächster Schritt + Footer

**Alle Platzhalter (n8n-ready mit {{VARIABLE}}):**
- {{FIRMENNAME}}, {{BRANCHE}}, {{DATUM}}
- {{GBP_SCREENSHOT}} – Bild wird manuell eingefügt
- {{SCORE_GESAMT}} – Gesamtpunktzahl 0-100
- {{SICHTBARKEIT}}, {{LETZTE_AKTIVITAET}}, {{ANZAHL_BEWERTUNGEN}}, {{BEWERTUNGS_SCHNITT}}
- {{BEFUND_VOLLSTAENDIGKEIT}}, {{SCORE_VOLLSTAENDIGKEIT}}
- {{BEFUND_FOTOS}}, {{SCORE_FOTOS}}
- {{BEFUND_BEWERTUNGEN}}, {{SCORE_BEWERTUNGEN}}
- {{BEFUND_LEISTUNGEN}}, {{SCORE_LEISTUNGEN}}
- {{BEFUND_AKTIVITAET}}, {{SCORE_AKTIVITAET}}
- {{WETTB_SICHTBARKEIT_SIE}}, {{WETTB_1_NAME}}, {{WETTB_1_SICHTBARKEIT}}, {{WETTB_1_BEWERTUNGEN}}
- {{WETTB_2_NAME}}, {{WETTB_2_SICHTBARKEIT}}, {{WETTB_2_BEWERTUNGEN}}
- {{MASSNAHME_1_BEREICH}} bis {{MASSNAHME_5_BEREICH}} + _TEXT
- {{EMPFOHLENES_PAKET}}, {{PAKET_BEGRUENDUNG}}, {{PAKET_LEISTUNGEN}}, {{PAKET_PREIS}}
- {{TELEFON}}, {{EMAIL}}

**TODO: Telefonnummer + Email im Template eintragen ({{TELEFON}}, {{EMAIL}})**

### n8n Audit-Workflow (geplant, nächster Schritt!)
- Input: GBP-Link + Screenshot
- Claude analysiert GBP und füllt alle Platzhalter aus
- n8n kopiert die Google Doc Vorlage (copyFile) mit Firmenname als Titel
- n8n ersetzt alle {{VARIABLEN}} im kopierten Doc
- Output: Fertiges Audit-Dokument, Link zum Verschicken
- Screenshot wird danach manuell eingefügt (oder per Google Docs API)

## Nächste Schritte (Priorität)
1. 📝 {{TELEFON}} + {{EMAIL}} im Audit-Template eintragen
2. 📞 Elektro Kuhn Follow-up mit Audit (ab ~20.02.) – erstes Audit manuell ausfüllen
3. 📞 Nemanja – warten auf Rückmeldung
4. 🤖 n8n Audit-Workflow bauen (nach erstem manuellen Audit)
5. 📋 10+ neue Leads identifizieren (Google Maps screenen)

## Wichtige Links
- Website: https://trovilo.de
- GitHub: https://github.com/Ruzulo/Trovilo
- Google Sheet Leads: https://docs.google.com/spreadsheets/d/1sa6Gx0cMYbqYWU6wVE1tJWdql9k-tkAKtVqQRbj2CoE
- Audit-Template (Google Doc): https://docs.google.com/document/d/1Bpt9GbRgAQoc1LbtUpgw7Cn9rcDc8wtnRSmGcfABKHI/edit
- Ionos FTP: manuell (GitHub → PC → FTP)

## Preise
- Optimierung: €299 einmalig
- Kickstart: €599 einmalig  
- Premium: €999 einmalig
- Betreuung Basis: €75/Monat
- Betreuung Aktiv: €149/Monat

## Über Marco (Inhaber)
- Wohnt in Penzberg, südlich von München
- Aktuell im Sabbatical bis 28.02.2026
- Hauptjob wartet danach → Trovilo als Nebengeschäft
- Ziel: >15.000€/Monat Gewinn → dann Hauptjob kündigen
- Fokus: KMU in 50km Radius um Penzberg
