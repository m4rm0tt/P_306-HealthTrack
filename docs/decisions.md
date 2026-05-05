# Décisions techniques

## Format

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

- ## Décision 2

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
