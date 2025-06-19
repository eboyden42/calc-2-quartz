## Polar curves

#### Converting to polar: $\pi$-correction
Compute the polar coordinates of $\left(-\frac{1}{2},\,+\frac{\sqrt{3}}{2}\right)$ and of $\left(+\frac{\sqrt{2}}{2},\,-\frac{\sqrt{2}}{2}\right)$.

**Solution**

For $\left(-\frac{1}{2},\,\frac{\sqrt{3}}{2}\right)$ we observe first that it lies in Quadrant II. 

Next compute:

$$\tan^{-1}\left(\frac{\sqrt{3}/2}{-1/2}\right)\quad ⨠⨠ \quad \tan^{-1}\left(-\sqrt{3}\right)\quad ⨠⨠ \quad -\pi/3$$

This angle is in Quadrant IV. We *add $\pi$* to get the polar angle in Quadrant II:

$$\theta=\pi-\pi/3\quad ⨠⨠ \quad 2\pi/3$$

The radius is of course $1$ since this point lies on the unit circle. Therefore polar coordinates are $(r,\theta)=(1,2\pi/3)$.

For $\left(+\frac{\sqrt{2}}{2},\,-\frac{\sqrt{2}}{2}\right)$ we observe first that it lies in Quadrant IV. (No extra $\pi$ needed.)

Next compute: 

$$\tan^{-1}\left(\frac{-\sqrt{2}/2}{+\sqrt{2}/2}\right)\quad ⨠⨠ \quad \tan^{-1}(-1)\quad ⨠⨠ \quad -\pi/4$$

So the point in polar is $(1,-\pi/4)$.

#### Shifted circle in polar
For example, let’s convert a shifted circle to polar. Say we have the Cartesian equation: 

$$x^2+(y-3)^2=9$$

Then to find the polar we substitute $x=r\cos\theta$ and $y=r\sin\theta$ and simplify: 

$$\begin{gather*}x^2+(y-3)^2=9\\\\ ⨠⨠ \qquad r^2\cos^2\theta+(r\sin\theta-3)^2=9\\\\  ⨠⨠ \quad r^2\cos^2\theta+r^2\sin^2\theta-6r\sin\theta+9=9\\\\ ⨠⨠ \quad r^2(\sin^2\theta+\cos^2\theta)-6r\sin\theta=0\\\\ ⨠⨠ \qquad r^2-6r\sin\theta=0\qquad ⨠⨠ \qquad r=6\sin\theta\end{gather*}$$

So this shifted circle *is the polar graph of the polar function* $r(\theta)=6\sin\theta$.


## Calculus with polar curves

#### Finding vertical tangents to a limaçon
Let us find the vertical tangents to the limaçon (the cardioid) given by $r=1+\sin\theta$.

1. & Convert to Cartesian parametric.
    - Plug $r(\theta)$ into $x=r\cos\theta$ and $y=r\sin\theta$: $$r(\theta)=1+\sin\theta\quad ⨠⨠ \quad (x,y)=\Big((1+\sin\theta)\cos\theta,\;(1+\sin\theta)\sin\theta\Big)$$
2. && Compute $x'$ and $y'$.
    - Derivatives of both coordinates: $$\begin{gather*}(x',\,y')\quad ⨠⨠ \\\\ \Big(\cos\theta\cos\theta+(1+\sin\theta)(-\sin\theta),\;\cos\theta\sin\theta+(1+\sin\theta)\cos\theta\Big)\end{gather*}$$
    - Simplify: $$⨠⨠ \qquad \Big(\cos^2\theta-\sin^2\theta-\sin\theta,\;\cos\theta\,(1+2\sin\theta)\Big)$$
3. &&& The vertical tangents occur when $x'(\theta)=0$.
    - Set equation: $x'=0$: $$x'(\theta)=0\quad ⨠⨠ \quad \cos^2\theta-\sin^2\theta-\sin\theta=0$$
    - !! Solve equation.
        - Convert to *only $\sin\theta$*: $$⨠⨠ \quad (1-\sin^2\theta)-\sin^2\theta-\sin\theta=0$$
        - Substitute $A=\sin\theta$ and simplify: $$⨠⨠ \quad 1-2A^2-A=0\quad ⨠⨠ \quad 2A^2+A-1=0$$
        - Solve: $$\begin{gather*}A=\frac{-b\pm\sqrt{b^2-4ac}}{2a}\quad ⨠⨠ \\\\ \frac{-1\pm\sqrt{1-4\cdot2\cdot(-1)}}{2\cdot 2}\quad ⨠⨠ \quad \frac{1}{2},\,-1\end{gather*}$$
        - Solve for $\theta$: $$\begin{gather*}A=\sin\theta\quad ⨠⨠ \quad \sin\theta=\frac{1}{2},\,-1\\\\ ⨠⨠ \quad \theta=\frac{\pi}{6},\,\frac{5\pi}{6}\;(\text{for } 1/2)\quad\text{and}\quad \theta=\frac{3\pi}{2}\;(\text{for }-1)\end{gather*}$$
