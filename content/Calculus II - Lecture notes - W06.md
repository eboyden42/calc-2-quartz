---
cssclasses:
  - hide-embedded-header
title: W06 Notes
---
## Work

Videos, BlackPenRedPen:
- [Work performed](https://www.youtube.com/watch?v=-DEkriNuPNQ): pumping water from trough
- [Work performed](https://www.youtube.com/watch?v=LpiGIxMvO24): pumping water from rectangular tank
- [Work performed](https://www.youtube.com/watch?v=Ab0omZH2fFc): pumping water from conical tank
- [Work performed](https://www.youtube.com/watch?v=exGqWWAkhto): pumping water from spherical tank

### 01 Theory

Work is a measure of energy expended to achieve some effect. According to physics: 
$$\text{Work}=\text{Force}\times\text{Distance}$$
$$W=\int_a^b F(x)\,dx$$

To compute the work performed against gravity while *lifting some matter*, decompose the matter into *horizontal layers* at height $y$ and thickness $dy$. Each layer is lifted some distance. The weight of the layer gives the force applied.

The work performed on each single layer is summed by an integral to determine the total work performed to lift all the layers:

> [!concept] Work performed
> $$\text{Work to lift a layer} = g\times\text{density}\times A(y)\times\text{height raised}\times dy$$
> 
> $$\text{Total work} = \int_a^b \rho g\, h(y) A(y)\,dy$$
> 
> - $A(y)=\text{area of layer}$
> - $h(y)=\text{height layer is lifted}$
> - $\rho=\text{mass density}$
> - $g=9.8\,\mathrm{m/s^2}=\text{constant of gravitational acceleration}$

### 02 Illustration

> [!mexample] Example - Pumping water from spherical tank
> ![Pumping water from spherical tank](Calculus/2025%20Spring/W06%20-%20Examples.md#Pumping%20water%20from%20spherical%20tank)

> [!mexample] Example - Water pumped from a frustum
> ![Water pumped from a frustum](Calculus/2025%20Spring/W06%20-%20Examples.md#Water%20pumped%20from%20a%20frustum)

> [!mexample] Example - Raising a building
> ![Raising a building](Calculus/2025%20Spring/W06%20-%20Examples.md#Raising%20a%20building)

> [!mexample] Example - Raising a chain
> ![Raising a chain](Calculus/2025%20Spring/W06%20-%20Examples.md#Raising%20a%20chain)

> [!mexample] Example - Raising a leaky bucket
> ![Raising a leaky bucket](Calculus/2025%20Spring/W06%20-%20Examples.md#Raising%20a%20leaky%20bucket)

- !!! In the last example, the same bucket passes through each height, it is not sliced into layers.
    - This integral adds work done to lift matter through each $dy$ as if in parallel, and $dy$ is thus representing *distance lifted*.
    - Previous examples have integral adding work done to lift matter through some $y$ or $5-y$; the matter was sliced into layers with $dy$ featuring in the *weight* of a portion.


## Improper integrals

Videos, Math Dr. Bob: 
- [Improper integrals](https://www.youtube.com/watch?v=LN9oxGWUJso&ab_channel=MathDoctorBob): Infinite limits
- [Improper integrals](https://www.youtube.com/watch?v=KmSEORtpeMk&ab_channel=MathDoctorBob): Vertical asymptote
- [Improper integrals](https://www.youtube.com/watch?v=lFfPY2E2uno&ab_channel=MathDoctorBob): $\int\frac{1}{x^p}\,dx$
- [Improper integrals](https://www.youtube.com/watch?v=gi1zuWmFVCE&ab_channel=MathDoctorBob): $\int\frac{1}{x^2}e^{-1/x}\,dx$

### 03 Theory

**Improper integrals** are those for which either a *bound* or the *integrand* itself become *infinite* somewhere on the interval of integration.

Examples:
$$(a)\quad\int_1^\infty\frac{1}{x^2}\,dx,\qquad\qquad (b)\quad \int_0^2\frac{1}{x}\,dx, \qquad\qquad (c)\quad \int_{-1}^{+1}\frac{1}{x^2}\,dx$$

- (a) the upper bound is $\infty$
- (b) the integrand goes to $\infty$ as $x\to 0^+$
- $(c)$ the integrand is $\infty$ at the point $0\in[-1,1]$

The limit interpretation of $(a)$ is this: 
$$\int_1^\infty\frac{1}{x^2}\,dx\quad=\quad\lim_{R\to\infty}\int_1^R\frac{1}{x^2}\,dx$$
The limit interpretation of $(b)$ is this: 
$$\int_0^2\frac{1}{x}\,dx\quad=\quad\lim_{R\to0^+}\int_R^2\frac{1}{x}\,dx$$
The limit interpretation of $(c)$ is this: $$\begin{gather*}\int_{-1}^{+1}\frac{1}{x^2}\,dx\quad=\quad\int_{-1}^0\frac{1}{x^2}\,dx+\int_0^{+1}\frac{1}{x^2}\,dx\\\\ =\quad\lim_{R\to0^-}\int_{-1}^R\frac{1}{x^2}\,dx+\lim_{R\to0^+}\int_R^{+1}\frac{1}{x^2}\,dx\end{gather*}$$
These limits are evaluated using familiar methods.

An improper integral is said to be **convergent** or **divergent** according to whether it may be assigned a finite value through the appropriate *limit interpretation*.

For example, $(a)$ converges while $(b)$ diverges.

### 04 Illustration

> [!mexample] Example - Improper integral - infinite bound
> ![Improper integral - infinite bound](Calculus/2025%20Spring/W06%20-%20Examples.md#Improper%20integral%20-%20infinite%20bound)

> [!mexample] Improper integral - infinite integrand
> ![Improper integral - infinite integrand](Calculus/2025%20Spring/W06%20-%20Examples.md#Improper%20integral%20-%20infinite%20integrand)

> [!mexample] Example - Improper integral - infinity inside the interval
> ![Example - Improper integral - infinity inside the interval](Calculus/2025%20Spring/W06%20-%20Examples.md#Example%20-%20Improper%20integral%20-%20infinity%20inside%20the%20interval)

### 05 Theory

Two tools allow us to determine convergence of a large variety of integrals. They are the **comparison test** and the **$p$-integral cases**.

> [!concept] Comparison test - integrals
> The comparison test says:
> - When an improper integral converges, every *smaller* integral converges.
> - When an improper integral diverges, every *bigger* integral diverges.

Here, smaller and bigger are comparisons of the *integrand* (accounting properly for signs), and the bounds are assumed to be the same.

For example, since $\int_2^\infty\frac{dx}{x^3}$ converges, and $x^4>x^3$ implies $\frac{1}{x^4}<\frac{1}{x^3}$ (when $x>1$), the comparison test implies that $\int_2^\infty \frac{dx}{x^4}$ also converges.

> [!concept] $p$-integral cases
> Assume $p>0$ and $a>0$. We have:
> $$\begin{align*}p>1:\qquad& \int_a^\infty\frac{dx}{x^p}\quad\text{converges} &\text{and}\quad&\int_0^a\frac{dx}{x^p}\quad\text{diverges}\\\\ p<1:\qquad& \int_a^\infty\frac{dx}{x^p}\quad\text{diverges} &\text{and}\quad&\int_0^a\frac{dx}{x^p}\quad\text{converges}\\\\ p=1:\qquad& \int_a^\infty\frac{dx}{x}\quad\text{diverges} &\text{and}\quad&\int_0^a\frac{dx}{x}\quad\text{diverges}\end{align*}$$

> [!extra] Proving the $p$-integral cases
> It is easy to prove the convergence / divergence of each $p$-integral case using the limit interpretation and the power rule for integrals. (Or for $p=1$, using $\int\frac{1}{x}\,dx=\ln x+C$.)

> [!concept] Additional improper integral types
> The improper integral $\int_{-\infty}^a f(x)\,dx$ also has a limit interpretation: $$\int_{-\infty}^af(x)\,dx\quad=\quad\lim_{R\to-\infty}\int_R^a f(x)\,dx$$
> 
> The **double improper** integral $\int_{-\infty}^{\infty} f(x)\,dx$ has this limit interpretation: $$\int_{-\infty}^{\infty} f(x)\,dx\quad=\quad\lim_{R\to-\infty}\int_R^a f(x)\,dx+\lim_{R\to\infty}\int_a^R f(x)\,dx$$
> Where $a$ is any finite number. This double integral does not exist if either limit does not exist for any value of $a$.

> [!warning] Double improper is not simultaneous!
> Watch out! This may happen: $$\int_{-\infty}^{\infty} f(x)\,dx\quad\neq\quad \lim_{R\to\infty}\int_{-R}^R f(x)\,dx$$
> 
> This simultaneous limit might exist only due to internal cancellation, in a case where the separate individual limits do not exist!

### 06 Illustration

> [!mexample] Example - Comparison to $p$-integrals
> ![Comparison to $p$-integrals](Calculus/2025%20Spring/W06%20-%20Examples.md#Comparison%20to%20$p$-integrals)

