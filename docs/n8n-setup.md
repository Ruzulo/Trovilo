# n8n Setup Guide

## Übersicht

Diese Anleitung erklärt, wie die n8n-Infrastruktur für Trovilo aufgesetzt ist.

## Infrastruktur

### n8n Cloud
- **URL:** https://trovilo.app.n8n.cloud
- **Verwendung:** Produktive Business-Workflows
- **Zugriff:** Web-UI + API

### n8n VPS (Optional)
- **Verwendung:** Experimente, Prototyping
- **Zugriff:** Nur lokal/VPN

## Claude Integration via MCP

### Installation

1. **n8n MCP Server installieren:**
```bash
npm install -g @n8n/mcp-server
```

2. **Claude Desktop Config** (`claude_desktop_config.json`):
```json
{
  "mcpServers": {
    "n8n-cloud-full": {
      "command": "node",
      "args": [
        "<PATH_TO>/n8n_mcp_server/server.js"
      ],
      "env": {
        "N8N_HOST": "https://<YOUR_INSTANCE>.app.n8n.cloud",
        "N8N_API_KEY": "YOUR_API_KEY_HERE"
      }
    }
  }
}
```

3. **API Key erstellen:**
   - In n8n Cloud: Settings → API → Create API Key
   - Key in Config eintragen
   - Claude Desktop neu starten

### Workflow-Import

1. **Workflow JSON herunterladen** aus `/workflows/`
2. In n8n Cloud → **Import from File**
3. **Credentials anpassen:**
   - Anthropic API Key in Header Auth Credential
   - Ggf. Google Sheets Credentials

## Anthropic API Setup

### API Key erstellen
1. https://console.anthropic.com/settings/keys
2. Create Key → Kopieren
3. In n8n: **Credentials** → **Header Auth** → Neuer Credential
   - Name: `Anthropic API`
   - Header Name: `x-api-key`
   - Value: Dein API Key

### Verwendung in Workflows
- Model: `claude-sonnet-4-20250514`
- Required Headers:
  - `anthropic-version: 2023-06-01`
  - `content-type: application/json`

## Best Practices

### Workflow-Entwicklung

1. **Code Nodes für komplexe Logik:**
   - Template Literals funktionieren nur in Code Nodes
   - Set Nodes nur für simple Werte

2. **API Body Preparation:**
```javascript
// ✅ RICHTIG: Code Node
const apiBody = {
  model: 'claude-sonnet-4-20250514',
  messages: [{
    role: 'user',
    content: `Mein Prompt mit ${variable}`
  }]
};
return { json: { api_body: JSON.stringify(apiBody) } };

// ❌ FALSCH: Set Node mit Expression
// Führt zu "undefined" bei Variablen
```

3. **HTTP Request Configuration:**
   - Body Content Type: **Raw/Custom**
   - Content Type: `application/json`
   - Body: `={{ $json.api_body }}`

### Credential Management

- **NIE** API Keys in Workflow-JSON speichern
- Immer n8n Credentials verwenden
- Bei Export: Credentials werden automatisch entfernt

### Error Handling

Code Nodes sollten immer Error-Handling haben:

```javascript
try {
  const response = JSON.parse(data);
  return { json: response };
} catch (error) {
  throw new Error(`Parse failed: ${error.message}`);
}
```

## Troubleshooting

### "undefined" in Code Node
**Problem:** Variables sind undefined im Code Node  
**Lösung:** Separater Set Node VOR dem Code Node

### "JSON parameter needs to be valid JSON"
**Problem:** Expression in HTTP Request Body  
**Lösung:** JSON.stringify() in Code Node, dann Raw Body

### "Input does not match expected shape"
**Problem:** Zeilenumbrüche fehlen im API Body  
**Lösung:** Template Literals in Code Node verwenden

## Monitoring

- **n8n Cloud Dashboard:** Execution History
- **Workflow Status:** Active/Inactive
- **Error Notifications:** Email-Benachrichtigungen konfigurieren

## Backup

1. **Workflows exportieren:**
   - Settings → Export → JSON Download
2. **In Git speichern:**
   ```bash
   cp workflow.json workflows/
   git add workflows/
   git commit -m "Update workflow"
   ```

## Support

- **n8n Docs:** https://docs.n8n.io
- **Anthropic Docs:** https://docs.anthropic.com
