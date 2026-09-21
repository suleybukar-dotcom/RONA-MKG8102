# Schémas du dispositif

Six schémas Mermaid, rendus directement par GitHub. Ils décrivent le dispositif **tel que documenté** dans ce dépôt ; les étapes non essayées sont signalées sous chaque schéma.

## 1. Architecture générale

```mermaid
flowchart TB
  K["KIQ et hypothèses"] --> S["Sources cotées (48)"]
  S --> C["Collecte : Firecrawl, Apify, manuelle"]
  C --> J["Journal de collecte"]
  C --> T["Traitement Claude (Skill fiche-de-veille)"]
  T --> F["Fiches de veille, statut À valider"]
  F --> V{{"Contrôle humain 1 : validation ou rejet"}}
  V --> Q["Vue Validée"]
  Q --> B["Brief BLUF et alertes"]
  B --> D{{"Contrôle humain 2 : accord avant diffusion"}}
  D --> R["Décideur"]
```

## 2. Modèle de données

Cinq tables reliées. Le détail des champs est dans [02_schema_airtable.md](02_schema_airtable.md).

```mermaid
erDiagram
  KIQ ||--o{ FICHES : "répond à"
  KIQ ||--o{ KIQ : "parente et dérivées"
  ACTEURS ||--o{ SOURCES : "possède"
  ACTEURS ||--o{ FICHES : "concerné par"
  SOURCES ||--o{ FICHES : "rapporte"
  SOURCES ||--o{ JOURNAL : "collectée par"
  KIQ {
    text Enonce
    text Decideur
    date Echeance
    text Hypotheses
  }
  ACTEURS {
    text Nom
    select Type
  }
  SOURCES {
    text Nom
    url Adresse
    select Fiabilite
    select Connecteur
    text BiaisConnu
  }
  FICHES {
    text Titre
    text ExtraitCite
    select Nature
    select Statut
    collaborator ValidePar
    select MotifRejet
  }
  JOURNAL {
    datetime DateHeure
    select Connecteur
    number ElementsRetenus
    text Erreurs
  }
```

## 3. Cycle de vie d'une fiche

La machine s'arrête à « À valider » : la bascule est un acte humain.

```mermaid
stateDiagram-v2
  state "À valider" as AValider
  state "Validée" as Validee
  state "Rejetée" as Rejetee
  [*] --> AValider : la machine crée la fiche
  AValider --> Validee : contrôle humain 1, nom dans Validé par
  AValider --> Rejetee : contrôle humain 1, motif de rejet
  Validee --> Cite : citée par identifiant dans un brief
  state "Citée dans un brief" as Cite
  Cite --> [*]
  Rejetee --> [*]
```

Constat au 20 sept. 2026 : 120 fiches, dont 60 à valider, 53 validées et 7 rejetées.

## 4. Calendrier hebdomadaire de collecte

Rythme déclaré par le mandat ; trois tâches planifiées actives d'après la capture fournie par l'équipe.

```mermaid
flowchart TB
  subgraph LUN["Lundi 8 h"]
    L1["Prix du panier fixe et promotions (Firecrawl)"]
    L2["Six collectes manuelles : circulaires et pages Home Depot"]
  end
  subgraph MAR["Mardi 9 h"]
    M1["Sources institutionnelles, emploi et presse (Firecrawl)"]
  end
  subgraph MER["Mercredi 9 h"]
    W1["Avis publics de 12 succursales (Apify)"]
    W2["Localisateurs de succursales (Firecrawl)"]
  end
  L1 --> J["Ligne de Journal par source"]
  L2 --> J
  M1 --> J
  W1 --> J
  W2 --> J
  J --> F["Fiches au statut À valider"]
```

Une septième collecte manuelle, le localisateur BMR, est prévue chaque mois par le mandat.

## 5. Diffusion et contrôles humains

```mermaid
sequenceDiagram
  participant C as Collecte
  participant K as Claude et Skill
  participant A as Airtable
  participant I as Responsable des insights
  participant D as Direction de l'intelligence marketing
  participant R as Décideur
  C->>K: page en texte
  K->>A: fiche À valider et ligne de Journal
  I->>A: valide ou rejette la fiche (contrôle 1)
  A-->>K: vue Validée
  K->>D: projet de brief ou d'alerte
  D->>D: accord explicite (contrôle 2)
  D->>R: brief BLUF ou alerte
```

**Non essayé à ce jour** : l'envoi du brief et des alertes par Gmail (dernière étape). Les trois automatisations Airtable d'alerte interne sont un mécanisme distinct, décrit dans [04_alertes_et_seuils.md](04_alertes_et_seuils.md).

## 6. Gestion des échecs de collecte

```mermaid
flowchart TD
  A["Collecte automatique"] --> B{"Page lue ?"}
  B -->|oui| C["Fiche selon la Skill"]
  B -->|non| D["Ligne de Journal avec l'erreur"]
  D --> E{"Repli manuel prévu ?"}
  E -->|oui| F["Collecte manuelle, raison consignée dans Erreurs"]
  E -->|non| G["Source remontée à l'équipe après deux cycles en échec"]
  F --> C
```

Exemples réels : panne d'authentification d'Apify le 9 sept. (12 échecs puis 12 reprises), circulaires inaccessibles aux robots, pages Home Depot dépendantes de la succursale. Voir [06_defaillances_connues.md](06_defaillances_connues.md).
