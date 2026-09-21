# Exemples de fiches réellement produites

Deux fiches réelles de la base, validées par une personne, reproduites champ par champ pour montrer le format de sortie et le signalement des limites. Les identifiants d'enregistrement et le nom du validateur ne sont pas publiés. Le contenu cité provient de pages publiques des enseignes.

Ces exemples illustrent ce que le dispositif **a produit** ; ils ne prouvent pas, à eux seuls, quelle part de chaque champ a été rédigée par Claude et quelle part a été corrigée par l'équipe (Airtable ne conserve pas l'auteur d'un champ). Un troisième exemple, commenté, figure dans le [SKILL.md](../SKILL.md).

## Exemple 1 : une date qui n'est pas une date du fait (BMR, emplois du siège social)

Illustre la règle « ne jamais inventer une date » et le niveau de confiance moyen justifié.

```text
Titre : BMR — un poste de direction au siège social annonce un programme de regroupement des opérations dans un centre de distribution unique
Date du fait : non indiquée (colonne « Ouverte » : 31/08/2026; date de captation : 9 septembre 2026)
Date de captation : 2026-09-09
Adresse exacte : https://www.bmr.ca/fr/emplois-siege-social
Extrait cité : « pilotera l'un des trois volets stratégiques d'un programme de transformation majeur visant à regrouper les opérations au sein d'un centre de distribution unique »
Source : BMR — emplois siège social (primaire, Fiable)
Acteur : BMR
KIQ : KIQ 1.1, secondaire, dynamisme commercial relatif
Forme de veille : Concurrentielle
Résumé : L'affichage « Directeur / directrice principal(e), design et implantation », à Boucherville, décrit un programme de transformation visant à regrouper les opérations de BMR au sein d'un centre de distribution unique, avec conception opérationnelle, aménagement du site et intégration de solutions d'automatisation. Le mandat couvre aussi un plan de transition des opérations jusqu'à l'atteinte du régime permanent. La page siège social affiche 11 postes, tous en Permanent - Temps plein et tous à Boucherville, dont 3 en Opérations et 2 en Chaine d'approvisionnement et excellence opérationnelle.
Nature : Fait
Hypothèse concernée : H2
Crédibilité : Fiable
Niveau de confiance : Moyen
Pertinence : 5
Statut : Validée
Validé par : (nom non publié dans ce dépôt)
Motif de rejet :
Champs vides signalés : Date du fait : non indiquée. La seule date visible est celle de la colonne « Ouverte », 31/08/2026, dont le Biais connu de la source précise expressément qu'elle n'est pas une date de publication et ne peut servir de date du fait. Niveau de confiance moyen : le fait que BMR recrute pour ce mandat est avéré et cité mot pour mot; le calendrier, la localisation et le périmètre du regroupement annoncé ne sont pas documentés sur la page et restent à vérifier. Conséquence éventuelle sur les centres de distribution existants : non documentée, ne pas inférer.
Connecteur : Firecrawl
```

## Exemple 2 : une divergence de prix signalée, non tranchée en silence (RONA, sacs Maximum)

Illustre la règle du prix affiché comme valeur de référence, le signalement de la divergence avec la valeur structurée et de la disponibilité non exploitable.

```text
Titre : RONA — sacs à déchets Maximum 32/boîte, 26,99 $ affiché contre 14,99 $ en données structurées
Date du fait : non indiquée
Date de captation : 2026-09-09
Adresse exacte : https://www.rona.ca/fr/produit/sacs-a-dechets-ultra-resistant-pour-entrepreneur-maximum-3-mil-plastique-noir-159-l-33-po-x-48-po-32-boite-33483-0028029
Extrait cité : Sacs à déchets ultra résistant pour entrepreneur Maximum 3 mil plastique noir 159 L 33 po x 48 po 32/boîte
    N° d'article 0028029N° de produit 000160501N° de modèle 33483Format 33x48"x3 MILxBT/32
    26,99Boite
    Cet article n'est pas offert pour le moment, mais il peut être commandé en visitant le magasin sélectionné.
    RONA+ Galeries d'Anjou
    279 en magasin
    [données structurées de la page] <meta itemprop="price" content="14.99"> <meta itemprop="priceCurrency" content="CAD"> <meta itemprop="availability" href="https://schema.org/InStock">
Source : RONA — sacs à déchets Maximum (panier fixe) (primaire, Fiable)
Acteur : RONA
KIQ : KIQ 1, centrale (voir documentation/01_kiq_et_hypotheses.md)
Forme de veille : Commerciale
Résumé : Le prix affiché est de 26,99 $ la boîte pour le magasin RONA+ Galeries d'Anjou, sans prix régulier barré ni mention de rabais. Les données structurées de la page portent 14,99 $ pour le même article, soit une divergence de 12,00 $ avec le prix affiché. La disponibilité indiquée est « 279 en magasin » et la page affiche « Cet article n'est pas offert pour le moment ».
Nature : Fait
Hypothèse concernée : H1
Crédibilité : Fiable
Niveau de confiance : Élevé
Pertinence : 5
Statut : Validée
Validé par : (nom non publié dans ce dépôt)
Motif de rejet :
Champs vides signalés : Prix régulier barré : absent de la page. Mention de rabais : absente de la page. Date du fait : non indiquée, aucune période de validité affichée.
    DIVERGENCE : prix affiché 26,99 $ contre valeur structurée 14,99 $ (microdonnées schema.org/Offer, itemprop="price", content="14.99"). Le prix affiché est retenu comme valeur de référence; aucun choix silencieux n'a été fait entre les deux valeurs. Divergence identique à celle constatée au test du 8 septembre 2026 : elle persiste.
    Disponibilité relevée depuis une collecte automatisée sans succursale confirmée, non exploitable selon le biais connu de la source.
Connecteur : Firecrawl
```
