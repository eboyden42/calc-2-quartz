## Parametric curves

#### Parametric circles
The standard equation of a circle of radius $R$ centered at the point $(h,k)$: 

$$(x-h)^2+(y-k)^2=R^2$$

This equation says that the *distance* from a point $(x,y)$ on the circle to the center point $(h,k)$ equals $R$. This fact defines the circle.

Parametric coordinates for the circle: 

$$x=h+R\cos t,\qquad y=k+R\sin t,\qquad t\in[0,2\pi)$$

For example, the unit circle $x^2+y^2=1$ is parametrized by $x=\cos t$ and $y=\sin t$.

#### Parametric lines
Parametric coordinate functions for a line: 

$$x=a+rt,\qquad y=b+st,\qquad t\in(-\infty,+\infty)$$

Compare this to the graph of linear function: 

$$y=mx+b\qquad \text{some }m,b$$

Vertical lines cannot be described as the graph of a function. We must use $x=a$.

---

Parametric lines can describe all lines equally well, including horizontal and vertical lines.

A vertical line $x=a$ is achieved by setting $s=0$ and $r\neq 0$.

A horizontal line $y=b$ is achieved by setting $r=0$ and $s\neq 0$.

A non-vertical line $y=mx+b$ may be achieved by setting $s=m$ and $r=1$, and $a=0$.

---

Assuming that $r\neq 0$, the parametric coordinate functions describe a line satisfying: 

$$\begin{gather*}y=b+s\left(\frac{x-a}{r}\right)\\\\ ⨠⨠ \quad y=\frac{s}{r}\cdot x+\left(b-\frac{s}{r}\cdot a\right)\end{gather*}$$

and therefore the slope is $m=\frac{s}{r}$ and the $y$-intercept is $b-\frac{s}{r}\cdot a$.

---

The point-slope construction of a line has a parametric analogue: 

$$\begin{array}{c}\text{point-slope line:}\\\\ y-a=m(x-b)\qquad\qquad (x,y)=(a+t,\,b+mt)\end{array}$$

![center|200](Pasted%20image%2020241123123714.png)

#### Parametric ellipses
The general equation of an ellipse centered at $(h,k)$ with half-axes $a$ and $b$ is: 

$$\left(\frac{x-h}{a}\right)^2+\left(\frac{y-k}{b}\right)^2=1$$

This equation represents a *stretched unit circle*:
- by $a$ in the $x$-axis
- by $b$ in the $y$-axis

Parametric coordinate functions for the general ellipse: 

$$x=h+a\cos t,\qquad y=k+b\sin t,\qquad t\in[0,2\pi)$$

#### Parametric cycloids
The cycloid is the curve traced by a pen attached to the rim of a wheel as it rolls.

![center|400](Pasted%20image%2020241123125715.png)

It is easy to describe the cycloid parametrically. Consider the geometry of the situation:

![center|350](Pasted%20image%2020241123124907.png)

![center|250](Pasted%20image%2020241123125010.png)

The center $C$ of the wheel is moving rightwards at a constant speed of $1$, so its position is $(t,1)$. The angle is revolving at the same constant rate of $1$ (in *radians*) because the *radius* is $1$.

The triangle shown has base $\sin t$, so the $x$ coordinate is $t-\sin t$. The $y$ coordinate is $1-\cos t$.

So the coordinates of the point $P=(x,y)$ are given parametrically by:

$$x=t-\sin t,\qquad y=1-\cos t,\qquad t>0$$

If the circle has another radius, say $R$, then the parametric formulas change to: 

$$x=Rt-R\sin t,\qquad y=R-R\cos t,\qquad t>0$$


## Calculus with parametric curves

#### Tangent to a cycloid
Find the tangent line (described parametrically) to the cycloid $(4t-4\sin t,\,4-4\cos t)$ when $t=\pi/4$.

**Solution**

Compute $x'$ and $y'$.

Find $x'(t)$: 

$$x(t)=4t-4\sin t\quad ⨠⨠ \quad x'(t)=4-4\cos t$$

Find $y'(t)$: 

$$y(t)=4-4\cos t \quad ⨠⨠ \quad y'(t)=4\sin t$$

---

Plug in $t=\pi/4$: 

$$x'(\pi/4)\quad ⨠⨠ \quad  4-4\cos(\pi/4)\quad ⨠⨠ \quad  4-2\sqrt{2}$$

