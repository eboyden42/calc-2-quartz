#### 03 - Parametric concavity

Find $\displaystyle\frac{d^2 y}{d x^2}$ at $t=1$ for the curve given parametrically by $x=4-t^{-2}$, $y=t^{-1}+t$.

**Solution**

1. & Compute derivatives. $$\left(x', y'\right) = \left(2t^{-3},1-t^{-2}\right)$$
2. & Compute $\frac{dy}{dx}$. $$\frac{dy}{dx} = \frac{\frac{dy}{dt}}{\frac{dx}{dt}} = \frac{1-t^{-2}}{2t^{-3}} = \frac{t^{3}}{2}-\frac{t}{2}$$
3. & Compute $\frac{d^{2}y}{dx^{2}}$. $$\frac{d^{2}y}{dx^{2}} = \frac{\frac{d\left(y'\right)}{dt}}{\frac{dx}{dt}} = \frac{-\frac{1}{2}+\frac{3t^{2}}{2}}{2t^{-3}} = \frac{3}{4}t^{5}-\frac{t^{3}}{4}$$
4. & Evaluate at $t = 1$. $$\left.\frac{d^{2}y}{dx^{2}}\right|_{t = 1} = \frac{3}{4}-\frac{1}{4} = \frac{1}{2}$$


#### 06 - Parametric concavity

Find the intervals of $t$ on which the parametric curve $c(t)=(t^2,\,t^3-4t)$ is concave up.


**Solution**

1. & Compute derivatives. $$\left(x', y'\right) = \left(2t, 3t^{2}-4\right)$$
2. & Compute $\frac{dy}{dx}$. $$\frac{dy}{dx}=\frac{\frac{dy}{dt}}{\frac{dx}{dt}} = \frac{3t^{2}-4}{2t} = \frac{3}{2}t-2t^{-1}$$
3. & Compute $\frac{d^{2}y}{dx^{2}}$. $$\frac{d^{2}y}{dx^{2}}=\frac{\frac{d\left(y'\right)}{dt}}{\frac{dx}{dt}}=\frac{\frac{3}{2}+2t^{-2}}{2t}=\frac{3}{4}t^{-1}+t^{-3}$$
4. & Examine when second derivative is greater than 0.
    - The above expression is greater zero only when $t > 0$. So, the interval is $(0, \infty)$.


#### 07 - Parametric arclength

Find the arclength of the curve given parametrically by $x=2t^2$, $y=3t^2-1$ over the time interval $0\leq t\leq 4$.

**Solution**

1. & Compute derivatives. $$\left(x', y'\right) = (4t, 6t)$$
2. && Compute length. $$\ell = \int_{0}^{4}\sqrt{(4t)^{2}+(6t)^{2}}dt = \int_{0}^{4}\sqrt{52t^{2}}dt = \left.\frac{\sqrt{52}}{2}t^{2}\right|_{0}^{4} = 16\sqrt{13}$$


#### 08 - Minimum speed of a particle

Suppose a travelling particle has position modelled by the parametric curve $c(t) = \left(t^{3}-4t, t^{2}+1\right)$ for $t \geq 0$. What is the *slowest speed* that the particle experiences?

**Solution**

1. & Compute derivatives. $$\left(x', y'\right) = \left(3t^{2}-4, 2t\right)$$
2. && Compute the speed. $$v(t) = \sqrt{\left(x'\right)^{2}+\left(y'\right)^{2}} = \sqrt{9t^{4}-24t^{2}+16+4t^{2}} = \sqrt{9t^{4} -20t^{2}+16}$$
3. & Find critical points of the *square* of the speed function. $$\frac{d\left[v(t)^{2}\right]}{dt} = 36t^{3}-40t = 0\quad ⨠⨠\quad4t\left(9t^{2}-10\right) = 0 \quad ⨠⨠\quad t = 0, \pm \frac{\sqrt{10}}{3}$$
4. & Evaluate $v(t)$ for each of the critical points. $$\begin{align*}v(0) &= \sqrt{16} = 4 \\ v\left(\frac{\sqrt{10}}{3}\right) &= \frac{\sqrt{44}}{3} = \frac{2\sqrt{11}}{3}\end{align*}$$
5. & The minimum of these speeds is $\frac{2\sqrt{11}}{3}$ units per time unit.



#### 09 - Cycloid - length and surface area of revolution
Consider the cycloid given parametrically by $c(t) = (t-\sin{t}, 1-\cos{t})$.

(a) Find the length of one arch of the cycloid.

(b) Suppose one arch of the cycloid is revolved around the $x$-axis. Find the area of this surface of revolution.

**Solution**

**(a)**
1. & Compute derivatives. $$\left(x',y'\right) = (1-\cos{t}, \sin{t})$$
2. && Compute length. $$\begin{gather*}\ell = \int_{0}^{2\pi}\sqrt{(1-\cos{t})^{2}+\sin^{2}t}dt = \int_{0}^{2\pi}\sqrt{2-2\cos{t}}dt \\\\= \int_{0}^{2\pi}2\sin{\frac{t}{2}}dt = \left.-4\cos{\frac{t}{2}}\right|_{0}^{2\pi} = 8\end{gather*}$$

**(b)**
1. &&& Compute surface area. $$\begin{align*}S &= 2\pi\int rds \\ &= 2\pi\int_{0}^{2\pi}(1-\cos{t})\left(2\sin{\frac{t}{2}}\right)dt \\ &= 8\pi \int_{0}^{2\pi}\sin^{3}\frac{t}{2}dt \\ &= 16\pi\int_{0}^{\pi}\left(1-\cos^{2}u\right)\sin{u}du \\ &= -16\pi\int_{1}^{-1}\left(1-v^{2}\right)dv \\&=16\pi\left.\left[w-\frac{w^{3}}{3}\right]\right|^{1}_{-1} =\frac{64\pi}{3}      \end{align*}$$

