---
cssclasses:
  - hide-embedded-header
title: W04 Notes
---
## Arc length

Videos, Math Dr. Bob:
- [Formula for Arc Length 01](https://www.youtube.com/watch?v=QwSjeXfZ5FI): Theory and catenary
- [Formula for Arc Length 02](https://www.youtube.com/watch?v=4FLhCZ7yso0): Curve given by integral
- [Formula for Arc Length 03](https://www.youtube.com/watch?v=viYUInk-Y3k&ab_channel=MathDoctorBob): Reverse engineering
- [Arc Length of Parabola 01](https://www.youtube.com/watch?v=otd8DwxXOKU&ab_channel=MathDoctorBob): Base case
- [Arc Length of Parabola 02](https://www.youtube.com/watch?v=zJK-hXriV6I&ab_channel=MathDoctorBob): Sinh formula
- [Arc Length of Parabola 03](https://www.youtube.com/watch?v=n907KIXCAoU&ab_channel=MathDoctorBob): Log formula

Videos, Khan Academy:
- [Arc length integration example](https://www.youtube.com/watch?v=MtRXjXdXDow&ab_channel=KhanAcademy)

### 01 Theory
The **total arc length** of a curve is just the length of the curve.

The ‘arc length’ (not “total”) is a quantity measuring the length “as you go along,” usually given as a function of the points on the curve. It measures the length from some starting point ‘up to’ the given point.

We can use calculus to calculate the arc length of many curves. If the curve is the graph of a function, and we know the function and its derivative (whether from a formula or a data table), we can use integration to find the arc length.

> [!concept] Arc-length formula
> The arc length $s$ of the graph of $f(x)$ over $x\in[a,b]$ is: $$s=\int_a^b \sqrt{1+\big(f'(x)\big)^2}\,dx$$
> (This formula applies when $f'(x)$ exists and is continuous on $[a,b]$.)
> 
> The arc length *function* $s(x)$ of the graph of $f(x)$, starting from $x=a$, is: $$s(x)=\int_a^x \sqrt{1+\big(f'(t)\big)^2}\,dt$$

> [!extra] Arc-length formula - explanation
> The arc-length integral is the limit of Riemann sums that add the lengths of straight line segments whose endpoints lie on the curve, and which together approximate the curve.
> ![600](Pasted%20image%2020240915151831.png)
> 
> Each tiny line segment is the hypotenuse of a triangle with horizontal $\Delta x$ and vertical $\Delta y$.
> ![300](Pasted%20image%2020240915152458.png)
> 
> We can approximate the vertical $\Delta y$ using the *derivative*: $$\Delta y \approx \frac{dy}{dx}\Delta x = f'(x)\Delta x$$
> 
> Considering infinitesimals in the limit, we have $\Delta x\to dx$ (horizontal side) and $\Delta y \to dy=f'\,dx$ (vertical side). The Pythagorean Theorem gives: 
> $$ds=\sqrt{dx^2+dy^2}$$
> which we can simplify using $dy=f'\,dx$: 
> $$⨠⨠ \quad \sqrt{dx^2+\left(f'dx\right)^2}\qquad ⨠⨠ \qquad \sqrt{1+\big(f'\big)^2}\,dx$$
> The integral of these infinitesimals gives the arc length: $$s(a)=\int_0^a ds=\int\sqrt{1+\big(f'\big)^2}\,dx$$

### 02 Illustration
> [!mexample] Example - Arc length of chain in terms of position
> ![12 - Arc length of chain, via position](Calculus%20II%20-%20Examples%20-%20Unit%2002.md#12%20-%20Arc%20length%20of%20chain,%20via%20position)

%%  %%
> [!exercise] Exercise - Arc length of a line segment
> ![13 - Arc length, line segment](Calculus%20II%20-%20Examples%20-%20Unit%2002.md#13%20-%20Arc%20length,%20line%20segment)

## Surface areas of revolutions - thin bands
Videos, Math Dr. Bob
- [Area of a Surface of Revolution](https://www.youtube.com/watch?v=m8Ut9oiVVmU): Derivation, cylinder, cone, sphere

### 03 Theory
The infinitesimal of arc length along a curve, $ds$, can be used to find the **surface area** of a surface of revolution. The circumference of an **infinitesimal band** is $2\pi R$ and the width of such a band is $ds$.

![400](Pasted%20image%2020240919084248.png)

The general formula for the surface area is: $$S=\int_a^b 2\pi R\,ds$$

In any given problem we need to find the appropriate expressions for $R$ and $ds$ in terms of the variable of integration. For regions rotated around the $x$-axis, the variable will be $x$; for regions rotated about the $y$-axis it will be $y$.

Assuming the region is rotated around the $x$-axis, and the cross section in the $xy$-plane is the graph of $f$ and so $R=f(x)$, the formula above becomes: 

> [!concept] Area of revolution formula - thin bands
> The surface area $S$ of the surface of revolution given by $R=f(x)$ is given by the formula: $$S=\int_a^b 2\pi f(x)\sqrt{1+\big(f'\big)^2}\,dx$$
> 
> In this formula, we assume $f(x)\geq 0$ and $f'$ is continuous. The surface is the revolution of $f(x)$ on $x\in[a,b]$ around the $x$-axis.

### 04 Illustration
> [!mexample] Example - Surface area of a sphere
> ![14 - Surface area of a sphere](Calculus%20II%20-%20Examples%20-%20Unit%2002.md#14%20-%20Surface%20area%20of%20a%20sphere)

