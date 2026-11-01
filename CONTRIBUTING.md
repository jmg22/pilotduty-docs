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
  - Google Wallet, Google Agenda par connexion (seuls les liens iCal sont acceptés), la connexion par lien ou par SMS, la double authentification.
- Exception confirmée par JMG : la confirmation « safe » du suivi de vol est active.
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
- En-tête YAML : toujours mettre `title`, `description` et `question` entre guillemets doubles (« : » casse le YAML).
- Pas de JSX ni de HTML dans les fichiers : Markdown simple. Éviter les caractères `{`, `}`, `<` et `>` dans le texte (ils ont un sens en MDX).
