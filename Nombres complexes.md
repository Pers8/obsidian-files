---
tags: [math] 
---
Created: 2023-04-28

# Nombres complexes
$\sqrt{-1}$=::$i$
<!--SR:!2024-02-26,141,310-->

$$\LARGE{z=a+bi}$$
- Re($z$) =:: $a$
<!--SR:!2024-01-15,99,290-->
- Im($z$) =:: $b$
<!--SR:!2024-03-10,133,290-->

--- 
$(a+bi)(c+di)$=
?
$$\Large{(ac-bd)+i(ad+bc)}$$
<!--SR:!2023-11-22,24,270-->

$(a+bi)^{2}$=
?
$$\Large{a^{2}-b^{2}+i2ab}$$
<!--SR:!2023-12-07,37,230-->

$(a-bi)^{2}$=
?
$$\Large{a^{2}-b^{2}-i2ab}$$
<!--SR:!2024-01-02,90,290-->

$(a+ib)(a-ib)$=
?
$$\Large{a^{2}+b^{2}}$$
<!--SR:!2024-01-06,93,290-->

---

$z^{*}$=
?
$$\Large{a-ib}$$
<!--SR:!2024-06-11,226,310-->

$z+z^*$=
?
$$\Large{2a}$$
<!--SR:!2023-11-03,5,210-->

$z-z^{*}$=
?
$$\Large{2bi}$$
<!--SR:!2023-11-13,15,230-->

$zz^{*}$=
?
$$\Large{a^{2}+b^{2}}$$
<!--SR:!2024-02-07,115,290-->

---
$|z|$=
?
$$\Large{\sqrt{a^{2}+b^{2}}}$$
<!--SR:!2024-02-08,116,290-->

$|z|^{2}$=
?
$$\Large{zz^{*}}$$
<!--SR:!2023-11-05,7,230-->

Propriétés des sommes, soustractions, multiplication et division de deux conjuguées:
?
![[Pasted image 20230712084000.png]]
<!--SR:!2024-03-13,136,290-->

## Forme polaire

Nombre complexe forme polaire et exponentielle::$$\large{z=r(\cos\theta+i\sin\theta)=re^{i\theta}}$$

- $\cos\theta$=::$\frac{a}{|z|}$
- $\sin\theta$=::$\frac{b}{|z|}$
- $|zw|$=::$|z||w|$
- $|\frac{z}{w}|$=::$\frac{|z|}{|w|}$
- $zw$=::$|z||w|[\cos(\theta+\alpha)+i\sin(\theta+\alpha)]$
- $\frac{z}{w}$=::$\frac{|z|}{|w|}[\cos(\theta-\alpha)+i\sin(\theta-\alpha)]$
- $z^{n}$=::$|z|^{n}(\cos n\theta+i\sin n\theta)$
- $\theta$=::$\tan^{-1}(\frac{b}{a})$
- $z_{k}$=::$\sqrt[n]{|z|}\text{cis}\left(\frac{\theta}{n}+\frac{2k\pi}{n}\right)=\sqrt[n]{|z|}\exp\left(\frac{i(\theta +2k\pi)}{n}\right),\,k=0,1,2,...,n-1$
- $(z-w)(z-w^{*})$=::$z^{2}-z\text{Re}(w)+|w|^{2}$

## Formules d'Euler (module=1)
Si $|z|=1$ alors $z^{*}$=::$z^{-1}$
$e^{i\pi}$=::$-1$

- $z^{n}+z^{-n}$=::$2\cos(n\theta)$
- $z^{n}-z^{-n}$=::$2i\sin(n\theta)$
- $e^{in\theta}+e^{-in\theta}$=::$2\cos(n\theta)$
- $e^{in\theta}-e^{-in\theta}$=::$2i\sin(n\theta)$