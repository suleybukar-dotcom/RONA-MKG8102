---
name: fiche-de-veille
description: À utiliser dès qu'un contenu collecté (page web récupérée par Firecrawl, communiqué, publication, avis) doit entrer dans la base de veille de l'équipe sous forme de fiche conforme à la table « Fiches de veille ». Ne pas utiliser pour résumer un document sans l'inscrire dans la base.
---

# Fiche de veille — MKG8102, ESG UQAM

## Finalité
Transformer le texte brut d'une page collectée en un enregistrement de la table
« Fiches de veille » : un fait daté, sourcé, coté, classé et rattaché à une question
d'intelligence clé (KIQ). Une fiche = un fait, jamais un résumé de page.

## Intrants
- Le contenu de la page (Markdown produit par Firecrawl ou texte collé) et son adresse exacte
- La KIQ visée : Dans quelle mesure la stratégie promotionnelle de RONA (mises en avant produits, positionnement prix, offres spéciales) lui permettra-t-elle de gagner des parts de marché sur le segment de la rénovation résidentielle au Québec d’ici la fin de 2026?
- La source et sa cote de fiabilité, telles qu'inscrites dans la table « Sources »
- L'échelle de cotation de l'équipe : Fiable · Moyen · Pauvre · À coter (Fiable = source primaire officielle, produite par l'acteur lui-même, permettant d'observer directement l'information; Moyen = source crédible mais indirecte, ou nécessitant une vérification complémentaire; Pauvre = source faible, difficile à vérifier, ancienne ou insuffisamment documentée; À coter = source dont la qualité n'a pas encore été évaluée)

## Méthode
1. Lire le contenu en entier avant d'écrire quoi que ce soit.
2. Relever uniquement les faits datés qui concernent la KIQ. Si la page ne contient
   aucun fait lié à la KIQ, le dire et ne créer aucune fiche.
3. S'il y a plusieurs faits distincts, produire une fiche par fait.
4. Rédiger le résumé en trois phrases au maximum, faits seulement.
5. Classer : forme de veille (concurrentielle, commerciale, technologique, sociétale);
   nature (fait, interprétation ou recommandation); hypothèse concernée (H1, H2, H3 ou aucune).
6. Coter la crédibilité de l'information selon l'échelle de l'équipe, puis donner le
   niveau de confiance (élevé, moyen, faible) et la pertinence (1 à 5).
7. Relire la fiche contre les règles de qualité ci-dessous avant de la livrer.

## Format de sortie
Un champ par ligne, dans cet ordre exact, avec le nom du champ suivi de deux-points :

Titre
Date du fait
Date de captation
Adresse exacte
Extrait cité
Source
Acteur
KIQ
Forme de veille
Résumé
Nature
Hypothèse concernée
Crédibilité
Niveau de confiance
Pertinence
Statut
Validé par

## Règles de qualité
1. Ne jamais inventer une date. Si la page ne date pas le fait, écrire « non indiquée ».
2. L'adresse doit être celle de la page effectivement collectée, jamais reconstruite.
3. L'extrait cité doit être copié mot pour mot depuis la page, entre guillemets.
4. Un champ que la page ne permet pas de remplir reste vide et est signalé en fin de fiche.
5. Le résumé ne contient que des faits; toute inférence va dans le champ « Nature ».
6. Le niveau de confiance est obligatoire et justifié en une ligne.
7. Statut est toujours « à valider ». Validé par reste vide : ces deux champs
   appartiennent à l'humain, jamais au modèle.

## Exemple de fiche conforme
Titre : La Cordée offre la location de ski de fond hors-piste dans trois de ses magasins
Date du fait : non indiquée
Date de captation : 2026-09-02
Adresse exacte : https://www.lacordee.com/pages/magasins
Extrait cité : « Location de ski de fond hors-piste »
Source : Site de La Cordée — page Magasins (primaire)
Acteur : La Cordée
KIQ : Lequel de nos concurrents directs lancera une offre de location d'équipement de camping au Québec d'ici avril?
Forme de veille : concurrentielle
Résumé : La page Magasins de La Cordée mentionne un service de location de ski de fond hors-piste dans les magasins Saint-Laurent, Saint-Hubert et Québec. Le magasin de Laval y est indiqué comme fermé. Le menu du site comporte une entrée « Entretien | Location ».
Nature : fait
Hypothèse concernée : H2 (un concurrent teste la location sans l'étendre au camping)
Crédibilité : information publiée par l'acteur lui-même, non contredite
Niveau de confiance : élevé — la mention figure sur le site de l'entreprise
Pertinence : 4
Statut : à valider
Validé par :
Champs vides signalés : la date du fait n'est pas indiquée sur la page.