Plug in $t=\pi/4$: 

$$y'(\pi/4)\quad ⨠⨠ \quad 4\sin(\pi/4)\quad ⨠⨠ \quad 2\sqrt{2}$$

---

Apply formula: $\;\displaystyle\frac{dy}{dx}=\frac{y'}{x'}$: 

Calculate $\frac{dy}{dx}$ at $t=\pi/4$: 

$$\frac{dy}{dx}(\pi/4)=\frac{y'(\pi/4)}{x'(\pi/4)}\qquad ⨠⨠ \qquad \frac{2\sqrt{2}}{4-2\sqrt{2}}$$

Simplify: 

$$\begin{gather*}⨠⨠ \qquad \frac{2\sqrt{2}}{4-2\sqrt{2}}\cdot\frac{4+2\sqrt{2}}{4+2\sqrt{2}}\\\\⨠⨠ \qquad \frac{8\sqrt{2}+8}{16-8}\quad ⨠⨠ \quad \sqrt{2}+1\end{gather*}$$

So: $$\;\left.\frac{dy}{dx}\right|_{t=\pi/4}\;=\; \sqrt{2}+1$$
This is the slope $m$ for our line.

---

Need the point $P$ for our line. Find $(x,y)$ at $t=\pi/4$.

Plug $t=\pi/4$ into parametric formulas: 

$$\begin{gather*}\big(x(t),\,y(t)\big)\Big|_{t=\pi/4}\quad ⨠⨠ \quad \left(4\frac{\pi}{4}-4\sin(\pi/4),\;4-4\cos(\pi/4)\right) 
\\\\ ⨠⨠ \quad \left(\pi-2\sqrt{2},4-2\sqrt{2}\right)\end{gather*}$$

---

Point-slope formulation of tangent line: 

$$x=a+t,\quad y=b+mt$$

Inserting our data:

$$x\;=\; (\pi-2\sqrt{2})+t,\qquad y\;=\; (4-2\sqrt{2})+(\sqrt{2}+1)t$$


#### Vertical and horizontal tangents of the circle
Consider the circle parametrized by $x=\cos t$ and $y=\sin t$. Find the points where the tangent lines are vertical or horizontal.

**Solution**

For the points with vertical tangent line, we find where the moving point has $x'(t)=0$ (purely vertical motion): 

$$\begin{gather*}x'(t)=-\sin t,\\\\ x'(t)=0\qquad ⨠⨠ \qquad -\sin t=0\\\\ ⨠⨠ \qquad t=0,\,\pi\end{gather*}$$

The moving point is at $(1,0)$ when $t=0$, and at $(-1,0)$ when $t=\pi$.

---

For the points with horizontal tangent line, we find where the moving point has $y'(t)=0$ (purely horizontal motion): 

$$\begin{gather*}y'(t)=\cos t,\\\\ y'(t)=0\qquad ⨠⨠ \qquad \cos t=0\\\\ ⨠⨠ \qquad t=\frac{\pi}{2},\;\frac{3\pi}{2}\end{gather*}$$

The moving point is at $(0,1)$ when $t=\pi/2$, and at $(0,-1)$ when $t=3\pi/2$.


#### Finding the point with specified slope
Consider the parametric curve given by $(x,y)=(t^2,\,t^3)$. Find the point where the slope of the tangent line to this curve equals 5.

**Solution**

Compute the derivatives: 

$$x'(t)\;=\; 2t,\qquad y'(t)\;=\; 3t^2$$

Therefore the slope of the tangent line, in terms of $t$: 

$$\begin{gather*}m=\frac{dy}{dx}\;=\; \frac{y'(t)}{x'(t)}\\\\ ⨠⨠ \quad\frac{3t^2}{2t}\quad ⨠⨠ \quad\frac{3}{2}t\end{gather*}$$

---

Set up equation: 

$$\begin{gather*}m\quad=\quad 5\\\\ \frac{3}{2}t\quad=\quad 5\end{gather*}$$

Solve. Obtain $t=\frac{10}{3}$.

---

Find the point: 

$$(x,y)\Big|_{t=10/3}\quad ⨠⨠ \quad \left(\frac{100}{9},\;\frac{1000}{27}\right)$$


#### Perimeter of a circle
The perimeter of the circle $(R\cos t, R\sin t)$ is easily found. We have $(x',y')=(-R\sin t, R\cos t)$, and therefore: 

