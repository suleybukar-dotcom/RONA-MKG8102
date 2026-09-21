# Historique de la Skill fiche-de-veille

La Skill décrit une procédure écrite une fois, exécutée à chaque fois. Ce fichier conserve l'histoire des versions et des erreurs corrigées (le versionnement Git du dépôt conserve le texte de chaque version).

## Registre des rejets de la base (instrument de révision)

Au 20 septembre 2026, 7 fiches sur 120 sont rejetées : **6 « hors KIQ »** et **1 « citation inexacte »** ; aucune « date inventée » ni « autre ». Le taux de rejet parmi les fiches décidées est d'environ 12 % (7 rejets sur 60 fiches, soit 53 validées et 7 rejetées) : ni nul, ni très élevé. Les six rejets « hors KIQ » portent sur des faits anciens ou hors périmètre (ouvertures de 2025, acquisition antérieure à la fenêtre d'observation, canal de presse inactif, relevé d'implantation sans comparaison possible, relevé Home Depot servi depuis l'Ontario). La v2 renforce la règle de pertinence (aucune fiche si la page ne contient aucun fait lié à la KIQ) et la teste (page 5 du jeu de test).

## Versions

| Version | Date | Contenu | Statut |
|---|---|---|---|
| v0 | 5 sept. 2026 | Skill fournie par le cours ; l'énoncé de la KIQ est à remplacer ; exemple du cours | Point de départ |
| v1 | 6 sept. 2026 (version locale) ; versionnée dans ce dépôt le 19 sept. 2026, commit `585eab4` | v0 avec la KIQ centrale de RONA et l'échelle de cotation de l'équipe (Fiable, Moyen, Pauvre, À coter) dans les intrants ; exemple du cours conservé | En usage jusqu'à la v2 |
| v2 | 20 sept. 2026 | Voir ci-dessous | **Proposée, à valider par l'équipe** (Responsable des insights) |

## Changements de la v1 à la v2 et leur justification

| # | Changement | Constat réel qui le justifie |
|---|---|---|
| 1 | Le format de sortie suit l'ordre exact des champs de la table : ajout de « Motif de rejet » (vide, humain), « Champs vides signalés » et « Connecteur » ; « Ville » signalé comme automatique | La table « Fiches de veille » compte 21 champs ; la v1 n'en listait que 17 (schéma lu dans la base) |
| 2 | Méthode : étape « Vérifier avant d'écrire » (date et extrait contrôlés mot pour mot sur la page) et étape de dédoublonnage | Règles déjà appliquées dans les instructions de tâches planifiées du 9 sept. ; une extraction structurée est assistée par un modèle et peut se tromper |
| 3 | Règle 1 : contre-exemple sur la colonne « Ouverte » d'un affichage de poste | Fiche validée sur les emplois du siège social de BMR : la seule date visible n'était pas une date de publication et a été écartée |
| 4 | Règle 8 : prix affiché comme valeur de référence, divergence avec la valeur structurée rapportée, jamais de substitution silencieuse | Fiche validée sur les sacs Maximum de RONA (26,99 $ affiché contre 14,99 $ structuré) ; « correction du 9 septembre » dans le Biais connu de la page Husky de Home Depot |
| 5 | Règle 9 : noter la succursale servie ; un prix hors Québec ou non confirmé n'est pas comparable | Fiche validée sur la peinture SICO de RONA servie depuis l'Ontario ; Biais connu des pages Home Depot (magasin par défaut Niagara Falls) |
| 6 | Règle 10 : comparer chaque bannière à elle-même | Règle de comparaison adoptée par l'équipe le 8 sept. dans le Biais connu de la page carrières de Home Depot ; mandat |
| 7 | Méthode 7 : ne jamais écrire qu'une hypothèse est validée | Règle absolue de la tâche mensuelle du 9 sept. |
| 8 | Règle 11 : aucun renseignement identifiant une personne dans les avis | Règle de la tâche mensuelle du 9 sept. |
| 9 | Règle 12 : périmètre d'écriture en exécution planifiée | Tâches planifiées du 9 sept. |
| 10 | L'exemple de fiche est une fiche réelle de RONA ; ajout d'un exemple de signalement ; l'exemple du cours (autre KIQ) est retiré | L'exemple du cours portait sur une autre entreprise et une autre KIQ |

## Ce que la v2 ne change pas

Statut toujours « à valider » ; « Validé par » et « Motif de rejet » réservés à l'humain ; extrait cité mot pour mot ; date « non indiquée » quand la page ne date pas le fait ; une fiche par fait ; résumé de faits seulement.

## Limites de cette révision

- La v2 a été rédigée avec Claude Code le 20 sept. 2026 à partir de la base, des instructions de tâches et des documents du cours. Elle n'a pas été validée par l'équipe.
- Le jeu de test ([tests/jeu_de_test.md](../../tests/jeu_de_test.md)) n'a **pas été réexécuté** : aucune comparaison mesurée entre v1 et v2.
- Le comportement du modèle peut varier entre versions : à chaque réexécution du jeu de test, consigner ici la date, la version de la Skill, le modèle et les écarts.

## Registre des réexécutions du jeu de test

| Date | Version de la Skill | Modèle | Écarts constatés | Décision |
|---|---|---|---|---|
| (aucune) | | | | |
