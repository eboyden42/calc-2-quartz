#### 02 - Center of mass of a house
A "house" is a region bounded by the (non-regular) pentagon with vertex points at $(0, 5)$, (2, 3), (-2, 0), (-2, 3). Find the CoM of the house using additivity of moments by computing the moment of the rectangular base and the moment of the triangular roof separately.
1. && Calculate the mass $m$ of the figure by calculating the areas of the rectangle and triangle separately. 
    - Here: $$ \begin{align*}m &= m_{r} + m_{t} \\ &= \rho A_{r} + \rho A_{t} \\ &= \rho(4)(3) + \rho\left(\frac{1}{2}\right)(4)(2)  \\ &= 16\rho \end{align*}$$
2. !! By symmetry, note that $\bar{x}_{r} = 0$, and $\bar{y}_{r} = \frac{3}{2}$.
3. && Find $M_{xr}$ and $M_{yr}$ by the moment relation. 
    - Here: $$\begin{align*} \bar{x}_{r} &= \frac{M_{yr}}{m_{r}} \quad ⨠ ⨠ \quad M_{yr} = 0 \\ \bar{y}_{r} &= \frac{M_{xr}}{m_{r}} \quad ⨠ ⨠ \quad M_{xr} = 12\rho\left(\frac{3}{2}\right) = 18\rho \end{align*}$$
 4. &&& Find $\bar{x}_{t}$ and $\bar{y}_{t}$ by averaging out the $x$ and $y$ coordinates, respectively.
     - Here: $$\begin{align*}\bar{x}_{t}  &= \frac{-2+0+2}{3} = 0 \\ \bar{y}_{t} &= \frac{3+3+5}{3} = \frac{11}{3} \end{align*}$$
  5. && Find $M_{xt}$ and $M_{yt}$ by the moment relation. 
      - Here: $$\begin{align*} \bar{x}_{t} &= \frac{M_{yt}}{m_{t}} \quad ⨠ ⨠ \quad M_{yt} = 0 \\ \bar{y}_{t} &= \frac{M_{xt}}{m_{t}} \quad ⨠ ⨠ \quad M_{xr} = 4\rho\left(\frac{11}{3}\right) = \frac{44}{3}\rho \end{align*}$$
 6. && Additivity of moments to find $M_{x}$ and $M_{y}$. 
     - Here: $$\begin{align*} M_{x} &= \frac{44}{3}\rho + 18\rho = \frac{98}{3}\rho \\ M_{y} &= 0 + 0 = 0 \end{align*}$$
  7. & Compute $(\bar{x}, \bar{y})$. 
      - Here: $$\begin{align*}(\bar{x},\bar{y}) &= \left(\frac{M_{y}}{m}, \frac{M_{x}}{m}\right) \\ &= \left(0, \frac{\frac{98}{3}\rho}{16\rho}\right) \\ &= \left(0, \frac{49}{24}\right)\end{align*}$$

#### 03 - CoM of region between curves
Find the CoM of the region between the graph of $y = e^{x}$ and the graph $y = 1$ over $x \in [0, 1]$.

**Solution**
1. && Compute mass of the region 
    - Here: $$\begin{align*}m &= \rho\int_{0}^{1}\left(e^{x}-1\right)dx \\ &= \rho\left.\left[e^{x}-x\right]\right|^{1}_{0} \\&= \rho(e-2)\end{align*}$$
2. & Write formula for $M_{x}$. 
    - Here: $$M_{x} = \rho \int_{a}^{b}\frac{1}{2}\left(f(x)^{2}-g(x)^{2}\right)dx$$
3. && Compute $M_{x}$. 
    - Here: $$\begin{align*}M_{x} &= \frac{\rho}{2} \int_{0}^{1}e^{2x}-1dx \\  
    &= \frac{\rho}{2}\left.\left[\frac{e^{2x}}{2}-x\right]\right|^{1}_{0} \\ &= \frac{\rho}{2}\left[\frac{e^{2}}{2}-1-\frac{1}{2}\right] \\ &= \rho \left(\frac{e^{2}-3}{4}\right)\end{align*}$$
4. & Write formula for $M_{y}$. 
    - Here: $$M_{y} = \rho\int_{a}^{b}x\left(f(x)-g(x)\right)dx$$
5. && Compute $M_{y}$. 
    - Here: $$\begin{align*} M_{y} &= \rho \int_{0}^{1}x\left(e^{x}-1\right)dx \\ &= \rho \int_{0}^{1}xe^{x}-xdx \\ &= \rho\left.\left[xe^{x}-e^{x}-\frac{x^{2}}{2}\right]\right|_{0}^{1} \\ &= \frac{\rho}{2}\end{align*}$$
6. & Compute $(\bar{x}, \bar{y})$. 
    - Here: $$\begin{align*}(\bar{x}, \bar{y}) &= \left(\frac{M_{y}}{m}, \frac{M_{x}}{m}\right) \\ &= \left(\frac{\frac{\rho}{2}}{\rho(e-2)},\frac{\rho\left(\frac{e^{2}-3}{4}\right)}{\rho(e-2)}\right) \\ &= \left(\frac{1}{e-2}, \frac{e^{2}-3}{4(e-2)}\right)
 \end{align*}$$

