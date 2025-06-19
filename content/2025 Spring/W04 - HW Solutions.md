#### 02 - Surface area of revolved cubic
The curve $y = x^{3}$ over $x \in [0, 2]$ is revolved around the $x$-axis. Find the area of the resulting surface.

**Solution**
1. && Write out formula for surface area of surface revolved around $x$-axis.
    - Here: $$S = \int_{a}^{b}2\pi f(x)\sqrt{1+\left[f'(x)\right]^{2}}dx$$
2. & Plug in $[a, b] = [0, 2]$, $f(x) = x^{3}$, and $f'(x) = 3x^{2}$.
    - Here: $$\int_{a}^{b}2\pi f(x)\sqrt{1+\left[f'(x)\right]^{2}}dx = \int_{0}^{2}2\pi x^{3}\sqrt{1+9x^{4}}dx$$
3. && Perform substitution: $u = 1+9x^{4}$, $du = 36x^{3}dx$
    - Adjust bounds $[0, 2] \quad ⨠⨠ \quad [1, 145]$ $$\int_{0}^{2}2\pi x^{3}\sqrt{1+9x^{4}}dx = \frac{\pi}{18}\int_{1}^{145}\sqrt{u}du$$
4. & Evaluate integral.
    - Here: $$\begin{align*}\frac{\pi}{18}\int_{1}^{145}\sqrt{u}du &= \frac{\pi}{27}\left[u^{\frac{3}{2}}\right]^{145}_{1} \\ &= \frac{\pi}{27}\left(145\sqrt{145}-1\right)\end{align*}$$

#### 03 - Arc length of a curve - tricky algebra
Find the arc length of the curve $y = \frac{1}{8}x^{4} + \frac{1}{4x^{2}}$ for $x \in [1,2]$ .

(Hint: expand under the root, then simplify, then factor; now it's a square and the root disappears)

**Solution**
1. && Write down formula for arc length of a curve.
    - Here: $$s = \int_{a}^{b}\sqrt{1+\left[f'(x)\right]^{2}}dx$$
2. & Calculate $f'(x)$
    - Here: $$\begin{align*}f(x) &= \frac{1}{8}x^{4}+\frac{1}{4x^{2}} \\f'(x) &= \frac{1}{2}x^{3}-\frac{1}{2}x^{-3}\end{align*}$$
3. & Plug in values to compute integral. 
    - Here: $$\begin{align*}s &= \int_{a}^{b}\sqrt{1+\left[f'(x)\right]^{2}}dx \\&= \int_{1}^{2} \sqrt{1+ \left(\frac{x^{3}-x^{-3}}{2}\right)^{2}}dx\end{align*}$$
4. &&& Compute integral.
    - Here: $$\begin{align*}\int_{1}^{2}\sqrt{1+\left(\frac{1}{2}x^{3}-\frac{1}{2}x^{-3}\right)^{2}}dx &= int_{1}^{2}\sqrt{1+\frac{1}{4}x^{6}-\frac{1}{2}+\frac{1}{4}x^{-6}}dx \\ &= \int_{1}^{2}\sqrt{\frac{1}{4}x^{6}+\frac{1}{2}+\frac{1}{4}x^{-6}}dx \\&= \int_{1}^{2}\sqrt{\left(\frac{1}{2}x^{3}+\frac{1}{2}x^{-3}\right)^{2}}dx \\&= \int_{1}^{2}\frac{1}{2}x^{3}+\frac{1}{2}x^{-3}dx \\&= \left.\left[\frac{1}{8}x^{4}-\frac{1}{4}x^{-2}\right]\right|^{2}_{1} \\&= \left(2-\frac{1}{16}\right) - \left(\frac{1}{8}-\frac{1}{4}\right) \\&= \frac{33}{16}\end{align*}$$

#### 04 - Arc length of a curve - tricky integration
Find the arc length of the curve $y=e^{x}$ for $x \in \left[0, \frac{1}{2}\right]$.

(Hint: the integral can be done using either: (i) $u$-sub then trig sub, or (ii) 'rationalization' then partial fractions.)

**Solution**
1. && Write down formula for arc length.
    - Here: $$s = \int_{a}^{b}\sqrt{1+\left[f'(x)\right]^{2}}dx$$
2. & Set up integral.
    - $f(x) = f'(x) = e^{x}$.
    - $[a, b] = \left[0, \frac{1}{2}\right]$
      $$\int_{a}^{b}\sqrt{1+\left[f'(x)\right]^{2}}dx = \int_{0}^{\frac{1}{2}} \sqrt{1+e^{2x}} dx$$
3. && Perform $u$-substitution: $u = 2x$, $du=2dx$
    - Adjust bounds: $\left[0, \frac{1}{2}\right] \quad ⨠⨠ \quad [0, 1]$ 
      $$\int_{0}^{\frac{1}{2}}\sqrt{1+e^{2x}}dx = \frac{1}{2}\int_{0}^{1}\sqrt{1+e^{u}}du$$
4. &&& Perform substitution: $v = \sqrt{1+e^{u}}$
    - Here: $$v = \sqrt{1+e^{u}} \quad ⨠⨠\quad dv = \frac{e^{u}}{2\sqrt{1+e^{u}}}du$$
    - Here: $$ du = \frac{2\sqrt{1+e^{u}}}{e^{u}}dv = \frac{2v}{v^{2}-1}dv$$
    - Adjust bounds: $[0, 1] \quad ⨠⨠ \quad \left[\sqrt{2}, \sqrt{1+e}\right]$
      $$\frac{1}{2}\int_{0}^{1}\sqrt{1+e^{u}}du = \int_{\sqrt{2}}^{\sqrt{1+e}}\frac{v^{2}}{v^{2}-1}dv$$
5. &&& Compute partial fraction of integrand.
    - Expand: $$\frac{v^{2}}{v^{2}-1} = 1+\frac{1}{v^{2}-1}=1+\frac{1}{(v+1)(v-1)}$$
    - Write down general PFD: $$\frac{1}{(v+1)(v-1)} = \frac{A}{v+1}+\frac{B}{v-1}$$
    - Solve for $A$ and $B$: $$1 = A(v-1)+B(v+1)$$
        - $x = -1 \quad ⨠⨠ \quad A = -\frac{1}{2}$
        - $x = 1 \quad ⨠⨠ \quad B = \frac{1}{2}$ $$\begin{align*}\int_{\sqrt{2}}^{\sqrt{1+e}}\frac{v^{2}}{v^{2}-1}dv &= \int_{\sqrt{2}}^{\sqrt{1+e}}1-\frac{1}{2(v+1)}+\frac{1}{2(v-1)}dv \end{align*}$$
6. && Evaluate integral.
    - Here: $$\begin{align*}&\int_{\sqrt{2}}^{\sqrt{1+e}}1-\frac{1}{2(v+1)}+\frac{1}{2(v-1)}dv\\\\ &= \left.\left[v-\frac{1}{2}\ln{|v+1|}+\frac{1}{2}\ln{|v-1|}\right] \right|^{\sqrt{1+e}}_{\sqrt{2}} \\\\&= \left[\sqrt{1+e}-\frac{1}{2}\ln{ \left(\sqrt{1+e}+1\right)} +\frac{1}{2}\ln{\left(\sqrt{1+e}-1\right)}\right] - \left[\sqrt{2}-\frac{1}{2} \ln{\left(\sqrt{2}+1\right)}+\frac{1}{2}\ln{\left(\sqrt{2}-1\right)}\right] \\\\&= \sqrt{1+e}-\sqrt{2}+ \frac{\ln{\left(\sqrt{2}+1\right)-\ln{\left(\sqrt{1+e}+1\right) + \ln{\left(\sqrt{1+e}-1\right)-\ln{\left( \sqrt{2}-1\right)}}}}}{2}\end{align*}$$

#### 05 - Surface area of a cone
A *cone* may be described as the surface of revolution of a ray emanating from the origin, revolved around the $x$-axis.

Let $f(x) = mx$ for some $m > 0$. Find the surface area of the cone given by revolving the graph of $f$ over $x \in [0, h]$.

Can you also calculate this area using geometry? And verify the two methods give the same formula? (Hint: 'unroll' the cone into a sector.)

**Solution**
1. && Write out formula for surface area.
    - Here: $$S = \int_{a}^{b}2\pi f(x)\sqrt{1+\left[f'(x)\right]^{2}}dx$$
2. & Calculate $f'(x)$.
    - Here: $$f(x)=mx \quad⨠⨠\quad f'(x)=m$$
3. && Set up integral by plugging in $[a, b] =[0, h]$. 
    - Here: $$\begin{align*}S &= \int_{a}^{b}2\pi f(x)\sqrt{1+\left[f'(x)\right]^{2}}dx \\ &= \int_{0}^{h}2\pi x\sqrt{1+m^{2}}dx\end{align*}$$
4. && Evaluate integral. Note solution is just lateral area.
    - Here: $$\begin{align*}\int_{0}^{h}2\pi mx\sqrt{1+m^{2}}dx &= 2\pi m\sqrt{1+m^{2}}\int_{0}^{h}xdx \\&= 2\pi m\sqrt{1+m^{2}}\left.\left[\frac{x^{2}}{2}\right]\right|_{0}^{h} \\ &= \pi h^{2}m\sqrt{1+m^{2}}\end{align*}$$
5. &&& Verify with geometry. Note that unrolling the cone forms a sector with radius $h\sqrt{1+m^{2}}$ and arc length $2\pi m h$.
    - Radius is the lateral height of the cone: hypotenuse of right triangle with other sides $h$ and $mh$.
    - Arc length is $2\pi mh$, since $mh$ is radius of the base.
    - Calculate area of sector using ratios.
        - Circumference of full circle: $2\pi h\sqrt{1+m^{2}}$
        - Area of full circle: $\pi h^{2}(1+m^{2})$
          $$\begin{align*} \frac{x}{\pi h^{2}(1+m^{2})} &= \frac{2\pi mh}{2\pi h \sqrt{1+m^{2}}} \\ x &= \pi h^{2} m \sqrt{1+m^{2}} \end{align*}$$

#### 06 - Surface area of a parabolic reflector
A parabolic reflector is given by rotating the curve $y=x^{2}$ around the *y-axis* for $x \in [0, 2]$. 

What is the surface area of this reflector?
1. && Write out formula for surface area. 
    - This problem can be done with respect to $x$ or with respect to $y$. Note this will not always be the case.
      $$\begin{align*}S &= \int_{a}^{b}2\pi f(x)\sqrt{1+\left[f'(x)\right]^{2}}dx \\S &= \int_{a}^{b}2\pi g(y)\sqrt{1+\left[g'(y)\right]^{2}}dy\end{align*}$$
2. & Rewrite $f(x)= x^{2}$ in terms of $y$, and adjust bounds.
    - Here: $$f(x)=x^{2} \quad ⨠⨠ \quad g(y)=\sqrt{y}$$
    - Here: $$x\in[0, 2]\quad ⨠⨠\quad y\in [0, 4]$$
3. & Compute $f'(x)$ and $g'(y)$
    - Here: $$f(x) = x^{2} \quad ⨠⨠ \quad f'(x)=2x$$
    - Here: $$g(y) = \sqrt{y} \quad ⨠⨠ \quad g'(y) = \frac{1}{2\sqrt{y}}$$
4. && Evaluate integrals.
    - with respect to $x$: Note that $f(x) = x$ since that is the radius in this case.
      $$\begin{align*}\int_{a}^{b}2\pi f(x)\sqrt{1+\left[f'(x)\right]^{2}}dx &= 2\pi\int_{0}^{2}x\sqrt{1+(2x)^{2}}dx \\&= 2\pi \int_{0}^{2} x\sqrt{1+4x^{2}}dx \end{align*}$$
    - $u$-substitution: $u = 1+4x^{2}$, $du = 8xdx$, $[0, 2] ⨠⨠ [1, 17]$.
      $$\begin{align*}2\pi\int_{0}^{2}x\sqrt{1+4x^{2}}dx &= \frac{1}{4} \pi\int_{1}^{17}\sqrt{u}du \\&= \frac{\pi}{4}\left.\left[\frac{2}{3}u^{\frac{3}{2}}\right]\right|^{17}_{1} \\&= \frac{\pi}{6}\left[17\sqrt{17}-1\right] \end{align*}$$
    - with respect to $y$:
      $$\begin{align*}\int_{a}^{b}2\pi g(y)\sqrt{1+\left[g'(y)\right]^{2}}dy &= int_{0}^{4}\sqrt{y}\sqrt{1+\frac{1}{4y}}dy \\&= 2\pi \int_{0}^{4}\sqrt{y+\frac{1}{4}}dy \\&= 2\pi \int_{0}^{4}\frac{1}{2}\sqrt{4y+1}dy \\&= \pi \int_{0}^{4}\sqrt{4y+1}dy \\\end{align*}$$
    - $u$-substitution: $u = 4y+1, du = 4dy$, $[0, 4]⨠⨠ [1, 17]$
      $$\begin{align*}\pi \int_{0}^{4}\sqrt{4y+1}dy &= \frac{\pi}{4} \int_{1}^{17}\sqrt{u}du \\ &= \frac{\pi}{4}\left.\left[\frac{2}{3}u^{\frac{2}{3}}\right]\right|^{17}_{1} \\&= \frac{\pi}{6}\left[17\sqrt{17}-1\right]\end{align*}$$

#### 07 - Surface area of torus
A torus is created by revolving about the *x-axis* the circle with this equation:
$$x^{2}+(y-b)^{2}=a^{2}$$
Find the surface area of this torus.
(Hint: compute for the top and bottom of the circle separately and add the results.)

**Solution**
1. && Write down formula for surface area for surface revolved around $x$-axis.
    - Here: $$S = \int_{a}^{b}2\pi f(x)\sqrt{1+\left[f'(x)\right]^{2}}dx$$
2. && Identify formulas for bottom and top of the circle.
    - Here: $$\begin{align*}x^{2}+(y-b)^{2} &= a^{2} \\ y&= b \pm \sqrt{a^{2}-x^{2}}=f(x)\end{align*}$$
     - Let $f_{1}(x) = b + \sqrt{a^{2}-x^{2}}$ and $f_{2}(x)=b-\sqrt{a^{2}-x^{2}}$
3. & Compute $f_{1}'(x)$ and $f_{2}'(x)$.
    - Here: $$\begin{align*} f_{1}(x)=b+\sqrt{a^{2}-x^{2}} \quad ⨠⨠ \quad f_{1}'(x)=-\frac{x}{\sqrt{a^{2}-x^{2}}} \\ f_{2}(x)=b-\sqrt{a^{2}-x^{2}} \quad ⨠⨠ \quad f_{2}'(x)=\frac{x}{\sqrt{a^{2}-x^{2}}}\end{align*}$$
4. &&& Compute integral using $[a, b] = [-a, a]$
    - Here: $$\begin{align*}\int_{a}^{b}2\pi f(x)\sqrt{1+\left[f'(x)\right]^{2}}dx &= 2\pi\int_{-}^{a} \left[\left(b+\sqrt{a^{2}-x^{2}}\right)\sqrt{1+\frac{x^{2}}{a^{2}-x^{2}}} + \left(b-\sqrt{a^{2}-x^{2}}\right)\sqrt{1+\frac{x^{2}}{a^{2}-x^{2}}}\right]dx \\&= 2\pi \int_{-a}^{a} \sqrt{1+\frac{x^{2}}{a^{2}-x^{2}}}\left[\left(b+\sqrt{a^{2}-x^{2}}\right)+\left(b-\sqrt{a^{2}-x^{2}}\right)\right]dx \\ &= 4ab\pi \int_{-a}^{a}\frac{dx}{\sqrt{a^{2}-x^{2}}} \\\end{align*}$$
    - Use trig substitution: $x = a\sin{\theta}$. $dx = a\cos{\theta}d\theta$
    - Adjust bounds: $[-a, a]\quad ⨠⨠ \quad \left[-\frac{\pi}{2}, \frac{\pi}{2}\right]$
      $$\begin{align*} 4ab\pi\int_{-a}^{a}\frac{dx}{\sqrt{a^{2}-x^{2}}} &= 4ab\pi \int_{-\frac{\pi}{2}}^{\frac{\pi}{2}}\frac{a\cos{\theta}}{\sqrt{a^{2}-a^{2}\sin^{2}\theta}}d\theta \\ &= 4ab\pi\int_{-\frac{\pi}{2}}^{\frac{\pi}{2}}\frac{a\cos\theta}{\sqrt{a^{2}\left(1-\sin^{2}\theta\right)}}d\theta \\&= 4ab\pi \int_{-\frac{\pi}{2}}^{\frac{\pi}{2}}\frac{a\cos\theta}{\sqrt{a^{2}\cos^{2}\theta}} d\theta \\&= 4ab\pi\left.\left[\theta\right]\right|_{-\frac{\pi}{2}}^{\frac{\pi}{2}} \\&= 4ab\pi^{2}\end{align*}$$
