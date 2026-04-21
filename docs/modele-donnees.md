# Modèle de données

## Consigne
Vous devez définir VOUS-MEMES la structure des données.

## Tables

### BienEtre
| Colonne     | Type       | Description |
|-------------|------------|-------------|
|_RowNumber   | Number     |             |
|ID           | Text       |             |
|Date         | Date       |             |
|Sommeil      | Decimal    |             |
|Hydratation  | Number     |             |
|Humeur       | Number     |             |

### Nutrition
| Colonne     | Type       | Description |
|-------------|------------|-------------|
|_RowNumber   | Number     |             |
|ID           | Text       |             |
|Date         | Date       |             |
|Moment       | Text       |             |
|Categorie    | Enum       |             |
|Commentaire  | Text       |             |

### Sport
| Colonne     | Type       | Description |
|-------------|------------|-------------|
|_RowNumber   | Number     |             |
|ID           | Text       |             |
|Date         | Date       |             |
|TypeSport    | Text       |             |
|Duree        | Number     |             |
|Intensite    | Number     |             |
|Commentaire  | Text       |             |

## Questions à vous poser
- Quelles données sont nécessaires ? aucune
- Quelles contraintes doivent être respectées ? toutes
- Comment éviter les erreurs de saisie ? en metent des type specifique pour les differente colonne 
ainsi que mettre des unique pour eviter des doublons dans des colonne specifique
