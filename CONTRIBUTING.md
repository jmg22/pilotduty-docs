# Règles de rédaction

Ces textes sont publics. Ils doivent décrire **ce que les produits font vraiment**.

## Véracité

- N'écrire que des fonctions publiées. Source : les inventaires `FEATURES_PilotDuty_iOS` et `FEATURES_PilotDuty_Manager` (Linear, TOT-419).
- Respecter les sections « À ne pas présenter comme disponible » des inventaires. En particulier, ne jamais écrire :
  - que la maintenance bloque une réservation, ou qu'une alerte d'échéance est envoyée (médical, compétences, inspections) ;
  - que les forfaits prépayés comptent des heures (c'est un crédit en argent) ;
  - que la boutique vend en ligne (comptoir seulement, sur activation) ;
  - que les mémos partent par SMS (courriel et notification seulement) ;
  - qu'une signature électronique est « conforme », « certifiée » ou « approuvée » par une autorité ;
  - qu'il existe un essai gratuit, un rabais, PayPal, un « premier utilisateur gratuit » ou un « support prioritaire » ;
  - que l'app permet de réserver (elle n'a aucune fonction de réservation) ;
  - que le Manager fait un calcul réglementaire du temps de service (repères indicatifs 702 et 703 seulement) ;
  - la récupération d'un vol après l'arrêt forcé de l'app (pas encore livrée) ;
  - Google Agenda par connexion (seuls les liens iCal sont acceptés), la connexion par lien ou par SMS, la double authentification.
- Exception confirmée par JMG : la confirmation « safe » du suivi de vol est active.
- Exception confirmée par JMG (TOT-419, 2026-11-01) : les cartes d'embarquement Google Wallet sont en service, comme celles
  d'Apple Wallet (courriel de confirmation réel avec les deux boutons). Le code QR de la carte ouvre la réservation dans le
  Manager pour un membre connecté : pas d'écran de scan ni d'enregistrement dédié.
- Numérisation du carnet papier : comprise dans PilotDuty+ (décision JMG).
- Un point incertain ne s'écrit pas : il va dans les questions pour JMG.

## Vocabulaire

- Dire **organisation**, jamais « école ».
- L'app et le Manager partagent la même base : écrire « même base », « remonte », jamais « synchronisation ».
- Forfaits pilote : Gratuit, PilotDuty+, PilotDuty Pro (App Store). Forfaits d'organisation : Growth, Unlimited (Stripe). Les deux familles sont distinctes.
- Prix : en dollars américains, seulement sur la page Tarifs du site.
- Slogan « Because Time Matters » : toujours en anglais.

## Style

- Phrases courtes, voix active, « vous ».
- Un fichier = une tâche ou un sujet. Commencer par ce que la fonction permet de faire.
- Libellés de l'interface entre guillemets français « … » (en anglais : “…”).
- En-tête YAML écrit à la main : mettre `title`, `description` et `question` entre guillemets doubles (« : » casse le YAML). Keystatic met lui-même les guillemets nécessaires.
- Pas de JSX ni de HTML dans les fichiers : Markdown simple. Éviter les caractères `{`, `}`, `<` et `>` dans le texte (ils ont un sens en MDX).

## Images

- Une image appartient à une page : `media/<langue>/<section>/<nom-du-fichier-de-la-page>/<image>.png`,
  par exemple `media/fr/app/carnet-de-vol/logbook-summary.png`. Les versions française et anglaise ont chacune leur copie.
  Cette organisation est celle de l'éditeur Keystatic du site : il n'affiche et ne garde que les images rangées ainsi.
- Dans le texte : `![Texte alternatif descriptif](/docs-media/fr/app/carnet-de-vol/logbook-summary.png)`, sur sa propre ligne,
  après l'étape illustrée. Le site sert `media/` à l'adresse `/docs-media/`.
- Noms d'images en anglais, en minuscules et tirets. Texte alternatif dans la langue de la page. Les captures montrent l'interface en anglais.
- Pas de données personnelles réelles (numéro, courriel, nom, visage, photo de document) : floutez-les.
- Avec Keystatic (`/keystatic` sur le site), le bouton d'image du texte range le fichier au bon endroit.

### Images du site (accueil, pages App et Manager, boutique)

- Une fiche par image, dans Keystatic (menus « Site · … ») : `site/images/<fiche>.yaml`, fichiers dans `media/site/<fiche>/`.
  Liste des 33 fiches et de leurs endroits : `CAPTURES.md` du dépôt `pilotduty-site`.
- Le plus simple : sur le site, connecté à Keystatic, cliquer le crayon de l'image. Le site se republie en 2 à 3 minutes.
- Une fiche vide garde l'image par défaut. Pour revenir à l'image par défaut, vider le champ et enregistrer.
- Captures : données de démonstration seulement ; barre d'état avec réseau, Wi-Fi et batterie pleins (règles d'Apple).
- Badges d'Apple et de Google (App Store, iBeacon, Apple Wallet, Google Wallet) : fichiers officiels seulement, jamais modifiés.