$$
\begin{gathered}
(x')^2+(y')^2=(-R\sin t)^2+(R\cos t)^2\qquad \\\\
⨠⨠ \qquad R^2\sin^2t+R^2\cos^2t\qquad ⨠⨠ \qquad R^2\\\\ ds=\sqrt{(x')^2+(y')^2}\,dt=R\,dt
\end{gathered}
$$

---

Integrate around the circle: 

$$
\begin{gathered}
\text{Perimeter} \quad=\quad  \int_0^{2\pi}ds\qquad ⨠⨠ \qquad \int_0^{2\pi}R\,dt\\\\ 
⨠⨠ \qquad Rt\Big|_0^{2\pi}=2\pi R
\end{gathered}
$$

#### Perimeter of an asteroid
Find the perimeter length of the ‘asteroid’ given parametrically by $(x,y)=\left(a\cos^3\theta,\,a\sin^3\theta\right)$ for $a=2$.

![center|200](Pasted%20image%2020241123195858.png)

**Solution**

Notice: Throughout this problem we use the parameter $\theta$ instead of $t$. This does *not* mean we are using polar coordinates!

Compute the derivatives in $\theta$: 

$$\left(x',y'\right)=\left(3a\cos^2\theta\sin\theta,\,3a\sin^2\theta\cos\theta\right)$$

---

Compute the infinitesimal arc element.

$$\begin{gather*}(x')^2+(y')^2\quad ⨠⨠ \quad 9a^2\cos^4\theta\sin^2 \theta+9a^2\sin^4\theta\cos^2\theta \\\\ \qquad ⨠⨠ \qquad 9a^2\sin^2\theta\cos^2\theta \left(\cos^2\theta+ \sin^2\theta\right) \\\\ \qquad ⨠⨠ \qquad 9a^2\sin^2\theta \cos^2\theta\end{gather*}$$

Plug into the arc element, simplify: 

$$\begin{gather*}ds=\sqrt{(x')^2+y')^2}\,d\theta\\\\ ⨠⨠ \quad \sqrt{9a^2\sin^2\theta\cos^2\theta}\,d\theta\\\\ ⨠⨠ \qquad ds=3a\big|\sin\theta\cos\theta\big|\,d\theta\end{gather*}$$

---

Bounds of integration?

Easiest to use $\theta\in[0,\pi/2]$. This covers one edge of the asteroid. Then multiply by 4 for the final answer.

On the interval $\theta\in[0,\pi/2]$, the factor $3a\sin\theta\cos\theta$ is *positive*. So we can drop the absolute value and integrate directly.

> [!warning] Absolute values matter!
> If we tried to integrate on the whole range $\theta\in[0,2\pi]$, then $3a\sin\theta\cos\theta$ really does change sign.
> 
> To perform integration properly with these absolute values, we’d need to convert to a piecewise function by adding appropriate minus signs.

---

Integrate the arc element: 

$$\begin{gather*}\int_0^{\pi/2}ds\quad ⨠⨠ \quad \int_0^{\pi/2} 3a\sin\theta\cos\theta\,d\theta\\\\ ⨠⨠ \quad 3a\int_{u=0}^{1}u\,du \tag{$u=\sin\theta$}\\\\ ⨠⨠ \quad 3a\left.\frac{u^2}{2}\right|_0^1 \quad ⨠⨠ \quad \frac{3a}{2}\end{gather*}$$

Finally, multiply by 4 to get the total perimeter: $\colorbox{aqua}{L=6a}$

#### Speed, distance, displacement
The parametric curve $\left(t,\frac{2}{3}t^{3/2}\right)$ describes the position of a moving particle ($t$ measuring seconds).
(a) What is the speed function?

Suppose the particle travels for $8$ seconds starting at $t=0$.
(b) What is the total distance traveled?
(c) What is the total displacement?

**Solution**

(a)
Compute *derivatives*: 

$$\left(x',\,y'\right)=\left(1,\,t^{1/2}\right)$$

---

Now compute the *speed*.

Find sum of squares: 

$$(x')^2+(y')^2=1+(t^{1/2})^2=1+t$$

Get the speed function: 

$$v(t)=\sqrt{(x')^2+(y')^2}=\sqrt{1+t}$$

---

(b)
*Distance traveled* by using *speed*.
Compute total distance traveled function: 

$$s(t)=\int_{u=0}^t\sqrt{1+u}\,du$$

