# Sprint 1 — Bilan

## Objectif du Sprint

Livrer une application fonctionnelle (MVP) permettant à un étudiant de saisir et consulter ses habitudes quotidiennes liées au sport, à l'alimentation et au bien-être.

---

## User Stories du Sprint 1

| ID | User Story | Priorité | Statut |
|----|------------|----------|--------|
| 1 | En tant qu'étudiant, je veux pouvoir faire un suivi de mes séances de sport afin de faire des comparaisons entre mes dites séances. | HAUTE | DONE |
| 2 | En tant qu'étudiant, je veux pouvoir faire un suivi de mes repas afin de mieux me nourrir. | HAUTE | DONE |
| 3 | En tant qu'étudiant, je veux pouvoir faire un suivi de mon sommeil, hydratation et de mon humeur afin de voir s'il y a une corrélation entre ces différents points. | HAUTE | DONE |
| 4 | En tant qu'étudiant, je veux filtrer la liste de mes données par jour afin de consulter uniquement les informations qui me sont utiles à un moment donné. | HAUTE | DONE |

---

## Fonctionnalités livrées

### Journal Sport
L'utilisateur peut ajouter une séance de sport avec :
- Date
- Type de sport
- Durée (en minutes)
- Intensité (1 à 5)
- Commentaire (facultatif)

### Journal Nutrition
L'utilisateur peut ajouter un repas avec :
- Date
- Moment du repas (petit-déjeuner / midi / soir / snack)
- Catégorie (équilibré / correct / junk)
- Commentaire (facultatif)

### Journal Bien-être
L'utilisateur peut enregistrer :
- Sommeil : nombre d'heures
- Hydratation : nombre de verres d'eau (0 à 12)
- Humeur : échelle de 1 à 5

### Consultation
- Consultation de la liste des entrées par module
- Accès au détail d'une entrée
- Filtrage par date

---

## Vélocité Sprint 1

| US planifiées | US livrées (Done) | Vélocité |
|--------------|-------------------|----------|
| 4 | 4 | 4 |

---

## Ce qui n'a pas été livré

Aucune US abandonnée. Les 4 US planifiées ont été livrées.

---

## Impediments rencontrés

- La mise en place initiale de Google Sheets (nommage des colonnes, types) a pris plus de temps que prévu — AppSheet lit directement les noms de colonnes, une erreur de nommage cassait la synchronisation.
- Comprendre la logique de génération automatique des vues AppSheet (liste, détail, formulaire) a nécessité quelques essais-erreurs.

---

## Décisions techniques prises pendant ce sprint

- Utilisation d'AppSheet comme plateforme no-code (recommandée dans le cours, permet de se concentrer sur la démarche Agile).
- Données stockées dans Google Sheets — une feuille par table (Sport, Nutrition, BienEtre).
- Application créée entièrement depuis zéro, sans template existant.
