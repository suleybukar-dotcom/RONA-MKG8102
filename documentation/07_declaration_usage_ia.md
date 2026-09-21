# Déclaration d'usage de l'intelligence artificielle

Plateforme d'équipe : niveau AIAS 4 (tout usage permis, déclaré et tracé). Ce document réunit la déclaration remise avec le mandat, ses corrections et compléments constatés le 20 septembre 2026, et l'usage de l'IA propre à la préparation de ce dépôt.

## 1. Déclaration remise avec le mandat (11 septembre 2026, texte de l'équipe)

> **Outils et modèles.** Claude (Anthropic, Opus 5) comme modèle d'orchestration, dans l'application Claude et dans Claude Code, avec les connecteurs MCP Firecrawl (ingestion web), Apify (avis publics) et Airtable (écriture), ainsi que l'extension navigateur Claude pour la recherche de sources sur le web ouvert. Aucun autre modèle.
>
> **Principales requêtes.** À partir du contexte d'affaires de RONA, génération puis confrontation de formulations candidates de KIQ, chacune évaluée selon les cinq propriétés présentées dans le cours. La requête utilisée pour amorcer la sélection était : « À partir des informations du plan de cours et des lectures et diapositives, identifie pour une KIQ principale, deux KIQ secondaires et justifies le tout pour discussion avec mes coéquipiers. » À la suite des discussions et de l'évaluation collective, la KIQ principale a été rejetée une fois avant le choix final, tandis que les deux KIQ secondaires ont chacune été rejetées deux fois. Le choix final a été discuté et validé en classe le 5 septembre 2026. Pour les KIQ secondaires, la requête exacte utilisée était : « Dans quelle mesure la stratégie promotionnelle de RONA […] lui permettra-t-elle de gagner des parts de marché sur le segment de la rénovation résidentielle au Québec d'ici fin 2026 ? Aide-moi à déterminer 2 KIQs secondaires SVP » Nous avons également précisé à Claude : « Ne tiens pas compte de notre date de remise, il s'agit d'une veille active dédiée aux décideurs de RONA ».
>
> Les autres requêtes ont porté sur l'audit en lecture seule de la base Airtable, les tests de faisabilité de collecte, source par source, avec consigne de documenter les échecs, ainsi que la rédaction des prompts de collecte et des tâches planifiées.
>
> **Généré par l'IA.** La structure des documents de travail, les propositions de sources et de requêtes, les tests techniques de faisabilité, les textes des champs Biais connu tirés des résultats de test, et une première rédaction des sept blocs.
>
> **Rédigé, décidé ou modifié par l'équipe.** Le choix du cas et de la décision à éclairer ; la formulation finale des trois KIQ et leur évaluation sur les cinq propriétés ; la sélection, la justification et la cotation des 49 sources — toutes les adresses ont été recherchées et vérifiées par un membre de l'équipe, le modèle ayant pour consigne de ne jamais deviner une URL ; l'échelle de fiabilité et les huit seuils d'alerte ; les règles de substitution du panier fixe et de comparaison des affichages ; la répartition des rôles.
>
> **Trace de la validation humaine.** Chaque écriture dans Airtable a été présentée en texte et exécutée seulement après accord explicite, sauf les tâches planifiées, qui écrivent au seul statut « À valider » ; les fiches sont validées ou rejetées par un humain nommé dans le champ Validé par. Le journal de collecte conserve les échecs, dont les douze échecs Apify du 9 septembre et leurs reprises. Trois conclusions produites par le modèle, démenties par les tests, ont été corrigées dans la base, consignées et datées dans les champs Biais connu. La KIQ principal a été remise en question par le groupe, des itérations ont été apportées et nous avons également sollicité l'expertise du professeur pour s'assurer d'être sur la bonne voie.

## 2. Corrections et compléments constatés le 20 septembre 2026

