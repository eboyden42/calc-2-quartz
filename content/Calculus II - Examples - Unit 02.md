## Arc length
#### 12 - Arc length of chain, via position
A hanging chain describes a **catenary** shape. (‘Catenary’ is to hyperbolic trig as ‘sinusoid’ is to normal trig.) The graph of the hyperbolic cosine is a catenary: $$y = f(x) = \cosh x$$
![250](Pasted%20image%2020240915165034.png)

Let us compute the arc length of this catenary on the portion from $x=0$ to $x=a$.

**Solution**
1. !! Arc-length formula.
    - Give arc length $s(a)$, a function of $a\geq 0$: $$s(a)=\int_0^a \sqrt{1+\big(f'\big)^2}\,dx$$
2. & Compute $f'(x)$.
    - Hyperbolic trig derivative: $$\frac{d}{dx}\cosh(x)=\sinh(x)$$
3. & Plug into formula.
    - Arc length: $$s(a)=\int_0^a \sqrt{1+\sinh^2(x)}\,dx$$
4. ! Hyperbolic trig identity.
    - Fundamental identity: $$\cosh^2 x - \sinh^2 x = 1$$
    - Rearrange: $$1+\sinh^2x=\cosh^2x$$
5. && Plug into formula and compute.
    - Arc length: $$\int_0^a \sqrt{1+\sinh^2(x)}\,dx \qquad ⨠⨠ \qquad \int_0^a \sqrt{\cosh^2x}\,dx\qquad ⨠⨠ \qquad \int_0^a\cosh x\,dx$$
    - Compute integral: $$\int_0^a\cosh x\,dx = \sinh a$$
    - !!! The arc length of a catenary curve matches the area under the catenary curve!

#### 13 - Arc length, line segment
Find the arc length of the *straight line* given by the formula $y=3x+1$ over $x\in[0,3]$.

Check your answer using the Pythagorean Theorem.

## Surface areas of revolutions - thin bands
#### 14 - Surface area of a sphere
Using the fact that a sphere is given by revolving a semicircle, verify the formula $S=4\pi r^2$ for the surface area of a sphere.

**Solution**
1. && Sphere as surface of revolution.
    - Sphere of radius $r$ given by revolving upper semicircle.
    - Upper semicircle: $$x^2+y^2=r^2,\qquad y\geq 0$$
    - Upper semicircle as function of $x$: $$y=f(x)=\sqrt{r^2-x^2},\qquad x\in[-r,r]$$
2. && Surface area formula.
    - Bounds are $x=-r$ and $x=+r$.
    - Function is $f(x)=\sqrt{r^2-x^2}$
    - Plug data into formula: $$S=\int_{-r}^{+r}2\pi\sqrt{r^2-x^2}\sqrt{1+\big(f'\big)^2}\,dx$$
3. & Compute $\big(f'\big)^2$.
    - Power rule and chain rule: $$f'(x)=\frac{1}{2}(r^2-x^2)^{-1/2}(-2x)$$
    - Algebra: $$\qquad ⨠⨠ \qquad -x(r^2-x^2)^{-1/2}$$
    - Squaring: $$\big(f'\big)^2=\frac{x^2}{r^2-x^2}$$
4. && Compute integrand.
    - Compute $1+\big(f'\big)^2$: $$\begin{gather*}1=\frac{r^2-x^2}{r^2-x^2}\\ 1+\big(f'\big)^2\qquad ⨠⨠ \qquad \frac{r^2-x^2}{r^2-x^2}+\frac{x^2}{r^2-x^2}\qquad ⨠⨠ \qquad \frac{r^2}{r^2-x^2}\end{gather*}$$
    - Integrand factors become: $$\sqrt{r^2-x^2}\sqrt{1+\big(f'\big)^2}\qquad ⨠⨠ \qquad \sqrt{r^2-x^2}\sqrt{\frac{r^2}{r^2-x^2}}\qquad ⨠⨠ \qquad r$$
5. && Compute integral.
    - Surface area again: $$\begin{align*}S&= \int_{-r}^{+r}2\pi r\,dx\\\\ &=2\pi r x\Big|_{-r}^{+r}= 2\pi rr-2\pi r(-r)\\&= 4\pi r^2\end{align*}$$
    - This is the desired surface area formula $S=4\pi r^2$.

## Hydrostatic force

#### 15 - Fluid force on a triangular plate
Find the total force on the submerged *vertical* plate with the following shape: Equilateral triangle, sides $2\mathrm{m}$, top vertex at the surface, liquid is oil with density $\rho=900\mathrm{kg/m^3}$.
![200](Pasted%20image%2020240924220205.png)

**Solution**
1. & Establish coordinate system: height $y$ increases going *down*.
2. &&& Compute width function $w(y)$.
    - Drop a perpendicular from top vertex to the base.
    - Pythagorean Theorem: vertical height is $\sqrt{3}$.
    - Similar triangles: ratio $w(y)/y$ must equal ratio $2/\sqrt{3}$.
    - Solve for $w(y)$: $$w(y)=2y/\sqrt{3}$$
3. & Write integral using width function.
    - Bounds: shallowest: $y=0$; deepest: $y=\sqrt{3}$.
    - Integral formula: $$F=\rho g\int_0^{\sqrt{3}}y\, w(y)\,dy=900\cdot9.8\int_0^{\sqrt{3}}y\cdot 2y/\sqrt{3}\,dy$$
4. && Compute integral.
    - Simplify constants: $$900\cdot9.8\cdot\frac{2}{\sqrt{3}}\approx 10184.5$$
    - Compute integral without constants: $$\int_0^\sqrt{3}y^2\,dy=\frac{y^3}{3}\Big|_0^\sqrt{3}=\sqrt{3}$$
    - Combine for the final answer: $10184.5\cdot\sqrt{3}=17640$

#### 16 - Weight of water on a dam
Find the total hydrostatic force on an angled dam with the following geometric description: Tilted trapezoid. Base $=2,000\mathrm{m}$, Top $=3,000\mathrm{m}$, and *vertical* height $185\mathrm{m}$. The base is tilted at an angle of $\theta=55^\circ$.

![200](Pasted%20image%2020240925082231.png)

**Solution**
1. & Establish coordinate system: height $y$ increases going *down*.
2. !! Find similar triangles to describe width function.
    - Draw line from lower corner to upper edge, perpendicular to upper and lower edges.
    - Identify $b(y)$ as the distance from drawn line to outer edge of the trapezoid.
    - So $b(y)$ ranges from $0$ at the bottom ($y=185$) to $500$ at the top $y=0$.
    - Similar triangles yields equal ratios *similarity equation*: $$\frac{b(y)}{500}=\frac{185-y}{185}$$
    - Width function is $$w(y)=2,000+2b(y)$$
3. && Simplify width function.
    - Solve *similarity equation* $$\frac{b(y)}{500}=\frac{185-y}{185}\qquad ⨠⨠ \qquad b(y)=500\left(1-\frac{y}{185}\right)$$
    - Plug result into width function: $$w(y)=2,000+1,000\left(1-\frac{y}{185}\right)$$
    - Simplify: $$w(y)=3,000+\tfrac{1,000}{185}y$$
4. & Incorporate angle of incline in strip thickness.
    - Infinitesimal thickness element is $dz=\csc 55^\circ\,dy$.
5. && Calculate total force using integral formula.
    - Plug data into formula: $$F=\rho g\int_a^b y\,w\,dz=\rho g\int_0^{185} y\,\left(3,000-\tfrac{1,000}{185}y\right)\csc 55^\circ\,dy$$
    - Simplify: $$\qquad ⨠⨠ \qquad 3000\rho g \csc 55^\circ \int_0^{185}y\,dy-\tfrac{1000}{185}\rho g \csc 55^\circ \int_0^{185}y^2\,dy$$
    - Plug in constants $\rho=1000\mathrm{kg/m^3}$ and $g=9.8\mathrm{m/s^2}$ if the final number is desired.

## Moments and center of mass
#### 17 - CoM of a parabolic plate
Find the CoM of the region depicted:
![200](Pasted%20image%2020240928082458.png)

**Solution**
1. & Compute the total mass.
    - Area under the curve with density factor $\rho$: $$M=\int_0^2\rho\, x^2\,dx\quad ⨠⨠ \quad \rho\,\left.\frac{x^3}{3}\right|_0^2\quad ⨠⨠ \quad \frac{8\rho }{3}$$
2. && Compute $M_y$.
    - Formula: $$M_y=\int_a^b \rho\,x\,dA$$
    - Interpret and calculate: $$\begin{gather*}M_y=\int_0^2 \rho\,xf(x)\,dx\quad ⨠⨠ \quad \rho\int_0^2x^3\,dx\\\\ ⨠⨠ \quad 4\rho=M_y\end{gather*}$$
3. &&& Compute $M_x$.
    - Formula: $$M_x=\int_c^d \rho\,y\,dA$$
    - Width of horizontal strips between the curves: $$w(y)=2-\sqrt{y}$$
    - Interpret $dA$: $$dA=(2-\sqrt{y})\,dy$$
    - Plug data into integral: $$M_x=\int_c^d \rho\,y\,dA\quad ⨠⨠ \quad \int_0^4 \rho\,y(2-\sqrt{y})\,dy$$
    - Calculate integral: $$\begin{gather*}\int_0^4 \rho\,y(2-\sqrt{y})\,dy\quad ⨠⨠ \quad \int_0^4 \rho\,2y\,dy-\int_0^4 \rho\,y^{3/2}\,dy\\\\ ⨠⨠ \quad \frac{16\rho}{5}=M_x\end{gather*}$$
4. & Compute CoM coordinates from moments.
    - CoM formulas: $$\bar{x}=\frac{M_y}{M},\qquad \bar{y}=\frac{M_x}{M}$$
    - Insert data: $$\begin{align*}\bar{x}&= \frac{4\rho}{8\rho/3}\quad ⨠⨠ \quad \frac{3}{2}\\\\ \bar{y}&= \frac{16\rho/5}{8\rho/3}\quad ⨠⨠ \quad \frac{6}{5}\end{align*}$$
    - Therefore CoM is located at $(\bar{x},\bar{y})=(\frac{3}{2},\frac{6}{5})$.

#### 18 - Computing CoM using only vertical strips
Find the CoM of the region: 
![300](Pasted%20image%2020240929093221.png)

**Solution**
1. & Compute the total mass $M$.
    - Area under the curve times density $\rho$: $$\int_0^{\pi/2}\rho\,\cos x\,dx=\rho\sin x\Big|_0^{\pi/2}=\rho$$
2. && Compute $M_y$ using vertical strips.
    - Plug $f(x)=\cos x$ into formula: $$M_y=\int_a^{b}\rho\,x\,f(x)\,dx\quad ⨠⨠ \quad \int_0^{\pi/2}\rho\,x\cos x\,dx$$
    - Integration by parts.
        - Set $u=x$, $v'=\cos x$; then $u'=1$, $v=\sin x$.
        - IBP formula: $$\int_a^b uv'\,dx=uv\Big|_a^b-\int_a^b u'v\,dx$$
        - Plug in data: $$\int_0^{\pi/2}\rho\,x\cos x\,dx=\rho\,x\sin x\Big|_0^{\pi/2}-\rho\,\int_0^{\pi/2}\sin x\,dx$$
        - Evaluate: $$\qquad ⨠⨠ \qquad \frac{\pi\rho\,}{2}\cdot 1-\rho\,(-\cos\frac{\pi}{2}--\cos 0)=\rho\,\left(\frac{\pi}{2}-1\right)$$
3. &&& Compute $M_x$ *also* using vertical strips.
    - Plug $f_2(x)=f(x)=\cos x$ and $f_1(x)=0$ into formula: $$M_x=\int_0^{\pi/2}\rho\,\tfrac{1}{2}f_2^2\,dx\quad ⨠⨠ \quad \int_0^{\pi/2}\rho\,\tfrac{1}{2}\cos^2x\,dx$$
    - Integration by ‘power to frequency conversion’:
        - Use $\cos^2x=\frac{1}{2}(1+\cos 2x)$: $$\int_0^{\pi/2}\rho\,\tfrac{1}{2}\cos^2x\,dx=\frac{\rho}{4}\int_0^{\pi/2}(1+\cos 2x)\,dx$$
        - Integrate: $$\qquad ⨠⨠ \qquad \frac{\rho}{4}x\Big|_0^{\pi/2}+\left.\frac{\rho\sin 2x}{8}\right|_0^{\pi/2}=\frac{\pi\rho}{8}$$
4. & Compute CoM.
    - CoM via moment formulas: $$\bar{x}=\frac{M_y}{M},\qquad \bar{y}=\frac{M_x}{M}$$
    - Plug in data: $$\bar{x}=\frac{\rho(\pi/2-1)}{\rho}\quad ⨠⨠ \quad \frac{\pi}{2}-1$$
    - Plug in data: $$\bar{y}=\frac{\pi\rho/8}{\rho}\quad ⨠⨠ \quad \frac{\pi}{8}$$
    - CoM is given by $(\bar{x},\bar{y})=\left(\frac{\pi}{2}-1,\frac{\pi}{8}\right)$.

#### 19 - CoM of region between line and parabola
Compute the CoM of the region below $y=x$ and above $y=x^2$ with $x\in[0,1]$.

**Solution**
1. & Name the functions: $f_1(x)=x^2$ (lower) and $f_2(x)=x$ (upper) over $x\in[0,1]$.
2. & Compute the mass $M$.
    - Area between curves times density: $$M=\int_0^1\rho\,(f_2-f_1)\,dx\quad ⨠⨠ \quad \rho\int_0^1 x-x^2\,dx=\frac{\rho}{6}$$
3. && Compute $M_y$ using vertical strips.
    - Plug into formula: $$M_y=\int_0^1\rho\,x\,(f_2-f_1)\,dx=\rho\int_0^1x(x-x^2)\,dx=\frac{\rho}{12}$$
4. && Compute $M_x$ also using vertical strips.
    - Plug into formula: $$M_x=\int_0^1\rho\,\tfrac{1}{2}\left(f_2^2-f_1^2\right)\,dx\quad ⨠⨠ \quad \rho\int_0^1\tfrac{1}{2}(x^2-x^4)\,dx=\frac{2\rho}{30}$$
5. & Compute CoM.
    - Using CoM via moment formulas: $$\begin{align*}\bar{x}&= \frac{\rho/12}{\rho/6}\quad ⨠⨠ \quad \frac{1}{2} \\\\ \bar{y}&= \frac{2\rho/30}{\rho/6}\quad ⨠⨠ \quad \frac{2}{5}\end{align*}$$
    - CoM is given by $(\bar{x},\bar{y})=\left(\frac{1}{2},\frac{2}{5}\right)$.

#### 20 - Center of mass using moments and symmetry
Find the center of mass of the region below.
![200](Pasted%20image%2020240929220228.png)

**Solution**
1. & Symmetry: CoM on $y$-axis.
    - Because the region is symmetric in the $y$-axis, the CoM must lie on that axis.
    - Therefore $\bar{x}=0$.
2. !! Additivity of moments.
    - Write $M_x$ for the total $x$-moment (distance measured to the $x$-axis from above).
    - Write $M_x^{\mathrm{tri}}$ and $M_x^{\mathrm{circ}}$ for the $x$-moments of the triangle and circle.
    - *Additivity of moments* equation: $$M_x = M_x^{\mathrm{tri}} + M_x^{\mathrm{circ}}$$
3. &&& Find moment of the circle $M_x^{\mathrm{circ}}$.
    - By symmetry we know $\bar{x}^{\mathrm{circ}}=0$.
    - By symmetry we know $\bar{y}^{\mathrm{circ}}=5$.
    - Area of circle with $r=2$ is $A=4\pi$, so total mass is $M=4\pi\rho$.
    - Centroid-from-moments equation: $$\bar{y}^{\mathrm{circ}}=\frac{M_x^{\mathrm{circ}}}{M}$$
    - !! Solve the equation for $M_x^{\mathrm{circ}}$.
        - Solve: $$\begin{gather*}\bar{y}^{\mathrm{circ}}=\frac{M_x^{\mathrm{circ}}}{M}\quad ⨠⨠ \quad 5=\frac{M_x^{\mathrm{circ}}}{4\pi\rho}\\\\ ⨠⨠ \quad M_x^{\mathrm{circ}}=20\pi\rho\end{gather*}$$
4. &&& Find moment of the triangle $M_x^{\mathrm{tri}}$ using integral formula
    - Similar triangles: 
      ![200](Pasted%20image%2020240930082013.png)
    - Similarity equation: $$\frac{\ell(y)}{h-y}=\frac{b}{h}\quad ⨠⨠ \quad \ell(y)=b-\frac{b}{h}y$$
    - Integral formula: $$M_x^{\mathrm{tri}}=\rho\int_0^h y\ell(y)\,dy=\rho\int_0^h y\,\left(b-\frac{b}{h}y\right)\,dy$$
    - Perform integral: $$\rho\int_0^h y\,\left(b-\frac{b}{h}y\right)\,dy\quad ⨠⨠ \quad \rho\left.\left(\frac{by^2}{2}-\frac{by^3}{3h}\right)\right|_0^h=\frac{\rho bh^2}{6}$$
    - Conclude: $$M_x^{\mathrm{tri}}=\frac{\rho bh^2}{6}=\frac{\rho 4\cdot 3^2}{6}=6\rho$$
5. && Apply additivity.
    - Additivity formula: $$M_x = M_x^{\mathrm{tri}} + M_x^{\mathrm{circ}} = \rho(20\pi+6)$$
6. & Total mass of region.
    - Area of circle is $4\pi$.
    - Area of triangle is $\frac{1}{2}\cdot 4\cdot 3=6$.
    - Thus $M=\rho A=\rho(4\pi+6)$.
7. & Compute center of mass $\bar{y}$ from total $M_x$ and total $M$.
    - We have $M_x=\rho(20\pi+6)$ and $M=\rho(4\pi+6)$.
    - Plug into formula: $$\bar{y}=\frac{M_x}{M}=\frac{\rho(20\pi+6)}{\rho(4\pi+6)}\approx 3.71$$
8. & Final answer is $(\bar{x},\bar{y})=(0,3.71)$.

#### 21 - Center of mass - two part region
Find the center of mass of the region which combines a rectangle and triangle (as in the figure) *by computing separate moments*. What are those separate moments? Assume the mass density is $\rho=1$.
![200](Pasted%20image%2020241001223552.png)

**Solution**
1. !! By symmetry, the center of mass of the rectangle is located at $(-1,2)$.
    - Thus $\bar{x}^{\text{rect}}=-1$ and $\bar{y}^{\text{rect}}=2$.
2. && Find moments of the rectangle.
    - Total mass of rectangle $=M^\text{rect}=\rho\times\text{area}=1\cdot 8=8$.
    - Apply moment relation: $$\begin{align*}\bar{x}^{\text{rect}}=\frac{M_y^\text{rect}}{M^\text{rect}}\qquad &⨠⨠ \qquad M_y^\text{rect}=-8\\\\ \bar{y}^{\text{rect}}=\frac{M_x^\text{rect}}{M^\text{rect}}\qquad &⨠⨠ \qquad M_x^\text{rect}=16\end{align*}$$
3. &&& Find moments of the triangle.
    - Area of vertical slice $=\left(4-\frac{4}{4}x\right)\,dx$.
    - Distance from $y$-axis $=x$.
    - Total $M_y^\text{tri}$ integral: $$\begin{align*}M_y^\text{tri} &= \int_0^4\rho x\left(4-\frac{4}{4}x\right)\,dx\\\\&= \int_0^4 1\cdot(4-x)x\,dx=\frac{32}{3}\end{align*}$$
    - Total $M_x^\text{tri}$ integral: $$\begin{align*}M_x^\text{tri} &= \int_0^4\rho\frac{1}{2}f(x)^2\,dx=\int_0^4\rho \frac{1}{2}\left(4-\frac{4}{4}x\right)^2\,dx\\\\ &= 1\cdot\frac{1}{2}\int_0^4(16-8x+x^2)\,dx=\frac{32}{3} \end{align*}$$
4. &&& Add up total moments.
    - General formulas: $M_x=M_x^\text{tri}+M_x^\text{rect}$ and $M_y=M_y^\text{tri}+M_y^\text{rect}$
    - Plug in data: $M_x=\frac{32}{3}+16=\frac{80}{3}$ and $M_y=\frac{32}{3}-8=\frac{8}{3}$
5. &&& Find center of mass from moments.
    - Total mass of triangle  $=M^\text{tri}=\rho\times\text{area}=1\cdot \frac{1}{2}\cdot 4\cdot 4=8$.
    - Total combined mass $=M=M^\text{tri}+M^\text{rect}=8+8=16$.
    - Apply moment relation: $$\begin{align*}\bar{x}=\frac{M_y}{M}= \frac{8/3}{16}=\frac{1}{6} \\\\ \bar{y}=\frac{M_x}{M}= \frac{80/3}{16}=\frac{5}{3} \end{align*}$$
    - Therefore, center of mass is $(\bar{x},\bar{y})=\left(\frac{1}{6},\frac{5}{3}\right)$.