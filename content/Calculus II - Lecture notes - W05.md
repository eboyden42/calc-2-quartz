---
cssclasses:
  - hide-embedded-header
title: W05 Notes
---
## Hydrostatic force

Videos, Organic Chemistry Tutor
- [Hydrostatic pressure problems](https://www.youtube.com/watch?v=3jG-hWgUJko&t=540s&ab_channel=TheOrganicChemistryTutor)

### 01 Theory
The pressure in a liquid is a function of the depth alone. This is a fundamental fact about liquids.

> [!concept] Pressure function
> The fluid pressure in a liquid is a function of depth: $$p(h)=\rho g h$$
> - $\rho=\text{fluid density}$
> - $g=\text{gravity constant}$

In SI units:
- $\rho=1000\mathrm{kg/m^3}$
- $g=9.8\mathrm{m/s^2}$

The pressure of a fluid acts upon any surface in the fluid by exerting a force perpendicular to the surface. Force is pressure times area. If the pressure varies across the surface, the total force must be calculated using an integral to add up differing contributions of force on each portion of the surface.
![200](Pasted%20image%2020240924214821.png)

> [!concept] Fluid force on submerged plate
> Total fluid force on plate: $$F=\rho g \int_a^b y\, w(y)\,dy$$
> - $w(y)=\text{width of horizontal slice}$
> - $a,\,b=\text{vertical limits of surface}$
> 
> Use $y=a$ for top of plate (shallow) and $y=b$ for bottom of plate (deepest).
> Have $y=0$ at the surface.

- !! This formula assumes the plate is *oriented straight vertically*, not slanting.
- !!! Note that $y$ *increases with depth*, reverse from the usual $y$-axis.

![200](Pasted%20image%2020240924214902.png)
![300](Pasted%20image%2020240924215103.png)

### 02 Illustration

> [!mexample] Fluid force on a triangular plate
> ![15 - Fluid force on a triangular plate](Calculus%20II%20-%20Examples%20-%20Unit%2002.md#15%20-%20Fluid%20force%20on%20a%20triangular%20plate)

%% 
### 03 Theory

What if the submerged surface is *not* oriented straight vertically?

The amount of surface for a horizontal strip at a given depth will be increased by a factor of $\csc\theta$ where $\theta$ is the angle of incline of the surface (with $\theta=0$ corresponding to horizontal and $\theta=\pi/2$ to vertical). Thus: $$dz=\csc\theta\,dy$$
where $dz$ is the thickness of a strip.

So the total force formula becomes: 
> [!concept] Fluid force for tilted surface
> Total fluid force on tilted plate: $$F=\rho g\int_a^b y\,w\,dz=\rho g\int_a^b y\,w(y)\csc\theta\,dy$$
> As before, $y$ measures depth with $y=0$ at the surface.

### 04 Illustration

> [!mexample] Weight of water on a dam
> ![16 - Weight of water on a dam](Calculus%20II%20-%20Examples%20-%20Unit%2002.md#16%20-%20Weight%20of%20water%20on%20a%20dam)

 %%

## Moments and center of mass

Videos, Math Dr. Bob:
- [Moments and CoM 01: Points masses on a line](https://www.youtube.com/watch?v=ZxOIlCjh_pw&ab_channel=MathDoctorBob)
- [Moments and CoM 02: Points masses in the plane](https://www.youtube.com/watch?v=9B2QWixxv5s&ab_channel=MathDoctorBob)
- [Moments and CoM 03: Planar lamina of uniform density](https://www.youtube.com/watch?v=pS-RwiGlwv4&ab_channel=MathDoctorBob)
- [Moments and CoM 04: Integral formula for planar lamina](https://www.youtube.com/watch?v=uh5pskuly1g&ab_channel=MathDoctorBob)
- [Moments and CoM 05: Rod of non-uniform density](https://www.youtube.com/watch?v=xxXUCYzdrlM&ab_channel=MathDoctorBob)

### 03 Theory

> [!concept] Moment
> The **moment** of a region to an axis is the total (integral) of mass times distance to that axis:
> 
> “Moment to $x$:”
> $$\begin{align*}M_x&= \int \rho\,y\,dA \qquad \text{(general formula)}\\\\ M_x&= \int_c^d \rho\,y\,\big(g_2(y)-g_1(y)\big)\,dy \qquad \text{(region between functions $g_2$ and $g_1$)}\end{align*}$$
> 
> “Moment to $y$:”
> $$\begin{align*}M_y&= \int \rho\, x\,dA \qquad \text{(general formula)}\\\\ M_y&= \int_a^b \rho \,x\,\big(f_2(x)-f_1(x)\big)\,dx \qquad \text{(region between functions $f_2$ and $f_1$)}\end{align*}$$

- !!! Notice the *swap* in letters! $M_y$ has integral with $x$ while $M_x$ has integral with $y$.
    - Because $M_y$ needs distance to *$x$-axis*.
- ! Notice that if you remove $x$ or $y$ factors from the integrands, the integrals give **total mass $M$**.

These formulas are obtained by slicing the region into rectangular strips that are parallel to the axis in question.

The area *per strip* is then: 
- $f(x)\,dx$ — region under $y=f(x)$
- $(f_2-f_1)\,dx$  — region between $f_1$ and $f_2$
- $g(y)\,dy$ — region ‘under’ $x=g(y)$
- $(g_2-g_1)\,dy$ — region between $g_1$ and $g_2$

![500](Pasted%20image%2020250205185504.png)

![200](Pasted%20image%2020250205190049.png)

---

The idea of moment is related to:
- Torque balance and angular inertia
- Center of mass

The **center of mass (CoM)** of a solid body is a single point with two important properties: 
1. $\text{CoM}=$ “average position” of the body
    - The average position determines an *effective center* of dynamics. For example, gravity acting on every bit of mass of a rigid body acts the same as a force on the CoM alone.
2. $\text{CoM}=$ “balance point” of the body
    - The net *torque* (rotational force) about the CoM, generated by a force distributed over the body’s mass, equivalently a force on the CoM, is zero.

Note:
- %& When the body has *uniform density*, then the CoM is also called the **centroid**.

---

> [!concept] Center of mass from moments
> Coordinates of the CoM: $$\bar{x}=\frac{M_y}{M},\qquad \bar{y}=\frac{M_x}{M}$$
> 
> Here $M_x$ and $M_y$ are the moments and $M$ is the total mass of the body.

> [!extra] Center of mass from moments - explanation
> Notice how these formulas work. The total mass is always $M=\int\rho\,dA$. The moment to $y$ (for example) is $M_y=\int\rho\,x\,dA$. Dividing these: 
> $$\bar{x}=\frac{M_y}{M}\quad ⨠⨠ \quad \frac{\int\rho\,x\,dA}{\int\rho\,dA}\quad ⨠⨠ \quad \frac{\int x\,dA}{\int\,dA}\quad ⨠⨠ \quad \frac{\int x\,dA}{A}$$
> where $A=\text{total area}$.
> 
> In other words, through the formula $\bar{x}=\displaystyle\frac{M_y}{M}$, we find that $\bar{x}$ is the *average value of $x$* over the region with area $A$.

### 04 Illustration

> [!mexample] CoM of a parabolic plate
> ![17 - CoM of a parabolic plate](Calculus%20II%20-%20Examples%20-%20Unit%2002.md#17%20-%20CoM%20of%20a%20parabolic%20plate)

### 05 Theory

A downside of the technique above is that to find $M_x$ we needed to convert the region into functions in $y$. This would be hard to do if the region was given as the area under a curve $y=f(x)$ but $f^{-1}(y)$ cannot be found analytically. An alternative formula that works in this situation.

> [!summary] Midpoint of strips for opposite variables
> When the region lies between $f_1(x)$ and $f_2(x)$, we can find $M_x$ with an $x$-integral: $$M_x = \int_c^d\rho\,\tfrac{1}{2}\big(f_2^2-f_1^2\big)\,dx \qquad \text{(region between $f_1$ and $f_2$)}$$
> 
> When the region lies between $g_1(y)$ and $g_2(y)$, we can find $M_y$ with a $y$-integral: $$M_y = \int_a^b\rho\,\tfrac{1}{2}\big(g_2^2-g_1^2\big)\,dx \qquad \text{(region between $g_1$ and $g_2$)}$$

- ! Use $f_1=0$ or $g_1=0$ for regions “under a curve” $y=f_2(x)$ or $x=g_2(y)$.

The idea for these formulas is to treat each vertical strip as a point concentrated at the CoM of the vertical strip itself.

![300](Pasted%20image%2020240929090751.png)

The height to this midpoint is $\frac{1}{2}f(x)$, and the area of the strip is $f(x)\,dx$, so the integral becomes $\int\rho\,\frac{1}{2}f(x)^2\,dx$.

> [!extra] Midpoint of strips formula - full explanation
> - If the strip is located at some $x$, with $y$ values from $0$ up to $f(x)$, then: $$\text{CoM of strip}=\left(x,\,\frac{1}{2}f(x)\right)$$
> - The area of the strip is $dA=f(x)\,dx$. So the integral formula for $M_x$ can be recast: $$M_x=\int y\,dA \quad ⨠⨠ \quad  \int_a^b \tfrac{1}{2}f(x)\cdot f(x)\,dx\quad ⨠⨠ \quad \int_a^b \tfrac{1}{2}f^2\,dx$$
> - If the vertical strips are between $f_1(x)$ and $f_2(x)$, then the *midpoints* of the strips are given by the ‘average’ function: $$\frac{1}{2}\Big(f_1(x)+f_2(x)\Big)$$
> - The *height* of each strip is $f_2(x)-f_1(x)$, so $dA=(f_2-f_1)\,dx$.
> - Putting this together: $$\begin{gather*}M_x=\int y\,dA\quad ⨠⨠ \quad \int_a^b \tfrac{1}{2}\big(f_1(x)+f_2(x)\big)\cdot (f_2-f_1)\,dx\\\\ ⨠⨠ \quad \int_a^b\tfrac{1}{2}\big(f_2^2-f_1^2\big)\,dx\end{gather*}$$

### 06 Illustration

> [!mexample] Computing CoM using only vertical strips
> ![18 - Computing CoM using only vertical strips](Calculus%20II%20-%20Examples%20-%20Unit%2002.md#18%20-%20Computing%20CoM%20using%20only%20vertical%20strips)


> [!mexample] CoM of region between line and parabola
> ![19 - CoM of region between line and parabola](Calculus%20II%20-%20Examples%20-%20Unit%2002.md#19%20-%20CoM%20of%20region%20between%20line%20and%20parabola)


### 07 Theory

Two useful techniques for calculating moments and (thereby) CoMs:
- Additivity principle
- Symmetry

Additivity says that you can *add moments of parts* of a region to get the total moment of the region (to a given axis).

A symmetry principle is that if a region is *mirror symmetric across some line*, then the CoM must lie on that line.

### 08 Illustration

> [!mexample] Center of mass using moments and symmetry
> ![20 - Center of mass using moments and symmetry](Calculus%20II%20-%20Examples%20-%20Unit%2002.md#20%20-%20Center%20of%20mass%20using%20moments%20and%20symmetry)

> [!mexample] Center of mass - two part region
> ![21 - Center of mass - two part region](Calculus%20II%20-%20Examples%20-%20Unit%2002.md#21%20-%20Center%20of%20mass%20-%20two%20part%20region)

