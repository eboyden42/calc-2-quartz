---
cssclasses:
  - hide-embedded-header
title: W15 Notes
---
## Complex algebra
Videos, Organic Chemistry Tutor
- [Complex numbers basics](https://www.youtube.com/watch?v=OQz1ydBcQSA&t=2854s)

### 01 Theory - Complex arithmetic

The complex numbers $\mathbb{C}$ are sums of real and imaginary numbers. Every complex number can be written uniquely in ‘Cartesian’ form: 

$$z=a+bi,\qquad a,\,b\in\mathbb{R}$$

To add, subtract, scale, and multiply complex numbers, treat ‘$i$’ like a constant.

Simplify the result using $i^2=-1$.

For example:

$$\begin{gather*}(1+3i)(2-2i)\quad ⨠⨠ \quad 2-2i+6i-6i^2\\\\ ⨠⨠ \quad2+4i-6(-1)\quad ⨠⨠ \quad8+4i\end{gather*}$$

---

> [!concept] Complex conjugate
> Every complex number has a **complex conjugate**: 
> 
> $$z=a+bi\qquad ⨠⨠ \qquad \bar{z}=a-bi$$

For example: 

$$\begin{align*}\overline{2+5i}\quad &= \quad 2-5i\\\\ \overline{2-5i} \quad&= \quad 2+5i\end{align*}$$

In general, $\bar{\bar{z}}=z$.

Conjugates are useful mainly because they eliminate imaginary parts: 

$$(2+5i)(2-5i)\quad ⨠⨠ \quad 4+25\quad ⨠⨠ \quad 29$$

In general: 

$$(a+bi)(a-bi)\quad ⨠⨠ \quad a^2-abi+bia-b^2i^2\quad ⨠⨠ \quad a^2+b^2\in\mathbb{R}$$

---

> [!tip] Complex division
> To divide complex numbers, use the conjugate to eliminate the imaginary part in the denominator.

For example, reciprocals: 

$$\begin{gather*}\frac{1}{a+bi}\quad ⨠⨠ \quad \frac{1}{a+bi}\cdot\frac{a-bi}{a-bi}\\\\ ⨠⨠ \quad \frac{a-bi}{a^2+b^2}\quad ⨠⨠ \quad \left(\frac{a}{a^2+b^2}\right)+\left(\frac{-b}{a^2+b^2}\right)i\end{gather*}$$

More general fractions: 

$$\begin{gather*}\frac{a+bi}{c+di}\quad ⨠⨠ \quad \frac{a+bi}{c+di}\cdot\frac{c-di}{c-di}\\\\ ⨠⨠ \quad \frac{ac+bd+(bc-ad)i}{c^2+d^2}\quad ⨠⨠ \quad \frac{ac+bd}{c^2+d^2}+\frac{bc-ad}{c^2+d^2}i\end{gather*}$$

> [!abstract] Multiplication preserves conjugation
> For any $z,\,w\in\mathbb{C}$: 
> 
> $$\overline{zw}=\bar{z}\bar{w}$$
> 
> Therefore, one can take products or conjugates in either order.

### 02 Illustration

> [!mexample] Example - Complex multiplication
> ![Complex multiplication](W15%20-%20Examples.md#Complex%20multiplication)

> [!mexample] Example - Complex division
> ![Complex division](W15%20-%20Examples.md#Complex%20division)


## Complex exponential
Videos, Khan Academy
- [Complex exponential form](https://www.youtube.com/watch?v=N0Y8ia57C24&t=586s)

### 03 Theory - cis, Euler, products, powers

Multiplication of complex numbers is much easier to understand when the numbers are written using polar form.

There is a shorthand ‘$\mathrm{cis}$’ notation: 

$$\begin{align*}a+bi \quad &⨠⨠ \quad   r\cos\theta+r\sin\theta\, i \\\\ &⨠⨠ \quad  r\big(\cos\theta+i\sin\theta\big)\\\\ &⨠⨠ \quad  r\,\mathrm{cis}\,\theta\end{align*}$$

The $\mathrm{cis}$ notation stands for $\cos\theta + i \sin\theta$.

For example: 

$$\begin{gather*}\sqrt{2}-\sqrt{2}i \quad ⨠⨠ \quad 2\left(\frac{1}{\sqrt{2}}-\frac{1}{\sqrt{2}}i\right)\\\\ ⨠⨠ \quad 2\cos\left(-\frac{\pi}{4}\right)+2\sin\left(-\frac{\pi}{4}\right)\,i\\\\ ⨠⨠ \quad 2\,\mathrm{cis}\left(-\frac{\pi}{4}\right)\end{gather*}$$

---

> [!abstract] Euler Formula
>  General **Euler Formula**: 
>  
>  $$re^{i\theta}\quad=\quad r\cos\theta+i\,r\sin\theta$$
>  
>  On the unit circle: 
>  
>  $$e^{i\theta}\quad=\quad \cos\theta+i\sin\theta$$

The form $re^{i\theta}$ expresses the *same data* as the $\mathrm{cis}$ form.

The principal advantage of the form $re^{i\theta}$ is that it *reveals the rule for multiplication*: 

> [!abstract] Complex multiplication - Exponential form
> $$r_1e^{\textstyle i\theta_1}\, \cdot\, r_2e^{\textstyle i\theta_2} \quad=\quad (r_1r_2)\,e^{\textstyle i(\theta_1+\theta_2)}$$
> 
> In words:
> - Multiply radii
> - Add angles

Notice: 

$$\text{multiply by } e^{\textstyle  i\frac{\pi}{2}}\qquad\iff\qquad \text{rotate by }+90^\circ$$

Notice: 

$$e^{i\frac{\pi}{2}}=+i$$

Therefore $i$ ‘acts upon’ other numbers by rotating them $90^\circ$ counterclockwise!

---

> [!abstract] De Moivre’s Theorem - Complex powers
> In exponential notation:
> 
> $$\big(re^{i\theta}\big)^n \;=\; r^ne^{i\cdot n\theta}$$
> 
> In $\mathrm{cis}$ notation:
> 
> $$\big(r\,\mathrm{cis}\,\theta\big)^n \;=\; r^n\,\mathrm{cis}\,(n\theta)$$
> 
> Expanded $\mathrm{cis}$ notation: 
> 
> $$\big(r\cos\theta+i\,r\sin\theta\big)^n \;=\; r^n\cos(n\theta)+i\,r^n\sin(n\theta)$$

So the power of $n$ acts like this: 
- **Stretch**: $r$ to $r^n$
- **Rotate** by $n$ increments of $\theta$

---

> [!extra] Extra - Derivation of Euler Formula
> Recall the power series for $e^x$: 
> 
> $$ e^x = 1+\frac{1}{1!}x+\frac{1}{2!}x^2+\frac{1}{3!}x^3 + \dots \quad= \sum_{i=0}^\infty \frac{1}{i!}x^i $$
> 
> Plug in $x=i\theta$: 
> 
> $$\begin{gather*}e^{i\theta}\quad ⨠⨠ \quad 1+(i\theta)+ \frac{1}{2!}(i\theta)^2 + \frac{1}{3!}(i\theta)^3 + \dots +\end{gather*}$$
> 
> Simplify terms: 
> 
> $$⨠⨠ \quad 1+i\theta-\frac{1}{2!}\theta^2-\frac{1}{3!}i\theta^3+\frac{1}{4!}\theta^4+\frac{1}{5!}i\theta^5-\frac{1}{6!}\theta^6-\frac{1}{7!}i\theta^7+\frac{1}{8!}\theta^8+\cdots$$
> 
> Separate by $i$-factor. Select out the $\overbracket{\text{terms with } i}$: 
> 
> $$⨠⨠ \quad 1\overbracket{+i\theta}-\frac{1}{2!}\theta^2\overbracket{-\frac{1}{3!}i\theta^3}+\frac{1}{4!}\theta^4\overbracket{+\frac{1}{5!}i\theta^5}-\frac{1}{6!}\theta^6\overbracket{-\frac{1}{7!}i\theta^7}+\frac{1}{8!}\theta^8+\cdots$$
> 
> Separate into a series without $i$ and a series with $i$: 
> 
> $$⨠⨠ \quad \left(1 - \frac{1}{2!}\theta^2 + \frac{1}{4!}\theta^4 - \cdots \right) + \left( \theta- \frac{1}{3!}\theta^3 + \frac{1}{5!}\theta^5 - \cdots \right)i$$
> 
> Identify $\cos\theta$ and $\sin \theta\,i$. Write trig series: 
> 
> $$\begin{align*}\cos\theta&= 1 - \frac{1}{2!}\theta^2 + \frac{1}{4!}\theta^4 - \cdots\\\\ \sin\theta &= \theta- \frac{1}{3!}\theta^3 + \frac{1}{5!}\theta^5 - \cdots\end{align*}$$
> 
> Therefore $e^{i\theta}=\cos\theta+i\sin\theta$.

### 04 Illustration

> [!mexample] Example - Complex product, quotient, power using Euler
> ![Complex product, quotient, power using Euler](W15%20-%20Examples.md#Complex%20product,%20quotient,%20power%20using%20Euler)

> [!mexample] Example - Complex power from Cartesian
> ![Complex power from Cartesian](W15%20-%20Examples.md#Complex%20power%20from%20Cartesian)


## Complex roots
Videos, Trefor Bazett
- [Finding cube roots](https://youtu.be/25x6lsxHVpU?feature=shared&t=485): Find cube roots of $-1$

Videos, Brain Gainz
- [Finding nth roots](https://www.youtube.com/watch?v=bGFMxfO0eK4): Fourth roots of $\sqrt{3}-i$ and cube roots of $-8$

### 05 Theory - Roots formula

The exponential notation leads to a formula for a complex $n^\text{th}$ root of any complex number: 

$$\sqrt[n]{re^{i\theta}} \quad=\quad \sqrt[n]{r}\;e^{\textstyle i\frac{\theta}{n}}$$

⚠️ Every complex number actually has $n$ distinct complex $n^\text{th}$ roots!

That’s two square roots, three cube roots, four $4^\text{th}$ roots, etc.

> [!concept] All complex roots
> The complex roots of $z=re^{i\theta}$ are given by: 
> 
> $$w_k \;=\; \sqrt[n]{r}\,\cdot e^{\textstyle i\left(\frac{\theta}{n}+k\frac{2\pi}{n}\right)}\qquad \text{for each }\, k=0,\,1,\,2,\,\dots,\,n-1$$
> 
> In Cartesian notation: 
> 
> $$w_k \;=\;  \sqrt[n]{r}\;\cos\left(\frac{\theta}{n}+k\frac{2\pi}{n}\right)+\sqrt[n]{r}\;\sin\left(\frac{\theta}{n}+k\frac{2\pi}{n}\right)i$$
> 
> In words:
> - Start with the basic root: $\,\sqrt[n]{r}\cdot e^{i\frac{\theta}{n}}$
> - Rotate by increments of $\frac{2\pi}{n}$ to get all other roots

> [!extra] Extra - Complex roots proof
> We must verify that $w_k^n=re^{i\theta}$: 
> 
> $$\begin{gather*}\left(\sqrt[n]{r}\,\cdot e^{\textstyle i\left(\frac{\theta}{n}+k\frac{2\pi}{n}\right)}\right)^n \quad ⨠⨠ \quad r^{\frac{n}{n}}\cdot e^{\textstyle i\left(\frac{\theta}{n}+k\frac{2\pi}{n}\right)n} \\\\ ⨠⨠ \quad r\cdot e^{\textstyle i\left(\theta+2\pi k\right)} \quad ⨠⨠ \quad re^{i\theta}e^{i\,2\pi k} \quad ⨠⨠ \quad re^{i\theta}\end{gather*}$$

### 06 Illustration

> [!mexample] Example - Finding all $4^\text{th}$ roots of $16$
> ![Finding all $4^\text{th}$ roots of $16$](W15%20-%20Examples.md#Finding%20all%20$4%20text{th}$%20roots%20of%20$16$)

> [!mexample] Example - Finding $2^\text{nd}$ roots of $2i$
> ![Finding $2^\text{nd}$ roots of $2i$](W15%20-%20Examples.md#Finding%20$2%20text{nd}$%20roots%20of%20$2i$)

> [!mexample] Example - Some roots of unity
> ![Some roots of unity](W15%20-%20Examples.md#Some%20roots%20of%20unity)

