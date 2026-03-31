# Product Listing Generator — Vercel Deploy

## Bestandsstructuur
```
listing-tool/
├── api/
│   └── generate.js      ← serverless API (API key staat hier veilig)
├── public/
│   └── index.html       ← de tool die de VA gebruikt
├── vercel.json          ← Vercel configuratie
└── README.md
```

## Deploy in 5 stappen

### 1. GitHub repo aanmaken
- Ga naar github.com → New repository
- Naam: `listing-tool` (of wat je wil)
- Upload alle bestanden

### 2. Vercel account
- Ga naar vercel.com → Sign up (gratis)
- Koppel je GitHub account

### 3. Project importeren
- Vercel dashboard → "Add New Project"
- Kies je `listing-tool` repo
- Klik Deploy (geen extra instellingen nodig)

### 4. API key instellen ← BELANGRIJK
- Ga in Vercel naar: Project → Settings → Environment Variables
- Voeg toe:
  - Name:  `ANTHROPIC_API_KEY`
  - Value: `sk-ant-xxxxxxxx...` (jouw echte key)
- Klik Save → daarna Redeploy

### 5. Klaar!
- Vercel geeft je een URL zoals: `https://listing-tool-xyz.vercel.app`
- Deel die URL met de VA
- Optioneel: koppel een eigen domein via Vercel → Settings → Domains

## API key ophalen
- Ga naar console.anthropic.com
- API Keys → Create Key
- Kopieer de key en plak in Vercel (stap 4)

## Kosten
- Vercel hosting: gratis
- Anthropic API: ~€0.01–0.03 per gegenereerde listing
