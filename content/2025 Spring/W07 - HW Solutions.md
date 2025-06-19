#### 02 - Squeeze theorem
Determine whether the sequence converges, and if it does find its limit:
- (a) $a_{n} = \frac{\cos^{2}{n}}{2^{n}}$
- (b) $b_{n} = \left(2^{n}+3^{n}\right)^{\frac{1}{n}}$

**Solution**

**(a)**
1. & Note that since $-1 \leq \cos{n} \leq 1$, $0 \leq \cos^{2}{n} \leq 1$
2. & Divide all terms by $2^{n}$. $$0 \leq \frac{\cos^{2}{n}}{2^{n}}\leq \frac{1}{2^{n}}$$
3. &&& Use squeeze theorem.
    - $\lim_{n \to \infty} 0 = 0$
    - $\lim_{n \to \infty} \frac{1}{2^{n}} = 0$
    - Thus, $\lim_{n \to \infty}\frac{\cos^{2}{n}}{2^{n}} = 0$
4. & We conclude that $a_{n}$ converges.

**(b)**
1. & Note that $3^{n} \leq 2^{n} + 3^{n} \leq 2 \cdot 3^{n}$.
2. & Raise all terms to the power of $\frac{1}{n}$ $$3\leq \left(2^{n}+3^{n}\right)^{\frac{1}{n}}\leq 3(2)^{\frac{1}{n}}$$
3. &&& Use squeeze theorem.
    - $\lim_{n \to \infty} 3 = 3$
    - $\lim_{n \to \infty} 3(2)^{\frac{1}{n}} = 3(1) = 3$
    - Thus, $\lim_{n \to \infty}\left(2^{n} + 3^{n}\right)^{\frac{1}{n}} = 3$
4. & We conclude that $b_{n}$ converges.

#### 07 - Limits and convergence
Determine whether each sequence converges or diverges (C or D). If it converges, find the limit.
\[Refer to HW for the problem statements.]

**Solution**

**(a)**
1. & Find the limit. Note that the degree of the numerator and denominator is the same. $$\lim_{n \to \infty} \frac{5n-1}{12n+9} = \frac{5}{12}$$
2. & We conclude that $b_{n}$ converges.

**(b)**
1. & Find the limit. 
    - Because of the $(-1)^{n}$ term, the limit $\lim_{n \to \infty}b_{n}$ does not exist.
2. & We conclude that $b_{n}$ diverges.

**(c)**
1. & Find the limit. $$\lim_{n \to \infty}\sqrt{4+\frac{1}{n}} = \sqrt{4+0} = 2$$
2. & We conclude that $a_{n}$ converges.

**(d)**
1. & Find the limit. $$\lim_{n \to \infty}\cos^{-1}\left(\frac{n^{3}}{n^{3}+1}\right) = \cos^{-1}(1) = 0$$
2. & We conclude that $a_{n}$ converges.

**(e)**
1. & Find the limit. $$\lim_{n \to \infty}\left(10 + \left(-\frac{1}{9}\right)^{n}\right) = 10 + 0 =10$$
2. & We conclude that $a_{n}$ converges.

**(f)**
1. & Find the limit. $$\lim_{n \to \infty}1.01^{n} = \infty$$
2. & We conclude that $c_{n}$ diverges.

**(g)**
1. & Find the limit. $$\lim_{n \to \infty}2^{\frac{1}{n}} = 2^{0} = 1$$
2. & We conclude that $a_{n}$ diverges.

**(h)**
1. & Find the limit. Note that factorial expressions increase at a faster rate than exponential expressions. $$\lim_{n \to \infty}\frac{n!}{9^{n}} = \infty$$
2. & We conclude that $c_{n}$ diverges.

**(i)**
1. & Find the limit. $$\lim_{n\to\infty} \frac{3n^{2}+n+2}{2n^{2}-3} = \frac{3}{2}$$
2. & We conclude that $a_{n}$ converges.

**(j)**
1. & Find the limit. $$\lim_{n\to\infty}\frac{\cos{n}}{n} =  0$$
2. & We conclude that $a_{n}$ converges.

**(k)**
1. & Find the limit. $$\lim_{n \to \infty} \left(\ln{5^{n}} - \ln{n!}\right) = -\infty$$
2. & We conclude that $d_{n}$ diverges.

**(l)**
1. & Find the limit. $$\lim_{n \to \infty}\left(2+\frac{4}{n^{2}}\right)^{\frac{1}{3}} = (2+0)^{\frac{1}{3}} = 2^{\frac{1}{3}}$$
2. & We conclude that $a_{n}$ converges.

**(m)**
1. & Find the limit. $$\lim_{n \to \infty}\ln{\left(\frac{2n+1}{3n+4}\right)} = \ln{\frac{2}{3}}$$
2. & We conclude that $c_{n}$ converges.

**(n)**
1. & Find the limit. Note that $e > 2$. $$\lim_{n \to \infty}\frac{e^{n}}{2^{n}} = \infty$$
2. & We conclude that $y_{n}$ diverges.

**(o)**
1. & Find the limit. $$\lim_{n \to\infty}\frac{(\ln{n})^{2}}{n} = 0$$
2. & We conclude that $a_{n}$ converges.

**(p)**
1. & Find the limit. $$\lim_{n \to \infty}\frac{(-1)^{n}(\ln{n})^{2}}{n} = 0$$
2. & We conclude that $a_{n}$ converges.

