# Ludovica Benedetta Dagna — Art Curator

Personal website for Ludovica Benedetta Dagna, Art Curator, Art Manager, and Project Coordinator.

## File Structure

```
/
├── index.html                         ← Main page (legge i JSON e si aggiorna)
├── privacy-policy.html
├── cookie-policy.html
├── logo.png                           ← Logo senza sfondo
├── PHOTO-2026-03-24-07-59-51.jpg      ← Foto ritratto
├── admin/
│   ├── index.html                     ← Pannello CMS (Decap CMS)
│   └── config.yml                     ← Definizione di tutti i campi editabili
├── content/
│   ├── hero.json                      ← Testi Hero
│   ├── about.json                     ← Bio e statistiche
│   ├── services.json                  ← Servizi (cards)
│   ├── philosophy.json                ← Citazione / filosofia
│   ├── contact.json                   ← Testi sezione contatti
│   └── tags.json                      ← Tag "Areas of Practice"
├── netlify.toml
├── _redirects
├── robots.txt
└── README.md
```

---

## Come modificare i contenuti (flusso Admin)

1. Vai su `https://tuo-sito.netlify.app/admin`
2. Fai login con email e password
3. Scegli la sezione da modificare (Hero, About, Services, ecc.)
4. Modifica i testi nei campi
5. Clicca **Save** in alto a destra
6. Netlify riceve il commit automaticamente e fa il deploy — il sito si aggiorna in ~30 secondi

> Non serve nessun step manuale dopo Save. Il deploy è automatico.

---

## Setup iniziale su Netlify (una tantum)

### Step 1 — Deploy
Metodo rapido: app.netlify.com/drop — trascina lo zip

Metodo con repo GitHub (consigliato per storico modifiche):

  git init
  git add .
  git commit -m "Initial commit"
  git branch -M main
  git remote add origin https://github.com/TUO-USERNAME/ludovica-dagna.git
  git push -u origin main

Poi: Netlify > Add new site > Import from GitHub > seleziona repo > Deploy site

### Step 2 — Attiva Netlify Identity
Netlify > sito > tab Identity > Enable Identity

### Step 3 — Attiva Git Gateway
Identity > Services > Enable Git Gateway
(Permette al CMS di salvare modifiche direttamente nella repo)

### Step 4 — Invita l'editor
Identity > Invite users > inserisci email di Ludovica
Riceverà un link per impostare la password.

### Step 5 — Accesso admin
https://tuo-sito.netlify.app/admin > login > modifica > Save > deploy automatico

---

## Campi editabili dall'admin

Sezione       | Cosa si può modificare
Hero          | Overline, nome (3 righe), ruolo, testo CTA
About         | Label, titolo, 4 paragrafi bio, 3 statistiche
Services      | Label, titolo, e per ogni card: numero, titolo, descrizione, tag
Philosophy    | Label, testo citazione, firma
Contact       | Label, titolo, testo intro, frase corsivo, handle Instagram
Tags          | Lista "Areas of Practice" (aggiungere/rimuovere/rinominare)

---

## Dominio personalizzato (opzionale)
Netlify > sito > Domain settings > Add custom domain
