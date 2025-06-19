#### 03 - Complex forms - exponential to Cartesian
Write each number in the form $a+bi$.

(a) $2{\large e}^{\textstyle i\frac{\pi}{4}}$ $\quad$ (b) ${\large e}^{\textstyle \ln 4+i\frac{\pi}{2}}$

**Solution**

**(a)**
1. &&& State Euler's formula. $$re^{i\theta} = r\cos{\theta} + r\sin{\theta}i$$
2. & Plug given expression into formula with $r =2$ and $\theta = \frac{\pi}{4}$. $$2e^{i\frac{\pi}{4}} = 2\cos{\frac{\pi}{4}} +2i\sin{\frac{\pi}{4}} = \sqrt{2} + i\sqrt{2}$$

**(b)**
1. & Write as expression product of exponents. $$e^{\ln 4 + i\frac{\pi}2} = e^{\ln{4}}e^{i\frac{\pi}{2}}=4e^{i\frac{\pi}{2}}$$
2. & Plug computed expression into Euler's formula with $r = 4$ and $\theta = \frac{\pi}{2}$ $$4e^{i\frac{\pi}{2}} = 4\cos{\frac{\pi}{2}}+4i\sin{\frac{\pi}{2}} = 4i$$


#### 05 - Complex roots using polar
Find the three cube ($3^\text{rd}$) roots of $27i$.

Write your answer in the form $a+bi$.

**Solution**

1. && Write $27i = 27e^{i\frac{\pi}{2}}$
2. & Use the roots formula where $r = 27$, $n = 3$, and $\theta = \frac{\pi}{2}$. $$\left(27e^{i\frac{\pi}{2}}\right)^{\frac{1}{3}} \quad ⨠ ⨠\quad w_{k} = 27^{\frac{1}{3}}e^{i\left(\frac{\frac{\pi}{2}}{3} + k\frac{2\pi}{3}\right)}=3e^{i\left(\frac{\pi}{6}+k\frac{2\pi}{3}\right)}$$
3. & Write out roots by evaluating $w_{k}$ at $k = 0, 1, 2$ $$3e^{i\frac{\pi}{6}}, 3e^{i\frac{5\pi}{6}},3e^{i\frac{3\pi}{2}} = \frac{3\sqrt{3}}{2}+\frac{3}{2}i, -\frac{3\sqrt{3}}{2}+\frac{3}{2}i,-3i$$


#### 09 - Complex products and quotients using polar
For each pair of complex numbers $z$ and $w$, compute:

$$zw,\qquad \frac{z}{w},\qquad \frac{1}{z}$$

(a) $z=1+\sqrt{3}i,\quad w=\sqrt{3}+i$

(b) $z=2\sqrt{3}-2i,\quad w=6i$

(Use polar forms with $\theta\in[0,2\pi)$.)

**Solution**

**(a)**
1. & Compute $zw$.
    - $zw = \left(1 + \sqrt{3}i\right)\left(\sqrt{3} + i\right) = \sqrt{3}+i + 3i + i^{2}\sqrt{3} = 4i$
    - $4i = 4\cos{\frac{\pi}{2}} + 4i\sin{\frac{\pi}{2}} = 4e^{i\frac{\pi}{2}}$.
2. & Compute $\frac{z}{w}$. Multiply numerator and denominator by the conjugate and simplify.
    - $\frac{z}{w} = \frac{1+i\sqrt{3}}{\sqrt{3} + i} = \frac{1+i\sqrt{3}}{\sqrt{3} + i} \cdot \frac{\sqrt{3} - i}{\sqrt{3} - i} = \frac{2\sqrt{3}+2i}{4} = \frac{\sqrt{3}}{2} + \frac{1}{2}i$
    - $\frac{\sqrt{3}}{2} + \frac{1}{2} = \cos{\frac{\pi}{6}} + i \sin{\frac{\pi}{6}} = e^{i\frac{\pi}{6}}$ 
3. && Compute $\frac{1}{z}$. Multiply numerator and denominator by the conjugate and simplify.
    - $\frac{1}{z} = \frac{1}{1+i\sqrt{3}} = \frac{1}{1+i\sqrt{3}} \cdot \frac{1-i\sqrt{3}}{1-i\sqrt{3}} = \frac{1-i\sqrt{3}}{4} = \frac{1}{4} - \frac{\sqrt{3}}{4}i$ 
    - $\frac{1}{4} - \frac{\sqrt{3}}{4}i = \frac{1}{2}\cos{\frac{5\pi}{3}} + \frac{1}{2}i\sin{\frac{5\pi}{3}} = \frac{1}{2}e^{i\frac{5\pi}{3}}$ 

