# Conformité aux exigences officielles du dépôt d'équipe

État au 20 septembre 2026. Ce document rapproche le contenu du dépôt des exigences écrites dans les documents du cours. Il distingue ce qui est **exigé** (formulé comme tel dans un document officiel), ce qui est **attendu** (décrit comme pratique dans une lecture obligatoire) et ce qui est **non confirmé**.

## 1. Documents officiels consultés

| Sigle | Document | Ce qu'il établit pour le dépôt |
|---|---|---|
| PC | Plan de cours MKG8102 A26 | Échéance du dépôt GitHub d'équipe ; rôle de GitHub (héberge le portfolio SKILL.md et le code des dispositifs d'équipe) ; rôle Connaissance et diffusion responsable du dépôt ; niveau d'usage de l'IA de la plateforme d'équipe |
| J1 | Journée 1 (5 sept.), diapositive 43 | Échéance : lundi 21 septembre, 23 h 59, dépôt GitHub d'équipe avec le SKILL.md d'équipe |
| J2 | Journée 2 (19 sept.), diapositives 4, 26, 28, 41 | Contenu du dépôt : Skill v2, schéma, sources, chaîne, seuils, grille de confiance, jeu de test, défaillances, sans clé ; aucune clé, aucun jeton, aucun mot de passe dans un dépôt |
| L | Lecture obligatoire des séances 3 et 4, sections 8.2 et 9.2 | Liste du contenu minimal d'un dépôt reproductible ; archivage des briefs et des alertes ; interdiction de clés, jetons, mots de passe et données personnelles ; critère de reproductibilité |

Les consignes détaillées de l'évaluation 2 (page Moodle, grille de correction, boîte de dépôt) ne figuraient pas parmi les documents disponibles : tout ce qui en dépend est marqué **non vérifié**.

## 2. Exigences et état

| # | Exigence | Statut de l'exigence | Source | Fichier du dépôt | État |
|---|---|---|---|---|---|
| 1 | Dépôt GitHub d'équipe remis le 21 sept. 2026, 23 h 59 | Exigé | PC, J1 | Ce dépôt | Dépôt créé ; remise à confirmer |
| 2 | SKILL.md d'équipe | Exigé | J1, PC | [SKILL.md](../SKILL.md) | Présent (v2 proposée, à valider par l'équipe) |
| 3 | Skill v2 et historique des versions | Exigé | J2 (diap. 41), L 9.2 | [SKILL.md](../SKILL.md), [skills/historique/](../skills/historique/) | Présent ; **v2 non encore réexécutée sur le jeu de test** |
| 4 | KIQ et hypothèses | Exigé | L 9.2 | [01_kiq_et_hypotheses.md](01_kiq_et_hypotheses.md) | Couvert, vérifié contre la table KIQ |
| 5 | Sources avec type, cote, connecteur, fréquence, biais connu | Exigé | J2, L 9.2 | [sources.csv](../configuration/sources.csv) | Couvert, 48 sources exportées de la base |
| 6 | Schéma de la base | Exigé | J2, L 9.2 | [02_schema_airtable.md](02_schema_airtable.md) | Couvert, vérifié le 20 sept. |
| 7 | Chaîne maillon par maillon, niveaux d'automatisation, points de contrôle | Exigé | J2, L 9.2 | [03_chaine_de_veille.md](03_chaine_de_veille.md), [workflows/](../workflows/) | Couvert ; mécanisme de planification non vérifié |
| 8 | Règles d'alerte et seuils | Exigé | J2, L 9.2 | [04_alertes_et_seuils.md](04_alertes_et_seuils.md) | Couvert (règles) ; détection automatique des seuils non démontrée |
| 9 | Grille de confiance | Exigé | J2, L 9.2 | [05_grille_de_confiance.md](05_grille_de_confiance.md) | Couvert |
| 10 | Jeu de test (3 à 5 pages difficiles avec fiche attendue) | Exigé | J2, L 9.2 | [jeu_de_test.md](../tests/jeu_de_test.md) | Défini (5 pages) ; **résultats de réexécution : aucun** |
| 11 | Défaillances connues avec leur repli | Exigé | J2, L 9.2 | [06_defaillances_connues.md](06_defaillances_connues.md) | Couvert |
| 12 | Aucune clé, jeton, mot de passe ni donnée personnelle | Exigé | J2 (diap. 4), L 9.2 | Ensemble du dépôt | Audit effectué avant chaque commit ; voir section 3 |
| 13 | Usage de l'IA déclaré et tracé (niveau 4 pour la plateforme d'équipe) | Exigé | PC, J2 (diap. 4) | [07_declaration_usage_ia.md](07_declaration_usage_ia.md) | **Partiel : parties à compléter par l'équipe** |
| 14 | Archivage des briefs (date, version, destinataires, fiches citées) et des alertes | Attendu | L 8.2 | [outputs/archive_briefs.md](../outputs/archive_briefs.md) | Registre créé, **aucune entrée vérifiée** |
| 15 | Exemples de sorties réellement produites | Non exigé explicitement | Aucune | [outputs/](../outputs/) | Fourni à titre de preuve d'exécution |
| 16 | README, structure en dossiers, .gitignore | Non exigé explicitement | Aucune (bonne pratique) | [README.md](../README.md) | Fournis |
| 17 | Dépôt public | **Non confirmé** | Aucune exigence trouvée | Sans objet | Décision de l'équipe |
| 18 | Format de la remise sur Moodle (lien, texte en ligne) | **Non confirmé** | Page Moodle non disponible | Sans objet | À vérifier sur Moodle |

## 3. Sécurité et confidentialité

- **Sans clé ni secret** : contrôle par motifs (clés d'API, jetons, mots de passe, en-têtes d'autorisation) sur tous les fichiers avant publication.
- **Sans donnée personnelle** : aucun nom de membre, aucune adresse courriel, aucun identifiant de compte ; les rôles remplacent les noms.
- **Sans identifiants Airtable** : identifiant de base, de tables, de vues et d'enregistrements retirés.
- **Documents protégés** : les documents du cours (plan de cours, diapositives, gabarits) sont cités par leur titre et ne sont pas reproduits.
- **Briefs** : non publiés (voir [archive_briefs.md](../outputs/archive_briefs.md)).

## 4. Livrables individuels (hors de ce dépôt)

Le prototype individuel, la réflexion analytique de 2 000 mots, la capsule vidéo et la Skill individuelle sont des évaluations **individuelles** (échéance le 2 octobre 2026, dépôt Moodle) et ne font pas partie du dépôt d'équipe.
