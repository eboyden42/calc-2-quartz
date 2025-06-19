## Work performed
#### Pumping water from spherical tank
Calculate the work done pumping water out of a spherical tank of radius $R=5\,\mathrm{m}$.

**Solution**
1. & Divide the sphere of water into horizontal layers.
    ![400](Pasted%20image%2020240930223115.png)
    - Coordinate $y$ is $y=0$ at the center of the sphere.
2. & Work done pumping out water is constant across any single layer.
3. && Find formula for weight of a single layer.
    - Area of the layer at $y$ is $A(y)=\pi(5^2-y^2)$ because its radius is $r=\sqrt{5^2-y^2}$.
    - Volume of the layer at $y$ is then $\pi(5^2-y^2)\,dy$.
    - Weight of the layer is then $F(y)\,dy=g\cdot\rho\cdot\pi(5^2-y^2)\,dy$.
        - Plug in: $$g=9.8\tfrac{m}{s^2},\quad \rho=1000\tfrac{kg}{m^3}\qquad ⨠⨠ \qquad F(y)\,dy=\left(9800\tfrac{kg}{m^2s^2}\right)\pi(5^2-y^2)\,dy$$
4. & Find formula for vertical distance a given layer is lifted.
    - Layer at $y$ must be lifted by $5-y$ to the top of the tank.
5. & Work per layer is the product.
    - Product of weight times height lifted: $$\left(9800\tfrac{kg}{m^2s^2}\right)\pi(5^2-y^2)(5-y)\,dy$$
6. & Total work done is the integral.
    - Integrate over the layers: $$W=\int_{-5}^{+5}\left(9800\tfrac{kg}{m^2s^2}\right)\pi(5^2-y^2)(5-y)\,dy\quad \approx\quad 2.6\times 10^7\,\mathrm{J}$$
7. !! Supplement: what if the spigot sits $2\mathrm{m}$ above the tank?
    - Increase the height function from $5-y$ to $7-y$.
8. !! Supplement: what if the tank starts at just $3\mathrm{m}$ of water depth?
    - Integrate the water layers only: change bounds to $\int_{-5}^{-2}$.

#### Water pumped from a frustum
Find the work required to pump water out of the frustum in the figure. Assume the weight of water is $\rho=62.5\,\mathrm{lb/ft^3}$.
![200](Pasted%20image%2020241002081926.png)

**Solution**
1. &&& Find weight of a horizontal slice.
    - Coordinate $y=0$ at top, increasing downwards.
    - Use $r(y)$ for radius of cross-section circle.
    - Linear decrease in $r$ from $r(0)=6$ to $r(8)=3$: $$r(y)=6-\frac{3}{8}y$$
    - Area is $\pi r^2$: $$\text{Area}(y)=\pi\left(6-\tfrac{3}{8}y\right)^2$$
    - $\text{Weight}=\text{density}\times\text{area}\times\text{thickness}$: $$\text{weight of layer}=\rho \pi\left(6-\tfrac{3}{8}y\right)^2 \,dy$$
2. && Find work to pump out a horizontal layer.
    - Layer at $y$ is raised a distance of $y$.
    - Work to raise layer at $y$: $$\rho \pi y\left(6-\tfrac{3}{8}y\right)^2 \,dy$$
3. && Integrate over all layers.
    - Integrate from top to bottom of frustum: $$\begin{align*}\int_0^8 \rho \pi y\left(6-\tfrac{3}{8}y\right)^2 \,dy&= 528\pi\rho\\&=  528\pi\cdot 62.5\\&\approx  1.04\times 10^5\,\mathrm{ft\text{-}lb}\end{align*}$$
    - Final answer is $1.04\times 10^5\,\mathrm{ft\text{-}lb}$.

#### Raising a building
Find the work done to raise a cement columnar building of height $5\,\mathrm{m}$ and square base $2\,\mathrm{m}$ per side. Cement has a density of $1500\,\mathrm{kg/m^3}$.
![300](Pasted%20image%2020240930230044.png)

**Solution**
1. & Divide the building into horizontal layers.
    - Work done raising up the layers is constant for each layer.
2. && Find formula for weight of each layer.
    - Volume $=\text{area}\times\text{thickness}=4\,dy$
    - Mass $=\text{density}\times\text{volume}=1500\times 4\,dy=6000\,dy$
    - Weight of layer $=g\times\text{mass}=9.8\times 6000\,dy=58800\,dy$
