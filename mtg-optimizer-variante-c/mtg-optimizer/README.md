# MTG Commander Deck Optimizer

## Deployment auf Netlify (kostenlos, ~10 Minuten)

### Schritt 1: GitHub Account erstellen
1. Gehe auf https://github.com und klicke "Sign up"
2. E-Mail, Passwort, Username eingeben → Account bestätigen

### Schritt 2: Repository erstellen
1. Klicke auf "+" oben rechts → "New repository"
2. Name: `mtg-optimizer`
3. Visibility: **Public**
4. Klicke "Create repository"

### Schritt 3: Dateien hochladen
1. Im neuen Repository: "uploading an existing file" klicken
2. Den kompletten Ordner `mtg-optimizer` hochladen (drag & drop)
   - `public/index.html`
   - `netlify/functions/claude.js`
   - `netlify.toml`
3. Klicke "Commit changes"

### Schritt 4: Netlify Account erstellen
1. Gehe auf https://netlify.com → "Sign up" → "Sign up with GitHub"
2. GitHub autorisieren

### Schritt 5: Site deployen
1. Im Netlify Dashboard: "Add new site" → "Import an existing project"
2. "Deploy with GitHub" → `mtg-optimizer` auswählen
3. Build settings werden automatisch aus `netlify.toml` gelesen
4. Klicke "Deploy site"

### Schritt 6: Anthropic API Key eintragen ⚠️ WICHTIG
1. Gehe auf https://console.anthropic.com → "API Keys" → neuen Key erstellen
2. Zurück im Netlify Dashboard: Site Settings → Environment variables
3. "Add a variable":
   - Key: `ANTHROPIC_API_KEY`
   - Value: deinen API Key (beginnt mit `sk-ant-...`)
4. "Save" → dann "Deploys" → "Trigger deploy" → "Deploy site"

### Fertig!
Netlify gibt dir eine URL wie `https://amazing-name-123.netlify.app`
Diese URL kannst du mit Freunden teilen — der Optimizer läuft für alle.

---

## Kosten
- GitHub: kostenlos
- Netlify Hosting: kostenlos
- Netlify Functions: 125.000 Requests/Monat kostenlos
- Anthropic API: ~$0.003 pro Deck-Analyse (sehr günstig)

## Eigene Domain (optional)
In Netlify unter "Domain settings" kannst du eine eigene Domain wie
`mtg-optimizer.deinname.de` eintragen wenn du eine hast.
