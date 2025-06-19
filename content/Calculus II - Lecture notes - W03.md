---
cssclasses:
  - hide-embedded-header
title: W03 Notes
---
## Partial fractions
Videos, Math Dr. Bob:
- [Partial Fractions 01](https://www.youtube.com/watch?v=2gA3mYG5xBA) - Distinct Linear Factors
- [Partial Fractions 02](https://www.youtube.com/watch?v=JT6Y0gDU1Ck) - Repeated Linear Factors
- [Partial Fractions 03](https://www.youtube.com/watch?v=mMHOwjCg31g) - Distinct Mixed Factors
- [Partial Fractions 04](https://www.youtube.com/watch?v=72MAfFXeWbU) - Repeated Quadratic Factors
- [Partial Fractions 05](https://www.youtube.com/watch?v=8nZgL_ayT9k) - Composition with $e^x$

### 01 Theory
A *rational function* is a ratio of polynomials, for example:
$$\frac{P(x)}{Q(x)}=\frac{5x^2+x-28}{x^3-4x^2+x+6}$$

> [!concept] Partial fraction decomposition
> The **partial fraction decomposition** of a rational function is a way of writing it as a *sum of simple terms*, like this: 
> $$\frac{3x^3 - 5x^2 - 6x + 20}{x^4 - 3x^3 + 4x} = -\frac{2}{x+1}+\frac{2}{(x-2)^2}+\frac{5}{x}$$
> 
> Allowed denominators:
> - Linear, as any $x-a$, or linear power, as any $(x-a)^n$
> - Quadratic, as any $x^2+bx+c$, or quadratic power, as any $(x^2+bx+c)^n$
>     - Condition: quadratics must be *irreducible* (no roots, or i.e. $b^2<4c$)
> 
> Allowed numerators: constant (over linear power) or linear (over quadratic power)

These are *allowed* as simple terms in partial fraction decompositions: 
$$\frac{1}{x^2+1},\qquad\frac{2x+1}{x^2+5},\qquad\frac{7}{5x-8},\qquad\frac{1}{x},\qquad \frac{1}{x^3}$$
These are *not allowed*: 
$$\frac{x}{x-1},\qquad\frac{x^3+2}{x^2+1},\qquad \frac{1}{x^2-1},\qquad \frac{1}{x(x-1)}$$

These are allowed, showing irreducible quadratic and higher powers: $$\frac{x}{x^2+1},\qquad \frac{x^3+2x+1}{(x^2+2)^2}$$
In this example the numerator is linear and the denominator is quadratic and irreducible.

To *create* a partial fraction decomposition, follow these steps: 

1. *Check* denominator degree is higher
    - Else do *long division*
2. *Factor* denominator completely (even using irrational roots)
3. *Write the generic* sum of partial fraction terms with their constants
    - !! Repeated factors – special treatment: sum with incrementing powers
4. *Solve* for constants

### 02 Illustration
> [!mexample] Partial fractions with repeated factor
> ![09 - Partial fractions with repeated factor](Calculus%20II%20-%20Examples%20-%20Unit%2001.md#09%20-%20Partial%20fractions%20with%20repeated%20factor)

### 03 Theory
Partial fractions can be *integrated* using just a few techniques. We consider three kinds of terms: 
$$\begin{gather*}\frac{A}{x-a},\quad\frac{A}{(x-a)^2},\quad\frac{A}{(x-a)^3},\quad\dots,\\\\ \text{and}\qquad \frac{A}{x^2+h^2},\qquad\text{and}\qquad \frac{Ax+B}{x^2+h^2}\end{gather*}$$

> [!summary] Linear power bottom
> To integrate terms like this: $$\frac{A}{(x-a)^n}$$
> 
> If $n=1$ then use log: $$\int\frac{A}{x-a}\,dx=A\ln|x-a|+C$$
> 
> If $n>1$ then use power rule: $$\int\frac{A}{(x-a)^n}\,dx\quad ⨠⨠ \quad \int A(x-a)^{-n}\,dx \quad ⨠⨠ \quad  A\frac{(x-a)^{-n+1}}{-n+1}+C$$

> [!summary] Quadratic bottom, constant top
> We have a formula for simple irreducible quadratics: $$\int\frac{dx}{x^2+h^2}=\frac{1}{h}\tan^{-1}\left(\frac{x}{h}\right)+C$$

- !! This formula should be memorized!

> [!summary] Quadratic bottom, linear top
> To integrate terms like this: $$\frac{Ax+B}{x^2+h^2}$$
> Break into separate terms: $$\frac{Ax+B}{x^2+h^2}\qquad ⨠⨠ \qquad \frac{Ax}{x^2+h^2}+\frac{B}{x^2+h^2}$$
> 
> Then:
> 
> - First term *with* $x$ in top: $$\int\frac{Ax}{x^2+h^2}\,dx\quad ⨠⨠ \quad \frac{A}{2}\ln\left|x^2+h^2\right|+C$$
> 
> - Second term *lacking* $x$ in top: $$\int\frac{B}{x^2+h^2}\,dx\quad ⨠⨠ \quad \frac{B}{h}\tan^{-1}\left(\frac{x}{h}\right)+C$$

> [!extra] Extra - Completing the square when “no real roots”
> To integrate terms with more general quadratics, like this: $$\frac{A}{x^2+bx+c}$$
> we need $b^2-4c<0$, i.e. “no real roots” of the quadratic. If that holds, then we can *complete the square* and substitute $u=\tan\theta$ as follows.
> 
> Look what happens when completing the square: 
> $$x^2+bx+c\quad ⨠⨠ \quad \left(x+\frac{b}{2}\right)^2-\frac{b^2}{4}+c$$
> Notice that $b^2-4c<0$ is *equivalent* to the condition $-\frac{b^2}{4}+c>0$. Create a new label $Z=-\frac{b^2}{4}+c$. So this condition means $Z>0$ and we can safely define $\sqrt{Z}$.
> 
> Then a $u$-substitution $u=x+\frac{b}{2}$ simplifies the equation like this: 
> $$x^2+bx+c\quad ⨠⨠ \quad u^2+\sqrt{Z}^2$$
> 
> The quadratic formula $x=\frac{-b\pm\sqrt{b^2-4ac}}{2a}$ shows that the condition $b^2-4c<0$ is *equivalent* to the condition “no real roots.” (In our case $a=1$. If we had $a\neq 1$, we could divide out this $a$ and change the others.)
> 
> So we see that “no real roots” is *equivalent* to the condition that the denominator can be converted to the format $x^2+h^2$ with some constant $h$.
> 
> At this point, to compute the integral, do trig sub with $u=\sqrt{Z}\tan\theta$ and $du=\sqrt{Z}\sec^2\theta\,d\theta$: $$\begin{gather*}\int\frac{A\,dx}{x^2+bx+c}\qquad ⨠⨠ \qquad \int \frac{A\sqrt{Z}\sec^2\theta\,d\theta}{Z\sec^2\theta}\\\\ \quad ⨠⨠ \quad  \frac{A}{\sqrt{Z}}\int d\theta \quad ⨠⨠ \quad  \frac{A}{\sqrt{Z}}\theta + C \\\\ ⨠⨠ \quad  \frac{A}{\sqrt{Z}}\tan^{-1}\left(\frac{x+b/2}{\sqrt{Z}}\right)+C\end{gather*}$$

### 04 Illustration
> [!mexample] Example - Repeated quadratic, linear tops
> ![10 - Partial fractions - repeated quadratic, linear tops](Calculus%20II%20-%20Examples%20-%20Unit%2001.md#10%20-%20Partial%20fractions%20-%20repeated%20quadratic,%20linear%20tops)

%%  %%
> [!extra] Extra - “Rationalize a quotient” - convert into PFD
> Sometimes an integrand may be *converted* to a rational function using a *substitution*.
> 
> Consider this integral: $$\int\frac{\sqrt{x+4}}{x}\,dx$$
> 
> Set $u=\sqrt{x+4}$, so $x=u^2-4$ and $dx=2u\,du$: $$⨠⨠ \quad \int\frac{2u\,du}{u^2-4}$$
> Now this rational function has a partial fraction decomposition: $$\frac{2u}{u^2-4}\quad ⨠⨠ \quad \frac{2u}{(u-2)(u+2)}\quad ⨠⨠ \quad \frac{1}{u-2}+\frac{1}{u+2}$$
> 
> It is easy to integrate from there!
> 
> Exercise examples: 
> - To compute $\int\frac{\sqrt{x}}{x-1}\,dx$, try the substitution $u=\sqrt{x}$.
> - To compute $\int\frac{dx}{\sqrt[2]{x}-\sqrt[3]{x}}$, try the substitution $u=\sqrt[6]{x}$.
> - To compute $\int\frac{1}{x-\sqrt{x+2}}\,dx$, try the substitution $u=\sqrt{x+2}$.

## Simpson’s Rule
Videos, Math Dr. Bob:
- [Simpson’s Rule with Error Bound](https://www.youtube.com/watch?v=6Sir_ItpCBE)

Videos, Organic Chemistry Tutor:
- [Midpoint Rule and Riemans Sums](https://www.youtube.com/watch?v=5XreKMJDJsg&pp=ygUNbWlkcG9pbnQgcnVsZQ%3D%3D)
- [Simpson’s Rule and Numerical Integration](https://www.youtube.com/watch?v=7EqRRuh-5Lk&t=274s&pp=ygUNbWlkcG9pbnQgcnVsZQ%3D%3D)

### 05 Theory - review
The **Trapezoid Rule** is a technique to approximate the area under a curve as the sum of areas of thin trapezoids whose top corners lie on the curve.

![250](Pasted%20image%2020240912134942.png)
The tops of the trapezoids are lines that approximate the curve. They are determined as lines that agree with the curve at two points.

> [!concept] Trapezoid rule - area formula
> Given a function $f$ and a partition of the range $[a,b]$ labeled by $x_0,\,x_1,\,\dots,\,x_n$ (with $x_0=a$ and $x_n=b$), the Trapezoid Rule determines the area formula: $$T_n = \frac{1}{2}\Delta x\Big(y_0+2y_1+2y_2+\cdots+2y_{n-1}+y_n\Big)$$

Notice the pattern in $2$s and see how this formula comes about:
The area of one trapezoid is $\Delta x\left(\frac{y_{j-1}+y_j}{2}\right)$. All vertical values $y_1,\,\dots,\,y_{n-1}$ (excepting the endpoints $f(a)$ and $f(b)$) are represented in *two* trapezoids, so their contribution is doubled.

> [!extra] Extra - Trapezoid rule - error bound
> The **error** of the Trapezoid Rule approximation is **bounded** by this formula: $$\mathrm{Error}(T_n)\leq \frac{K_2(b-a)^3}{12n^2}$$
> Here $K_2$ is any number satisfying $K_2\geq |f''(x)|$ for $x\in[a,b]$.


The **Midpoint Rule** is a technique to approximate the area under a curve as the sum of areas of thin rectangles whose top midpoints lies on the curve.

![250](Pasted%20image%2020240912140821.png)

The very same formula also represents the areas of trapezoids whose top midpoints lie on the curve and whose top line is *tangent* to the curve: 
![250](Pasted%20image%2020240912140915.png)

The *reason* they are equal is simple: when pivoting the top line on the ‘attached’ midpoint, the area of the trapezoid does not change.

> [!concept] Midpoint Rule - area formula
> Given a function $f$ and a partition of the range $[a,b]$ labeled by $x_0,\,x_1,\,\dots,\,x_n$ (with $x_0=a$ and $x_n=b$), the Midpoint Rule determines the area formula: $$M_n = \Delta x\Big(f(c_1)+f(c_2)+\cdots+f(c_{n-1})+f(c_n)\Big)$$
> Here each $c_i$ is the midpoint of the interval $[x_{i-1},x_i]$. It can be given by the formula $c_i=a+(i-1/2)\Delta x$.

> [!extra] Extra - Midpoint Rule - error bound
> The **error** of the Midpoint Rule approximation is **bounded** by this formula: $$\mathrm{Error}(M_n)\leq \frac{K_2(b-a)^3}{24n^2}$$
> Here $K_2$ is any number satisfying $K_2\geq |f''(x)|$ for $x\in[a,b]$.

Notice that $M_n$ has an error bound that is $1/2$ of the bound for $T_n$. This does not mean that $M_n$ always has a smaller error than $T_n$. It means that *without calculating the error*, simply plugging numbers into the error bound formulas, we obtain a smaller bound for $M_n$ than for $T_n$. This is about our *knowledge* of the error, not the *reality* of the error.

### 06 Theory
It turns out that the Midpoint Rule and the Trapezoid Rule tend to differ from the exact integral in *opposite directions*, and the Midpoint Rule tends to be twice as accurate. Therefore we may improve on both of them by constructing a *weighted average* of the formulas. This is called **Simpson’s Rule**.

![250](Pasted%20image%2020240912150438.png)

> [!concept] Simpson’s Rule - defining formula
> Simpson’s Rule is given by the weighted sum of the Trapezoid and Midpoint Rules: $$S_n = \frac{1}{2}T_n+\frac{2}{3}M_n$$

> [!concept] Simpson’s Rule - computing formula
> Given a function $f$ and a partition of the range $[a,b]$ labeled by $x_0,\,x_1,\,\dots,\,x_n$ (with $x_0=a$ and $x_n=b$), Simpson’s Rule determines the area formula: $$S_n = \frac{1}{3}\Delta x\Big(y_0+4y_1+2y_2+4y_3+2y_4+\cdots+2y_{n-2}+4y_{n-1}+y_n\Big)$$

- !! Note the pattern for Simpson’s Rule: 1, 4, 2, 4, 2, 4, 2, $\dots$, 1

> [!summary] Simpson’s Rule - error bound
> The **error** of Simpson’s Rule approximation is **bounded** by this formula: $$\mathrm{Error}(S_n)\leq \frac{K_4(b-a)^5}{180n^4}$$
> Here $K_4$ is any number satisfying $K_4\geq |f^{(4)}(x)|$ for $x\in[a,b]$.

> [!extra] Simpson’s Rule $=$ “Parabola Rule”
> The formula of Simpson’s Rule can also be explained or defined geometrically: it is the formula giving the sum of areas under small *parabolas* that meet the curve in three points.
> 
> There is a unique parabola passing through any three points with differing $x$-values:
> ![150](Pasted%20image%2020240912152020.png)
> 
> These may be pieced together to form an approximation to the curve:
> ![350](Pasted%20image%2020240912152139.png)
> The area under the parabola through $P_0$, $P_1$, and $P_2$ is given by this formula: 
> $$\frac{h}{3}\big(y_0+4y_1+y_2\big)$$
> This formula may be verified using basic calculus (area under a parabola) and a lot of algebra. (Ambitious students should derive it.)
> 
> The area under the parabola through $P_2$, $P_3$, and $P_4$ is given by a similar formula: 
> $$\frac{h}{3}\big(y_2+4y_3+y_4\big)$$
> The Simpson’s Rule formula is the sum of all these formulas! So the $2$s in Simpson’s come from duplication of endpoint terms as the “rectangular” regions are stacked end-to-end.

### 07 Illustration
> [!mexample] Example - Simpson’s Rule on the Gaussian Distribution
> ![11 - Simpson’s Rule on the Gaussian distribution](Calculus%20II%20-%20Examples%20-%20Unit%2001.md#11%20-%20Simpson’s%20Rule%20on%20the%20Gaussian%20distribution)

