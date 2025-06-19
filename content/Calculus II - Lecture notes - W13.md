---
cssclasses:
  - hide-embedded-header
title: W13 Notes
---
## Parametric curves
Videos, Organic Chemistry Tutor
- [Intro to parametric equations and graphing](https://www.youtube.com/watch?v=97pe-QlSGqA)

### 01 Theory
Parametric curves are curves traced by the path of a ‘moving’ point. An independent parameter, such as $t$ for ‘time’, controls *both $x$ and $y$* values through **Cartesian coordinate functions** $x(t)$ and $y(t)$. The coordinates of the moving point are $\big(x(t),\,y(t)\big)$.

> [!concept] Parametric curve
> A **parametric curve** is a function from parameter space $\mathbb{R}$ to the plane $\mathbb{R}^2$ given in terms of coordinate functions: $$t\longmapsto \big(\,x(t),\,y(t)\,\big)$$

> [!warning] Other notations
> Be aware that sometimes the coordinate functions are written with $f$ and $g$ (or yet other letters) like this: $\;(x,y)=(\,f(t),\,g(t)\,\big)$
> 
> Or simply equating coordinate letters with functions: $\;x=f(t),\;\; y=g(t)$
> 
> Sometimes a different parameter is used, like $s$ or $u$.

For example, suppose: $$x=t^2-2t,\qquad y=t+1$$ 
The curve traced out is a parabola that opens horizontally: 

![center|300](Pasted%20image%2020241122171406.png)

---

Given a parametric curve, we can create an equation satisfied by $x$ and $y$ variables by solving for $t$ in either coordinate function (inverting either $f$ or $g$) and plugging the result into the other function.

In the example: 

$$\begin{gather*}y=t+1\quad ⨠⨠ \quad t=y-1\\\\ ⨠⨠ \quad x=t^2-2t\quad ⨠⨠ \quad x=(y-1)^2-2(y-1)\\\\⨠⨠ \quad x=y^2-4y+3 \quad ⨠⨠ \quad \colorbox{aqua}{$x=(y-2)^2-1$}\end{gather*}$$

This is the equation of a parabola centered at $(-1,2)$ that opens to the right.

> [!concept] Image of a parametric curve
> The **image** of a parametric curve is the *set* of output points $\big(\,x(t),\,y(t)\,)$ that are traversed by the moving point.

A parametric curve has *hidden information* that isn’t contained in the image: 
- The *time values* $t$ when the moving point is found in various locations.
- The *speed* at which the curve is traversed.
- The *direction* in which the curve is traversed.

---

We can **reparametrize** a parametric curve to use a different parameter or different coordinate functions while leaving the *image unchanged*.

In the previous example, shift $t$ by $1$: 
$$\begin{gather*}x=(t+1)^2-2(t+1),\qquad y=(t+1)+1\\\\ \qquad ⨠⨠ \qquad x=t^2-1,\qquad y=t+2\hspace{4cm}\end{gather*}$$

Since the parameter $t$ and the parameter $t+1$ both cover the same values for $t\in(-\infty,\infty)$, the same curve is traversed. But the moving point in the second, shifted version reaches any given location *one unit earlier* in time. (When $t=-1$ in the second version, the input to $x(t)$ and $y(t)$ is the same as when $t=0$ in the first one.)

### 02 Illustration

> [!mexample] Example - Parametric circles
> ![Parametric circles](Calculus/2025%20Spring/W13%20-%20Examples.md#Parametric%20circles)

> [!mexample] Example - Parametric lines
> ![Parametric lines](Calculus/2025%20Spring/W13%20-%20Examples.md#Parametric%20lines)

> [!mexample] Example - Parametric ellipses
> ![Parametric ellipses](Calculus/2025%20Spring/W13%20-%20Examples.md#Parametric%20ellipses)

> [!mexample] Example - Parametric cycloids
> ![Parametric cycloids](Calculus/2025%20Spring/W13%20-%20Examples.md#Parametric%20cycloids)


## Calculus with parametric curves
### 03 Theory - Slope, concavity

We can use $x(t)$ and $y(t)$ data to compute the slope of a parametric curve in terms of $t$.

> [!abstract] Slope formula
> Given a parametric curve $\big(x(t),\,y(t)\big)$, its slope satisfies: 
> 
> $$\frac{dy}{dx}\;=\; \frac{y'(t)}{x'(t)}\qquad (\text{where }x'(t)\neq 0)$$

> [!abstract] Concavity formula
> Given a parametric curve $\big(x(t),\,y(t)\big)$, its concavity satisfies the formula: 
> 
> $$\frac{d^2y}{dx^2}\;=\;\frac{d}{dt}\left(\frac{y'(t)}{x'(t)}\right)\cdot\frac{1}{x'(t)}\qquad (\text{where }x'(t)\neq 0)$$

> [!extra] Extra - Derivation of slope and concavity formulas
> For both derivations, it is necessary to view $t$ as a function of $x$ through the inverse parameter function. For example if $x=f(t)$ is the parametrization, then $t=f^{-1}(x)$ is the inverse parameter function.
> 
> We will need the derivative $\frac{dt}{dx}$ in terms of $t$. For this we use the formula for derivative of inverse functions: $$\frac{dt}{dx}=\frac{1}{\frac{dx}{dt}}$$
> 
> Given all this, both formulas are simple applications of the chain rule.
> 
> For the slope: $$\begin{gather*}\frac{dy}{dx}=\frac{dy}{dt}\cdot\frac{dt}{dx}\qquad ⨠⨠ \qquad y'(t)\cdot\frac{1}{dx/dt}\\\\ ⨠⨠ \qquad \frac{y'(t)}{x'(t)}\end{gather*}$$
> 
> For the concavity: $$\begin{gather*}\frac{d^2y}{dx^2}=\frac{d}{dx}\left(\frac{dy}{dx}\right)\qquad ⨠⨠ \qquad \frac{d}{dt}\left(\frac{dy}{dx}\right)\cdot\frac{dt}{dx}\\\\ ⨠⨠ \qquad \frac{d}{dt}\left(\frac{y'(t)}{x'(t)}\right)\cdot\frac{1}{x'(t)}\end{gather*}$$
> 
> (In the second step we inserted the formula for $\frac{dy}{dx}$ from the slope.)

---

> [!concept] Pure vertical, Pure horizontal movement
> In view of the formula $\frac{dy}{dx}=\frac{y'(t)}{x'(t)}$, we see: 
> - Pure vertical: when $x'(t)=0$ and yet $y'(t)\neq 0$
> - Pure horizontal: when $y'(t)=0$ and yet $x'(t)\neq 0$

When $x'(t_0)=y'(t_0)=0$ for the same $t=t_0$, we have a **stationary point**, which might subsequently progress into pure vertical, pure horizontal, or neither.

### 04 Illustration

> [!mexample] Example - Tangent to a cycloid
> ![Tangent to a cycloid](Calculus/2025%20Spring/W13%20-%20Examples.md#Tangent%20to%20a%20cycloid)

> [!mexample] Example - Vertical and horizontal tangents of the circle
> ![Vertical and horizontal tangents of the circle](Calculus/2025%20Spring/W13%20-%20Examples.md#Vertical%20and%20horizontal%20tangents%20of%20the%20circle)

> [!mexample] Example - Finding the point with specified slope
> ![Finding the point with specified slope](Calculus/2025%20Spring/W13%20-%20Examples.md#Finding%20the%20point%20with%20specified%20slope)

### 05 Theory - Arclength

> [!concept] Arclength formula
> The **arclength** of a parametric curve with coordinate functions $x(t)$ and $y(t)$ is: 
> 
> $$L=\int_a^b \sqrt{(x')^2+(y')^2}\,dt$$
> 
> This formula assumes the curve is traversed one time as $t$ increases from $a$ to $b$.

> [!warning] Counts total traversal
> This formula applies when the curve image is traversed *one time* by the moving point.
> 
> Sometimes a parametric curve traverses its image with repetitions. The arclength formula would add length from each repetition!

> [!extra] Extra - Derivation of arclength formula
> The arclength of a parametric curve is calculated by integrating the infinitesimal arc element:
> 
> $$\begin{gather*}ds=\sqrt{dx^2+dy^2}\\\\ L=\int_a^b ds\end{gather*}$$
> 
> In order to integrate $ds$ in the $t$ variable, as we must for parametric curves, we convert $ds$ to a function of $t$: 
> 
> $$\begin{gather*}ds=\sqrt{dx^2+dy^2}\qquad ⨠⨠ \qquad \sqrt{\frac{1}{dt^2}\cdot\left(dx^2+dy^2\right)\cdot dt^2}\\\\ ⨠⨠ \qquad \sqrt{\frac{dx^2}{dt^2}+\frac{dy^2}{dt^2}}\cdot\sqrt{dt^2} \qquad ⨠⨠ \qquad \sqrt{\left(\frac{dx}{dt}\right)^2+\left(\frac{dy}{dt}\right)^2}\,dt\\\\  ⨠⨠ \qquad ds=\sqrt{x'(t)^2+y'(t)^2}\,dt\end{gather*}$$
> 
> So we obtain $ds=\sqrt{(x')^2+(y')^2}\,dt$ and the arclength formula follows from this: 
> 
> $$L=\int_a^b \sqrt{(x')^2+(y')^2}\,dt$$

### 06 Illustration

> [!mexample] Example - Perimeter of a circle
> ![Perimeter of a circle](Calculus/2025%20Spring/W13%20-%20Examples.md#Perimeter%20of%20a%20circle)

> [!mexample] Example - Perimeter of an asteroid
> ![Perimeter of an asteroid](Calculus/2025%20Spring/W13%20-%20Examples.md#Perimeter%20of%20an%20asteroid)


### 07 Theory - Distance, speed

> [!concept] Distance function
> The **distance function** $s(t)$ returns the total distance traveled by the particle from a chosen starting time $t_0$ up to the (input) time $t$: 
> 
> $$s(t)\;=\; \int_{t_0}^t ds\quad=\quad \int_{t_0}^t\sqrt{x'(u)^2+y'(u)^2}\,du$$

We need the dummy variable $u$ so that the integration process does not conflict with $t$ in the upper bound.

---

> [!concept] Speed function
> The **speed** of a moving particle is the *rate of change of distance*: 
> 
> $$v(t)\;=\; s'(t)\quad=\quad \sqrt{x'(t)^2+y'(t)^2}$$

This formula can be explained in either of two ways:
1. Apply the Fundamental Theorem of Calculus to the integral formula for $s(t)$.
2. Consider $ds=\sqrt{x'(t)^2+y'(t)^2}\,dt$ for a small change $dt$: so the *rate of change* of arclength is $\frac{ds}{dt}$, in other words $s'(t)$.

### 08 Illustration

> [!mexample] Example - Speed, distance, displacement
> ![Speed, distance, displacement](Calculus/2025%20Spring/W13%20-%20Examples.md#Speed,%20distance,%20displacement)


### 09 Theory - Surface area of revolutions

> [!concept] Surface area of a surface of revolution: thin bands
> Suppose a parametric curve $\big(x(t),\,y(t)\big)$ is revolved around the $x$-axis or the $y$-axis.
> 
> The surface area is: 
> 
> $$A\quad=\quad \int_a^b 2\pi R(t)\,\sqrt{(x')^2+(y')^2}\,dt$$
> 
> The radius $R(t)$ should be the distance to the axis:
> 
> $$\begin{align*}R(t)\;&= \; y(t)\qquad \text{revolution about $x$-axis}\\ R(t)\;&= \; x(t)\qquad \text{revolution about $y$-axis}\end{align*}$$

This formulas adds the areas of thin bands, but the bands are demarcated using parametric functions instead of input values of a graphed function.

The formula assumes that the curve is traversed one time as $t$ increases from $a$ to $b$.

### 10 Illustration

> [!mexample] Example - Surface of revolution - parametric circle
> ![Surface of revolution - parametric circle](Calculus/2025%20Spring/W13%20-%20Examples.md#Surface%20of%20revolution%20-%20parametric%20circle)

> [!mexample] Example - Surface of revolution - parametric curve
> ![Surface of revolution - parametric curve](Calculus/2025%20Spring/W13%20-%20Examples.md#Surface%20of%20revolution%20-%20parametric%20curve)