**(b)**
1. & Compute $zw$.
    - $zw = \left(2\sqrt{3}-2i\right)(6i) = 12i\sqrt{3} + 12$
    - $12+12i\sqrt{3} = 24\cos{\frac{\pi}{6}}+24i\sin{\frac{\pi}{6}} = 24e^{i\frac{\pi}{6}}$.
2. && Compute $\frac{z}{w}$. Multiply numerator and denominator by the conjugate and simplify.
    - $\frac{z}{w} = \frac{2\sqrt{3}-2i}{6i} = \frac{2\sqrt{3}-2i}{6i} \cdot \frac{-6i}{-6i} = \frac{12i\sqrt{3}-12}{36} = \frac{\sqrt{3}}{3}i - \frac{1}{3}$.
    - $-\frac{1}{3}+\frac{\sqrt{3}}{3}i = \frac{2}{3}\cos{\frac{2\pi}{3}}+\frac{2}{3}i\sin{\frac{2\pi}{3}} = \frac{2}{3}e^{i\frac{2\pi}{3}}$
3. && Compute $\frac{1}{z}$. Multiply numerator and denominator by the conjugate and simplify.
    - $\frac{1}{z} = \frac{1}{2\sqrt{3}-2i} = \frac{1}{2\sqrt{3}-2i}\cdot\frac{2\sqrt{3}+2i}{2\sqrt{3}+2i} = \frac{2\sqrt{3}+2i}{16} = \frac{\sqrt{3}}{8} + \frac{1}{8}i$
    - $\frac{\sqrt{3}}{8} + \frac{1}{8}i = \frac{1}{4}\cos{\frac{\pi}{6}}+\frac{1}{4}i\sin{\frac{\pi}{6}} = \frac{1}{4}e^{i\frac{\pi}{6}}$ .


#### 10 - Complex powers using polar
Using De Moivre’s Theorem, write each number in the form $a+bi$.

(a) $(1+i)^{16}$ $\quad$ (b) $(\sqrt{3}-i)^5$

(First convert to polar/exponential, then compute the power, then convert back.)

**Solution**

**(a)**
1. & Convert to polar form. $$1 + i = \sqrt{2}\cos{\frac{\pi}{4}}+\sqrt{2}i\sin\frac{\pi}{4}$$
2. & Use De Moivre's Theorem. $$(r\text{cis}\theta)^{16} = 2^{8}\cos{4\pi}+2^{8}i\sin{4\pi} = 256$$

**(b)**
1. & Convert to polar form. $$\sqrt{3}- i = 2\cos{\frac{11\pi}{6}}+2i\sin{\frac{11\pi}{6}}$$
2. & Use De Moivre's Theorem. $$(r\text{cis}\theta)^{5}=2^{5}\cos{\frac{7\pi}{6}}+2^{5}i\sin{\frac{7\pi}{6}} = -16\sqrt{3}-16i$$


#### 11 - Complex roots using polar
Find each of the indicated roots. Try to write your answer in $a + bi$ form if that is not hard, otherwise leave it in polar form.

(a) The four $4^\text{th}$ roots of $1$.

(b) The three cube ($3^\text{rd}$) roots of $\sqrt{2}+\sqrt{2}i$.

Try to write your answer in $a+bi$ form if that is not hard, otherwise leave it in polar form.


**Solution**

**(a)**
1. & Write $1 = e^{0i}$
2. & Use the roots formula where $n = 4,$ $r = 1$ and $\theta = 0$.  $$\left(e^{0i}\right)^{\frac{1}{4}} \quad ⨠ ⨠\quad w_{k}=e^{i\left(\frac{0}{4}+k\frac{2\pi}{4}\right)}=e^{\frac{2\pi}{4}ki}$$
3. & Write out roots by evaluating $w_{k}$ at $k = 0, 1, 2, 3$. $$1, e^{i\frac{\pi}{2}},e^{i\pi},e^{i\frac{3\pi}{2}} \quad ⨠ ⨠\quad 1, i, -1, -i$$

**(b)**
1. &&& Write $\sqrt{2}+\sqrt{2}i = 2e^{i\frac{\pi}{4}}$
2. & Use the roots formula where $r = 2$, $n = 3$, and $\theta = \frac{\pi}{4}$. $$\left(2e^{i\frac{\pi}{4}}\right)^{\frac{1}{3}} \quad ⨠ ⨠ \quad 2^{\frac{1}{3}}e^{i\left(\frac{\frac{\pi}{4}}{3} + k\frac{2\pi}{3}\right)} = 2^{\frac{1}{3}}e^{i\left(\frac{\pi}{12}+k\frac{2\pi}{3}\right)}$$
3. & Write out roots by evaluating $w_{k}$ at $k = 0, 1, 2$ $$2^\frac{1}{3}e^{i\frac{\pi}{12}}, 2^{\frac{1}{3}}e^{i\frac{3\pi}{4}},2^{\frac{1}{3}}e^{i\frac{17\pi}{12}}$$

