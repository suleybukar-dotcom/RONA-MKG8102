# Grille de confiance

Grille déclarée par l'équipe dans le mandat (bloc 4) et appliquée par la [Skill](../SKILL.md). Trois cotes distinctes qualifient trois objets différents ; elles ne se substituent pas les unes aux autres.

## 1. Fiabilité de la **source** (table Sources)

| Cote | Définition |
|---|---|
| Fiable | Source primaire officielle, produite par l'acteur lui-même, permettant d'observer directement l'information |
| Moyen | Source crédible mais indirecte, ou nécessitant une vérification complémentaire |
| Pauvre | Source faible, difficile à vérifier, ancienne ou insuffisamment documentée |
| À coter | Source dont la qualité n'a pas encore été évaluée |

Répartition des 48 sources au 20 sept. 2026 : 30 Fiable, 6 Moyen, 12 Pauvre, 0 À coter. Les 12 sources cotées Pauvre sont les avis publics (échantillon d'opinions extrêmes, corpus édité par la plateforme). Le biais de chaque source est inscrit dans son champ « Biais connu » ([sources.csv](../configuration/sources.csv)).

## 2. Crédibilité de l'**information** (champ Crédibilité de la fiche)

Même échelle (Fiable, Moyen, Pauvre, À coter), appliquée à une information précise et non à la source. Une information publiée par l'acteur lui-même et non contredite est Fiable ; la même page peut porter une information de crédibilité moindre (par exemple un prix affiché contredit par une valeur structurée).

## 3. Niveau de confiance (champ Niveau de confiance de la fiche)

| Niveau | Sens |
|---|---|
| Élevé | La mention figure sur la source primaire, vérifiée mot pour mot sur la page |
| Moyen | Fait cité exactement, mais contexte, calendrier ou périmètre non documentés |
| Faible | Signal isolé, extraction incomplète ou contexte manquant qui limite l'usage |

Ces définitions sont dégagées de la pratique observée dans les fiches ; elles ne sont pas formalisées dans le mandat et sont **à valider par l'équipe**. Chaque niveau est justifié en une ligne au moment de la production de la fiche (justification donnée dans la conversation, non conservée dans un champ de la base : limite connue).

## 4. Pertinence

Note de 1 à 5 au regard de la KIQ rattachée. Un fait hors KIQ n'est pas coté : il est rejeté (motif « hors KIQ »).

## 5. Registres de connaissance

| Nature | Définition opératoire |
|---|---|
| Fait | Observation datée sur une source ; sa vérité est sa traçabilité (extrait cité et adresse exacte) |
| Interprétation | Lecture qui répond à une KIQ ; porte un niveau de confiance et un validateur |
| Recommandation | Décision proposée, identifiée comme telle |

Au 18 sept. 2026, les six fiches de nature « Interprétation » (synthèses de la KIQ 1.2, croisements implantation et embauche, bilans de collecte) étaient toutes encore « À valider » : aucun insight validé n'existait à cette date.

## 6. Ce que la grille ne fait pas (limites)

- Le cours propose six propriétés pour construire une cote (fiabilité, rang, ancrage, corroboration, actualité, stabilité, la clause la plus basse l'emportant). L'équipe n'a pas déclaré les avoir adoptées : **non adopté, non vérifié**.
- La confiance exprimée par un modèle n'est pas une mesure ; elle est confirmée ou corrigée par l'humain lors de la validation.
- Aucun échantillon de contrôle mesurant la qualité réelle des classifications n'a été constitué : **non vérifié**.
