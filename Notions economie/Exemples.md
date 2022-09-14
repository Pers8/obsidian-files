---
tags: [economy]
---

 [[Economy]] > [[Exemples]]
$$\huge{Exemples}$$

<br/>
## [[Economy#Chapitre 1]]
<br>
| Prix (FCFA) | Qté Samba | Qté Moussa | Qté Marché |
| ----------- | ----------- |  ----------- | -----------|
| 1000 | 1 |  2 | 3 |
| 900 | 2 | 4 | 6 |
| 800 | 3 | 6 | 9 |
| 700 | 4 | 8 | 12 |
| 600 | 5 | 10 |15 |
```chart
type: line
labels: [1,2,3,4,5]
series:
  - title: Moussa
    data: [1000,900,800,700,600]
tension: 0.2
width: 80%
labelColors: false
fill: false
beginAtZero: false
```
<br>

```chart
type: line
labels: [3,6,9,12,15]
series:

  - title: Qté du marché
    data: [1000,900,800,700,600]
tension: 0.2
width: 80%
labelColors: false
fill: false
beginAtZero: false
```
