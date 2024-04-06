---
tags:
  - math
---

# Nombre dérivée
- $f'(a)$=::$$\lim_{h\rightarrow 0}\frac{f(a+h)-f(a)}{h}$$
- Autre notation de $f'(x)$::$\frac{dy}{dx}$
- Autre notation de $f''(x)$::$\frac{d^{2}y}{dx^{2}}$
- $\frac{d^{2}y}{dx^{2}}$ équivaut à:: $\frac{d\left(\frac{dy}{dx}\right)}{dx}$


Tangente et normale pour une fonction représente:
?
![[Pasted image 20240406090258.png]]

- Formule de la tangente $T:y$=:: $f'(a)(x-a)+f(a)$
- Formule de la normale $N:y$=:: $\frac{-1}{f'(a)}(x-a)+f(a)$


## Identités
### Fondamentales
- $f(x)=c\rightarrow f'(x)=$::$0$
- $f(x)=x^{n}\rightarrow f'(x)=$::$nx^{n-1}$
- $f(x)=x^{-n}=\frac{1}{x^{n}}\rightarrow f'(x)=$::$\frac{-n}{x^{n+1}}$
- $f(x)=x^{1/n}=\sqrt[n]{x}\rightarrow f'(x)=$::$\frac{\sqrt[n]{x^{1-n}}}{n}$
- $f(x)=a^{x}\rightarrow f'(x)=$::$\ln(a)a^{x}$
- $f(x)=e^{x}\rightarrow f'(x)=$::$e^{x}$
- $f(x)=\log_{a}(x)\rightarrow f'(x)=$::$\frac{1}{\ln(a)x}$
- $f(x)=\ln(x)\rightarrow f'(x)=$::$\frac{1}{x}$
- $f(x)=\sin(x)\rightarrow f'(x)=$::$\cos(x)$
- $f(x)=\cos(x)\rightarrow f'(x)=$::$-\sin(x)$
- $f(x)=\tan(x)\rightarrow f'(x)=$::$\sec^{2}(x)$
- $f(x)=\sec(x)\rightarrow f'(x)=$::$\sec(x)\tan(x)$
- $f(x)=\csc(x)\rightarrow f'(x)=$::$-\csc(x)\cot(x)$
- $f(x)=\cot(x)\rightarrow f'(x)=$::$-\csc^{2}(x)$
- $f(x)=\sin^{-1}(\frac{x}{a})\rightarrow f'(x)=$::$\frac{1}{\sqrt{a-x^{2}}}$
- $f(x)=\cos^{-1}(\frac{x}{a})\rightarrow f'(x)=$::$\frac{-1}{\sqrt{a-x^{2}}}$
- $f(x)=\tan^{-1}(\frac{x}{a})\rightarrow f'(x)=$::$\frac{1}{a^{2}+x^{2}}$
### Opérations
- $g(x)=c\cdot f(x)\rightarrow g'(x)=$::$c\cdot f'(x)$
- $h(x)=f(x)\pm g(x)\rightarrow h'(x)=$::$f'(x)\pm g'(x)$
- $h(x)=f(x)g(x)\rightarrow h'(x)=$::$f'(x)g(x)+f(x)g'(x)$
- $h(x)=\frac{f(x)}{g(x)}\rightarrow h'(x)=$::$\frac{f'(x)g(x)-f(x)g'(x)}{g(x)^{2}}$
- $h(x)=f(g(x))\rightarrow h'(x)=$::$f'(g(x))g'(x)$

### Première et seconde dérivée
- Si $f'(x)=0$ alors ce point est:: un extremum local
- Si $f''(x)=0$ alors ce point est:: un point d'inflexion
- Si $f'(x)=0$ et $f''(x)<0$ alors ce point est:: un maximum local
- Si $f'(x)=0$ et $f''(x)>0$ alors ce point est:: un minimum local
- $f$ est concave haut si $f''(x)$::$>0$
- $f$ est concave bas si $f''(x)$::$<0$

## Dérivation implicite
$\frac{df(y)}{dx}=$::$\frac{df(y)}{dy}\cdot \frac{dy}{dx}=f'(y)\frac{dy}{dx}$
$\frac{d}{dx}(f(x)g(y))=$::$g(y)\frac{df(x)}{dx}+f(x)\frac{dg(y)}{dx}=g(y)f'(x)+f(x)g'(y)\frac{dy}{dx}$

Si on a $f(x,\,y)$ et on veut $\frac{dy}{dx}$ alors les étapes sont :
?
- Appliquer $\frac{d}{dx}$ pour chaque terme
- Appliquer la règle en chaîne pour les termes avec une variable $y$ pour obtenir $\frac{dy}{dx}$ en facteur
- Factoriser par $\frac{dy}{dx}$ et l'isoler
ou
- Appliquer la dérivée pour chaque terme
- Factoriser par $dy$ et $dx$
- Diviser $dy$ par $dx$

$df(x)=$::$f'(x)dx$

$\frac{d(xy)}{dx}=$::$y+x\frac{dy}{dx}$


