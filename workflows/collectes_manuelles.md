# Collectes manuelles

> Procédure des sept sources que l'automatisation ne peut pas servir (texte du 9 septembre 2026). Le rythme exact (six le lundi, une chaque mois) est celui du mandat ; le champ « Fréquence » de la base indique « Hebdomadaire » pour les sept sources.

Sept collectes que l'automatisation ne peut pas servir, pour une raison testée et documentée.

## Chaque lundi, six collectes

### 1. RONA — circulaire
`https://www.rona.ca/fr/circulaire`
Sélectionne la succursale **RONA+ Galeries d'Anjou**. Télécharge le PDF de la circulaire. Note la période de validité affichée. Colle le texte dans Claude avec l'adresse.
*Pourquoi manuelle : contenu affiché dans un visualiseur de publication, hors du HTML. Testé le 6 septembre, code 200 mais aucun produit lisible.*

### 2. BMR — circulaire
`https://www.bmr.ca/fr/circulaire`
Succursale servie par défaut : **Matco St-Léonard**. Même procédure.
*Même cause.*

### 3. Canac — circulaire
`https://www.canac.ca/canac/fr/2/circulaire-reguliere`
Le `/2/` de l'adresse désigne **L'Ancienne-Lorette**, succursale de référence de toutes les sources Canac. Même procédure.
*Même cause.*

### 4. Home Depot — circulaire
`https://www.homedepot.ca/circulaire`
**Confirme d'abord une succursale québécoise**, Beaubien Ouest de préférence. Sans cela le site sert Niagara Falls, en Ontario. Même procédure.
*Double cause : visualiseur de publication, et magasin par défaut hors Québec.*

### 5. Home Depot — peinture Behr Marquee, panier fixe
`https://www.homedepot.ca/product/behr-marquee-interior-semi-gloss-enamel-paint-primer-in-ultra-pure-white-3-79l/1000787191`
Confirme **Beaubien Ouest**, puis relève le prix affiché.
*Pourquoi manuelle : cette page n'affiche aucun prix tant qu'un magasin n'est pas confirmé. Vérifié deux fois, les 7 et 8 septembre. La page des sacs Husky, elle, rend un prix par défaut : seule celle-ci résiste.*

### 6. Home Depot — aubaines et promotions
`https://www.homedepot.ca/recherche?q=*&filter=6y5`
Confirme **Beaubien Ouest**, puis note le **nombre total de résultats** affiché. Au 8 septembre : 3 297. Relève aussi les premiers produits si le temps le permet.
*Pourquoi manuelle : sans magasin confirmé, la liste entière est vide pour un robot. Blocage plus radical que sur les pages produits.*
*À revérifier à chaque révision du mandat : le paramètre `filter=6y5` est un identifiant interne de facette, il peut changer sans erreur visible.*

## Une fois par mois, le 2

### 7. BMR — localisateur de succursales
`https://www.bmr.ca/fr/storelocator/`
Note le compteur affiché, au 8 septembre « 238 magasins trouvés », et le nombre de succursales québécoises.
*Pourquoi manuelle : la liste dépend d'une géolocalisation du visiteur. Un robot reçoit « Aucun magasin n'a été trouvé à partir de l'information fournie ».*
*Écart à surveiller : la page carrières de BMR annonce 275 succursales, le localisateur en compte 238.*

## Après chaque collecte manuelle

Colle le texte dans Claude avec l'adresse exacte, et demande la production des fiches selon la Skill fiche-de-veille. La ligne de Journal doit porter **Connecteur = Manuel** et, dans le champ Erreurs, la raison documentée de l'échec automatisé. Un repli manuel n'est jamais silencieux.

---

## Contrôle humain, chaque semaine

Les tâches planifiées remplissent la file d'attente. Elles ne valident rien.

1. Ouvre la vue Kanban des Fiches de veille, groupée par Statut.
2. Passe en revue les fiches « À valider » : date, extrait mot pour mot, adresse exacte, rattachement à la bonne KIQ.
3. Bascule chaque fiche vers Validée ou Rejetée, et renseigne Validé par. Une fiche rejetée porte un motif de la liste fermée : date inventée, citation inexacte, hors KIQ, autre.
4. Lis les erreurs du Journal de la semaine. Une source qui échoue deux cycles de suite doit être remontée à l'équipe, pas réparée en silence.

C'est ce geste, et lui seul, qui distingue un dispositif de veille d'un robot qui remplit une base.