4. &&& Compute final points.
    - In polar coordinates, the final points are: $$\begin{gather*}(r,\theta)=(1+\sin\theta,\,\theta)\Big|_{\theta=\frac{\pi}{6},\,\frac{5\pi}{6},\,\frac{3\pi}{2}}\\\\ ⨠⨠ \quad \left(\frac{3}{2},\frac{\pi}{6}\right),\;\left(\frac{3}{2},\frac{5\pi}{6}\right),\;\left(0,\frac{3\pi}{2}\right)\end{gather*}$$
    - In Cartesian coordinates:
        - For $\theta=\frac{\pi}{6}$: $$\begin{gather*}(x,y)\Big|_{\theta=\frac{\pi}{6}}\quad ⨠⨠ \quad \Big((1+\sin\theta)\cos\theta,\,(1+\sin\theta)\sin\theta\Big)\Bigg|_{\theta=\frac{\pi}{6}}\\\\ ⨠⨠ \quad \left(\left(1+\frac{1}{2}\right)\frac{\sqrt{3}}{2},\;\left(1+\frac{1}{2}\right)\frac{1}{2}\right)\quad ⨠⨠ \quad \left(\frac{3\sqrt{3}}{4},\;\frac{3}{4}\right)\end{gather*}$$
        - For $\theta=\frac{5\pi}{6}$: $$\begin{gather*}(x,y)\Big|_{\theta=\frac{5\pi}{6}}\quad ⨠⨠ \quad \Big((1+\sin\theta)\cos\theta,\,(1+\sin\theta)\sin\theta\Big)\Bigg|_{\theta=\frac{5\pi}{6}}\\\\ ⨠⨠ \quad \left(\left(1+\frac{1}{2}\right)\frac{-\sqrt{3}}{2},\;\left(1+\frac{1}{2}\right)\frac{1}{2}\right)\quad ⨠⨠ \quad \left(-\frac{3\sqrt{3}}{4},\;\frac{3}{4}\right)\end{gather*}$$
        - For $\theta=\frac{3\pi}{2}$:  $$\begin{gather*}(x,y)\Big|_{\theta=\frac{3\pi}{2}}\quad ⨠⨠ \quad \Big((1+\sin\theta)\cos\theta,\,(1+\sin\theta)\sin\theta\Big)\Bigg|_{\theta=\frac{3\pi}{2}}\\\\ ⨠⨠ \quad \Big((1-1)\cdot 0,\;(1-1)\cdot(-1)\Big)\quad ⨠⨠ \quad (0,0)\end{gather*}$$
5. !! Correction: $(0,0)$ is a cusp.
    - The point $(0,0)$ at $\theta=\frac{3\pi}{2}$ is on the cardioid, but the curve is not smooth there, this is a cusp.
    - Still, the left- and right-sided tangents exists and are equal, so in a sense we can still say the curve has vertical tangent at $\theta=\frac{3\pi}{2}$.


#### Length of the inner loop
Consider the limaçon given by $r(\theta)=\frac{1}{2}+\cos\theta$. How long is its inner loop? Set up an integral for this quantity.

**Solution**

The inner loop is traced by the moving point when $\frac{2\pi}{3}\leq\theta\leq\frac{4\pi}{3}$. This can be seen from the graph: 
![500](Pasted%20image%2020241124160512.png)

Therefore the length of the inner loop is given by this integral: 

$$L=\int_{2\pi/3}^{4\pi/3}\sqrt{(-\sin\theta)^2+\left(\frac{1}{2}+\cos\theta\right)^2}\,d\theta\quad ⨠⨠ \quad \int_{2\pi/3}^{4\pi/3}\sqrt{5/4+\cos\theta}\,d\theta$$

#### Area between circle and limaçon
Find the area of the region enclosed between the circle $r_0(\theta)=1$ and the limaçon $r_1(\theta)=1+\cos\theta$.

**Solution**

First draw the region:
![200](Pasted%20image%2020241125135029.png)

The two curves intersect at $\theta=\pm \frac{\pi}{2}$. Therefore the area enclosed is given by integrating over $-\frac{\pi}{2}\leq\theta\leq+\frac{\pi}{2}$: 

