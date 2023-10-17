
# Test d'informatique

## Exercice 1 :
```python
INPUT A
INPUT B

if A > B then
	OUTPUT "Le plus petit nombre est", B
end if
if A < B then
	OUTPUT "Le plus petit nombre est", A
end if

else
	OUTPUT "Ils sont égaux"
end else
```


## Exercice 3 :

| SEARCHVAL | FOUND |  MAXPOS | MINPOS | MINPOS <= MAXPOS and not FOUND? |  MIDPOS | ARR[MIDPOS] |  Output | 
| ----------- | ----------- |  ----------- | ----------- | ----------- |  ----------- | ----------- |  ----------- |  
| |  | | |  | |  | |
| |  | | |  | |  | |
| |  | | |  | |  | |

## Exercice 4 :
1. L'algorithme n'est pas correcte
2. Il faudra changer par ```FOUND = FALSE```

## Exercice 5 :
1. 
$$ 10\hspace{2mm} 1101_{(2)} = 1\times 2^0 + 0\times 2^1 + 1\times 2^2 + 1\times 2^3 + 0\times 2^4 + 1\times 2^5 =\boxed{45_{(10)}} $$
2. 
![[Pasted image 20231017110244.png]]
$$\Large \boxed{55_{(10)}=110\hspace{2mm}111_{(2)}}$$
## Exercice 6 :
1. 

$$\Large \text{ Z = A AND B OR NOT C }$$

| A | B |  C | NOT C | A AND B |  **Z** |  
| ----------- | ----------- |  ----------- | ----------- | ----------- |  ----------- |  
| 0 | 0 | 0 | 1 | 0 | **1** | 
| 0 | 0 | 1 | 0 | 0 | **0** |
| 0 | 1 | 0 | 1 | 0 | **1** |
| 0 | 1 | 1 | 0 | 0 | **0** | 
| 1 | 0 | 0 | 1 | 0 | **1** |
| 1 | 0 | 1 | 0 | 0 | **0** |
| 1 | 1 | 0 | 1 | 1 | **1** | 
| 1 | 1 | 1 | 0 | 1 | **1** |


$$\Large \text{ T = (NOT A) AND C AND (A OR B)}$$

| A | B |  C | NOT A | A OR B | (NOT A) AND C | **T** |  
| ----------- | ----------- |  ----------- | ----------- | ----------- |  ----------- |  ----------- | 
| 0 | 0 | 0 | 1 | 0 | 0 | **0** | 
| 0 | 0 | 1 | 1 | 0 | 1 | **0** |
| 0 | 1 | 0 | 1 | 1 | 0 | **0** |
| 0 | 1 | 1 | 1 | 1 | 1 | **1** | 
| 1 | 0 | 0 | 0 | 1 | 0 | **0** |
| 1 | 0 | 1 | 0 | 1 | 0 | **0** |
| 1 | 1 | 0 | 0 | 1 | 0 | **0** | 
| 1 | 1 | 1 | 0 | 1 | 0 | **0** |

















