© Aleesha Khurram \<wma9tt@virginia.edu> 9/2024
– Permitted for use in McMillan’s Calc II only, NOT FOR DISTRIBUTION –
#### 02
Compute the integral: $$\int (2x+9)e^x\,dx$$

**Solution**
1. && Select $u$ and $dv$, and compute $du$ and $v$. Use LIATE acronym.

$$\begin{align*}u &= 2x + 9 \\ du &= 2dx \\ \\ dv &= e^{x}dx \\ v &= e^{x}\end{align*}$$
2. &&& Use the integration by parts formula $uv - \int vdu$ to evaluate the integral.
$$\begin{align*}
uv - \int v du &= (2x+9)e^{x} - \int 2e^{x}dx \\ &= (2x+9)e^{x} -2e^{x}+C \\ &= e^{x}(2x+7)+C, \quad C \in \mathbb{R}
\end{align*}$$

#### 05
Consider the region in the $xy$-plane, First Quadrant, bounded by the $y$-axis on the left, by $y = 8-6x^{2}$ on the top, and $y=2x^{2}$ on the bottom. A 3D solid is given by revolving this region around the $y$-axis.
- (a) Find the volume of the solid using the method of shells.
- (b) *Attempt* to find the volume of the solid using the method of washers/disks. Explain what happens. Why is this harder? (There are *two* issues!)

**Solution**
(a)
1. &&& Formula for calculating the volume of a figure using shells.
$$V = \int_{a}^{b}2\pi Rhdr$$
2. & Define the cross section region. 
    - Bounded above by $y = 8-6x^{2}$
    - Bounded below by $y = 2x^{2}$
    - Bounded left by $x = 0$
    - Bounded right by intersection at line $x = 1$.
    
3. & Interpret $R$, the radius of shell-cylinder.
$$R(x) = x$$
4. && Interpret $h$. The height of shell-cylinder equals distance from lower to upper bounding lines:
$$\begin{align*}y &= \left(8-6x^{2}\right) - 2x^{2} \\ &= 8-8x^{2}\end{align*}$$
5. & Interpret $dr$. 
    - $dr$ is the limit of $\Delta x$ here so $dr = dx$.

6. &&& Use the values to compute the integral.
    - $$\begin{align*} V &= \int_{a}^{b}2\pi Rhdr \\ &= \int_{0}^{1}2\pi (x)\left(8-8x^{2}\right) dx \\ &= 16\pi\int_{0}^{1}x-x^{3}dx \\ &= 16\pi \left.\left[\frac{x^{2}}{2} - \frac{x^{4}}{4}\right]\right|_{0}^{1} \\ &= 16\pi\left[\frac{1}{2} - \frac{1}{4}\right] \\ &= 4\pi \end{align*}$$

(b) 
1. &&& Formula for computing volume using washers/disks rotated around line parallel to the $y-$axis.
$$V = \int_{a}^{b} \pi\left(R^{2} - r^{2}\right)dy$$
2. && Rewrite the bounds of the cross section in terms of $y$.
$$\begin{align*}y &= 8-6x^{2}  ⨠⨠  \quad x = \sqrt{\frac{8 - y}{6}} \\ y &= 2x^{2} \quad ⨠⨠ \quad x = \sqrt{\frac{y}{2}} \end{align*} $$
3. && Define cross section region.
    - Bounded above by $y = 8$
    - Bounded below by $y = 0$
    - Intersection at $y = 2$.

4. !! Define $R$, the outermost radius.
    - Since $R$ varies based on $y$, we have to compute two integrals; one from $y = 0$ to $y = 2$, and one from $y = 0$ to $y = 8$.
    - From $y = 0$ to $y = 2$, $R = \sqrt{\frac{y}{2}}$ . From $y = 2$ to $y = 8$, $R = \sqrt{\frac{8-y}{6}}$ . 

5. & Define $r$, the innermost radius. Since there is no ring in the center, $r = 0$ for both integrals. 

6. &&& Compute the integral using derived values.
$$\begin{align*}V &= \int_{a}^{b}\pi \left(R^{2}-r^{2}\right)dy \\ &= \pi\left[\int_{0}^{2}\left(\sqrt{\frac{y}{2}}\right)^{2} dy + \int_{2}^{8}\left(\sqrt{\frac{8-y}{6}}\right)^{2}dy\right] \\ &= \pi\left[\int_{0}^{2} \frac{y}{2} dy + \int_{2}^{8}\frac{8-y}{6} dy\right] \\ &= \pi \left[\left.\left[\frac{y^{2}}{4}\right]\right|_{0}^{2} + \left.\left[\frac{4}{3}y-\frac{y^{2}}{12}\right]\right|_{2}^{8}\right] \\
&= \pi \left[1 + \left[\left(\frac{32}{3} - \frac{16}{3} \right) - \left(\frac{8}{3} - \frac{1}{3}\right)\right]\right] \\ &= 4\pi\end{align*}$$ 
7. &&& Concluding thoughts: why are shells preferable?
    - No need to compute two integrals.
    - No need to rewrite equations in terms of $y$.