$$\begin{gather*}A = \int_a^b\frac{1}{2}(r_1^2-r_0^2)\,d\theta\quad ⨠⨠ \quad \int_{-\pi/2}^{\pi/2}\frac{1}{2}\Big((1+\cos\theta)^2-1^2\Big)\,d\theta\\\\ ⨠⨠ \quad \frac{1}{2}\int_{-\pi/2}^{\pi/2}2\cos\theta+\cos^2\theta\,d\theta\quad ⨠⨠ \quad \int_{-\pi/2}^{\pi/2}\cos\theta+\frac{1}{4}\big(1+\cos(2\theta)\big)\,d\theta\\\\ ⨠⨠ \quad \left.\sin\theta+\frac{\theta}{4}+\frac{1}{8}\sin(2\theta)\right|_{-\pi/2}^{\pi/2}\quad ⨠⨠ \quad 2+\frac{\pi}{4}\end{gather*}$$


#### Area of small loops
Consider the following polar graph of $r(\theta)=1+2\cos(4\theta)$: 
![200](Pasted%20image%2020241125140024.png)

Find the area of the shaded region.

**Solution**

1. && Bounds for one small loop.
    - Lower left loop occurs first.
    - This loop when $1+2\cos(4\theta)\leq0$.
    - Solve this: $$\begin{gather*}1+2\cos(4\theta)\leq0\qquad ⨠⨠ \qquad \cos(4\theta)\leq-\frac{1}{2}\\\\ ⨠⨠ \qquad \frac{2\pi}{3}\leq 4\theta\leq \frac{4\pi}{3}\qquad ⨠⨠ \qquad \frac{\pi}{6}\leq \theta\leq \frac{\pi}{3}\end{gather*}$$
2. && Area integral.
    - Arrange and expand area integral: $$\begin{gather*}A = 4\int_\alpha^\beta\frac{1}{2}r(\theta)^2\,d\theta \quad ⨠⨠ \quad  4\int_{\pi/6}^{\pi/3}\frac{1}{2}\big(1+2\cos(4\theta)\big)^2\,d\theta\\\\ ⨠⨠ \quad 2\int_{\pi/6}^{\pi/3}1+4\cos(4\theta)+4\cos^2(4\theta)\,d\theta\end{gather*}$$
    - Simplify integral using power-to-frequency: $\cos^2A\rightsquigarrow \frac{1}{2}(1+\cos(2A))$ with $A=4\theta$: $$⨠⨠ \quad 2\int_{\pi/6}^{\pi/3}1+4\cos(4\theta)+4\cdot\frac{1}{2}\big(1+\cos(8\theta)\big)\,d\theta$$
    - Compute integral: $$\begin{gather*}⨠⨠ \quad \left.6\theta+2\sin(4\theta)+\frac{1}{4}\sin(8\theta)\right|_{\pi/6}^{\pi/3} \\\\ ⨠⨠ \quad   \pi-\frac{3\sqrt{3}}{2}\end{gather*}$$


#### Overlap area of circles
Compute the area of the overlap between crossing circles. For concreteness, suppose one of the circles is given by $r(\theta)=\sin\theta$ and the other is given by $r(\theta)=\cos\theta$.

**Solution**

Here is a drawing of the overlap:
![200](Pasted%20image%2020241125142911.png)

1. & Notice: total overlap area = $2\times$ area of red region.
2. & Bounds: $0\leq\theta\leq\frac{\pi}{4}$.
3. && Apply area formula for the red region.
    - Area formula applied to $r(\theta)=\sin\theta$: $$A=\int_\alpha^\beta\frac{1}{2}r(\theta)^2\,d\theta\qquad ⨠⨠ \qquad \int_0^{\pi/4}\frac{1}{2}\sin^2\theta\,d\theta$$
    - Power-to-frequency: $\sin^2\theta\rightsquigarrow\frac{1}{2}\big(1-\cos(2\theta)\big)$: $$\begin{gather*}⨠⨠ \quad \int_0^{\pi/4}\frac{1}{4}\big(1-\cos(2\theta)\big)\,d\theta \\\\ ⨠⨠ \quad \frac{1}{4}\theta-\left.\frac{1}{8}\sin(2\theta)\right|_0^{\pi/4}\quad ⨠⨠ \quad \frac{\pi}{16}-\frac{1}{8}\end{gather*}$$
    - Double the result to include the black region: $$⨠⨠ \quad \frac{\pi}{8}-\frac{1}{4}$$


