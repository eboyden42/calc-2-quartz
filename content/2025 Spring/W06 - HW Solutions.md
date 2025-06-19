#### 05 - Pumping water from a tank
A cylindrical tank is full of water and the water is pumped out the top. The length of the tank is 7m and the radius is 5m.
- (a) Set up an integral for the total work performed assuming the tank is initially completely full.
- (b) Set up an integral for the total work performed assuming the tank is initially full to 3m and is pumped up to a height of 1m before exiting the tank.

**Solution**
**(a)**
1. & Identify line $y = 0$.
    - Set $y = 0$ to be the center of the cylinder.
    - Make the top of the cylinder $y = -5$ and  base $y = 5$.
2. && Find formula for weight of a single layer.
    - Area of a layer at $y$ is $A(y) = 7\left(2\sqrt{25-x^{2}}\right)$
        - One layer is a rectangle with length 7m.
        - The width is directly related to the formula for a circle of radius 5,
    - Volume of a layer at $y$ is therefore $14\sqrt{25-x^{2}}dy$.
    - Weight of the layer is then $F(y)dy = g\rho V$.
3. & Find formula for vertical distance a plate is lifted.
    - Layer at $y$ must be lifted by $y + 5$ to the top of the tank.
4. & Set up integral. 
    - Here: $$W = \int_{-5}^{5}\rho g\left(14\sqrt{25-y^{2}}\right)(y+5)dx$$

**(b)**
1. & Find formula for vertical distance a plate is lifted.
    - Layer at $y$ must be lifted by $y + 6$. 
2. & Adjust bounds.
    - Since the tank is full 3m deep, the water starts at $x = 2$.
3. & Set up integral. 
    - Here: $$W = \int_{2}^{5}\rho g \left(14\sqrt{25-y^{2}}\right)(y+6)dy$$

#### 06 - Work required to build a pyramid
The Great Pyramid of Giza is 140m tall and has a square base with 230m on each side. It is built of stone with mass density 2000kg/m$^{3}$ . 
Set up an integral that computes the work (against gravity) required to build the pyramid.

**Solution**
1. & Identify line $y = 0$.
    - Set $y = 0$ at the base of the pyramid.
    - Let the top of the pyramid be at $y = 146$.
2. && Find formula for weight of a single layer.
    - At $y = 0$, the length of a side is $230$m.
    - At $y = 146$, the length of a side is $0$m.
    - The formula for the side is thus $f(y) = 230-\frac{230}{146}y$.
    - The area is $\left[f(y)\right]^{2}$ and volume is $\left[f(y)\right]^{2}dy$.
    - Weight would be $\rho g \left[f(y)\right]^{2}dy$.
3. & Set up integral. 
    - Here: $$W = \int_{0}^{146}\rho g \left(230-\frac{230}{146}x\right)^{2}xdx$$

#### 09 - Computing improper integrals, Part I
For each integral below, give the limit interpretation and compute that limit. Based on that result, state whether the integral converges. If it converges, what is its value?
- (a) $\int_{1}^{\infty}\frac{1}{x^{\frac{19}{20}}}dx$.
- (b) $\int_{0}^{5}\frac{1}{x^{\frac{20}{19}}}dx$.
- (c) $\int_{1}^{\infty}e^{-x}dx$

**Solution**
**(a)**
1. & Rewrite using limits. 
    - Here: $$\int_{1}^{\infty}\frac{dx}{x^{\frac{19}{20}}} = \lim_{b \rightarrow \infty}\int_{1}^{b}\frac{dx}{x^{\frac{19}{20}}}$$
2. & Compute integral. 
    - Here: $$\begin{align*}\lim_{b \rightarrow \infty}\int_{1}^{b}\frac{dx}{x^{\frac{19}{20}}} &= \lim_{b\to \infty}\left.\left[20x^{\frac{1}{20}}\right]\right|^{b}_{1} \\ &= \lim_{b \to \infty}20\left[b^{\frac{1}{20}} - 1\right] \\  &= \infty \qquad  \text{the integral diverges}\end{align*}$$

