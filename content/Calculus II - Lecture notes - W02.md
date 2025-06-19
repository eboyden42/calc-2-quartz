---
cssclasses:
  - hide-embedded-header
title: W02 Notes
---
## Trig power products
Videos, Math Dr. Bob:
- [Trig power products](https://www.youtube.com/watch?v=3imhs7feiqk): $\int\cos^mx \sin^nx\,dx$
- [Trig differing frequencies](https://www.youtube.com/watch?v=Jug4fSuSw5Y): $\int\cos mx \sin nx\,dx$
- [Trig tan and sec](https://www.youtube.com/watch?v=O17BpzkBUUo): $\int\tan^mx \sec^nx\,dx$
- [Secant power](https://www.youtube.com/watch?v=bS87_hjxcMI): $\int\sec^5x\,dx$

Videos, Organic Chemistry Tutor:
- [Trig power product techniques](https://www.youtube.com/watch?v=3pXALn2ovIE)
- [Trig substitution](https://www.youtube.com/watch?v=ocgjfF2AboA)

### 01 Theory

**Review: trig identities**
- $\sin^2 x + \cos^2 x = 1$
- $\sin^2 x = \frac{1}{2}(1-\cos 2x)$
- $\cos^2 x = \frac{1}{2}(1+\cos 2x)$

> [!concept] Trig power product: $\sin /\cos$
> A $\sin / \cos$ power product has this form: $$\int \cos^m x\cdot \sin^n x \,dx$$
> 
> for some integers $m$ and $n$ (even negative!).
> 
> To compute these integrals, use a sequence of these techniques:
> - **Swap an even bunch.**
> - **$u$-sub for power-one.**
> - **Power-to-frequency conversion.**

- !!! Memorize these three techniques!

Examples of trig power products: 
- $\displaystyle\int \sin x\cdot \cos^7 x\,dx$
- $\displaystyle\int \sin^3 x\,dx$
- $\displaystyle\int \sin^2 x\cdot\cos^2 x\,dx$

> [!summary] Swap an even bunch
> If *either* $\cos^m x$ or $\sin^n x$ is an *odd* power, use $$\begin{align*}\sin^2x\quad ⨠⨠& \quad 1-\cos^2x\\\\\text{OR}\quad \cos^2x\quad ⨠⨠& \quad 1-\sin^2x\end{align*}$$ (maybe repeatedly) to convert an **even bunch** to the opposite trig type.
> 
> An **even bunch** is *all but one* from the odd power.

For example: $$\begin{align*}\sin^5 x\cdot \cos^8 x \qquad &⨠⨠ \qquad  \sin x\, (\sin^2 x)^2\cdot\cos^8 x\\\\ \qquad &⨠⨠ \qquad  \sin x\, (1-\cos^2 x)^2\cdot\cos^8 x\\\\ \qquad &⨠⨠ \qquad \sin x\,\big( 1-2\cos^2 x+\cos^4 x \big)\cdot\cos^8 x \\\\ \qquad &⨠⨠ \qquad \sin x\,\big( \cos^8 x - 2\cos^{10} x + \cos^{12}x \big) \\\\ \qquad &⨠⨠ \qquad \sin x \cos^8 x -2\sin x\cos^{10}x+\sin x\cos^{12}x \end{align*}$$

> [!summary] $u$-sub for power-one
> If $m=1$ or $n=1$, *perform $u$-substitution* to do the integral.
> 
> The *other* trig power becomes a $u$ power; the power-one becomes $du$.

For example, using $u=\cos x$ and thus $du=-\sin x\,dx$ we can do: 
$$\int \sin x \cos^8 x\,dx \quad ⨠⨠ \quad  \int -\cos^8x (-\sin x\,dx) \quad ⨠⨠ \quad  -\int u^8\,du$$

- ! By combining these tricks you can do any power product with at least one odd power!
    - Leave a power-one from the odd power when swapping an even bunch.
- !! Notice: $1=\sin^0x=\cos^0x$, even powers. So the method works for $\int \sin^3 x\,dx$ and similar.

> [!summary] Power-to-frequency conversion
> Using these ‘power-to-frequency’ identities (maybe repeatedly): $$\sin^2 x = \tfrac{1}{2}(1-\cos 2x),\qquad \cos^2 x = \tfrac{1}{2}(1+\cos 2x)$$
> 
> change an even power (either type) into an odd power of cosine.

For example, consider the power product: 
$$\sin^4x\cdot\cos^6 x$$
You can substitute appropriate powers of $\sin^2 x = \frac{1}{2}(1-\cos 2x)$ and $\cos^2 x = \frac{1}{2}(1+\cos 2x)$: 
$$\begin{align*}\sin^4x\cdot\cos^6 x \qquad &⨠⨠ \qquad \big(\sin^2x\big)^2\cdot \big(\cos^2x\big)^3\\\\ \qquad &⨠⨠ \qquad \Big(\tfrac{1}{2}(1-\cos 2x)\Big)^2\cdot \Big(\tfrac{1}{2}(1+\cos 2x)\Big)^3 \end{align*}$$
By doing some annoying algebra, this expression can be expanded as a sum of *smaller* powers of $\cos 2x$: 
$$\begin{gather*}\Big(\tfrac{1}{2}(1-\cos 2x)\Big)^2\cdot \Big(\tfrac{1}{2}(1+\cos 2x)\Big)^3\\\\⨠⨠ \quad  \frac{1}{32}\Big(1 + \cos(2 x) - 2 \cos^2(2 x) - 2 \cos^3(2 x) + \cos^4(2 x) + \cos^5(2 x)\Big)\end{gather*}$$

Each of these terms can be integrated by repeating the same techniques.

### 02 Illustration
> [!mexample] Example - Trig power product with an odd power
> ![05 - Power product - odd power](Calculus%20II%20-%20Examples%20-%20Unit%2001.md#05%20-%20Power%20product%20-%20odd%20power)

### 03 Theory
> [!concept] Trig power product: $\tan /\sec$ or $\cot /\csc$
> A $\tan / \sec$ power product has this form: $$\int \tan^m x\cdot\sec^n x\,dx$$
> A $\cot /\csc$ power product has this form: $$\int \cot^m x\cdot \csc^n x\,dx$$

To integrate these, **swap an even bunch** using: 
- $\tan^2 x + 1 = \sec^2 x$

OR:
- $\cot^2 x + 1 = \csc^2 x$

Or do **$u$-substitution** using: 
- $u=\tan x\;\rightsquigarrow\; du=\sec^2x\,dx$
- $u=\sec x\;\rightsquigarrow\;du=\sec x\,\tan x\,dx$

OR: 
- $u=\cot x\;\rightsquigarrow\;du=-\csc^2x\,dx$
- $u=\csc x\;\rightsquigarrow\;du=-\csc u\,\cot u\,dx$

Note:
- !!! There is no simple “power-to-frequency conversion” for tan / sec !


We can modify the power-one technique to solve some of these. We need to swap over an even bunch *from the odd power* so that exactly the $du$ factor is left behind.

Considering all the possibilities, one sees that this method works when: 
- $\tan^mx$ is an *odd* power (with some secants present!)
- $\sec^nx$ is an *even* power

Quite a few cases escape this method:
- Any $\int \tan^mx\,dx$ with no power of $\sec x$
- Any $\int\tan^mx\cdot\sec^nx\,dx$ for $m$ even and $n$ odd

These tricks don’t work for $\int \tan x\,dx$ or $\int \sec x\,dx$ or $\int \tan^4x\,\sec^5x\,dx$, among others.

> [!concept] Special integrals: tan and sec
> We have: $$\begin{align*}\int\tan x\,dx&= \ln|\sec x|+C\\\\ \int\sec x\,dx &= \ln|\sec x + \tan x|+C\end{align*}$$

- !!! These integrals should be memorized individually.

> [!extra] Extra - Deriving special integrals - tan and sec
> The first formula can be found by $u$-substitution, considering that $\tan x=\frac{\sin x}{\cos x}$.
> 
> The second formula can be derived by multiplying $\sec x$ by a special “$1$”, computing instead $\int\frac{\sec x(\sec x+\tan x)}{\sec x+\tan x}\,dx$ by expanding the numerator and doing $u$-sub on the denominator.

### 04 Illustration
> [!mexample] Example - Trig power product with tan and sec
> ![06 - Power product - tan and sec](Calculus%20II%20-%20Examples%20-%20Unit%2001.md#06%20-%20Power%20product%20-%20tan%20and%20sec)



## Trig substitution
Videos, Math Dr. Bob:
- [Trig sub 1](https://www.youtube.com/watch?v=V6wrKvcnYrA): Basics and $\int\frac{1}{\sqrt{36-x^2}}\,dx$ and $\int\frac{x}{36+x^2}\,dx$ and $\int\frac{1}{\sqrt{x^2-36}}\,dx$
- [Trig sub 2](https://www.youtube.com/watch?v=gWG2Ln3__eI): $\int\frac{dx}{(1+x^2)^{5/2}}$
- [Trig sub 3](https://www.youtube.com/watch?v=MOTk8wjiDQM): $\int\frac{x^2}{\sqrt{1-4x^2}}\,dx$
- [Trig sub 4](https://www.youtube.com/watch?v=zrWpjq8P_Dw): $\int\sqrt{e^{2x} - 1}\,dx$
- [Trig sub 5](https://www.youtube.com/watch?v=FIvSSKKDguE): $\int\frac{\sqrt{4-36x^2}}{x^2}\,dx$

### 05 Theory

Certain algebraic expressions have a secret meaning that comes from the Pythagorean Theorem. This meaning has a very simple expression in terms of trig functions of a certain angle.

For example, consider the integral: $$\int\frac{1}{x^2\sqrt{x^2-9}}\,dx$$
Now consider this triangle: 
![300](Pasted%20image%2020240906205158.png)

The triangle determines the relation $x=3\sec\theta$, and it implies $\sqrt{x^2-9}=3\tan\theta$.

Now plug these into the integrand above:

$$\frac{1}{x^2\sqrt{x^2-9^2}}\qquad ⨠⨠ \qquad \frac{1}{9\sec^2\theta \cdot3\tan\theta}$$

Considering that $dx=3\sec\theta\,\tan\theta\,d\theta$, we obtain a very reasonable trig integral: 

$$\begin{align*}\int\frac{1}{x^2\sqrt{x^2-9^2}}\,dx \qquad ⨠⨠& \qquad \int \frac{3\sec\theta\,\tan\theta}{27\sec^2\theta\,\tan\theta}\,d\theta\\\\ ⨠⨠& \quad \frac{1}{9}\int\cos\theta\,d\theta\quad ⨠⨠ \quad \frac{1}{9}\sin\theta+C\end{align*}$$

We must rewrite this in terms of $x$ using $x=3\sec\theta$ to finish the problem. We need to find $\sin\theta$ assuming that $\sec\theta=\frac{x}{3}$. To do this, refer back to the triangle to see that $\sin\theta=\frac{\sqrt{x^2-9}}{x}$. Plug this in for our final value of the integral:

$$\frac{1}{9}\sin\theta+C\quad ⨠⨠ \quad  \frac{\sqrt{x^2-9}}{9x}+C$$

Here is the moral of the story: 
- ! Re-express the Pythagorean expression *using a triangle and a trig substitution*.
    - In this way, square roots of quadratic polynomials can be eliminated.

There are always three steps for these trig sub problems: 
- (1) Identify the trig sub: find the sides of a triangle and relevant angle $\theta$.
- (2) Solve a trig integral (often a power product).
- (3) Refer back to the triangle to convert the answer back to $x$.

To speed up your solution process for these problems, *memorize* these three transformations: 

(1)
$$\sqrt{a^2-x^2}\qquad \overset{x=a\sin\theta}{⨠⨠} \qquad \sqrt{a^2-a^2\sin^2\theta}=a\cos\theta\qquad \text{from}\quad 1-\sin^2\theta=\cos^2\theta$$

(2)
$$\sqrt{a^2+x^2}\qquad \overset{x=a\tan\theta}{⨠⨠} \qquad \sqrt{a^2+a^2\tan^2\theta}=a\sec\theta\qquad \text{from}\quad 1+\tan^2\theta=\sec^2\theta$$

(3)
$$\sqrt{x^2-a^2}\qquad \overset{x=a\sec\theta}{⨠⨠} \qquad \sqrt{a^2\sec^2\theta-a^2}=a\tan\theta\qquad \text{from}\quad \sec^2\theta-1=\tan^2\theta$$

For a more complex quadratic with linear and constant terms, you will need to first *complete the square* for the quadratic and then do the trig substitution.

### 06 Illustration
> [!mexample] Example - Trig sub in quadratic: completing the square
> ![08 - Trig sub in quadratic - completing the square](Calculus%20II%20-%20Examples%20-%20Unit%2001.md#08%20-%20Trig%20sub%20in%20quadratic%20-%20completing%20the%20square)

