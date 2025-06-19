## Complex algebra

#### Complex multiplication
Compute the products: 

(a) $(1-i)(4-7i)$ $\quad$ (b) $(2+5i)(2-5i)$

**Solution**

(a) $(1-i)(4-7i)$

Expand: 

$$(1-i)(4-7i)\quad ⨠⨠ \quad 4-7i-4i+7i^2$$

Simplify $i^2$: 

$$\begin{gather*}⨠⨠ \quad 4-7i-4i+7(-1)\\\\ ⨠⨠ \quad -3-11i\end{gather*}$$

---

(b) $(2+5i)(2-5i)$

Expand: 

$$(2+5i)(2-5i)\quad ⨠⨠ \quad 4-10i+10i-25i^2$$

Simplify $i^2$: 

$$⨠⨠ \quad 4-10i+10i-25(-1)\quad ⨠⨠ \quad 29$$

#### Complex division
Compute the following divisions of complex numbers: 

(a) $\displaystyle\frac{1}{-3+i}$ $\quad$ (b) $\displaystyle\frac{1}{i}$ $\quad$ (c) $\displaystyle\frac{1}{7i}$ $\quad$ (d) $\displaystyle\frac{2+5i}{2-5i}$

**Solution**

(a) $\displaystyle\frac{1}{-3+i}$

Conjugate is $-3-i$: 

$$\frac{1}{-3+i}\quad ⨠⨠ \quad \frac{1}{-3+i}\cdot\frac{-3-i}{-3-i}$$

Simplify: 

$$⨠⨠ \quad \frac{-3-i}{9+1}\quad ⨠⨠ \quad \frac{-3}{10}+\frac{-1}{10}i$$

---

(b) $\displaystyle\frac{1}{i}$

Conjugate is $-i$: 

$$\frac{1}{i}\quad ⨠⨠ \quad \frac{1}{i}\cdot\frac{-i}{-i}\quad ⨠⨠ \quad -i$$

---

(c) $\displaystyle\frac{1}{7i}$

Factor out the $1/7$: 

$$\frac{1}{7i}\quad ⨠⨠ \quad \frac{1}{7}\cdot\frac{1}{i}$$

Use $\frac{1}{i}=-i$: 

$$⨠⨠ \quad \frac{1}{7}\cdot(-i)\quad ⨠⨠ \quad \frac{-1}{7}i$$

---

(d) $\displaystyle\frac{2+5i}{2-5i}$

Denominator conjugate is $2+5i$: 

$$\frac{2+5i}{2-5i}\quad ⨠⨠ \quad \frac{2+5i}{2-5i}\cdot\frac{2+5i}{2+5i}$$

Simplify: 

$$⨠⨠ \quad \frac{4+20i+25i^2}{4+25}\quad ⨠⨠ \quad \frac{-21}{29}+\frac{20}{29}i$$


#### Complex product, quotient, power using Euler
Start with two complex numbers: 

$$z=2e^{i\frac{\pi}{2}}\quad \qquad w=5e^{i\frac{\pi}{3}}$$

---

Product $zw$: 

$$\begin{gather*}zw \quad ⨠⨠ \quad  \left(2e^{i\frac{\pi}{2}}\right)\cdot\left(5e^{i\frac{\pi}{3}}\right) \\\\ ⨠⨠ \quad (2\cdot 5)\left(e^{i\frac{\pi}{2}}\right)\left(e^{i\frac{\pi}{3}}\right)\quad ⨠⨠ \quad 10e^{i\frac{\pi}{2}+i\frac{\pi}{3}}\quad ⨠⨠ \quad 10e^{i\frac{5\pi}{6}}\end{gather*}$$

Quotient $z/w$: 

