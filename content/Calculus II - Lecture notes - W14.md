---
cssclasses:
  - hide-embedded-header
title: W14 Notes
---
## Polar curves
Videos, Organic Chemistry Tutor
- [Polar coordinates intro](https://www.youtube.com/watch?v=aSdaT62ndYE&t=9s)
- [Graphing polar curves](https://www.youtube.com/watch?v=jO4lwddfeDA)

### 01 Theory - Polar points, polar curves

Polar coordinates are pairs of numbers $(r,\theta)$ which identify points in the plane in terms of *distance to origin* and *angle from $+x$-axis*: 

![center|500](Pasted%20image%2020241124134632.png)


> [!concept] Converting $\mathrm{Polar}\leftrightarrow \mathrm{Cartesian}$
> $$\begin{array}{l}\text{Polar}\to\text{Cartesian}\\x=r\cos\theta\\ y=r\sin\theta\end{array}\qquad\qquad \begin{array}{l}\text{Cartesian}\to\text{Polar}\\r=\sqrt{x^2+y^2}\\ \tan\theta=\displaystyle\frac{y}{x}\quad (x\neq 0)\end{array}$$

---

Polar coordinates have *many redundancies*: unlike Cartesian which are unique!

- For example: $(r,\theta)=(r,\theta+2\pi)$
    - And therefore also $(r,\theta)=(r,\theta-2\pi)$ (negative $\theta$ can happen)
- For example: $(-r,\theta)=(r,\theta+\pi)$ for every $r,\,\theta$
- For example: $(0,\theta)=(0,0)$ for any $\theta$

Polar coordinates *cannot be added*: they are not vector components!

- For example $(5,\pi/3)+(2,\pi/6)\neq (7,\pi/2)$
- Whereas Cartesian coordinates can be added: $(1,4)+(2,-2)=(3,2)$

---

⚠️ The transition formulas $\text{Cartesian}\to\text{Polar}$ require careful choice of $\theta$.

- The standard definition of $\tan^{-1}\left(\frac{y}{x}\right)$ sometimes gives *wrong $\theta$*
    - This is because it uses the restricted domain $\theta\in (-\pi/2,\pi/2)$; the polar interpretation is: only points in Quadrant I and Quadrant IV (SAFE QUADRANTS)
- Therefore: *check signs* of $x$ and $y$ to see *which quadrant*, maybe need $\pi$-correction!
    - Quadrant I or IV: polar angle is $\tan^{-1}\left(\frac{y}{x}\right)$ 
    - $\colorbox{orange}{Quadrant II or III:}$ polar angle is $\tan^{-1}\left(\frac{y}{x}\right)+\pi$ 

![center|400](Pasted%20image%2020241124143709.png)

---

Equations (as well as points) can also be converted to polar.

For $\text{Cartesian}\to\text{Polar}$, look for cancellation from $\cos^2\theta+\sin^2\theta=1$.

For $\text{Polar}\to\text{Cartesian}$, try to keep $\theta$ inside of trig functions.
- For example: $$r=\sin^2\theta\qquad ⨠⨠ \qquad  \sqrt{x^2+y^2}=\left(\frac{y}{\sqrt{x^2+y^2}}\right)^2$$

### 02 Illustration

> [!mexample] Converting to polar: $\pi$-correction
> 
> ![Converting to polar: $\pi$-correction](Calculus/2025%20Spring/W14%20-%20Examples.md#Converting%20to%20polar%20$%20pi$-correction)
> 

> [!mexample] Shifted circle in polar
> 
> ![Shifted circle in polar](Calculus/2025%20Spring/W14%20-%20Examples.md#Shifted%20circle%20in%20polar)
> 


### 03 Theory - Polar limaçons

To draw the polar graph of some function, it can help to first draw the Cartesian graph of the function. (In other words, set $y=r$ and $x=\theta$, and draw the usual graph.) By tracing through the points on the Cartesian graph, one can visualize the trajectory of the polar graph.

This Cartesian graph may be called a **graphing tool** for the polar graph.

---

A limaçon is the polar graph of $r(\theta)\;=\; a+b\cos\theta$.

*Any* limaçon shape can be obtained by adjusting $c$ in this function (and rescaling): 

$$r=1+c\cos\theta$$

Limaçon satisfying $r(\theta)=1$: unit circle.

Limaçon satisfying $r(\theta)=2+\cos\theta$: ‘outer loop’ circle with ‘dimple’: 

![center|500](Pasted%20image%2020241124143142.png)

Limaçon satisfying $r(\theta)=1+\cos\theta$: ‘cardioid’ $=$ ‘outer loop’ circle with ‘dimple’ that creates a cusp: 

![center|500](Pasted%20image%2020241124143109.png)

Limaçon satisfying $r(\theta)=1+2\cos\theta$: ‘dimple’ pushes past cusp to create ‘inner loop’: 

![center|500](Pasted%20image%2020241124143207.png)

Limaçon satisfying $r(\theta)=\cos\theta$: ‘inner loop’ only, no outer loop exists: 

![center|500](Pasted%20image%2020241124142824.png)

Limaçon satisfying $r(\theta)=1+2\sin\theta$: ‘inner loop’ and ‘outer loop’ and rotated $\circlearrowleft 90^\circ$: 

![center|500](Pasted%20image%2020241124143242.png)

---

Transitions between limaçon types, $r(\theta)\;=\; 1+c\sin\theta$: 

![center|700](Pasted%20image%2020241124144416.png)

Notice the transition points at $|c|=0.5$ and $|c|=1$: 

The *flat spot* occurs when $c=\pm0.5$
- Smaller $c$ gives *convex shape*

The *cusp* occurs when $c=\pm 1$
- Smaller $c$ gives *dimple* (assuming $|c|>0.5$)
- Larger $c$ gives *inner loop*

### 04 Theory - Polar roses

Roses are polar graphs of this form: 

$$r\;=\; \cos(\theta),\qquad r\;=\; \sin(2\theta),\qquad r\;=\; \sin(3\theta),\qquad r\;=\; \sin(4\theta)$$

![center|700](Pasted%20image%2020241124145202.png)

The pattern of petals: 
- $n=2k$ (even): obtain $2n$ petals
    - These petals traversed *once*
- $n=2k+1$ (odd): obtain $n$ petals
    - These petals traversed *twice*
- Either way: total-petal-traversals: always $2n$


## Calculus with polar curves

### 05 Theory - Polar tangent lines, arclength

> [!concept] Polar arclength formula
> The arclength of the polar graph of $r(\theta)$, for $\theta\in[\theta_0,\,\theta_1]$: 
> 
> $$L\quad=\quad \int_{\theta_0}^{\theta_1}\sqrt{r'(u)^2+r(u)^2}\,du$$

To derive this formula, *convert to Cartesian* with parameter $\theta$: 

$$r=r(\theta)\quad ⨠⨠ \quad (x,y)=(r\cos\theta,\,r\sin\theta)$$

From here you can apply the familiar arclength formula with $\theta$ in the place of $t$.

> [!extra] Extra - Derivation of polar arclength formula
> Let $r=r(\theta)$ and convert to parametric Cartesian, so $x(\theta)=r\cos\theta$ and $y(\theta)=r\sin\theta$.
> 
> Then: 
> 
> $$\begin{gather*}ds=\sqrt{(x')^2+(y')^2}\,d\theta\\\\ x'=(r\cos\theta)'\quad ⨠⨠ \quad r'\cos\theta-r\sin\theta\\y'=(r\sin\theta)'\quad ⨠⨠ \quad r'\sin\theta+r\cos\theta\end{gather*}$$
> 
> Therefore: 
> 
> $$\begin{align*}(x')^2+(y')^2\quad ⨠⨠ \quad &\phantom{,+} r'^2\cos^2\theta-2rr'\cos\theta\sin\theta+r^2\sin^2\theta\\&+r'^2\sin^2\theta+2rr'\sin\theta\cos\theta+r^2\cos^2\theta\\\\ &= r'^2+r^2\end{align*}$$
> 
> Therefore: 
> 
> $$ds=\sqrt{(x')^2+(y')^2}\,d\theta\qquad ⨠⨠ \qquad \sqrt{r'^2+r^2}\,d\theta$$
> 
> Therefore: 
> 
> $$L\quad=\quad \int_{\theta_0}^{\theta_1}\sqrt{r'(u)^2+r(u)^2}\,du$$


### 06 Illustration

> [!mexample] Finding vertical tangents to a limaçon
> 
> ![Finding vertical tangents to a limaçon](Calculus/2025%20Spring/W14%20-%20Examples.md#Finding%20vertical%20tangents%20to%20a%20limaçon)
> 

> [!mexample] Length of the inner loop
> 
> ![Length of the inner loop](Calculus/2025%20Spring/W14%20-%20Examples.md#Length%20of%20the%20inner%20loop)
> 

### 07 Theory - Polar area

> [!concept] Sectorial area from polar curve
> $$A\quad=\quad \int_\alpha^\beta \frac{1}{2}r(\theta)^2\,d\theta$$

The “area under the curve” concept for graphs of functions in Cartesian coordinates translates to a “sectorial area” concept for polar graphs. To compute this area using an integral, we divide the region into Riemann sums of small sector slices.

![center|400](Pasted%20image%2020241124161226.png)

![center|200](Pasted%20image%2020241124161246.png)

To obtain a formula for the whole area, we need a formula for the area of each sector slice.

> [!note] Area of sector slice
> Let us verify that the area of a sector slice is $\displaystyle\frac{1}{2}r^2\theta$.
> 
> ![center|200](Pasted%20image%2020241124161514.png)
> 
> Take the angle $\theta$ in radians and divide by $2\pi$ to get the *fraction of the whole disk*.
> 
> Then multiply this fraction by $\pi r^2$ (whole disk area) to get the *area of the sector slice*. 
> 
> $$\frac{\theta}{2\pi}\cdot \pi r^2\quad ⨠⨠ \quad \frac{1}{2}r^2\theta$$

Now use $d\theta$ and $r(\theta)$ for an infinitesimal sector slice, and integrate these to get the total area formula: 

$$A\quad=\quad \int_\alpha^\beta \frac{1}{2}r(\theta)^2\,d\theta$$

---

One easily verifies this formula for a circle.

Let $r(\theta)=R$ be a constant. Then: 

$$\text{Area of circle}\quad=\quad \int_0^{2\pi}\frac{1}{2}R^2\,d\theta\quad ⨠⨠ \quad \frac{1}{2}R^2\theta\Bigg|_0^{2\pi}\quad ⨠⨠ \quad R^2\pi$$

---

The sectorial area *between curves*: 

> [!concept] Sectorial area between polar curves
> $$A\quad=\quad \int_\alpha^\beta\frac{1}{2}\Big(r_1(\theta)^2-r_0(\theta)^2\Big)\,d\theta$$

> [!warning] Subtract *after* squaring, not before!
> This aspect is *not* similar to the Cartesian version: $\;\displaystyle\int f-g\,dx$

### 08 Illustration

> [!mexample] Area between circle and limaçon
> 
> ![Area between circle and limaçon](Calculus/2025%20Spring/W14%20-%20Examples.md#Area%20between%20circle%20and%20limaçon)
> 

> [!mexample] Area of small loops
> 
> ![Area of small loops](Calculus/2025%20Spring/W14%20-%20Examples.md#Area%20of%20small%20loops)
> 

> [!mexample] Overlap area of circles
> 
> ![Overlap area of circles](Calculus/2025%20Spring/W14%20-%20Examples.md#Overlap%20area%20of%20circles)
> 