---

Integrate.

Substitute $w=1+u$ and $dw=du$.

New bounds are $1$ and $1+t$.

Calculate: 

$$
\begin{gathered}
⨠⨠ \quad \int_{1}^{1+t}\sqrt{w}\,dw\\\\ ⨠⨠ \quad \frac{2}{3}w^{3/2}\Bigg|_1^{1+t}\quad ⨠⨠ \quad \frac{2}{3}\left((1+t)^{3/2}-1\right)
\end{gathered}
$$

---

Insert $t=8$ for the answer.

The distance traveled up to $t=8$ is: 

$$s(8)=\frac{2}{3}\left(9^{3/2}-1\right)\quad ⨠⨠ \quad \frac{2}{3}(27-1)\quad ⨠⨠ \quad \frac{52}{3}$$

This is our final answer.

---

(c)

Displacement formula: $d=\sqrt{(x_1-x_0)^2+(y_1-y_0)^2}$

Pythagorean formula for distance between given points.

---

Compute starting and ending points.

For starting point, insert $t=0$: 

$$\big(x(t),y(t)\big)\Big|_{t=0}\qquad ⨠⨠ \qquad \left(t,\frac{2}{3}t^{3/2}\right) \Bigg|_{t=0} \qquad ⨠⨠ \qquad (0,0)$$

For ending point, insert $t=8$: 

$$
\begin{gathered}
\big(x(t),y(t)\big)\Big|_{t=8}\quad ⨠⨠ \quad \left(t,\frac{2}{3}t^{3/2}\right)\Bigg|_{t=8}\\\\ 
⨠⨠ \quad \left(8,\frac{2}{3}8^{3/2}\right)\quad ⨠⨠ \quad \left(8,\frac{32\sqrt{2}}{3}\right)
\end{gathered}
$$

---

Plug points into distance formula.

Insert $(0,0)$ and $\left(8,32\sqrt{2}\big/3\right)$: 

$$
\begin{gathered}
\sqrt{8^2+\left(\frac{32\sqrt{2}}{3}\right)^2}\qquad ⨠⨠ \qquad \sqrt{64+\frac{2048}{9}}\\\\ 
⨠⨠ \qquad \frac{\sqrt{2624}}{3}
\end{gathered}
$$

This is our final answer.


#### Surface of revolution - parametric circle
By revolving the unit upper semicircle about the $x$-axis, we can compute the surface area of the unit sphere.

The parametrization of the unit upper semicircle is: $\;(x,y)=(\cos t,\,\sin t)$.

The derivative is: $\;(x',y')=(-\sin t,\,\cos t)$.

---

Therefore, the arc element: 

$$
\begin{gathered}
ds=\sqrt{(x')^2+(y')^2}\,dt\\\\ 
⨠⨠ \quad \sqrt{(-\sin t)^2+(\cos t)^2}\,dt\quad ⨠⨠ \quad dt
\end{gathered}
$$

---

Now for $R$ we choose $R=y(t)=\sin t$ because we are revolving about the $x$-axis.

Plugging all this into the integral formula and evaluating gives: 

$$A=\int_0^{\pi} 2\pi\sin t\,dt\quad ⨠⨠ \quad -2\pi\cos t\Big|_0^\pi\quad ⨠⨠ \quad 4\pi$$

Notice: This method is a little easier than the method using the graph $y=\sqrt{1-x^2}$.

#### Surface of revolution - parametric curve
Set up the integral which computes the surface area of the surface generated by revolving about the $x$-axis the curve $(t^3,\,t^2-1)$ for $0\leq t\leq 1$.

**Solution**

For revolution about the $x$-axis, we set $R=y(t)=t^2-1$.

Then compute $ds$: 

$$
\begin{gathered}
ds=\sqrt{(x')^2+(y')^2}\quad ⨠⨠ \quad \sqrt{(3t^2)^2+(2t)^2}\quad ⨠⨠ \quad \sqrt{9t^4+4t^2}\\\\  ⨠⨠ \quad \sqrt{t^2(9t^2+4)}\quad ⨠⨠ \quad t\sqrt{9t^2+4}
\end{gathered}
$$

Therefore the desired integral is: 

$$A=\int_0^1 2\pi R\,ds\quad ⨠⨠ \quad \int_0^1 2\pi (t^2-1)t\sqrt{9t^2+4}\,dt$$

