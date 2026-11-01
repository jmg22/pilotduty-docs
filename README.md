# pilotduty-docs

Documentation, FAQ et blogue de **PilotDuty** (app iPhone) et **PilotDuty Manager** (web), en français et en anglais.
Ces fichiers sont affichés sur le site [pilotduty.com](https://pilotduty.com) (dépôt privé `pilotduty-site`) :

| Dossier | Affiché sur |
| --- | --- |
| `docs/fr/…`, `docs/en/…` | `/fr/docs/…`, `/en/docs/…` |
| `faq/fr/…`, `faq/en/…` | `/fr/faq`, `/en/faq` |
| `blog/fr/…`, `blog/en/…` | `/fr/blogue/…`, `/en/blog/…` |

Chaque modification poussée sur `main` republie le site (GitHub Action `deploy-site.yml`, voir plus bas).

## Organisation

```
docs/
  fr/app/         Guide de l'app iPhone (français)
  fr/manager/     Guide de PilotDuty Manager (français)
  en/app/         iPhone app guide (English)
  en/manager/     PilotDuty Manager guide (English)
  <langue>/<section>/_meta.json   Titre de la section
faq/fr/*.mdx, faq/en/*.mdx        Une question par fichier
blog/fr/*.mdx, blog/en/*.mdx      Un article par fichier (AAAA-MM-JJ-titre.mdx)
media/                            Images de la documentation et du blogue
```

Le nom du fichier (sans `.mdx`) devient l'adresse de la page. Le français et l'anglais ont chacun leurs noms ;
le champ `translationKey` relie les deux versions d'une même page.

## En-têtes

Documentation :

```yaml
---
title: Enregistrement automatique des vols
description: Comment l'app détecte vos décollages et vos atterrissages.
order: 3
translationKey: app-automatic-recording
updated: 2026-11-01
draft: false
---
```

FAQ :

```yaml
---
question: L'abonnement de mon organisation comprend-il PilotDuty+ ?
category: subscriptions   # app | manager | subscriptions | account
order: 1
translationKey: faq-org-vs-pilot
updated: 2026-11-01
draft: false
---
```

Blogue :

```yaml
---
title: Comment l'app enregistre vos vols toute seule
description: Résumé d'une ou deux phrases.
date: 2026-11-01
author: L'équipe PilotDuty
translationKey: blog-automatic-recording
draft: false
---
```

`draft: true` garde un fichier hors du site.

## Écrire et vérifier

Lire `CONTRIBUTING.md` avant d'écrire : règles de véracité et de vocabulaire.

## Republier le site à chaque modification

La GitHub Action `.github/workflows/deploy-site.yml` appelle le Deploy Hook Vercel du site à chaque push sur `main`.
Configuration à faire une fois :

1. Vercel → projet `pilotduty-site` → Settings → Git → **Deploy Hooks** : créer un hook sur la branche `main`.
2. GitHub → ce dépôt → Settings → Environments : environnement **`VERCEL_DEPLOY_HOOK_URL`**, secret d'environnement **`VERCEL_DEPLOY_HOOK_URL`** contenant l'adresse du hook (fait le 2026-11-01). Le job déclare cet environnement ; sans lui, il ne verrait pas le secret.
