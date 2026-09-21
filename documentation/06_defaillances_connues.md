# Défaillances connues et replis

Relevé des pannes, limites et incohérences réellement constatées, avec le repli prévu. Un dispositif dont on connaît les pannes est un dispositif qu'on peut opérer. État au 20 septembre 2026 ; les heures du Journal sont en UTC. « Statut » : **résolu** (corrigé et constaté), **contourné** (repli en place), **ouvert** (non corrigé) ou **non vérifié**.

## 1. Collecte

| # | Défaillance | Preuve | Impact | Repli | Statut |
|---|---|---|---|---|---|
| 1 | **Connecteur Apify indisponible** (état « needs_reconnect », non authentifié) lors de l'exécution planifiée du 9 sept. | Journal : 12 lignes en échec à 15 h 48, une par source d'avis ; 12 lignes de reprise réussie à 16 h 06 après reconnexion par l'équipe | Aucun avis collecté pendant l'échec | Reconnexion du connecteur, puis relance des 12 sources ; l'échec est consigné, jamais silencieux | Résolu |
| 2 | **Circulaires inaccessibles aux robots** : contenu chargé dans un visualiseur de publication, hors du HTML ; refus HTTP 403 avec l'extracteur Apify | Journal : essai Apify du 6 sept. en échec ; champ « Biais connu » des circulaires | Quatre sources non automatisables | Téléchargement manuel du PDF (vraie couche de texte, sans reconnaissance de caractères), puis fiche selon la Skill ; ligne de Journal « Manuel » avec la raison | Contourné |
| 3 | **Home Depot : la succursale dépend d'un témoin de navigateur**, non de l'adresse. Un robot sans magasin confirmé reçoit par défaut Niagara Falls (Ontario), en anglais, sans prix (page Behr Marquee) ou sans produit (liste de promotions) | Champs « Biais connu » de quatre sources Home Depot (vérifiés les 7 et 8 sept.) | Trois sources Home Depot manuelles ; prix non comparables sans succursale québécoise confirmée | Confirmer d'abord la succursale de Beaubien Ouest, puis relever à la main. Piste non testée : profil de navigateur persistant | Contourné |
| 4 | **Page Husky (Home Depot) instable** : le 9 sept., première collecte automatisée sans prix affiché, seule la valeur structurée présente, magasin Niagara Falls | Champ « Biais connu » de la source (« correction du 9 septembre ») ; une fiche rejetée | L'hypothèse d'un prix par défaut constant est invalidée | Règle révisée : relever le prix affiché s'il existe ; sinon consigner l'échec au Journal et faire un relevé manuel de secours ; ne jamais substituer silencieusement la valeur structurée | Contourné |
| 5 | **Page promotions RONA servie depuis une succursale ontarienne** (Fort Erie) le 14 sept., malgré le paramètre d'adresse censé fixer la succursale (la même page avait été servie par une succursale québécoise le 9 sept.) : comportement non reproductible | Fiche du 14 sept. (à valider) ; fiche validée du 9 sept. sur la peinture SICO signalant le même magasin | Prix ou compteurs non comparables au relevé du 8 sept. | Fiche signalée dans « Champs vides signalés » ; décision de l'équipe demandée avant toute comparaison hebdomadaire | Ouvert |
| 6 | **Portail d'emploi Home Depot : une ville du filtre est écartée en silence** (18 villes retenues sur 19 demandées le 9 sept., adresse ramenée à 18 villes ; le 15 sept., une autre ville est écartée et la première réintégrée) | Fiche validée du 9 sept. ; fiche du 15 sept. (à valider) ; fiche « 90 postes contre 121 » sur un périmètre réduit | Comparaison brute des volumes de postes non fiable | Comparer chaque bannière à elle-même à date comparable ; **périmètre de villes fixe non adopté** | Ouvert |
| 7 | **Localisateur BMR dépendant de la géolocalisation du visiteur** (« Aucun magasin n'a été trouvé » pour un robot) | Journal : ligne manuelle du 15 sept. | Source non automatisable | Collecte manuelle | Contourné |
| 8 | **Divergence entre prix affiché et valeur structurée** d'une même page (RONA sacs Maximum : 26,99 $ affiché contre 14,99 $ structuré le 9 sept.) | Fiche validée du 9 sept. ; Journal du 19 sept. (divergence toujours signalée) | Risque de retenir un prix périmé | Le prix affiché est la valeur de référence ; les deux valeurs sont rapportées ; divergence signalée | Contourné |

## 2. Contrôle humain et diffusion

| # | Défaillance | Preuve | Impact | Repli | Statut |
|---|---|---|---|---|---|
| 9 | **Automatisations Airtable d'alerte en échec** faute de destinataire collaborateur de la base | Historique d'exécutions : échecs du 8 au 19 sept. selon l'automatisation ; succès à partir du 19 sept. | Aucun courriel d'alerte n'a pu partir pendant la période | Ajouter le destinataire comme collaborateur (cause du rétablissement non vérifiée) | Résolu, réception non vérifiée |
| 10 | **Alerte du deuxième point de contrôle branchée sur la mauvaise vue** (Kanban au lieu de « Fiches - Validées ») : elle part à la création des fiches | Configuration de l'automatisation ; exécutions coïncidant avec l'heure de création des fiches | Le signal ne correspond pas à une validation | Corriger la vue déclencheuse | Ouvert |
| 11 | **Champ « Validé par » rempli avant validation** : 57 des 60 fiches « À valider » portent les cinq noms de l'équipe | Lecture de la base le 20 sept. | Le nom ne prouve pas la validation ; seul le statut la prouve | S'appuyer sur le statut ; vider le champ tant que la fiche n'est pas validée | Ouvert, cause non vérifiée |
| 12 | **Envoi de brief par Gmail non démontré** ; test de connexion refusé lors de l'audit | Erreur du connecteur le 20 sept. | Canal de diffusion non prouvé | Envoi manuel après accord de la Direction, tracé dans le registre des briefs | Non vérifié |
| 13 | **Aucun registre d'alertes ni de briefs** dans la base | Cinq tables seulement | Diffusion non reconstituable | [outputs/archive_briefs.md](../outputs/archive_briefs.md) | Ouvert |

## 3. Qualité et documentation

| # | Défaillance | Preuve | Repli | Statut |
|---|---|---|---|---|
| 14 | **Aucun registre distinct des validations croisées** ; Perplexity sans usage documenté | Cinq tables ; déclaration d'usage du mandat (aucun autre modèle que Claude) | Le motif de rejet et « Validé par » en tiennent lieu ; la vérification se fait contre la page source | Ouvert |
| 15 | **Justification du niveau de confiance non conservée** dans la base | Champ inexistant | Justification donnée dans la conversation | Ouvert |
| 16 | **Détection des seuils d'alerte non automatisée** | Aucune automatisation ni tâche ne les calcule | Évaluation manuelle à l'analyse | Ouvert |
| 17 | **Jeu de test jamais réexécuté** depuis la révision de la Skill | [tests/jeu_de_test.md](../tests/jeu_de_test.md) | À réexécuter après chaque révision et chaque changement de modèle | Ouvert |
| 18 | **Mécanisme des tâches planifiées non observable** depuis le dépôt ; le texte archivé des tâches (9 sept.) précède les cadences du mandat (11 sept.) | [workflows/](../workflows/) | Le Journal prouve les exécutions ; texte courant à verser au dépôt | Non vérifié |
| 19 | **Incohérences de la base** : fréquence uniforme « Hebdomadaire » malgré un rythme mensuel prévu pour le localisateur BMR ; descriptions de champs de cotation obsolètes ; 48 sources dans le mandat, 49 dans sa déclaration | [02_schema_airtable.md](02_schema_airtable.md) | Corriger la base ou la déclaration | Ouvert |
| 20 | **Fiche à valider en attente** : 60 fiches sur 120 (dont 19 créées le 19 sept.) | Lecture de la base le 20 sept. | Le délai de validation dépasse la cadence de collecte ; l'alerte quotidienne existe désormais | Ouvert |

## 4. Angles morts (rappel)

Veille technologique et sociétale exclues ; aucun acteur n'annonce ses fermetures ; prix en ligne différents des prix en magasin ; avis publics = opinions extrêmes (fiabilité Pauvre). Voir [01_kiq_et_hypotheses.md](01_kiq_et_hypotheses.md).
