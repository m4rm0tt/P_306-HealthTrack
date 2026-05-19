# Sprint 2 — Bilan

## Objectif du Sprint

Suite au feedback de la Sprint Review 1 — "C'est bien d'enregistrer, mais je veux me fixer des objectifs et savoir si je progresse." — ce sprint ajoute un système d'objectifs hebdomadaires paramétrables et des indicateurs de progression calculés automatiquement.

---

## User Stories du Sprint 2

| ID | User Story | Priorité | Statut |
|----|------------|----------|--------|
| 5 | En tant qu'utilisateur, je veux accéder à une page Sommaire centralisée, afin de visualiser en un coup d'œil l'ensemble de mes données et objectifs de la semaine. | HAUTE | DONE |
| 6 | En tant qu'utilisateur, je veux pouvoir paramétrer un objectif de séances de sport par semaine (ex : 3), afin que l'application génère une synthèse indiquant si cet objectif est atteint. | MOYENNE | DONE |
| 7 | En tant qu'utilisateur, je veux pouvoir définir un objectif d'hydratation journalière (ex : 6 verres/jour), afin que l'application génère une synthèse comparant ma moyenne réelle à cet objectif. | MOYENNE | DONE |
| 8 | En tant qu'utilisateur, je veux pouvoir définir un objectif de durée de sommeil moyen (ex : 7h), afin que l'application génère une synthèse me montrant si mon sommeil est suffisant par rapport à mon objectif. | MOYENNE | DONE |
| 9 | En tant qu'utilisateur, je veux que l'application calcule automatiquement le total de mes séances de sport sur la semaine, afin de suivre mon activité physique globale. | MOYENNE | DONE |
| 10 | En tant qu'utilisateur, je veux que l'application calcule automatiquement ma moyenne de sommeil sur la semaine, afin de mieux comprendre mes habitudes de récupération. | MOYENNE | DONE |
| 11 | En tant qu'utilisateur, je veux que l'application calcule automatiquement ma moyenne d'hydratation sur la semaine, afin de savoir si je bois suffisamment au quotidien. | MOYENNE | DONE |
| 12 | En tant qu'utilisateur, je veux voir pour chaque objectif un indicateur "Atteint / Non atteint" sur la semaine en cours, afin de savoir immédiatement si je respecte mes engagements. | MOYENNE | DONE |

---

## Fonctionnalités livrées

### Objectifs hebdomadaires
L'utilisateur peut définir ses objectifs personnels dans une table dédiée :
- Objectif séances sport / semaine (ex : 3)
- Objectif hydratation moyenne journalière (ex : 6 verres/jour)
- Objectif sommeil moyen (ex : 7h)

### Calculs automatiques (AppSheet)
- **Total séances semaine** — via `COUNTIF` sur la table Sport filtrée par `WEEKSTART(TODAY())`
- **Moyenne sommeil semaine** — via `AVERAGE(SELECT(BienEtre[Sommeil], ...))` sur la semaine en cours
- **Moyenne hydratation semaine** — via `AVERAGE(SELECT(BienEtre[Hydratation], ...))` sur la semaine en cours

### Indicateurs "Atteint / Non atteint"
- Comparaison automatique entre les valeurs calculées et les objectifs définis par l'utilisateur
- Affichage clair par indicateur : `IF([Total_Seances] >= [Objectif_Seances], "Atteint", "Non atteint")`

### Page Sommaire
- Vue centralisée regroupant les 3 indicateurs et les objectifs de la semaine en cours
- Se met à jour automatiquement à chaque nouvelle saisie

---

## Vélocité Sprint 2

| US planifiées | US livrées (Done) | Vélocité |
|--------------|-------------------|----------|
| 8 | 8 | 8 |

---

## Comparaison avec Sprint 1

| Sprint | Vélocité | Complexité |
|--------|----------|------------|
| Sprint 1 | 4 | Saisie et consultation simples |
| Sprint 2 | 8 | Calculs automatiques + table Objectifs + page Sommaire |

La hausse de vélocité reflète une meilleure maîtrise d'AppSheet et des User Stories mieux estimées dès le Sprint Planning.

---

## Ce qui n'a pas été livré

Aucune US abandonnée. Les 8 US planifiées ont été livrées.

---

## Impediments rencontrés

- La table "Objectifs" a nécessité une réflexion sur la structure : mettre les objectifs dans une table séparée plutôt que dans les formules en dur — décision prise après discussion en équipe (voir `docs/decisions.md` — Décision 3).
- Les formules `SELECT()` combinées avec `WEEKSTART()` ont demandé plusieurs essais avant de fonctionner correctement sur la semaine en cours.
- Les critères d'acceptation pour les indicateurs "Atteint / Non atteint" n'avaient pas été écrits avant de commencer — le PO a dû valider oralement en cours de sprint. À améliorer au Sprint 3.

---

## Critères de réussite vérifiés (selon CDC)

- Les objectifs sont paramétrables par l'utilisateur : **OUI**
- Les indicateurs se mettent à jour automatiquement : **OUI**