$$\begin{gather*}z/w \quad ⨠⨠ \quad \left(2e^{i\frac{\pi}{2}}\right)\Big/\left(5e^{i\frac{\pi}{3}}\right) \\\\ ⨠⨠ \frac{2e^{i\frac{\pi}{2}}}{5e^{i\frac{\pi}{3}}}\quad ⨠⨠ \quad \frac{2}{5}e^{i\frac{\pi}{2}}e^{-i\frac{\pi}{3}}\quad ⨠⨠ \quad \frac{2}{5}e^{i\frac{\pi}{6}}\end{gather*}$$

---

Power $z^8$: 

$$\begin{gather*}z^8\quad ⨠⨠ \quad \left(2e^{i\frac{\pi}{2}}\right)^8\\\\ ⨠⨠ \quad 2^8\left(e^{i\frac{\pi}{2}}\right)^8\quad ⨠⨠ \quad 512e^{i\cdot4\pi}\end{gather*}$$

Notice: 

$$e^{i\cdot4\pi}\quad ⨠⨠ \quad \left(e^{2\pi i}\right)^2\quad ⨠⨠ \quad 1^2\quad ⨠⨠ \quad 1$$

Simplify: 

$$512e^{i\cdot 4\pi}\quad ⨠⨠ \quad 512$$

Thus: $\,z^8=512$.


#### Complex power from Cartesian
Compute $(3+3i)^4$.

**Solution**

First convert to exponential form: 

$$\begin{gather*}3+3i\quad ⨠⨠ \quad 3\sqrt{2}\left(\frac{1}{\sqrt{2}}+\frac{1}{\sqrt{2}}i\right)\\\\ ⨠⨠ \quad 3\sqrt{2}e^{i\frac{\pi}{4}}\end{gather*}$$

Compute the power: 

$$\begin{gather*}(3+3i)^4\quad ⨠⨠ \quad \left(3\sqrt{2}e^{i\frac{\pi}{4}}\right)^4\\\\ ⨠⨠ \quad 324e^{i\pi}\quad ⨠⨠ \quad -324\end{gather*}$$


#### Finding all $4^\text{th}$ roots of $16$
Compute all the $4^\text{th}$ roots of $16$.

**Solution**

Write $16=16e^{0i}$.

Evaluate roots formula: 

$$\left(16e^{0i}\right)^\frac{1}{4}\quad ⨠⨠ \quad w_k=16^\frac{1}{4}e^{i\left(\frac{0}{4}+k\frac{2\pi}{4}\right)}$$

Simplify: 

$$⨠⨠ \quad 2e^{i\cdot k\frac{\pi}{2}}\quad ⨠⨠ \quad 2,\;2i,\;-2,\;-2i$$


#### Finding $2^\text{nd}$ roots of $2i$
Find both $2^\text{nd}$ roots of $2i$.

**Solution**

Write $2i=2e^{i\frac{\pi}{2}}$.
Evaluate roots formula: 

$$\begin{gather*}\left(2e^{\textstyle i\frac{\pi}{2}}\right)^\frac{1}{2}\quad ⨠⨠ \quad w_k=\sqrt{2}e^{\textstyle i\left(\frac{\pi/2}{2}+k\frac{2\pi}{2}\right)}\\\\ ⨠⨠ \quad \sqrt{2}e^{\textstyle i\left(\frac{\pi}{4}+k\pi\right)}\end{gather*}$$

Compute the options: $k=0,\,1$: 

$$⨠⨠ \quad \sqrt{2}e^{\textstyle i\frac{\pi}{4}},\;\sqrt{2}e^{\textstyle i\frac{5\pi}{4}}$$

Convert to rectangular: 

$$\begin{gather*}⨠⨠ \quad \sqrt{2}\left(\frac{1}{\sqrt{2}}+\frac{1}{\sqrt{2}}i\right),\;\sqrt{2}\left(-\frac{1}{\sqrt{2}}-\frac{1}{\sqrt{2}}i\right)\\\\ ⨠⨠ \quad 1+i,\;1-i\end{gather*}$$


