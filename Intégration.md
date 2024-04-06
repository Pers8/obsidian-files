---
tags:
  - math
---

# Intégration
Autre notation de $\int f(x)\,dx$=::$F(x)$
Si $g(x)$ = $u$ alors $g'(x)\,dx$=::$u'dx=du$
## Identités
### Fondamentales
- $\int a\,dx=$::$ax+C$
- $\int x^{n}\,dx=$::$\frac{x^{n+1}}{n+1}+C;\;n\neq-1$
- $\int x^{-n}\,dx=\int \frac{1}{x^{n}}\,dx=$::$\frac{x^{1-n}}{1-n}+C;\;n\neq1$
- $\int x^{1/n}\,dx=\int \sqrt{x^{n}}\,dx=$::$\frac{nx^{\frac{n+1}{n}}}{n+1}+C;\;n\neq-1$
- $\int x^{-1}\,dx=\int \frac{1}{x}\,dx=$::$\ln|x|+C$
- $\int a^{x}\,dx=$::$\frac{a^{x}}{\ln(a)}+C$
- $\int e^{x}\,dx=$::$e^{x}+C$
- $\int \log_{a}(x)\,dx=$::$\frac{x}{\ln a}(\ln x-1)+C$
- $\int \ln x\,dx=$::$x(\ln x -1)+C$
- $\int \sin x\,dx=$::$-\cos x +C$
- $\int \cos x\,dx=$::$\sin x +C$
- $\int \sec^{2} x\,dx=$::$\tan x +C$

### Opérations
- $\int af(x)\,dx=$::$a\int f(x)\,dx=aF(x)$
- $\int f(x)\pm g(x)\,=$::$F(x)\pm G(x)$
- $\int f(x)g(x)\,dx=$::$F(x)g(x)-\int F(x)g'(x)\,dx$
- $\int f'(x)g(x)\,dx=$::$f(x)g(x)-\int f(x)g'(x)\,dx$
- $\int f'(g(x))g'(x)\,dx=$::$\int f'(u)\,du$ avec $u=g(x)$
- $\int f(ax+b)\,dx=$::$\frac{1}{a}F(ax+b)$

### Intégration définies
- $\int_{a}^{b}f(x)\,dx=$::$[F(x)]_{a}^{b}=F(b)-F(a)$
- $[-F(x)]_{a}^{b}$=::$[F(x)]_{b}^{a}$
- $\int_{a}^{b}f'(g(x))g'(x)\,dx=$::$\int_{g(a)}^{g(b)}f'(u)\,du$ avec $u=g(x)$
- $\int_{a}^{c}f(x)\,dx+\int_{c}^{b}f(x)\,dx=$::$\int_{a}^{b}f(x)\,dx$