| Sujet | Déclaration du 11 sept. | Constat du 20 sept. | Action pour l'équipe |
|---|---|---|---|
| **Perplexity** | « Aucun autre modèle » | Perplexity est utilisé par le Responsable des insights pour vérifier les informations collectées (déclaré par l'équipe le 20 sept.) | **Corriger la déclaration** : la non-déclaration d'un outil d'IA est une infraction au sens du plan de cours. Tracer les requêtes, les fiches vérifiées, les sources extraites et les décisions prises |
| **Nombre de sources** | 49 sources | La base compte 48 sources (lecture du 20 sept.) et le mandat en indique 48 | Harmoniser à 48 dans la déclaration, ou expliquer l'écart |
| **Gmail** | Non mentionné | Connexion testée le 5 sept. ; envoi de briefs et réception d'alertes non essayés à ce jour | Déclarer l'usage de Gmail quand un envoi aura lieu |
| **Modèle** | Claude Opus 5 | Ce dépôt a été préparé avec Claude Code (modèle Claude Sonnet 5, selon l'attribution des commits) | Préciser le modèle utilisé pour chaque tâche si la version diffère |
| **Skill** | Non mentionnée | La Skill d'équipe est validée et déclarée testée ; une proposition de révision a été rédigée avec Claude Code et n'est pas adoptée | Rien tant que l'équipe ne l'adopte pas |

## 3. Usage de l'IA propre à la préparation de ce dépôt (20 septembre 2026)

| Registre | Contenu | Statut |
|---|---|---|
| **Requête** | Consigne de finalisation du dépôt : auditer le projet réel, lire les consignes officielles, identifier les livrables, préparer le dépôt, auditer la sécurité, publier sur confirmation explicite | Établi |
| **Généré par l'IA** | README, documentation, schémas Mermaid, jeu de test de référence, exports de la base (sources, extrait du Journal, exemples de fiches), proposition de révision de la Skill, à partir de lectures directes de la base et des documents du cours | Établi |
| **Vérifié** | Chiffres relus dans la base le 20 sept. ; exigences relues dans les documents du cours ; recherche de clés, jetons, courriels, noms et identifiants dans les fichiers et dans tout l'historique Git avant chaque publication | Établi |
| **Fourni ou décidé par l'équipe** | La déclaration du mandat ci-dessus ; la validation et le test de la Skill ; la confirmation que Gmail n'a pas été essayé ; l'usage de Perplexity ; la capture des tâches planifiées ; le brief remis ; la demande de rendre le dépôt public | Établi (messages du 20 sept. 2026) |
| **Modifié par l'équipe dans la documentation** | | **À compléter par l'équipe** |

### Sorties de l'IA non retenues ou corrigées

**Dans le dispositif (vérifiées dans la base)**

1. Hypothèse d'un « prix par défaut constant et reproductible » pour la page Husky de Home Depot : **invalidée** par la première collecte automatisée du 9 sept. ; correction consignée et datée dans le champ « Biais connu » de la source.
2. Constat du 8 sept. selon lequel le paramètre de succursale de l'adresse RONA fige la succursale de référence : **non reproduit** lors du relevé du 14 sept. (succursale ontarienne) ; signalé dans une fiche en attente de validation.
3. 7 fiches produites par la chaîne et **rejetées par un humain** (6 « hors KIQ », 1 « citation inexacte »). La déclaration du mandat mentionne trois conclusions du modèle démenties par les tests ; seules les deux ci-dessus ont été retrouvées lors de cet audit.

**Pendant la préparation de ce dépôt**

4. Une affirmation selon laquelle les lignes automatisées du Journal ne portent aucun nom d'opérateur a été **rejetée après vérification** : les 127 lignes de Firecrawl et d'Apify portent un opérateur ; la distinction automatisé et manuel repose sur le champ « Connecteur ».
5. Le nombre de sources Apify en échec le 9 septembre, cité à 4 dans un document d'appui, a été **corrigé à 12** d'après le Journal (12 échecs à 15 h 48 UTC, 12 reprises à 16 h 06 UTC).
6. L'affirmation « aucune alerte Airtable n'a réussi » (constat du 18 sept.) est **périmée** : des exécutions réussies existent depuis le 19 sept.
7. Une première version de la documentation présentait Gmail et Perplexity comme non vérifiés ou non utilisés ; l'équipe a précisé que Gmail n'a pas été essayé pour l'envoi et que Perplexity est utilisé : **corrigé**.
8. Une révision de la Skill avait été substituée à la Skill d'équipe dans le dépôt ; l'équipe ayant indiqué que la Skill déposée est validée et testée, la Skill d'équipe a été **rétablie** et la révision déplacée dans `skills/propositions/`.
9. Décisions de préparation : ne pas publier les noms de membres, les adresses courriel ni les identifiants de la base ; publier le brief en version texte sans noms ni identifiants.

## 4. Trace de la validation humaine

- Validation ou rejet de chaque fiche par une personne nommée dans le champ « Validé par » (noms non publiés ici). Limite : 57 des 60 fiches « À valider » portent déjà des noms (voir [défaillances](06_defaillances_connues.md)) ; le statut fait foi.
- Aucun brief ni aucune alerte sans accord de la Direction de l'intelligence marketing (règle du mandat) ; **aucune trace d'accord ni d'envoi documentée** à ce jour (voir [registre des briefs](../outputs/archive_briefs.md)).
- Historique des commits du dépôt (dates et attribution des modifications).
- Publication du dépôt demandée par la personne titulaire du dépôt le 20 septembre 2026.
