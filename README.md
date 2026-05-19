# HealthTrack - Groupe X

## Informations
- Classe : CIN1B
- Groupe : Hugo Minh et Esteban
- Sprint : 3

## Membres
- Product Owner : Hugo
- Scrum Master : Minh
- Developers : Esteban

## Liens
- App AppSheet : https://www.appsheet.com/start/9540f2ae-247a-4156-8bb2-624db3697229
- Google Sheet : https://docs.google.com/spreadsheets/d/1Gmtmf7e45rIbZ3PS6ZjAUWQbbRALFRWmtgar2p-VHaM/edit?usp=sharing

## Description du projet

HealthTrack est une application mobile no-code (AppSheet) qui permet à un utilisateur de suivre ses habitudes de santé au quotidien : activité sportive, nutrition, sommeil, hydratation et humeur.

L'application affiche un tableau de bord hebdomadaire avec les objectifs fixés par l'utilisateur et indique automatiquement si ces objectifs sont atteints.

---

## Fonctionnalités livrées

### Sprint 1

- Suivi des séances de sport (type, durée, intensité)
- Suivi de la nutrition (moment, catégorie, commentaire)
- Suivi du bien-être (sommeil, hydratation, humeur)
- Filtrage des données par date

### Sprint 2

- Page Sommaire centralisée
- Objectifs hebdomadaires paramétrables (sport, hydratation, sommeil)
- Calculs automatiques (total séances, moyenne sommeil, moyenne hydratation)
- Indicateurs "Atteint / Non atteint" pour chaque objectif

### Sprint 3

- Tableau de bord résumé de la semaine
- Bouton "+1 Verre" — incrémente l'hydratation sans ouvrir le formulaire
- Séance rapide — crée une entrée sport pré-remplie en 1 clic
- Validation des données (hydratation bloquée entre 0 et 12, doublon Bien-être interdit)
- Score du jour calculé automatiquement (+30 sommeil, +30 hydratation, +40 sport)
- Badges visuels : 🔥 "Top journée" (score ≥ 80 et humeur > 2) / ⚠️ "Journée difficile" (humeur ≤ 2)

---

## Comment utiliser l'application

1. **Ouvrir le lien AppSheet** sur smartphone ou navigateur
2. **Se connecter** avec un compte Google (ou utiliser le lien partagé en mode lecture)
3. **Naviguer** via le menu bas : Sport | Nutrition | Bien-être | Sommaire
4. **Ajouter une entrée** via le bouton "+" de chaque section
5. **Accès rapide** : utiliser le bouton "+1 Verre" ou "Séance rapide" depuis la vue Sommaire
6. **Consulter le tableau de bord** dans l'onglet Sommaire pour voir les objectifs de la semaine

### Plan B (si l'app ne charge pas)

- Des captures d'écran sont disponibles dans le dossier `/captures`
- Les données sont consultables directement dans le Google Sheet lié

---

## Structure du repo

```
P_306-HealthTrack/
├── README.md
├── captures/           # Screenshots de l'application
├── data/               # README données
├── docs/
│   ├── contexte.md
│   ├── decisions.md
│   ├── demo.md
│   ├── equipe.md
│   ├── formules-appsheet.md
│   ├── ia.md
│   ├── journal-de-bord.md
│   ├── modele-donnees.md
│   ├── product-backlog.md
│   ├── retrospective.md
│   ├── retrospective-finale.md
│   └── sprint-backlog.md
└── sprints/
    └── sprint-03.md
```

---

## Vélocité finale

| Sprint | US livrées |
|--------|-----------|
| Sprint 1 | 4/4 |
| Sprint 2 | 8/8 |
| Sprint 3 | 6/6 |
| **Total** | **18/18** |