**(b)**
1. & Rewrite using limits. ($f(x))$ is undefined at $x = 0$.)
    - Here: $$\int_{0}^{5}\frac{dx}{x^{\frac{20}{19}}} = \lim_{a\to0^{+}}\int_{a}^{5}\frac{dx}{x^{\frac{20}{19}}}$$
2. & Compute integral. 
    - Here: $$\begin{align*}\lim_{a\to0^{+}}\int_{a}^{5}\frac{dx}{x^{\frac{20}{19}}} &= \lim_{a \to 0^{+}}\left.\left[-19x^{-\frac{1}{19}}\right]\right|^{5}_{a} \\ &= -19\lim_{a \to 0^{+}}\left[5^{-\frac{1}{19}}-a^{-\frac{1}{19}}\right] \\ &= \infty \qquad \text{the integral diverges}\end{align*}$$

**(c)**
1. & Rewrite using limits. 
    - Here: $$\int_{1}^{\infty}e^{-x}dx = \lim_{b \to \infty}\int_{b}^{\infty}e^{-x}dx$$
2. & Compute integral. 
    - Here: $$\begin{align*}\lim_{b \to \infty}\int_{b}^{\infty}e^{-x}dx &= \lim_{b \to \infty}\left.\left[-e^{-x}\right]\right|_{1}^{b} \\ &= \lim_{b \to \infty}\left[-e^{-b}+e^{-1}\right] \\ &= e^{-1} \qquad \text{the integral converges}\end{align*}$$

#### 10 - Computing improper integrals, Part II
- (a) $\int_{0}^{1}\ln{x}dx$
- (b) $\int_{-\infty}^{\infty}xe^{-x^{2}}dx$
- (c) $\int_{1}^{2}\frac{1}{(x-1)^{2}}dx$

**Solution**
**(a)**
1. & Rewrite using limits. 
    - Here: $$\int_{0}^{1}\ln{x}dx = \lim_{a \to 0^{+}}\int_{a}^{1}\ln{x}dx$$
2. & Compute integral. 
    - Here: $$\begin{align*}\lim_{a \to 0^{+}}\int_{a}^{1}\ln{x}dx &= \lim_{a\to 0^{+}}\left.\left[x\ln{x}-x\right]\right|^{1}_{a} \\ &= \lim_{a\to 0^{+}}\left[-1-a\ln{a}+a\right] \\ &= -1 \qquad \text{the limit converges}\end{align*}$$

**(b)**
1. & Rewrite using limits. 
    - Here: $$\int_{-\infty}^{\infty}xe^{-x^{2}} = \lim_{a\to-\infty}\int_{a}^{0}xe^{-x^{2}} + \lim_{b\to\infty}\int_{0}^{b}xe^{-x^{2}}$$
2. & Compute integrals. 
    - Here: $$\begin{align*}\lim_{a\to-\infty}\int_{a}^{0}xe^{-x^{2}}dx + \lim_{b\to\infty}\int_{0}^{b}xe^{-x^{2}}dx &= \lim_{a\to-\infty}\left.\left[-\frac{1}{2}e^{-x^{2}}\right]\right|^{0}_{a} + \lim_{b\to\infty}\left.\left[-\frac{1}{2}e^{-x^{2}}\right]\right|^{b}_{0} \\ &= -\frac{1}{2}+\left(-\frac{1}{2}\right) \\ &= 0 \qquad \text{the integral converges}\end{align*}$$

**(c)**
1. & Rewrite using limits. 
    - Here: $$\int_{1}^{2}\frac{1}{(x-1)^{2}}dx = \lim_{a \to 1^{+}}\int_{a}^{2}\frac{dx}{(x-1)^{2}}$$
2. & Compute integral. 
    - Here: $$\begin{align*}\lim_{a\to1^{+}}\int_{a}^{2}\frac{dx}{(x-1)^{2}} &= \lim_{a \to 1^{+}}\left.\left[-\frac{1}{x-1}\right]\right|^{2}_{a} \\ &= \lim_{a \to 1^{+}}\left[-1+\frac{1}{a-1}\right] \\ &= \infty \qquad \text{the integral diverges}\end{align*} $$