**(r)**
1. & Find the limit. $$\lim_{n \to \infty} \left(1+\frac{1}{n}\right)^{n} = e $$
2. & We conclude that $a_{n}$ converges.

**(s)** 
1. & Find the limit. $$\lim_{n \to \infty}\frac{1}{\ln{\left(1+\frac{1}{n}\right)}} = \frac{1}{0} = \infty$$
2. & We conclude that $a_{n}$ diverges.

**(t)**
1. & Find the limit. Use squeeze theorem. $$\lim_{n \to \infty}n\sin{\frac{\pi}{n}} = \pi$$
2. & We conclude that $a_{n}$ converges.

#### 09 - Series from its partial sums
Suppose we know that the *partial sums* $S_{n}$ of a series $S = \sum^{\infty}_{n = 1}a_{n}$ are given by the formula $S_{n} = 5 - \frac{2}{n^{2}}$.
- (a) Compute $a_{3}$.
- (b) Find a formula for the general term $a_{n}$.
- (c) Find the sum $S$.

**Solution**

**(a)**
1. & Start by computing $a_{1} = S_{1}$. $$a_{1} = S_{1} = 5-\frac{2}{1^{2}} = 3$$
2. & Compute $a_{2}$ by noting $a_{2} = S_{2} - S_{1}$. $$a_{2} = S_{2} - S_{1} = \left(5-\frac{2}{2^{2}}\right) - 3= \frac{9}{2}-3 = \frac{3}{2}$$
3. & Compute $a_{3}$ by noting $a_{3} = S_{3} - S_{2}$. $$a_{3} = S_{3} - S_{2} = \left(5-\frac{2}{3^{2}}\right)-\frac{9}{2} = \frac{43}{9}-\frac{9}{2}=\frac{5}{18}$$

**(b)**
1. && Note that in part (a), we used $a_{n} = S_{n} - S_{n - 1}$  for all $n > 1$.$$\begin{align*} a_{n} &= S_{n} - S_{n-1} \\ &= \left(5-\frac{2}{n^{2}}\right) - \left(5-\frac{2}{(n-1)^{2}}\right) \\ &= \frac{2}{n^{2}-2n+1}-\frac{2}{n^{2}}\end{align*}$$
2. & Note that the above formula is undefined at $n = 1$.

**(c)**
1. & Find S by computing $\lim_{n \to \infty} S_{n}$. $$S = \lim_{n \to \infty}S_{n} = 5 - 0 = 5$$

#### 10 - Geometric series - partial sums and total sum
Consider the series: $$\sum_{n = 1}^{\infty}\frac{(-8)^{n-1}}{9^{n}}$$
- (a) Compute a formula for the $N^{\text{th}}$ partial sum $S_{N}$. (You may apply the known formula or derive it again in this case using the "shift method.")
- (b) By taking the limit of this formula as $N \to \infty$, find the value of the series.
- (c) Find the same value of the series by computing $a_{0}$ and $r$ and plugging into $S = \frac{a_{0}}{1-r}$

**Solution**

**(a)**
1. & Compute the first few terms of the sequence. $$\begin{align*}a_{1} &= \frac{1}{9} \\a_{2} &= -\frac{8}{9^{2}} \\ a_{3} &= \frac{8^{2}}{9^{3}}\end{align*}$$
2. & Evidently, this is a geometric sequence where $a_{0} = \frac{1}{9}$, and $r = -\frac{8}{9}$. $$a_{n} = \frac{1}{9}\left(-\frac{8}{9}\right)^{n} \quad n \in \mathbb{Z}_{\geq 0}$$
3. && Write out formula for $S_{n}$ for a geometric series. $$S_{n} = \frac{a_{0}\left(1-r^{n}\right)}{1-r}$$
4. & Plug in relevant terms. $$S_{n} = \frac{\left(\frac{1}{9}\right)\left(1-\left(-\frac{8}{9}\right)^{n}\right)}{1+\frac{8}{9}}$$

**(b)**
1. & Find the limit. $$\lim_{n \to \infty}S_{n} = \frac{1}{9}\left(\frac{1-0}{\frac{17} {9}}\right) = \frac{1}{17}$$

**(c)**
1. & Use $a_{0} = \frac{1}{9}$ and $r = -\frac{8}{9}$. $$S = \frac{\frac{1}{9}}{1 + \frac{8}{9}} = \frac{1}{17}$$

#### 11 - Total area of infinitely many triangles
Find the area of all the triangles as in the figure:
(The first triangle from the right starts at 1, and going left they never end).

**Solution**
1. & Compute the first few areas, with $a_{0}$ being the area of the largest triangle. $$\begin{align*}a_{0} &= \frac{1}{2}\cdot\frac{1}{2}\cdot\frac{1}{2} = \frac{1}{8} \\ a_{1} &= \frac{1}{2} \cdot \frac{1}{2} \cdot \frac{1}{4} = \frac{1}{16} \\ a_{2} &= \frac{1}{2} \cdot \frac{1}{2} \cdot \frac{1}{8} = \frac{1}{32}\end{align*}$$
2. & Evidently, this is a geometric series where $r = \frac{1}{2}$. $$a_{n} = \frac{1}{8}\left(\frac{1}{2}\right)^{n} \quad n \in \mathbb{Z}_{\geq 0}$$
3. && Write out formula for sum of geometric series. $$S = \frac{a_{0}}{1-r}$$
4. & Compute sum. $$S = \frac{\frac{1}{8}}{1-\frac{1}{2}} = \frac{1}{4}$$