3. & Find formula for work performed lifting one layer into place.
    - Work $=\text{weight}\times\text{distance lifted}=58800\times y\,dy$
4. & Find total work as integral over the layers.
    - Total work $=\int_0^5 58800y\,dy=735\,\mathrm{kJ}$

#### Raising a chain
An $80\,\mathrm{ft}$ chain is suspended from the top of a building. Suppose the chain has weight density $0.5\,\mathrm{lb/ft}$. What is the total work required to reel in the chain?

**Solution**
1. & Divide the chain into horizontal layers.
    - Each layer has vertical thickness $dy$.
    - Each layer has weight $0.5\,dy$ in $\mathrm{lb}$.
2. & Find formula for distance each layer is raised.
    - Each layer is raised from $y$ to $80\,\mathrm{ft}$, a distance of $(80-y)\,\mathrm{ft}$.
3. && Compute total work.
    - Work to raise each layer is weight times distance raised: $$\text{Work to raise layer}=(80-y)\cdot 0.5\,dy$$
    - Add the work over all layers: $$\int_0^{80}(80-y)\cdot 0.5\,dy=1600\,\mathrm{ft\text{-}lb}$$

#### Raising a leaky bucket
Suppose a bucket is hoisted by a cable up an $80\,\mathrm{ft}$ tower. The bucket is lifted at a constant rate of $2\,\mathrm{ft/sec}$ and is leaking water weight at a constant rate of $0.2\,\mathrm{lb/sec}$. The initial weight of water is $50\,\mathrm{lb}$. What is the total work performed against gravity in lifting the water? (Ignore the bucket itself and the cable.)

**Solution**
1. && Convert to static format.
    - Compute rate of water weight loss per unit of vertical height: $$\frac{\text{rate of leak}}{\text{rate of lift}}=\text{leaked weight per foot},\qquad \frac{0.2\,\mathrm{lb/sec}}{2\,\mathrm{ft/sec}}=0.1\,\mathrm{lb/ft}$$
    - Choose coordinate $y=0$ at base, $y=80$ at top.
    - Compute water weight at each height $y$: $$\text{water weight}=(50-0.1y)\,\mathrm{lb}$$
2. !! Work formula.
    - Total work is integral of force times infinitesimal distance: $$\text{work}=\int_a^b F(y)\,dy$$
3. && Integrate weight times $dy$.
    - Plug in weight as force: $$\text{work}=\int_0^{80}(50-0.1y)\,dy$$
    - Compute integral: $$\qquad ⨠⨠ \qquad 50y-0.05y^2\Big|_0^{80}=3680\,\mathrm{ft\text{-}lb}$$


## Improper integrals

#### Improper integral - infinite bound
Show that the improper integral $\displaystyle\int_2^\infty \frac{dx}{x^3}$ converges. What is its value?

**Solution**
1. & Replace infinity with a new symbol $R$.
    - Compute the integral: $$\int_2^R\frac{dx}{x^3}=-\frac{1}{2}x^{-2}\Bigg|_2^R=\frac{1}{8}-\frac{1}{2R^2}$$
2. & Take limit as $R\to\infty$.
    - Find limit: $$\lim_{R\to\infty}\frac{1}{8}-\frac{1}{2R^2}=\frac{1}{8}$$
3. & Apply definition of improper integral.
    - By definition: $$\int_2^\infty \frac{dx}{x^3}=\lim_{R\to\infty}\int_2^R \frac{dx}{x^3}=\frac{1}{8}$$
4. & Conclude that $\int_2^\infty\frac{dx}{x^3}$ converges and equals $\frac{1}{8}$.

#### Improper integral - infinite integrand
Show that the improper integral $\displaystyle\int_0^9 \frac{dx}{\sqrt{x}}$ converges. What is its value?

**Solution** 
1. & Replace the $0$ where $\frac{1}{\sqrt{x}}$ diverges with a new symbol $a$.
    - Compute the integral: $$\int_a^9\frac{dx}{\sqrt{x}}=\int_a^9 x^{-1/2}\,dx=2x^{+1/2}\Big|_a^9=6-2\sqrt{a}$$
2. & Take limit as $a\to 0^+$.
    - Find limit: $$\lim_{a\to 0^+}6-2\sqrt{a}=6$$
3. & Apply definition of improper integral.
    - By definition: $$\int_a^9\frac{dx}{\sqrt{x}}=\lim_{a\to 0^+}\int_a^9\frac{dx}{\sqrt{x}}=6$$
4. & Conclude that $\int_0^9\frac{dx}{\sqrt{x}}$ converges to $6$.