#### Some roots of unity
Find the $1^\text{st}$ and $2^\text{nd}$ and $3^\text{rd}$ and $4^\text{th}$ and $5^\text{th}$ and $6^\text{th}$ roots of the number $1$.

**Solution**

![center|350](Pasted%20image%2020241130125331.png)

$1^\text{st}$

Write $1=e^{0i}$. Evaluate roots formula. There is no possible $k$: 

$$\left(e^{0i}\right)^\frac{1}{1}\quad ⨠⨠ \quad e^{0i}\quad ⨠⨠ \quad 1$$

---

$2^\text{nd}$

Write $1=e^{0i}$. Evaluate roots formula in terms of $k$: 

$$\left(e^{0i}\right)^\frac{1}{2}\quad ⨠⨠ \quad w_k= e^{i\left(\frac{0}{2}+k\frac{2\pi}{2}\right)}\qquad k=0,\,1$$

Compute the two options, $k=0,\,1$: 

$$⨠⨠ \quad 1,\;e^{\pi i}\quad ⨠⨠ \quad 1,\;-1$$

---

$3^\text{rd}$

Evaluate roots formula in terms of $k$: 

$$\left(e^{0i}\right)^\frac{1}{3}\quad ⨠⨠ \quad w_k=e^{i\left(\frac{0}{3}+k\frac{2\pi}{3}\right)}$$

Compute the options: $k=0,\,1,\,2$: 

$$⨠⨠ \quad 1,\;e^{i\frac{2\pi}{3}},\;e^{i\frac{4\pi}{3}}\quad ⨠⨠ \quad 1,\quad-\frac{1}{2}+\frac{\sqrt{3}}{2}i,\quad-\frac{1}{2}-\frac{\sqrt{3}}{2}i$$

---

$4^\text{th}$

Evaluate roots formula: 

$$\left(e^{0i}\right)^\frac{1}{4}\quad ⨠⨠ \quad w_k=e^{i\left(\frac{0}{4}+k\frac{2\pi}{4}\right)}$$

Compute the options: $k=0,\,1,\,2,\,3$: 

$$1,\;e^{i\frac{\pi}{2}},\;e^{i\pi},\;e^{i\frac{3\pi}{2}}\quad ⨠⨠ \quad 1,\;i,\;-1,\;-i$$

---

$5^\text{th}$
Evaluate roots formula: 

$$\left(e^{0i}\right)^\frac{1}{5}\quad ⨠⨠ \quad w_k=e^{i\left(\frac{0}{5}+k\frac{2\pi}{5}\right)}$$

Compute the options: $k=0,\,1,\,2,\,3,\,4$: 

$$1,\; e^{i\frac{2\pi}{5}},\;e^{i\frac{4\pi}{5}},\;e^{i\frac{6\pi}{5}},\;e^{i\frac{8\pi}{5}}$$

Don’t simplify, it’s not feasible.

---

$6^\text{th}$

Evaluate roots formula: 

$$\left(e^{0i}\right)^\frac{1}{6}\quad ⨠⨠ \quad w_k=e^{i\left(\frac{0}{6}+k\frac{2\pi}{6}\right)}$$

Compute the options: $k=0,\,1,\,2,\,3,\,4,\,5$: 

$$1,\; e^{i\frac{2\pi}{6}},\;e^{i\frac{4\pi}{6}},\;e^{i\frac{6\pi}{6}},\;e^{i\frac{8\pi}{6}},\;e^{i\frac{10\pi}{6}}$$

Simplify: 

$$⨠⨠ \quad 1,\; \frac{1}{2}+\frac{\sqrt{3}}{2}i,\;-\frac{1}{2}+\frac{\sqrt{3}}{2}i,\;-1,\;-\frac{1}{2}-\frac{\sqrt{3}}{2}i,\;\frac{1}{2}-\frac{\sqrt{3}}{2}i$$

