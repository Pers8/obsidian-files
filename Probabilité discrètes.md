---
tags:
  - math
---
# Probabilité discrètes
## Experience aléatoire-événements
Une expérience aléatoire est une expérience dont l'issue dépend du:: hasard.
<!--SR:!2023-09-26,3,250-->
L'ensemble des résultats possibles d'une expérience aléatoire est appelé:: univers.
<!--SR:!2023-09-26,3,250-->
On appelle événement:: toute partie de l'univers (sous-ensemble)
<!--SR:!2023-09-24,1,230-->

### Définitions
- Evénement élémentaire:: a une seule issue
<!--SR:!2023-09-26,3,250-->
- Evénement composé:: a plusieurs issues
<!--SR:!2023-09-27,4,270-->
- Evénement A et B (conjonction d'événement):: événement constitué des issues communes aux deux événements
<!--SR:!2023-09-26,3,250-->
- Evénement contraire a A noté A':: événement dont les issues n'appartiennent pas a A
<!--SR:!2023-09-26,3,250-->
- Evénement A ou B (disjonction d'événement):: événement constitué de toutes les issues des deux événements
- Evénement incompatible (mutuellement exclusif):: conjonction des deux événements avec aucune issue
- Evénement certain:: toutes les issues
- Evénement impossible:: aucune issue

## Calcul de probabilité
- La probabilité d'un événement est la somme:: des éléments élémentaires qui le compose.
- Lorsque les événements élémentaires ont meme probabilité, on dit qu'il y a:: équiprobabilité ou équi-répartition.

### Propriété
- $P(U)$=::1 
- $P(0)$=::0
- $P(A)+P(A')$=::1 
- $P(A\cup B)$=::$P(A)+P(B)-P(A\cap B)$
- $P(A/B)$=::$\frac{P(A\cap B)}{P(B)}=\frac{n(A\cap B)}{n(B)}
- $P(A\cap B)$=::$P(A)\times P(B/A)$ ou $P(B)\times P(A/B)$
- Si deux événements sont indépendants alors $P(A/B)$=::$P(A)$