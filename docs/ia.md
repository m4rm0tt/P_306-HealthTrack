# Utilisation de l'IA — SEQ-16 (finale)

## Outils utilisés

- Claude (claude.ai) — Anthropic

---

## Atelier IA 1 — Rétro augmentée Belbin (IMI-3)

### Prompt soumis

```
Notre équipe Scrum a identifié ces axes d'amélioration en rétrospective :
1. Mieux estimer le temps nécessaire pour chaque tâche dès le Sprint Planning
2. Tester les fonctionnalités plus tôt pour éviter les mauvaises surprises en fin de sprint
3. Documenter les formules AppSheet au fur et à mesure plutôt qu'à la fin

Nous avons ces rôles Belbin dans notre équipe :
- Hugo : Coordinateur (Product Owner)
- Minh : Coordinateur d'équipe (Scrum Master)
- Esteban : Propulseur / Réalisateur (Developer)

Suggère 1 action concrète par axe, adaptée à notre composition d'équipe.
```

### Ce que l'IA a répondu (résumé)

1. **Estimation** — Utiliser le Planning Poker à chaque Sprint Planning : le PO présente la US, chaque membre donne une estimation en points (1/2/3/5), on discute les écarts. Le Coordinateur (Hugo) tranche en cas de désaccord.

2. **Tests plus tôt** — Le Developer (Esteban) fait une demo partielle au milieu du sprint devant le PO. Si une fonctionnalité ne passe pas, il reste du temps pour corriger.

3. **Documentation formules** — Documenter chaque formule dans formules-appsheet.md juste après l'avoir fait fonctionner. Le Scrum Master (Minh) vérifie que c'est fait lors du Daily.

### Ce que l'on a retenu

- La demo partielle à mi-sprint : réaliste, on peut l'appliquer dès le prochain projet.
- Documenter les formules au fur et à mesure : on a testé en Sprint 3, ça fonctionne.
- Planning Poker adapté : estimation rapide à main levée pour notre groupe de 3.

### Ce que l'on a écarté et pourquoi

L'IA suggérait d'utiliser un outil externe de suivi du temps (Toggl) — trop lourd pour la durée du projet, on n'a pas retenu cette suggestion.

---

## Atelier IA 2 — Coach de présentation (IMI-2)

### Prompt soumis

```
Nous devons présenter notre projet Scrum en 18 minutes demain.
Voici notre plan de présentation :
1. Introduction — contexte et objectif de l'app (2 min)
2. Démo AppSheet — les 3 modules + tableau de bord (6 min)
3. Bilan Scrum — vélocité, sprints, backlog (4 min)
4. Décisions techniques — pourquoi AppSheet, pourquoi Google Sheets (3 min)
5. Rétrospective et ce qu'on ferait différemment (2 min)
6. Questions (1 min tampon)

Nos forces selon notre rétrospective :
- 100% du backlog livré (18/18 US)
- Rôles clairs et communication efficace
- Maîtrise progressive d'AppSheet (formules, actions, badges)

Quelles sont les 2 questions difficiles qu'un jury Scrum nous poserait probablement ?
Comment nous conseilles-tu de nous y préparer ?
```

### Ce que l'IA a répondu

**Question 1** : "Votre vélocité a augmenté de Sprint 1 à Sprint 2 puis baissé à Sprint 3. Pourquoi ?"

Préparation : la vélocité dépend de la complexité des US, pas seulement de leur nombre. Les US du Sprint 3 étaient techniquement plus complexes (actions AppSheet, formules de score, badges). Ce n'est pas un recul, c'est une montée en complexité.

**Question 2** : "Comment avez-vous validé que les besoins utilisateurs étaient couverts ?"

Préparation : mentionner la Definition of Done (critères d'acceptation vérifiés par le PO), les tests avec données réelles, et le test depuis un compte externe pour valider l'accessibilité.

### Ce qu'on a retenu

- Réponse préparée sur la vélocité Sprint 3 : complexité technique, pas régression.
- On s'est entraîné à répondre aux 2 questions sans l'IA — chacun a préparé 2-3 phrases, chronométrées.

### Comment on a vérifié que la réponse est correcte

On a rejoué les 2 questions en interne (sans l'IA) et chronométré les réponses. Si on dépasse 90 secondes, on reformule pour être plus direct.

---

## Règle

Nous restons responsables de notre travail. L'IA a proposé, l'équipe a décidé.