#### Example - Improper integral - infinity inside the interval
Does the integral $\displaystyle\int_{-1}^{+1}\frac{1}{x}\,dx$ converge or diverge?

**Solution** 
It is *tempting* to compute the integral *incorrectly*, like this: $$\int_{-1}^{+1}\frac{1}{x}\,dx=\ln|x|\Big|_{-1}^{+1}=\ln|2|-\ln|-2|=0$$
But this is wrong. There is an infinite integrand at $x=0$. We must instead break it into parts.
1. !! Identify infinite integrand at $x=0$.
    - Integral becomes: $$\int_{-1}^{+1}\frac{1}{x}\,dx=\int_{-1}^{0}\frac{1}{x}\,dx + \int_{0}^{+1}\frac{1}{x}\,dx$$
2. & Interpret improper integrals.
    - Limit interpretations: $$\lim_{R\to0^-}\int_{-1}^{R}\frac{1}{x}\,dx + \lim_{R\to0^+}\int_{R}^{+1}\frac{1}{x}\,dx$$
3. & Compute integrals.
    - Using $\int\frac{1}{x}\,dx=\ln|x|+C$: $$\int_{-1}^R\frac{1}{x}\,dx=\ln|R| - \ln|-1|=\ln|R|,\qquad \int_R^{+1}\frac{1}{x}\,dx=\ln|1|-\ln|R|=-\ln R$$
4. & Take limits.
    - We have: $$\lim_{R\to0^-}\ln|R|=-\infty,\qquad\lim_{R\to0^+}-\ln R=+\infty$$
    - *Neither* limit is finite. For $\int_{-1}^{+1}\frac{1}{x}\,dx$ to exist we’d need *both* of these limits to be finite.

#### Comparison to $p$-integrals
Determine whether the integral converges:
- (a) $\displaystyle\int_2^\infty\frac{x^3}{x^4-1}\,dx$
- (b) $\displaystyle\int_1^\infty\frac{1}{x^2+x+1}\,dx$

**Solution** 
(a)
1. !! Integrand tends toward $1/x$ for large $x$.
    - Consider large $x$ values: $$\frac{x^3}{x^4-1}\quad\longrightarrow\quad\frac{x^3}{x^4}\quad\text{for}\quad x\to\infty,\qquad\text{and}\quad \frac{x^3}{x^4}=\frac{1}{x}$$
2. & Try comparison to $1/x$.
    - Comparison attempt: $$\frac{x^3}{x^4-1}\overset{?}{>}\frac{1}{x}$$
    - Validate. Notice $x^4-1>0$ and $x>0$ when $x\geq 2$. $$\frac{x^3}{x^4-1}\overset{?}{>}\frac{1}{x}\qquad ⨠⨠ \qquad x^3\cdot x\overset{?}{>}1\cdot(x^4-1)\qquad ⨠⨠ \qquad x^4\overset{\checkmark}{>}x^4-1$$
3. && Apply comparison test.
    - We know: $$\frac{x^3}{x^4-1}>\frac{1}{x}$$
    - We know: $$\int_2^\infty\frac{1}{x}\,dx\qquad\text{diverges}$$
    - We conclude: $$\int_2^\infty\frac{x^3}{x^4-1}\,dx\qquad\text{diverges}$$

(b)
1. !! Integrand tends toward $1/x^2$ for large $x$.
    - Consider large $x$ values: $$\frac{1}{x^2+x+1}\quad\longrightarrow\quad\frac{1}{x^2}\quad\text{for}\quad x\to\infty$$
2. & Try comparison to $1/x^2$.
    - Comparison attempt: $$\frac{1}{x^2+x+1}\overset{?}{<}\frac{1}{x^2}$$
    - Validate. Notice $x^2+x+1>0$ and $x^2>0$ when $x\geq 1$. $$\frac{1}{x^2+x+1}\overset{?}{<}\frac{1}{x^2}\qquad ⨠⨠ \qquad 1\cdot x^2\overset{?}{<}1\cdot(x^2+x+1)\qquad ⨠⨠ \qquad x^2\overset{\checkmark}{<}x^2+x+1$$
3. && Apply comparison test.
    - We know: $$\frac{1}{x^2+x+1}<\frac{1}{x^2}$$
    - We know: $$\int_1^\infty\frac{1}{x^2}\,dx\qquad\text{converges}$$
    - We conclude: $$\int_1^\infty\frac{1}{x^2+x+1}\,dx\qquad\text{converges}$$
