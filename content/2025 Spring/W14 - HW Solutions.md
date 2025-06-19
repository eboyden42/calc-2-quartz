#### 04 - Arclength of one loop of a rose
Consider the graph of the polar curve $r=2\cos 3\theta$.

Set up an integral which computes the arclength of one loop of this curve.

**Solution**

1. & Find when $r = 0$ for the bounds of the integral. $$2\cos{3\theta} = 0 \quad ⨠⨠ \quad 3\theta = \frac{\pi}{2}, \frac{3\pi}{2} \quad⨠⨠\quad \theta = \frac{\pi}{6}, \frac{\pi}{2}$$
2. && Set up integral. $$\ell = \int_{\frac{\pi}{6}}^{\frac{\pi}{2}}\sqrt{r^{2}+\left(\frac{dr}{d\theta}\right)^{2}}d\theta = \int_{\frac{\pi}{6}}^{\frac{\pi}{2}}\sqrt{4\cos^{2}{3\theta}+36\sin^{2}{3\theta}}d\theta$$


#### 07 - Sketching limaçons
Sketch the graphs of the following polar functions: 

(a) $r = 2 + \sin{\theta}$; $\quad$ (b) $r = 2 + \cos{\theta}$; $\quad$ (c) $r = 1 + 2\sin{\theta}$; $\quad$ (d) $r = 3 + 3\cos{\theta}$

**Solution**

(a)
![200](Pasted%20image%2020241204182316.png)

(b)
![200](Pasted%20image%2020241204185633.png)

(c)
![200](Pasted%20image%2020241204185657.png)

(d)
![200](Pasted%20image%2020241204185723.png)


#### 08 - Sketching roses
Sketch the graphs of the following polar functions.
Use numbers to label the *order* in which the leaves/loops are traversed.

(a) $r = \sin{2\theta}$; $\quad$ (b) $r = \sin{3\theta}$; $\quad$ (c) $r = 2\cos{2\theta}$

**Solution**

(a)
![200](Pasted%20image%2020241204185823.png)

(b)
![200](Pasted%20image%2020241204185841.png)

(c)
![200](Pasted%20image%2020241204185902.png)


#### 10 - Polar coordinates - lunar areas
(a) Find the area of the green region.

(b) Find the area of the yellow region.

**Solution**

**(a)**
1. & Find the angle of the line of intersection between the two curves in the first quadrant. $$\sqrt{2}\cos \theta = 1\quad ⨠⨠\quad \theta = \frac{\pi}{4}$$
2. & Compute the area below the line of intersection and above the $x$-axis. $$\int_{0}^{\frac{\pi}{4}}\frac{1}{2}\left(1^{2}\right)d\theta = \left.\frac{\theta}{2}\right|^{\frac{\pi}{4}}_{0} = \frac{\pi}{8}$$
3. && Compute the area above the line of intersection and the upper half of the curve. $$\int_{\frac{\pi}{4}}^{\frac{\pi}{2}} \frac{1}{2}\left(\sqrt{2}\cos{2\theta}\right)^{2}d\theta = \int_{\frac{\pi}{4}}^{\frac{\pi}{2}}\frac{1}{2}(1 + \cos{2\theta})d\theta = \left.\left[\frac{\theta}{2}+\frac{\sin{2\theta}}{4}\right]\right|^{\frac{\pi}{2}}_{\frac{\pi}{4}} = \frac{\pi}{4} - \frac{\pi}{8} - \frac{1}{4} = \frac{\pi}{8} - \frac{1}{4}$$
4. & Add both areas and multiply by two (to account for the part in the fourth quadrant). $$A_{G} = 2\left(\frac{\pi}{8} + \frac{\pi}{8} - \frac{1}{4}\right) = \frac{\pi}{2} - \frac{1}{2}$$