#### 06
Compute the integral:
$$\int x^{3}\ln{x}\,dx$$
Number your steps!

**Solution**
1. && Select appropriate $u$ and $dv$, and compute $du$ and $v$. Use LIATE acronym.
    - $$\begin{align*}
    u &= \ln{x} \\ du &= \frac{dx}{x} \\ \\ dv &= x^{3}dx \\ v &= \frac{x^{4}}{4}
    \end{align*}$$
2. &&& Use the integration by parts formula $uv - \int vdu$ to evaluate the integral.
    $$\begin{align*}
    uv - \int vdu &= \frac{x^{4}}{4}\ln{x}-\int \frac{x^{3}}{4}dx \\ &= \frac{x^{4}}{4}\ln{x}-\frac{x^{4}}{16} + C, \quad C \in \mathbb{R}
    \end{align*}$$


## Additional problems

#### Extra practice
Compute the integral:
$$\int x \ln{(5+x)dx}$$
(Hint: do substitution to get $\ln{(t)}$. And then, try *both* options for $u$, $v$ choices.) Number your steps!

**Solution**
1. && Make substitution $t = 5 + x$. 
    - $x = t - 5$
    - $dt = dx$
 $$ \int x \ln{(5 + x)}dx = \int (t-5)\ln{(t)}dt$$
 2. && Select appropriate $u$ and $dv$, and compute $du$ and $v$. Use LIATE acronym.
    $$ \begin{align*}
    u &= \ln{(t)} \\ du &= \frac{dt}{t} \\ \\ dv &= (t-5)dt \\ v&= \frac{t^{2}}{2}-5t
    \end{align*}$$
3. &&& Use the integration by parts formula $uv - \int vdu$ to evaluate the integral.
    $$\begin{align*}
    uv - \int vdu &= \left(\frac{t^{2}}{2} - 5t\right)\ln{t} - \int \frac{\frac{t^{2}}{2}-5t}{t}dt \\ &= \left(\frac{t^{2}}{2}-5t\right)\ln{t} - \int \frac{t}{2}-5dt \\ &= \left(\frac{t^{2}}{2}-5t\right)\ln{t} - \frac{t^{2}}{4}+5t + C, \quad C \in \mathbb{R}
    \end{align*}$$
4. && Substitute back $5+ x$ for $t$.
    $$\begin{align*}\left(\frac{t^{2}}{2}-5t\right)\ln{t} - \frac{t^{2}}{4}+5t + C &=  \left(\frac{(5+x)^{2}}{2}-5(5+x)\right)\ln{(5+x)} - \frac{(5+x)^{2}}{4}+5(5+x) + C\\ &= \left(\frac{(5+x)^{2}}{2}-5(5+x)\right)\ln{(5+x)} - \frac{1}{4}\left(x^{2}-10x-75\right) + C, \quad C \in \mathbb{R}\end{align*} $$

#### Extra practice
**Problem**
A solid is obtained by rotating the region in the first quadrant bounded by curves $y = 5x^{2}$, $y=5x^{3}$, and $x = \frac{1}{2}$. about the line $x = -2$.

- (a) Set up an integral to find the volume of the solid.
- (b) Evaluate the integral to find the volume of the solid.

**Solution**
(a)
1. &&& Formula for volume by cylindrical shells
    $$V = \int_{a}^{b}2\pi Rhdr$$
2. & Define cross section region
    - Bounded above by $y=5x^{2}$.
    - Bounded below by $y = 5x^{3}$.
    - Bounded left by line $x = 0$.
    - Bounded right by line $x = \frac{1}{2}$.
3. & Define $R$, the radius of the cylindrical shells.
    $$R(x) = x-(-2)=x+2$$
4. & Define $h$, the height of the cylindrical shells.
    $$h = 5x^{2}-5x^{3}$$
5. & Define $dr$.
    -  $dr$ is the limit of $\Delta x$ here so $dr = dx$.
6. && Plug in values to set up integral
    $$ \begin{align*}
    V &= \int_{a}^{b}2\pi Rhdr \\ &= \int_{0}^{\frac{1}{2}}2\pi(x+2)\left(5x^{2}-5x^{3}\right)dx
    \end{align*}$$

(b)
1. & Factor out constants
    $$\int_{0}^\frac{1}{2}2\pi(x+2)\left(5x^{2}-5x^{3}\right)dx = 10\pi\int_{0}^{\frac{1}{2}}(x+2)\left(x^{2}-x^{3}\right)dx$$
2. & Expand integrand
    $$10\pi\int_{0}^{\frac{1}{2}}(x+2)\left(x^{2}-x^{3}\right)dx = 10\pi\int_{0}^{\frac{1}{2}}-x^{3}-x^{4}+2x^{2}dx$$
