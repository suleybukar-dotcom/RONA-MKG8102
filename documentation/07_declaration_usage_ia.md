# Déclaration d'usage de l'intelligence artificielle

Plateforme d'équipe : niveau AIAS 4 (tout usage permis, déclaré et tracé). Cette déclaration couvre le contenu de ce dépôt. Elle distingue ce qui est **établi** (vérifiable dans le dépôt, la base ou les documents du cours) de ce que l'équipe doit **compléter**, car les parties humaines du travail ne sont pas observables par l'outil qui a rédigé la documentation.

## 1. Outils et modèles

| Outil | Usage dans le dispositif | Source de l'information |
|---|---|---|
| Claude (Anthropic), application Claude et Claude Code | Orchestration de la chaîne, production des fiches selon la Skill, rédaction de la documentation de ce dépôt | Déclaration du mandat (11 sept.) ; historique des commits de ce dépôt |
| Modèle de la préparation de ce dépôt | Claude Sonnet 5, via Claude Code | Attribution indiquée dans les commits du dépôt |
| Connecteurs MCP : Firecrawl, Apify, Airtable, GitHub | Collecte web, avis publics, mémoire structurée, versionnement | Journal de collecte ; dépôt |
| Gmail | Prévu pour l'envoi des briefs | **Non vérifié** (voir [défaillances](06_defaillances_connues.md)) |
| Perplexity | Prévu par le cours pour la vérification ancrée | **Aucun usage documenté** : la déclaration du mandat indique « aucun autre modèle » que Claude |

## 2. Requêtes significatives

- Consigne de finalisation du dépôt (20 sept. 2026) : auditer le projet réel, lire les consignes officielles, identifier les livrables, préparer le dépôt, auditer la sécurité, ne rien publier avant confirmation explicite.
- Requêtes antérieures liées au dispositif, déclarées dans le mandat : génération et confrontation de formulations de KIQ ; audit en lecture seule de la base ; tests de faisabilité de collecte, source par source, avec consigne de documenter les échecs ; rédaction des prompts de collecte et des tâches planifiées.
- **À compléter par l'équipe** : les requêtes significatives faites par les membres depuis le 11 septembre (Skill, briefs, validation), avec leur formulation.

## 3. Ce qui a été généré, vérifié, rejeté, décidé

| Registre | Contenu | Établi ou à compléter |
|---|---|---|
| **Généré par l'IA** | Les fichiers de ce dépôt (README, documentation, jeu de test, exports de la base, proposition de Skill v2), à partir de lectures directes de la base et des documents du cours | Établi |
| **Vérifié** | Chiffres relus dans la base le 20 sept. 2026 ; exigences du dépôt relues dans les documents du cours ; recherche de clés, de jetons, d'adresses courriel, de noms et d'identifiants avant publication | Établi |
| **Rejeté ou corrigé (sorties de l'IA non retenues)** | Voir la section 4 | Établi |
| **Rédigé ou décidé par l'équipe** | Choix du cas et de la décision ; formulation finale de la KIQ ; sélection et cotation des sources ; échelle de fiabilité ; seuils d'alerte ; règles de comparaison ; répartition des rôles (déclaration du mandat) | Établi pour le mandat ; **à compléter** pour ce dépôt : ce que l'équipe a modifié dans la documentation et la Skill v2 |

## 4. Sorties de l'IA non retenues ou corrigées

**Dans le dispositif (déclarées dans le mandat, vérifiées dans la base)**

1. Hypothèse d'un « prix par défaut constant et reproductible » pour la page Husky de Home Depot : **invalidée** par la première collecte automatisée du 9 sept. ; correction consignée et datée dans le champ « Biais connu » de la source.
2. Constat du 8 sept. selon lequel le paramètre de succursale de l'adresse RONA fige la succursale de référence : **non reproduit** lors du relevé du 14 sept. (succursale ontarienne) ; signalé dans une fiche en attente de validation.
3. 7 fiches produites par la chaîne et **rejetées par un humain** (6 « hors KIQ », 1 « citation inexacte »). La déclaration du mandat mentionne trois conclusions du modèle démenties par les tests ; seules les deux ci-dessus ont été retrouvées lors de cet audit.

**Pendant la préparation de ce dépôt (20 sept. 2026)**

4. Une affirmation selon laquelle les lignes automatisées du Journal ne portent aucun nom d'opérateur a été **rejetée après vérification** : les 127 lignes de Firecrawl et d'Apify portent un opérateur. La distinction automatisé et manuel repose sur le champ « Connecteur ».
5. Le nombre de sources Apify en échec le 9 septembre, cité à 4 dans un document d'appui, a été **corrigé à 12** d'après le Journal (12 échecs à 15 h 48 UTC, 12 reprises à 16 h 06 UTC).
6. L'affirmation « aucune alerte Airtable n'a réussi » (constat du 18 sept.) est **périmée** : des exécutions réussies existent depuis le 19 sept.
7. Décisions de la préparation, à confirmer par l'équipe : ne pas publier les briefs, les noms de membres, les adresses courriel ni les identifiants de la base ; ne pas présenter comme configuration courante le texte archivé des tâches planifiées du 9 sept.

## 5. Trace de la validation humaine

- Validation ou rejet de chaque fiche par une personne nommée dans le champ « Validé par » (noms non publiés ici). Limite : 57 des 60 fiches « À valider » portent déjà des noms (voir [défaillances](06_defaillances_connues.md)) ; le statut fait foi.
- Aucun brief ni aucune alerte sans accord de la Direction de l'intelligence marketing (règle du mandat) ; **aucune trace d'accord documentée** à ce jour (voir [registre des briefs](../outputs/archive_briefs.md)).
- Historique des commits du dépôt (dates et attribution des modifications).
- **À compléter par l'équipe** : date et personne qui approuve la publication de ce dépôt.
