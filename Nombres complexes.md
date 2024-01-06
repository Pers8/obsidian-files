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






**Problem**: Given that ( $w = 8e^{i\frac{7\pi}{6}}$ ), find the smallest positive integer ( N ) such that ( $(w)^N$ ) is a real number.

**Step 1**: Write ( w ) in Euler’s form. Euler’s formula states that for any real number ( x ), ( $e^{ix} = \cos(x) + i\sin(x)$ ). So, we can write ( w ) as ( $w = 8[\cos(\frac{7\pi}{6}) + i\sin(\frac{7\pi}{6})]$ ).

**Step 2**: We need to find an ( N ) such that ( $(w)^N$) is a real number. This means the imaginary part of ( $(w)^N$ ) should be zero.

**Step 3**: When we raise ( w ) to the power of ( N ), the angle of ( w ) gets multiplied by ( N ). So, ( $(w)^N = 8^N[\cos(N\frac{7\pi}{6}) + i\sin(N\frac{7\pi}{6})]$ ).

**Step 4**: For ( (w)^N ) to be a real number, ( $\sin(N\frac{7\pi}{6})$ ) must be zero because this term is the coefficient of ( i ) (the imaginary part). We know that sin function gives zero at all integral multiples of ( $\pi$ ). So, ( $N\frac{7\pi}{6}$ ) should be an integral multiple of ( $\pi$ ).

**Step 5**: The smallest positive ( N ) that satisfies this condition is ( N = 6 ) because ( $6\frac{7\pi}{6} = 7\pi$ ), which is an integral multiple of ( $\pi$ ).

So, the smallest positive integer ( N ) such that ( ($w)^N$ ) is a real number is ( N = 6 ).

Please note that this is a specific example and the solution may vary depending on the value of ( w ). For a different value of ( w ), you would need to adjust the calculation accordingly. If you have a different value of ( w ) and need help solving it, feel free to ask! I hope this helps! Let me know if you have any other questions.