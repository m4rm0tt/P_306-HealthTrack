# Décisions techniques

## Décision 1

### Décision
Utiliser AppSheet comme plateforme de développement de l'application

### Pourquoi
AppSheet est une plateforme no-code qui nous permet de créer une application mobile sans écrire de code. Cela nous permet de nous concentrer sur la démarche Agile et la compréhension du besoin plutôt que sur la programmation.

### Alternatives envisagées
- Développer une application web en HTML/CSS/JS → trop complexe pour le temps disponible
- Utiliser Glide (autre outil no-code) → moins connu de l'équipe, AppSheet était recommandé dans le cours

### Conséquences
- L'application est directement utilisable sur smartphone et navigateur
- Les données sont obligatoirement stockées dans Google Sheets
- Certaines fonctionnalités avancées sont limitées par ce que AppSheet permet

---

## Décision 2

### Décision
Stocker toutes les données dans Google Sheets

### Pourquoi
C'est la solution imposée par AppSheet. Google Sheets sert de base de données, chaque feuille correspond à une table (Sport, Nutrition, Bien-être, Objectifs).

### Alternatives envisagées
- Utiliser une vraie base de données SQL → non compatible avec AppSheet sans plan payant
- Tout mettre dans une seule feuille → trop difficile à gérer et à lire

### Conséquences
- Facile à modifier et à consulter directement dans Google Sheets
- Les données sont accessibles par toute l'équipe via Google Drive
- Il faut bien nommer les colonnes car AppSheet les lit directement

---

## Décision 3

### Décision
Créer une table séparée "Objectifs" pour stocker les objectifs hebdomadaires de l'utilisateur

### Pourquoi
Les objectifs (ex : 3 séances/semaine, 6 verres/jour, 7h de sommeil) doivent être paramétrables par l'utilisateur. Les mettre dans une table séparée permet de les modifier facilement sans toucher aux données du journal.

### Alternatives envisagées
- Mettre les objectifs en dur dans les formules → pas flexible, impossible à modifier sans retoucher AppSheet
- Mettre les objectifs dans la même table que les données → mélange les types de données, complique les calculs

### Conséquences
- L'utilisateur peut changer ses objectifs quand il veut
- Les formules de calcul des indicateurs "Atteint / Non atteint" peuvent référencer dynamiquement ces objectifs
- Il faut s'assurer qu'il y a toujours une ligne d'objectifs valide pour que les formules fonctionnent

---

## Décision 4 *(Sprint 3)*

### Décision
Utiliser les Actions AppSheet pour créer des raccourcis d'entrée rapide

### Pourquoi
L'utilisateur voulait pouvoir enregistrer des données fréquentes (ex : boire un verre d'eau, démarrer une séance de course) en un seul clic, sans passer par le formulaire complet.

### Alternatives envisagées
- Créer des formulaires pré-remplis séparés → plus de pages, navigation plus complexe
- Laisser l'utilisateur saisir manuellement à chaque fois → trop lent au quotidien

### Conséquences
- Le bouton "+1 Verre" incrémente directement la colonne Hydratation sans ouvrir de formulaire
- Le bouton "Séance rapide" crée une ligne Sport pré-remplie (Course, 30 min, intensité 3)
- L'expérience utilisateur est plus fluide et rapide

---

## Décision 5 *(Sprint 3)*

### Décision
Implémenter un système de Score du jour et de badges visuels

### Pourquoi
Pour motiver l'utilisateur à atteindre ses objectifs quotidiens, on calcule un score automatique basé sur le sommeil, l'hydratation et le sport de la journée. Des badges visuels (🔥 / ⚠️) s'affichent selon ce score.

### Alternatives envisagées
- Afficher uniquement les chiffres bruts → moins engageant pour l'utilisateur
- Utiliser un système de points complexe → trop long à développer dans AppSheet

### Conséquences
- Le ScoreJour est calculé automatiquement : +30 si sommeil ≥ 7h, +30 si hydratation ≥ 8 verres, +40 si sport saisi
- Le badge 🔥 "Top journée" s'affiche si ScoreJour ≥ 80 et humeur > 2
- Le badge ⚠️ "Journée difficile" s'affiche si humeur ≤ 2
- Les Format Rules d'AppSheet permettent d'appliquer ces badges sans code

---

## Décision 6 *(Sprint 3)*

### Décision
Ajouter des règles de validation sur les données saisies

### Pourquoi
Sans validation, l'utilisateur peut saisir des valeurs impossibles (ex : 25 verres d'eau, 2 entrées bien-être le même jour) qui faussent les calculs et les indicateurs.

### Alternatives envisagées
- Valider les données côté Google Sheets → AppSheet ne lit pas toujours les règles Sheets
- Ne pas valider → risque de données corrompues

### Conséquences
- L'hydratation est bloquée entre 0 et 12 verres avec un message clair
- Il est impossible de créer 2 entrées Bien-être pour la même date
- Les messages d'erreur sont rédigés en français pour l'utilisateur


## Plan B
- Préparer des captures d'écran de l'application en cas de problème de connexion
- Avoir des données de test déjà saisies à l'avance pour ne pas perdre de temps pendant la démo
- Si AppSheet ne charge pas, montrer directement les données dans Google Sheets
