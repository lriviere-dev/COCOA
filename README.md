# COCOA
Repo de thèse pour le sujet "Compilation de connaissances pour l'ordonnancement dynamique d'atelier d'assemblage"

# External content:
- Overleaf For WIP : https://www.overleaf.com/read/mbjfqsqhkfyq

## TODOs & Perspectives:
### Etat de l'art RCPSP: 
- Solver OR-TOols
- Edge-finding
- Time-tabling
- Branch and cut and price
- Column generation

### Experimentations GOP CP:
Le modèle actuel performe bizarrement mal sur certaines instances. Au point que ce pourrait être un bug.

Pistes pour amélioration modèle CP (de plus à moins concrète)
1. Facile à implémenter
- Symétries : forcer les groupes vides à être à la fin.
- Contraposée de l'implication: si une tâche est avant une autre, son groupe est le même ou avant.
- Fusion des variables égales.
2. Nécessite un peu de formation
- Utilisation des Search phases pour brancher d'abord sur le choix des groupes.
- Feed une solution au solveur.
3. Necesiite formation + imagination
- Etudier la contrainte IloCP "Distribute"
- Etudier la contrainte IloCP "Span"
- Etudier la possibilté d'un modèle utilisant les séquences : Une séquence par groupe ?
- Etudier liens avec balancement de tâches.
- Implementation d'un propagateur dédié
4. If all else fails:
- Fixer le nombre de groupe ou la taille max des groupes -> perte d'exactitude ou itérations.
- Etudier la trace du solveur

Autres pistes
- Utilisation de données réelles ( Dassault?)

### Carte de compilation:
- Reprendre et clarifier l'avancement actuel.
- Pour toutes les requêtes que l'on peut imaginer, pour chaque langage, comparer la complexité.

### Expérimentations Compilation:
- Modifier le compilateur **cn2mddg** pour l'adapter aux problèmes d'ordo : Regarder le code, si solveur en blackbox, changer le solveur, sinon, optimiser l'algo (utiliser Lazy clause generation?)
-Tenter la compilation d'encodage de différent modèles de problèmes d'ordo par différent compilateurs (cn2mddg, choco, saladd..)

 