#### 05 - Fluid force on various plates
For each of the plates shown, (a)-(i), set up an integral to compute the fluid force on one face of the plate which is submerged in water.

**Solution**
**(a)**
1. && Write down the formula to find the fluid force on a submerged surface.
    - Here: $$F = \rho g\int_{a}^{b}yw(y)dy$$
2. & Identify the line $y = 0$.
    - In this case, we can set $y = 0$ to the top of the plate, which is the same as the water line.
3. && Identify $w(y)$.
    - At $y = 0$, $w(y) = 3$.
    - At $y = 4, w(y) = 0$.
    - Using these points, the function $w(y)$ is the line $w(y) = -\frac{3}{4}y+3$.
4. & Identify bounds.
    - Shallowest point: $y = 0$.
    - Deepest point: $y = 4$.
    - $[a, b] = [0, 4]$.
5. && Set up integral. $$F = \rho g\int_{0}^{4}y\left(3-\frac{3}{4}y\right)dy$$

**(b)**
1. & Identify line $y = 0$.
     - Set $y = 0$ as the top of the plate, so the water line is at $y = -2$.
     - To adjust for our formula, the $y$ becomes $y + 2$.
2. && Identify $w(y)$.
    - At $y = 0$, $w(y) = 0$.
    - At $y = 3, w(y) = 2$.
    - Using these points, the function $w(y)$ is the line $w(y) = \frac{2}{3}y$.
3. & Identify bounds.
    - Shallowest point: $y = 0$.
    - Deepest point: $y = 3$.
    - $[a, b] = [0, 3]$.
4. && Set up integral. $$F = \rho g \int_{0}^{3}(y+2)\left(\frac{2}{3}y\right)dy$$

**(c)**
1. & Identify line $y = 0$.
    - Set $y = 0$ as the top of the plate, so the water line is at $y = 1$.
    - To adjust for our formula, the $y$ becomes $y - 1$.
2. && Identify $w(y)$.
    - At $y = 0$, $w(y) = 4$.
    - At $y = 5$, $w(y) = 0$.
    - Using these points, the function $w(y)$ is the line $w(y) = -\frac{4}{5}y+4$.
3. & Identify bounds. 
    - Shallowest point: $y = 1$.
    - Deepest point: $y = 5$.
    - $[a, b] = [1, 5]$.
4. && Set up integral. $$F = \rho g\int_{1}^{5}(y-1)\left(4-\frac{4}{5}y\right)dy$$

**(d)**
1. & Identify line $y = 0$.
    - Set $y = 0$ as the top of the plate, so the water line is at $y = -1$.
    - To adjust for our formula, the $y$ becomes $y + 1$.
2. && Identify $w(y)$.
    - At $y = 0$, $w(y) = 4$.
    - At $y = 3$, $w(y) = 5$.
    - Using these points, the function $w(y)$ is the line $w(y) = 4+\frac{y}{3}$.
3. & Identify bounds.
    - Shallowest point: $y = 0$.
    - Deepest point: $y = 3$.
    - $[a, b] = [0, 3]$
4. && Set up integral.
    - Here: $$F = \rho g \int_{0}^{3}(y+1)\left(4+\frac{y}{3}\right)dy$$

**(e)**
1. & Identify line $y = 0$.
    - Set $y = 0$ as the top of the plate, so the water line is at $y = 1$.
    - To adjust for our formula, the $y$ becomes $y - 1$.
2. && Identify $w(y)$.
    - At $y = 0$, $w(y) = 5$,
    - At $y = 3$, $w(y) = 4$.
    - Using these points, the function $w(y)$ is the line $w(y) = 5 - \frac{y}{3}$.
3. & Identify bounds.
    - Shallowest point: $y = 1$.
    - Deepest point: $y =3$.
    - $[a, b] = [1, 3]$.
4. && Set up integral.
    - Here: $$F = \rho g\int_{1}^{3}(y-1)\left(5-\frac{y}{3}\right)dy$$

**(f)**
1. & Identify line $y = 0$.
    - Set $y = 0$ as the water level.
2. &&& Identify $w(y)$.
    - The submerged portion of the plate can be split into two portions: a square and a triangle.
    - The square has a constant width $w(y) = 2$.
    - The triangle starts at $y = 2$.
        - At $y = 2$, $w(y) = 2$.
        - At $y = 3$, $w(y) = 0$.
        - Using these two points, the function $w(y)$ is the line $w(y) = 2- \frac{2}{3}(x-2)$.
3. && Identify bounds.
    - Square:
        - Shallowest point: $y = 0$.
        - Deepest point: $y = 2$.
        - $\left[a_{square},b_{square}\right] = [0, 2]$
    - Triangle: 
        - Shallowest point: $y = 2$.
        - Deepest point: $y = 5$.
        - $\left[a_{triangle},b_{triangle}\right] = [2, 5]$.
4. && Set up integral.
    - Here: $$F = \rho g\left(\int_{0}^{2}2ydy+\int_{2}^{5}y\left(2-\frac{2}{3}(x-2)\right)dy\right)$$

