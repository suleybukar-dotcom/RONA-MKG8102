# Alertes, seuils et diffusion

État vérifié le 20 septembre 2026. Les seuils viennent du texte de travail du mandat (adoptés par l'équipe le 9 septembre 2026) ; la version de deux pages remise le 11 septembre en donne un résumé.

## 1. Règle générale

- Une alerte est **proposée** au franchissement d'un seuil, **jamais envoyée automatiquement**.
- Destinataire de l'alerte : la **Direction de l'intelligence marketing**, qui décide de sa transmission au décideur. Exception : l'alerte de qualité de source s'adresse à l'équipe, non au décideur.
- Le brief BLUF, aux deux semaines, va à la **Direction du marchandisage et des promotions, Québec** (en copie : marketing et approvisionnement).
- **Contrôle humain 2** : aucun brief ni aucune alerte ne part sans l'accord explicite de la Direction de l'intelligence marketing.

## 2. Les huit seuils

| # | Indicateur | Seuil | Hypothèse ou KIQ servie |
|---|---|---|---|
| 1 | Prix d'une unité du panier fixe entre deux relevés | Variation de plus de 10 % | KIQ 1 (écart de prix) |
| 2 | Alignement d'un concurrent sur le prix de RONA après une baisse | À moins de 2 % dans les 14 jours | H1 |
| 3 | Nombre d'articles en promotion d'une bannière | Variation de plus de 25 % | KIQ 1 (part de voix, largeur) |
| 4 | Ouverture, fermeture, agrandissement ou acquisition au Québec | Toute mention, sans seuil quantitatif | KIQ 1.1 |
| 5 | Volume d'affichages de postes d'une bannière | Variation de plus de 20 % | KIQ 1.1 |
| 6 | Région ou ville nouvelle dans un portail d'emploi ou un localisateur | Toute apparition | KIQ 1.1 |
| 7 | Thème « prix » dans les avis | Gain d'un rang dans au moins 6 des 12 succursales | KIQ 1.2, H3 |
| 8 | Source qui échoue | Deux cycles consécutifs (alerte interne à l'équipe) | Qualité du dispositif |

Contenu minimal proposé pour toute alerte (**proposition, à valider par l'équipe**) : l'indicateur, le seuil franchi, les valeurs avant et après, les identifiants des fiches concernées, l'heure et l'action attendue de la personne qui reçoit.

## 3. État de la mise en œuvre

| Élément | État vérifié |
|---|---|
| Détection automatique des huit seuils | **Non démontrée** : aucune automatisation ni tâche consultée ne calcule ces seuils ; leur évaluation se fait à l'analyse |
| Registre des alertes proposées (indicateur, seuil, heure, suite) | **Absent** : aucune table ni aucun fichier consultés ne le contiennent |
| Brief BLUF | Un brief a été produit (version interactive et version PDF, puis une version graphique) ; **envoi non démontré** |
| Envoi par Gmail | Test refusé lors de l'audit du 20 sept. ; **non vérifié** |

## 4. Automatisations Airtable d'alerte interne

Ce sont des alertes de processus (elles ne détectent aucun des huit seuils ci-dessus) et elles n'écrivent aucune donnée.

| Automatisation | Déclencheur | Statut | Historique constaté |
|---|---|---|---|
| Fiches en attente de validation depuis plus de trois jours | Quotidien, 9 h (heure de Toronto) | Déployée | Échecs du 8 au 19 sept. (les six premiers sans cause détaillée, les suivants : destinataire non collaborateur de la base) ; **succès le 20 sept.** |
| Sources en retard de collecte | Hebdomadaire, lundi 13 h UTC | Déployée | Une exécution le 14 sept., en échec (même cause) ; prochaine exécution le lundi 21 sept. |
| Fiche validée, deuxième point de contrôle | Une fiche entre dans une vue | Déployée | Échecs du 9 au 16 sept. (même cause) ; **succès le 19 sept.** (20 exécutions) |
| « Automation 1 » | Mise à jour du statut | Non déployée (brouillon) | Aucune |

Points à noter :

1. **Le changement d'échec en succès n'est pas expliqué par la configuration** : les automatisations consultées le 20 sept. sont identiques à celles du 18 sept. La cause probable est une modification hors de la configuration (ajout du destinataire comme collaborateur), **non vérifiée**.
2. **Statut « succès » ne prouve pas la réception** : la réception des courriels n'a pas été vérifiée.
3. **Décalage entre nom et configuration** : l'automatisation du deuxième point de contrôle se décrit comme déclenchée par la vue « Fiches - Validées », mais son déclencheur technique pointe vers la vue « Fiches - Kanban par Statut ». Ses exécutions coïncident avec la création des fiches, non avec leur validation. À corriger avant de s'y fier comme second point de contrôle.
4. Le destinataire configuré n'est pas l'adresse dédiée du dispositif décrite dans les instructions du projet. Les adresses ne sont pas publiées dans ce dépôt.

## 5. Mode « tiré » et archivage

- Mode tiré du cours : vue Validée en lecture seule pour le décideur. Une vue de grille existe ; aucune interface Airtable n'a été construite.
- Archivage des briefs et des alertes (date, version, destinataires, fiches citées) : voir [outputs/archive_briefs.md](../outputs/archive_briefs.md).