3. && Evaluate integral
$$\begin{align*}
10\pi\int_{0}^{\frac{1}{2}}-x^{3}-x^{4}+2x^{2}dx &= 10\pi\left.\left[-\frac{x^{5}}{5}-\frac{x^{4}}{4}+\frac{2}{3}x^{3}\right]\right|^{\frac{1}{2}}_{0} \\ &= 10\pi\left[-\frac{1}{160}-\frac{1}{64}+\frac{1}{12}\right] \\ &= \frac{59\pi}{96}
\end{align*}$$

#### Extra practice
Evaluate the integral. (Use $C$ for the constant of integration.)
$$\int(\pi-x)\cos{(\pi x)}dx$$

**Solution**

1. && Choose appropriate $u$ and $dv$ to compute $du$ and $v$. Use LIATE acronym.
    $$\begin{align*}
    u &= \pi - x \\ du &= -dx \\ \\ dv &= \cos{(\pi x)}dx \\ v &= \frac{1}{\pi}\sin{(\pi x)}
    \end{align*}$$
2. &&& Use integration by parts formula $uv - \int vdu$ to evaluate integral.
    $$\begin{align*} uv - \int vdu &= \frac{1}{\pi}(\pi - x)\sin{(\pi x)} + \frac{1}{\pi}\int \sin{(\pi x)}dx \\ &= \frac{1}{\pi}(\pi- x)\sin{(\pi x) -\frac{1}{\pi^{2}}\cos{(\pi x)}} + C, \quad C \in \mathbb{R} \end{align*}$$

#### Extra practice
A solid is obtained by rotating the area in the first quadrant bounded by the curves $y = 8-6x^{2}$ and $y = 2x^{2}$ about the $x$-axis.
(a) Set up an integral to find the volume of the solid.
(b) Evaluate the integral to find the volume of the solid.

**Solution**
(a)
1. &&& Formula for calculating volume with washers/disks rotated around line parallel to $x$-axis.
    $$ V = \int_{a}^{b} \pi \left(R^{2}-r^{2}\right)dx$$
2. && Define cross section region.
    - Bounded above by $y = 8-6x^{2}$
    - Bounded below by $y = 2x^{2}$
    - Bounded right by intersection at $x = 1$.
    - Bounded left by $x = 0$.
3. & Define $R$, the outermost radius.
$$R = 8-6x^{2}$$
4. & Define $r$, the innermost radius.
    $$ r = 2x^{2}$$
5. && Set up integral using derived values.
    $$\begin{align*}V &= \int_{a}^{b}\pi\left(R^{2}-r^{2}\right)dx \\ &= 
    \int_{0}^{1}\pi\left(\left(8-6x^{2}\right)^{2}-\left(2x^{2}\right)^{2}\right)dx \\ &= \int_{0}^{1}\pi\left(\left(8-6x^{2}\right)^{2}-4x^{4}\right)dx
    \end{align*}$$
(b)
1. && Move constant outside and expand integrand.
$$\begin{align*}
\int_{0}^{1}\pi\left(\left(8-6x^{2}\right)^{2}-4x^{4}\right)dx &= \pi\int_{0}^{1}\left(64-96x^{2}+36x^{4}-4x^{4}\right)dx \\ &= \pi\int_{0}^{1}32x^{4}-96x^{2}+64dx \\&= 32\pi\int_{0}^{1}x^{4}-3x^{2}+2dx
\end{align*}$$
2. && Evaluate integral.
    $$\begin{align*}
    32\pi\int_{0}^{1}x^{4}-3x^{2}+2dx &= 32\pi\left.\left[\frac{x^{5}}{5}-x^{3}+2x\right]\right|^{1}_{0} \\ &= 32\pi\left[\frac{1}{5}+1\right] \\ &= \frac{192\pi}{5}
    \end{align*}$$

#### Extra practice
Evaluate the integral. (Remember the constant of integration.)
$$\int \cos^{-1}{(x)}dx$$

**Solution**

1. &&& Choose appropriate $u$ and $dv$ to compute $du$ and $v$. Use LIATE acronym.
    $$\begin{align*}
    u &= \cos^{-1}{(x)} \\ du &= -\frac{dx}{\sqrt{1-x^{2}}} \\ \\ dv &= dx \\ v &= x
    \end{align*}$$
2. &&& Use integration by parts formula $uv - \int v du$ to set up integral.
    $$\begin{align*}
    uv-\int vdu &= x\cos^{-1}{(x)}+\int\frac{x}{\sqrt{1-x^{2}}}dx 
    \end{align*}$$
3. && Use $u$-substitution. 
    - Set $t = 1 - x^{2}$, $dt = -2xdx$
$$\begin{align*}
x\cos^{-1}{(x)}+\int\frac{x}{\sqrt{1-x^{2}}}dx &= x\cos^{-1}{(x)}-\frac{1}{2}\int \frac{dt}{\sqrt{t}} \\ &= x\cos^{-1}(x)-\sqrt{t} + C, \quad C \in \mathbb{R}
\end{align*}$$
4. & Substitute back $1 -x^{2}$ for $t$.
    $$x\cos^{-1}(x)-\sqrt{t}+C = x\cos^{-1}(x)-\sqrt{1-x^{2}} + C, \quad C \in \mathbb{R}$$
    