**(g)**
1. & Identify line $y = 0$.
    - Set $y = 0$ as the center of the circle, so the water line is at $y = -3$.
    - To adjust for our formula, the $y$ becomes $y + 3$.
2. && Identify $w(y)$.
     - We know the formula for a circle of radius 2 is $x^{2} + y^{2} = 4$, so $x = \pm\sqrt{4-y^{2}}$.
     - Note that at $y = 0$, $\sqrt{4-y^{2}} = 2$, which is half of what we want. 
     - So, $w(y) = 2\sqrt{4-y^{2}}$.
3. & Identify bounds:
    - Shallowest point: $y = -2$.
    - Deepest point: $y = 2$.
    - $[a, b] = [-2, 2]$.
4. && Set up integral.
    - Here: $$F = \rho g \int_{-2}^{2}(y+3)\left(2\sqrt{4-y^{2}}\right)dy$$

**(h)**
1. & Identify line $y = 0$.
    - Set $y = 0$ as the center of the circle, which is the water line.
2. && Identify $w(y)$.
    - We know the formula for a circle of radius $3$ is $x = \pm \sqrt{9-y^{2}}$.
    - So, $w(y) = 2\sqrt{9-y^{2}}$.
3. & Identify bounds:
    - Shallowest point: $y = 0$.
    - Deepest point: $y = 3$.
    - $[a, b] = [0, 3]$
4. && Set up integral. 
    - Here: $$F = \rho g \int_{0}^{3}y\left(2\sqrt{9-x^{2}}\right)dy$$

**(i)**
1. & Identify line $y = 0$.
    - Set $y = 0$ as the center of the circle, so the water line is at $y = -2$.
    - To adjust for our formula, our $y$ becomes $y + 2$
2. && Identify $w(y)$.
    - We know the formula for a circle of radius 4 is $x = \pm \sqrt{16-y^{2}}$.
    - So, $w(y) = 2\sqrt{16-y^{2}}$.
3. & Identify bounds:
    - Shallowest point: $y = -2$.
    - Deepest point: $y = 0$.
    - $[a, b] = [-2, 0]$.
4. && Set up integral. 
    - Here: $$F = \rho g \int_{-2}^{0}(y+2)\left(2\sqrt{16-y^{2}}\right)dy$$


#### 07 - CoM from Simpson's
Use Simpson's rule (with 6 subintervals) to estimate the CoM of the region. You can use a calculator for your arithmetic.
1. & Write down formula for mass. 
    - Here: $$m = \rho \int_{a}^{b}f(x)dx$$
2. & Write down formula for Simpson's Rule. 
    - Here: $$\int_{a}^{b}f(x)dx \approx S_{n} = \frac{\Delta x}{3}\left[f(x_{0})+4f(x_{1}) + 2f(x_{2}) + \cdots + f(x_{n})\right]$$
3. && Evaluate $S_{6}$ to approximate $m$.
    - $\Delta x = \frac{b-a}{n} = \frac{8-2}{6} = 1$.
    $$S_{6} = \frac{1}{3}\left[0 + 4(1)+2(3)+4(3)+2(2)+4(3)+0\right] = \frac{38}{3}$$
    Thus, $m = \rho \int_{2}^{8}f(x)dx \approx \frac{38}{3}\rho$.

4. & Write down formula for $M_{x}$. 
    - Here: $$M_{x} = \frac{\rho}{2}\int_{a}^{b} \left[f(x)\right]^{2}dx$$
5. && Evaluate $S_{6}$ to approximate $\int_{2}^{8}\left[f(x)\right]^{2}dx$ and $M_{x}$.
    - Here: $$\begin{align*}S_{6} &= \frac{1}{3}\left[0^{2} + 4\left(1^{2}\right) + 2\left(3^{2}\right)+4\left(3^{2}\right) + 2\left(2^{2}\right)+4\left(3^{2}\right) + 0^{2} = 34\right] \\ M_{x} &= \frac{\rho}{2}\int_{2}^{8}\left[f(x)\right]^{2}dx \approx 17\rho \end{align*}$$
 6. & Write down formula for $M_{y}$. 
     - Here: $$M_{y} = \rho\int_{a}^{b}xf(x)dx$$
 7. && Evaluate $S_{6}$ to approximate $\int_{2}^{8}xf(x)dx$ 
     - Here: $$\begin{align*}
 S_{6} &= \frac{1}{3}\left[2(0) + 4(3)(1)+2(4)(3)+4(5)(3)+2(6)(2)+4(7)(3)+8(0)\right] = 68 \\
 M_{y} &= \rho\int_{a}^{b}xf(x)dx \approx 68\rho
  \end{align*}$$
  9. & Compute $(\bar{x}, \bar{y})$. 
      - Here: $$\begin{align*}  (\bar{x}, \bar{y}) &= \left(\frac{M_{y}}{m}, \frac{M_{x}}{m}\right) \\ &= \left(\frac{68\rho}{\frac{38}{3}\rho}, \frac{17\rho}{\frac{38}{3}\rho}\right) \\ &= \left(\frac{102}{19}, \frac{51}{38}\right) \end{align*}$$


