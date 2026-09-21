# Jeu de test de régression de la Skill

Cinq pages de référence couvrant les cas difficiles réellement rencontrés, avec le comportement attendu de la [Skill d'équipe](../SKILL.md). La Skill se réexécute sur ce jeu après chaque révision et chaque changement de modèle ; les écarts sont examinés avant remise en production.

> **État : jeu de référence proposé le 20 sept. 2026.** L'équipe déclare avoir testé la Skill validée avec un résultat conforme (message du 20 sept. 2026) ; le jeu qu'elle a utilisé et ses résultats n'ont pas été versés au dépôt, et les cinq pages ci-dessous n'ont pas été réexécutées par la personne qui a rédigé ce fichier : aucune colonne « résultat » n'est renseignée et aucun résultat n'est inventé. Les valeurs de prix changent d'une semaine à l'autre : le test vérifie les **règles** (dates, extrait, divergences, signalements, statut), non les montants. À l'équipe de verser ici son jeu et ses résultats.

Réglages communs : Skill d'équipe, KIQ centrale, échelle de fiabilité de l'équipe, connecteur de récupération indiqué. Pour chaque page, vérifier aussi : statut « À valider », champ « Validé par » vide, motif de rejet vide, une ligne de Journal produite même à zéro élément.

## Page 1 : page produit Home Depot sans prix affiché (sacs Husky)

| Élément | Contenu |
|---|---|
| Adresse | https://www.homedepot.ca/product/husky-contractor-clean-up-bags-158-l-capacity-32-count-/1000449142 |
| Cas difficile | Un visiteur non localisé reçoit le magasin par défaut hors Québec (Niagara Falls) ; le prix affiché est absent, seule une valeur structurée existe |
| Fiche attendue | **Aucune fiche de prix.** Ligne de Journal avec l'échec (prix affiché non rendu, magasin servi hors Québec). Si une fiche est produite : prix affiché vide, valeur structurée nommée comme telle et non substituée, magasin servi et absence de succursale québécoise dans « Champs vides signalés », date du fait « non indiquée » |
| Règle éprouvée | Ne jamais substituer silencieusement la valeur structurée au prix affiché ; repli manuel avec succursale québécoise confirmée |
| Origine du cas | Champ « Biais connu » de la source (correction du 9 septembre) |
| Résultat de réexécution | Résultat non versé au dépôt |

## Page 2 : divergence entre prix affiché et valeur structurée (sacs Maximum, RONA)

| Élément | Contenu |
|---|---|
| Adresse | https://www.rona.ca/fr/produit/sacs-a-dechets-ultra-resistant-pour-entrepreneur-maximum-3-mil-plastique-noir-159-l-33-po-x-48-po-32-boite-33483-0028029 |
| Cas difficile | Le prix affiché diffère de la valeur des données structurées de la même page ; disponibilité issue d'une collecte sans succursale confirmée |
| Fiche attendue | Une fiche dont le **prix affiché** est la valeur de référence ; les deux valeurs rapportées dans le résumé ; divergence, absence de prix régulier barré, absence de mention de rabais et disponibilité non exploitable signalées dans « Champs vides signalés » ; date du fait « non indiquée » |
| Fiche de référence | Fiche validée du 9 sept. (prix affiché 26,99 $, valeur structurée 14,99 $) |
| Résultat de réexécution | Résultat non versé au dépôt |

## Page 3 : page sans date de publication (emplois du siège social de BMR)

| Élément | Contenu |
|---|---|
| Adresse | https://www.bmr.ca/fr/emplois-siege-social |
| Cas difficile | La seule date visible (colonne « Ouverte ») n'est pas une date de publication |
| Fiche attendue | Date du fait « non indiquée » ; la date de la colonne « Ouverte » n'est pas reprise comme date du fait et sa nature est signalée dans « Champs vides signalés » ; niveau de confiance moyen justifié (le fait est cité exactement, calendrier et périmètre non documentés) ; aucune inférence sur les centres de distribution existants |
| Fiche de référence | Fiche validée du 9 sept. (programme de regroupement des opérations dans un centre de distribution unique) |
| Résultat de réexécution | Résultat non versé au dépôt |

## Page 4 : page à plusieurs faits et compteur absent (aubaines Canac)

| Élément | Contenu |
|---|---|
| Adresse | https://www.canac.ca/canac/fr/2/c/AUB |
| Cas difficile | La requête rend 48 produits sans compteur ; trois étiquettes différentes (En circulaire, Liquidation, Spécial) dont seule la première mesure la pression promotionnelle |
| Fiche attendue | Une fiche comptant **uniquement** les articles « En circulaire » sur les produits rendus (24 sur 48 au relevé de référence) ; les articles « Liquidation » et « Spécial » exclus du décompte de largeur ; « compteur absent du rendu » et absence de date de fin signalés ; magasin servi indiqué |
| Fiche de référence | Fiche validée du 9 sept. |
| Résultat de réexécution | Résultat non versé au dépôt |

## Page 5 : page sans fait lié à la KIQ (fil de communiqués BMR)

| Élément | Contenu |
|---|---|
| Adresse | https://www.newswire.ca/fr/news/groupe-bmr/ |
| Cas difficile | Le communiqué le plus récent date de novembre 2025 : rien ne tombe dans la fenêtre d'observation |
| Fiche attendue | **Aucune fiche.** Une ligne de Journal quand même, avec zéro élément retenu et l'inactivité de la source notée |
| Règle éprouvée | Une page sans fait lié à la KIQ ne donne aucune fiche ; ce n'est pas un échec |
| Origine du cas | Une fiche avait été produite lors d'une collecte réelle, puis **rejetée pour le motif « hors KIQ »** : ce cas éprouve la règle qui aurait évité ce rejet |
| Résultat de réexécution | Résultat non versé au dépôt |

## Procédure de réexécution

1. Récupérer chaque page avec le connecteur indiqué (Firecrawl, ou collecte manuelle si la page l'exige).
2. Exécuter la Skill v2 sur le texte récupéré, sans écrire dans la base de production (base de test ou sortie de conversation).
3. Comparer aux fiches attendues ci-dessus, règle par règle.
4. Consigner la date, la version de la Skill, le modèle utilisé et les écarts dans [skills/historique/CHANGELOG.md](../skills/historique/CHANGELOG.md).
