# Sprint 3 — Bilan final

## Objectif du Sprint

Finaliser l'application avec des fonctionnalités d'accès rapide, de validation des données et d'un système de score/badges visuels pour motiver l'utilisateur au quotidien.

---

## User Stories du Sprint 3

| ID | User Story | Priorité | Statut |
|----|------------|----------|--------|
| 13 | En tant qu'utilisateur, je veux voir un tableau de bord résumant mes données de la semaine (sport, sommeil, hydratation, humeur) afin d'avoir une vue d'ensemble. | HAUTE | DONE |
| 14 | En tant qu'utilisateur, je veux appuyer sur un bouton "+1 verre" afin d'enregistrer mon hydratation rapidement sans ouvrir le formulaire complet. | HAUTE | DONE |
| 15 | En tant qu'utilisateur, je veux lancer une séance rapide pré-remplie en 1 clic afin de gagner du temps lors de la saisie de mes entraînements. | HAUTE | DONE |
| 16 | En tant qu'utilisateur, je veux être bloqué si je saisis une valeur absurde (ex : hydratation > 12) afin d'éviter des données incorrectes dans mon journal. | MOYENNE | DONE |
| 17 | En tant qu'utilisateur, je veux voir un score du jour calculé automatiquement afin d'être motivé à atteindre mes objectifs quotidiens. | MOYENNE | DONE |
| 18 | En tant qu'utilisateur, je veux voir des badges visuels (🔥 / ⚠️) selon mon score et mon humeur afin d'avoir un retour visuel immédiat sur ma journée. | BASSE | DONE |

---

## Vélocité

| Sprint | US planifiées | US livrées (Done) | Vélocité |
|--------|--------------|-------------------|----------|
| Sprint 1 | 4 | 4 | 4 |
| Sprint 2 | 8 | 8 | 8 |
| Sprint 3 | 6 | 6 | 6 |
| **Total** | **18** | **18** | **18** |

---

## Ce qui a été livré (Done)

- **Tableau de bord hebdomadaire** — vue synthèse avec sport, sommeil, hydratation, humeur et objectifs
- **Bouton "+1 Verre"** — action AppSheet qui incrémente directement l'hydratation sans formulaire
- **Séance rapide** — action qui pré-remplit une entrée Sport (Course, 30 min, intensité 3) en 1 clic
- **Validation des données** — hydratation bloquée entre 0 et 12 verres, doublon Bien-être interdit par date
- **Score du jour** — calcul automatique : +30 si sommeil ≥ 7h, +30 si hydratation ≥ 8 verres, +40 si sport saisi
- **Badges visuels** — 🔥 "Top journée" si ScoreJour ≥ 80 et humeur > 2 ; ⚠️ "Journée difficile" si humeur ≤ 2

---

## Ce qui n'a pas été livré

Aucune User Story abandonnée en Sprint 3. Toutes les US planifiées ont été livrées.

La seule US restante en BACKLOG (US-18 badges) était déjà prévue comme optionnelle — elle a finalement été intégrée.

---

## Impediments rencontrés

- La formule du Score du jour a nécessité plusieurs itérations : AppSheet ne supportait pas directement l'addition de conditions multiples, solution trouvée avec des colonnes calculées intermédiaires.
- Le bouton "+1 Verre" créait initialement une nouvelle ligne au lieu de modifier l'existante — corrigé en utilisant une action de type "Set the values of some columns in this row".

---

## Démonstration

L'app AppSheet est accessible ici : https://www.appsheet.com/start/9540f2ae-247a-4156-8bb2-624db3697229

Données de test pré-saisies pour la démo. Plan B disponible dans `docs/demo.md` si problème de connexion.
