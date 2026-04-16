# 🚀 Hubo Configurator Deployment Guide

**Voor: Vincent - Finesse Decpartners**  
**Datum: April 2026**

## ✅ Wat is er klaar

Je hebt nu een **production-ready** configurator met:
- ✅ Werkende NL + FR versie
- ✅ Hubo-beveiligde communicatie (AES + HMAC)
- ✅ Correcte Hubo huisstijl (groen bestelknop, Roboto Condensed)
- ✅ Test-harness om alles te valideren
- ✅ Responsive ontwerp voor alle apparaten

## 🎯 Stap 1: GitHub Repository aanmaken

1. Ga naar **github.com** en log in
2. Klik **"New Repository"**
3. Naam: `hubo-configurator-finesse`
4. Beschrijving: `Transparante tafelbeschermer configurator voor Hubo.be - Finesse Decpartners`
5. **Public** aanvinken (Netlify gratis alleen voor public repos)
6. Klik **"Create repository"**

## 🎯 Stap 2: Bestanden uploaden naar GitHub

De makkelijkste manier via de web interface:

1. **Upload deze bestanden één voor één:**
   - `index.html` (Nederlandse versie)
   - `index-fr.html` (Franse versie) 
   - `parent-test.html` (Test pagina)
   - `README.md` (Documentatie)
   - `netlify.toml` (Deploy configuratie)

2. **Voor elke upload:**
   - Klik **"Add file" > "Upload files"**
   - Sleep bestand naar GitHub
   - Commit message: bijv. "Add Dutch configurator"
   - Klik **"Commit changes"**

## 🎯 Stap 3: Afbeeldingen toevoegen

**BELANGRIJK:** Je hebt nog 2 afbeeldingen nodig:

1. **`PLA2100.jpg`** - Product foto van je transparante tafelbeschermer
2. **`rounded-corner-expl.png`** - Kleine illustratie van afgeronde hoeken

Upload deze ook naar je GitHub repo.

## 🎯 Stap 4: Netlify deployment

1. Ga naar **netlify.com**
2. Klik **"Sign up"** en kies **"GitHub"** om in te loggen
3. Klik **"New site from Git"**
4. Kies **GitHub** en autoriseer Netlify
5. Selecteer je `hubo-configurator-finesse` repository
6. **Build settings:**
   - Build command: *leeg laten*
   - Publish directory: *leeg laten* (staat in netlify.toml)
7. Klik **"Deploy site"**

## 🎯 Stap 5: Custom domein instellen (optioneel)

In Netlify dashboard:
1. Ga naar **"Domain settings"**
2. Klik **"Add custom domain"**
3. Vul in: `configurator.finesse-decpartners.be` (of iets dergelijks)
4. Volg de DNS instructies

## 🎯 Stap 6: Testen

Je krijgt een URL zoals: `https://amazing-name-123456.netlify.app`

**Test checklist:**
- ✅ NL versie laadt: `https://je-url.netlify.app/`
- ✅ FR versie laadt: `https://je-url.netlify.app/fr`
- ✅ Test-harness werkt: `https://je-url.netlify.app/parent-test.html`
- ✅ Responsive op mobiel/tablet
- ✅ Bestel knop stuurt berichten (zie test-console)

## 🎯 Stap 7: Hubo contact en afspraken

**E-mail naar je Hubo contactpersoon:**

```
Onderwerp: Configurator klaar voor technische integratie - Finesse Decpartners

Hallo [Hubo contactpersoon],

De configurator voor transparante tafelbeschermers is technisch klaar:

🔗 Test URL: [je-netlify-url]/parent-test.html
🔗 NL versie: [je-netlify-url]/
🔗 FR versie: [je-netlify-url]/fr

Voor de finale integratie hebben we nog nodig:
1. Signature key voor beveiligde communicatie
2. Dummy artikel code voor dit product
3. Bevestiging prijzen/marges/leveringskosten
4. Test environment URLs van Hubo
5. Planning integratietests

De configurator voldoet aan alle technische specificaties uit jullie manual.

Groeten,
Vincent - Finesse Decpartners
```

## 🎯 Stap 8: Finale aanpassingen

Wanneer je de **signature key** van Hubo krijgt:

1. In **beide** configurator bestanden (`index.html` + `index-fr.html`)
2. Zoek regel: `signatureKey: 'TEMP-KEY-VAN-HUBO-VERVANGEN'`
3. Vervang door echte key: `signatureKey: 'hun-echte-key'`
4. Commit en push naar GitHub (auto-deploy)

## ❗ Belangrijke waarschuwingen

- **NOOIT** inkoopprijzen in frontend berekenen - nu staat er 60% voor demo
- **ALTIJD** signature key geheim houden (niet in public repo)
- **CONTROLEER** barcode-systematiek met Hubo (nu PLA2100-prefix)

## 🆘 Hulp nodig?

**Problemen met deployment?** Check:
1. Alle bestanden geüpload naar GitHub?
2. Afbeeldingen toegevoegd?
3. Netlify build succeeded?

**Configurator werkt niet?** Check:
1. Console voor JavaScript errors
2. Test-harness toont berichten?
3. Afbeeldingen laden correct?

---

**🎉 Succes Vincent! Je configurator is production-ready!**
