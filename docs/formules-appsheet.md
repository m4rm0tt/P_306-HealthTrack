# Formules AppSheet

## Consigne
Documentez uniquement les formules IMPORTANTES.

---

## Formule 1
- **Nom :** Total séances semaine
- **Où :** Table "Synthèse" ou colonne calculée dans la vue Sommaire
- **Formule :**
  ```
  COUNTIF(Sport[Date], AND([Date] >= WEEKSTART(TODAY()), [Date] <= TODAY()))
  ```
- **Explication avec nos mots :** On compte combien de séances de sport ont été enregistrées depuis le début de la semaine jusqu'à aujourd'hui. WEEKSTART donne le lundi de la semaine actuelle.

---

## Formule 2
- **Nom :** Moyenne hydratation semaine
- **Où :** Colonne calculée dans la vue Sommaire
- **Formule :**
  ```
  AVERAGE(SELECT(BienEtre[Hydratation], AND([Date] >= WEEKSTART(TODAY()), [Date] <= TODAY())))
  ```
- **Explication avec nos mots :** On sélectionne tous les enregistrements de la semaine dans la table Bien-être, et on calcule la moyenne des verres d'eau bus. SELECT filtre les lignes, AVERAGE fait la moyenne.

---

## Formule 3
- **Nom :** Moyenne sommeil semaine
- **Où :** Colonne calculée dans la vue Sommaire
- **Formule :**
  ```
  AVERAGE(SELECT(BienEtre[Sommeil], AND([Date] >= WEEKSTART(TODAY()), [Date] <= TODAY())))
  ```
- **Explication avec nos mots :** Même logique que l'hydratation, mais on prend la colonne Sommeil (heures dormies). Ça donne la moyenne d'heures de sommeil sur la semaine en cours.

---

## Formule 4
- **Nom :** Indicateur "Atteint / Non atteint" – Séances sport
- **Où :** Colonne calculée "Statut_Sport" dans la vue Sommaire
- **Formule :**
  ```
  IF([Total_Seances] >= [Objectif_Seances], "Atteint", "Non atteint")
  ```
- **Explication avec nos mots :** On compare le total des séances réalisées cette semaine avec l'objectif fixé par l'utilisateur. Si c'est supérieur ou égal, on affiche "Atteint", sinon "Non atteint".

---

## Formule 5
- **Nom :** Indicateur "Atteint / Non atteint" – Hydratation
- **Où :** Colonne calculée "Statut_Hydratation" dans la vue Sommaire
- **Formule :**
  ```
  IF([Moyenne_Hydratation] >= [Objectif_Hydratation], "Atteint", "Non atteint")
  ```
- **Explication avec nos mots :** On compare la moyenne d'hydratation de la semaine avec l'objectif en verres/jour que l'utilisateur a défini. Même principe que pour les séances.

---

## Règle
Vous devez comprendre chaque formule utilisée.