**(b)**
1. && Compute the integral from the $x$-axis to the line of intersection, subtracting the inner radius from the outer radius. $$\int_{0}^{\frac{\pi}{4}} \frac{1}{2}\left(\left(\sqrt{2}\cos{\theta}\right)^{2}-(1)^{2}\right)d\theta = \int_{0}^{\frac{\pi}{4}}\frac{1}{2}(\cos{2\theta})d\theta = \left.\frac{\sin{2\theta}}{4}\right|^{\frac{\pi}{4}}_{0}=\frac{1}{4}$$
2. & Multiply by two to account for the part in the fourth quadrant to find the total area. $$A_{Y} = 2\left(\frac{1}{4}\right) = \frac{1}{2}$$

#### 11 - Pickup region of a microphone - limaçon area
The pickup region of a microphone is described by a limaçon with equation $r=8+8\sin\theta$, and part of the region is on a stage.

Find the area of the part of the region on the stage.

**Solution**

1. && Find the intersection between the line $y = 6$ and the curve.
    - $y = 6 \quad ⨠⨠\quad r = 6\csc{\theta}$
    - $$\begin{align*}8+8\sin{\theta} &= 6\csc{\theta} \\ 8\sin{\theta}+8\sin^{2}{\theta} &= 6 \\ 4\sin^{2}\theta+4\sin{\theta}-3 &= 0 \\ \sin{\theta} &= \frac{-4\pm8}{8}=-\frac{1}{2}\pm 1\end{align*}$$
    - So, $\sin{\theta} = \frac{1}{2}$ and $\theta = \frac{\pi}{6}$.
2. && Find the area.  $$\begin{align*}A &= 2\int_{\frac{\pi}{6}}^{\frac{\pi}{2}}\frac{1}{2}\left[(8+8\sin{\theta})^{2}-(6\csc{\theta})^{2}\right]d\theta \\ &= \int_{\frac{\pi}{6}}^{\frac{\pi}{2}}64+128\sin{\theta}+32-32\cos{2\theta}-36\csc^{2}{\theta}d\theta \\ &= \left.\left[96\theta-128\cos{\theta}-16\sin{2\theta}+36\cot{\theta}\right]\right|^{\frac{\pi}{2}}_{\frac{\pi}{6}} \\ &= 48\pi-16\pi+36\sqrt{3}=32\pi +36\sqrt{3} \end{align*}$$


#### 12 - Area of an inner loop
A limaçon is given as the graph of the polar curve $r=1+2\sin\theta$.

Find the area of the inner loop of this limaçon.

**Solution**

1. & Find when $r = 0$ to determine the bounds of our area integral. $$\begin{gather*}1 + 2\sin{\theta} = 0 \quad ⨠⨠ \quad \sin{\theta}=-\frac{1}{2} \\\\ ⨠⨠ \quad\theta = \frac{7\pi}{6},\frac{11\pi}{6}\end{gather*}$$
2. && Compute area. $$\begin{align*}A &= \int_{\frac{7\pi}{6}}^{\frac{11\pi}{6}}\frac{1}{2}(1+2\sin{\theta})^{2}d\theta \\&= \frac{1}{2}\int_{\frac{7\pi}{6}}^{\frac{11\pi}{6}}1 + 4\sin{\theta}+4\sin^{2}{\theta}d\theta \\&= \frac{1}{2}\int_{\frac{7\pi}{6}}^{\frac{11\pi}{6}}3+4\sin{\theta}-2\cos{2\theta}d\theta \\&= \frac{1}{2}\left.\left[3\theta-4\cos{\theta}-\sin{2\theta}\right]\right|^{\frac{11\pi}{6}}_{\frac{7\pi}{6}} \\ &= \frac{1}{2}\left[\frac{11\pi}{2}-2\sqrt{3}+\frac{\sqrt{3}}{2}-\frac{7\pi}{2}-2\sqrt{3}+\frac{\sqrt{3}}{2}\right]=\pi-\frac{3\sqrt{3}}{2}\end{align*}$$
