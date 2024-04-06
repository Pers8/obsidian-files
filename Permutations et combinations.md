---
tags:
  - math
---
# Permutations et combinations
## Principes de comptage
- Le principe fondamental de comptage stipule que s'il y a $m$ façons de faire une chose et $n$ façons d'en faire une autre, alors pour faire les deux choses il y a:: $m\times n$ façons.
- Si une question demande de choisir un élément d'une liste ET un élément d'une autre liste, on doit:: multiplier le nombre d'options dans chaque liste.
- Si une question demande de choisir un élément d'une liste OU un élément d'une autre liste, on doit:: additionner le nombre d'options dans chaque liste.

## Permutation et combinations
- Dans une permutation, l'ordre des arrangements est important ou non?:: il est important.
- Dans une combination, l'ordre des arrangements est important ou non?:: il n'est pas important.
- Permutation formules (2)::$$P(n,r)=\frac{n!}{(n-r)!}=r!\times C(n,r)=r!\times{n\choose r}$$
- Combination formule::$$C(n,r)=\frac{n!}{r!(n-r!)}={n\choose r}$$
- Permutation avec répétition autorisé::$$n^r$$
- Le nombre de permutations de $n$ objets pris tous à la fois, où il y a $p_1$ objets à $p_k$ est::$$\frac{n!}{p_{1}!p_{2}!\dots p_{k}!}$$