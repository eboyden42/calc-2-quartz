## Ratio test and Root test

#### Ratio test examples

(a) Observe that $\displaystyle\sum_{n=0}^\infty\frac{10^n}{n!}$ has ratio $R_n=\frac{10}{n+1}$ and thus $R_n\to0=L<1$. Therefore the RaT implies that this series converges.

> [!warning] Notice this technique!
> Simplify the ratio: $$\begin{gather*}\frac{\displaystyle\frac{10^{n+1}}{(n+1)!}}{\displaystyle\frac{n!}{10^n}}\quad ⨠⨠ \quad \frac{(n+1)!}{10^{n+1}}\cdot\frac{n!}{10^n}\\\\ ⨠⨠ \quad  \frac{10\cdot 10^n}{(n+1)n!}\cdot\frac{n!}{10^n}\quad ⨠⨠ \quad \frac{10}{n+1}\;\overset{n\to\infty}{\longrightarrow}\;0\end{gather*}$$
> 
> We *frequently* use these rules: $$10^{n+1}=10^n\cdot 10,\qquad (n+1)!=(n+1)n!$$ to simplify ratios having exponents and factorials.

(b) $\displaystyle\sum_{n=1}^\infty\frac{n^2}{2^n}$ has ratio $R_n=\frac{(n+1)^2}{2^{n+1}}\Big/\frac{n^2}{2^n}$.

Simplify this: $$\frac{(n+1)^2}{2^{n+1}}\Big/\frac{n^2}{2^n}\qquad ⨠⨠ \qquad \frac{(n+1)^2}{2^{n+1}}\cdot\frac{2^n}{n^2}$$ $$⨠⨠ \qquad \frac{(n+1)^2\cdot 2^n}{n^2\cdot2\cdot 2^n}\qquad ⨠⨠ \qquad \frac{n^2+2n+1}{2n^2}\;\overset{n\to\infty}{\longrightarrow}\; \frac{1}{2}=L$$

So the series *converges absolutely* by the ratio test.

(c) Observe that $\displaystyle\sum_{n=1}^\infty n^2$ has ratio $R_n=\displaystyle\frac{n^2+2n+1}{n^2}\to 1$ as $n\to\infty$.

So the ratio test is *inconclusive*, even though this series fails the SDT and obviously diverges.

(d) Observe that $\displaystyle\sum_{n=1}^\infty \frac{1}{n^2}$ has ratio $R_n=\displaystyle\frac{n^2}{n^2+2n+1}\to 1$ as $n\to\infty$.

So the ratio test is *inconclusive*, even though the series converges as a $p$-series with $p=2>1$.

(e) More generally, the ratio test is usually *inconclusive for rational functions*; it is more effective to use LCT with a $p$-series.

#### Root test examples

(a) Observe that $\displaystyle\sum_{n=1}^\infty\left(\frac{1}{n}\right)^n$ has roots of terms: $$|a_n|^{1/n}=\left(\left(\frac{1}{n}\right)^n\right)^{1/n}=\frac{1}{n}\;\overset{n\to\infty}{\longrightarrow}0=L$$

Because $L<1$, the RooT shows that the series converges absolutely.

(b) Observe that $\displaystyle\sum_{n=1}^\infty (-1)^n\left(\frac{n}{2n+1}\right)^n$ has roots of terms: $$\sqrt[n]{|a_n|}=\frac{n}{2n+1}\;\overset{n\to\infty}{\longrightarrow}\;\frac{1}{2}=L$$
Because $L<1$, the RooT shows that the series converges absolutely.

(c) Observe that $\displaystyle\sum_{n=1}^\infty\left(\frac{3}{n}\right)^n$ converges because $\sqrt[n]{|a_n|}=\frac{3}{n}\to0$ as $n\to\infty$.

#### Ratio test versus root test

Determine whether the series $\displaystyle\sum_{n=1}^\infty\frac{n^2 4^n}{5^{n+2}}$ converges absolutely or conditionally or diverges.

**Solution**
Before proceeding, rewrite somewhat the general term as $\displaystyle\left(\frac{n}{5}\right)^2\cdot \left(\frac{4}{5}\right)^n$.

Now we solve the problem first using the ratio test. By plugging in $n+1$ we see that $$a_{n+1}=\left(\frac{n+1}{5}\right)^2\cdot\left(\frac{4}{5}\right)^{n+1}$$

So for the ratio $R_n$ we have: 

$$\begin{gather*}\left(\frac{n+1}{5}\right)^2\cdot\left(\frac{4}{5}\right)^{n+1}\cdot \left(\frac{5}{n}\right)^2\cdot\left(\frac{5}{4}\right)^n\\\\ ⨠⨠ \qquad \frac{n^2+2n+1}{n^2}\cdot\frac{4}{5}\longrightarrow\frac{4}{5}<1\text{ as }n\to\infty\end{gather*}$$

Therefore the series converges absolutely by the ratio test.

Now solve the problem again using the root test. We have for $\sqrt[n]{|a_n|}$:

$$\left(\left(\frac{n}{5}\right)^2\cdot \left(\frac{4}{5}\right)^n\right)^{1/n}=\left(\frac{n}{5}\right)^{2/n}\cdot \frac{4}{5}$$

To compute the limit as $n\to\infty$ we must use logarithmic limits and L’Hopital’s Rule. So, first take the log:

$$\ln \left(\left(\frac{n}{5}\right)^{2/n}\cdot \frac{4}{5}\right)=\frac{2}{n}\ln\frac{n}{5}+\ln\frac{4}{5}$$

Then for the first term apply L’Hopital’s Rule:

$$\frac{\ln\frac{n}{5}\overset{d/dx}{\longrightarrow}\frac{1}{n/5}\cdot\frac{1}{5}}{n/2\overset{d/dx}{\longrightarrow}1/2}\qquad ⨠⨠ \qquad \frac{1/n}{1/2}\qquad ⨠⨠ \qquad \frac{2}{n}\;\longrightarrow 0\text{ as }n\to\infty$$

So the first term goes to zero, and the second (constant) term is the value of the limit. So the log limit is $\ln\frac{4}{5}$, and the limit (before taking logs) must be $e^{\ln\frac{4}{5}}$ (inverting the log using $e^x$) and this is $\frac{4}{5}$. Since $\frac{4}{5}<1$, the root test also shows that the series converges absolutely.

## Power series: Radius and Interval

#### Radius of convergence
Find the radius of convergence of the series:

(a) $\displaystyle\sum_{n=0}^\infty\frac{x^n}{2^n}$$\qquad$ (b) $\displaystyle\sum_{n=0}^\infty\frac{x^{2n}}{(2n)!}$

**Solution**

(a) The ratio of coefficients is $R_n=\displaystyle\left|\frac{a_{n+1}}{a_n}\right|=\frac{1/2^{n+1}}{1/2^n}=1/2$.

Therefore $R=2$ and the series converges for $|x|<2$.

(b) This power series has $a_{2n+1}=0$, meaning it skips all odd terms.

Instead of the standard ratio function, we take the ratio of successive *even terms*. The series of even terms has coefficients $a_n=\frac{1}{(2n)!}$. So: 

$$\begin{gather*}\left|\frac{a_{n+1}}{a_n}\right|\quad ⨠⨠ \quad \frac{\frac{1}{(2(n+1))!}}{\frac{1}{(2n)!}}\\\\ ⨠⨠ \quad \frac{1}{(2n+2)(2n+1)(2n)!}\cdot\frac{(2n)!}{1}\quad ⨠⨠ \quad \frac{1}{(2n+2)(2n+1)}\end{gather*}$$

As $n\to\infty$, this converges to $0$, so $L=0$ and $R=\infty$.

#### Radius and interval for a few series

| Series                                                |   Radius   |      Interval       |
| :---------------------------------------------------- | :--------: | :-----------------: |
| $\displaystyle\sum_{n=0}^{\infty} x^n$                |   $R=1$    |      $(-1,1)$       |
| $\displaystyle\sum_{n=1}^{\infty} \frac{(x-2)^n}{n}$  |   $R=1$    |       $[1,3)$       |
| $\displaystyle\sum_{n=0}^{\infty} n!\,x^n$            |   $R=0$    |       $\{0\}$       |
| $\displaystyle\sum_{n=0}^{\infty} \frac{x^n}{(2 n)!}$ | $R=\infty$ | $(-\infty, \infty)$ |

#### Interval of convergence
Find the interval of convergence of the following series.

(a) $\displaystyle\sum_{n=1}^\infty\frac{(x-3)^n}{n}$ $\qquad$ (b) $\displaystyle\sum_{n=0}^\infty\frac{(-3)^nx^n}{\sqrt{n+1}}$

**Solution**

(a) $\displaystyle\sum_{n=1}^\infty\frac{(x-3)^n}{n}$

1. Apply ratio test.
    - Ratio of successive coefficients: $$R_n\;=\;\left|\frac{1}{n+1}\cdot\frac{n}{1}\right|\quad ⨠⨠ \quad \frac{n}{n+1}$$
    - Limit of ratios: $$R_n=\frac{n}{n+1}\;\overset{n\to\infty}{\longrightarrow}\;1$$
    - Deduce $L=1$ and therefore $R=1$.
    - Therefore: $$\begin{align*}|x-3|<1&\implies\text{converges}\\\\ |x-3|>1&\implies\text{diverges}\end{align*}$$
2. Preliminary interval of convergence.
    - Translate to interval notation: $$\begin{gather*}|x-3|<1\quad ⨠⨠ \quad x\in(3-1,3+1)\\\\ ⨠⨠ \quad x\in(2,4)\end{gather*}$$
3. Final interval of convergence.
    - Check endpoint $x=2$: $$\begin{gather*}\sum_{n=1}^\infty\frac{(2-3)^n}{n}\quad ⨠⨠ \quad \sum_{n=1}^\infty\frac{(-1)^n}{n}\\\\ ⨠⨠ \quad \text{converges by AST}\end{gather*}$$
    - Check endpoint $x=4$: $$\begin{gather*}\sum_{n=1}^\infty\frac{(4-3)^n}{n}\quad ⨠⨠ \quad \sum_{n=1}^\infty\frac{1}{n}\\\\ ⨠⨠ \quad \text{diverges as $p$-series}\end{gather*}$$
    - Final interval of convergence: $x\in[2,4)$

(b) $\displaystyle\sum_{n=0}^\infty\frac{(-3)^nx^n}{\sqrt{n+1}}$

1. Limit of coefficients ratio.
    - Ratio of successive coefficients: $$\begin{gather*}R_n=\left|\frac{a_{n+1}}{a_n}\right|\quad ⨠⨠ \quad \left|\frac{(-3)^{n+1}}{\sqrt{n+2}}\cdot\frac{\sqrt{n+1}}{(-3)^n}\right|\\\\ ⨠⨠ \quad \frac{3\sqrt{n+1}}{\sqrt{n+2}}\end{gather*}$$
    - Limit of ratios: $$\lim_{n\to\infty}\,R_n\quad ⨠⨠ \quad \lim_{n\to\infty}\,\frac{3\sqrt{n+1}}{\sqrt{n+2}}\quad ⨠⨠ \quad  3$$
    - Deduce $L=3$ and thus $R=1/3$.
    - Therefore: $$\begin{align*}|x|<\frac{1}{3}&\implies\text{converges}\\\\ |x|>\frac{1}{3}&\implies\text{diverges}\end{align*}$$
    - Preliminary interval of convergence: $\;x\in\left(-\frac{1}{3},\,\frac{1}{3}\right)$
2. Check endpoints.
    - Check endpoint $x=-1/3$: $$\begin{gather*}\sum_{n=0}^\infty\frac{\left(-3\cdot\left(-\frac{1}{3}\right)\right)^n}{\sqrt{n+1}}\quad ⨠⨠ \quad \sum_{n=0}^\infty\frac{1^n}{\sqrt{n+1}}\\\\ ⨠⨠ \quad \text{diverges by LCT with $b_n=1/\sqrt{n}$}\end{gather*}$$
    - Check endpoint $x=+1/3$: $$\begin{gather*}\sum_{n=0}^\infty\frac{\left(-3\cdot\left(+\frac{1}{3}\right)\right)^n}{\sqrt{n+1}}\quad ⨠⨠ \quad \sum_{n=0}^\infty\frac{(-1)^n}{\sqrt{n+1}}\\\\ ⨠⨠ \quad \text{converges by AST}\end{gather*}$$
    - Final interval of convergence: $\;x\in(-1/3,1/3]$

#### Interval of convergence - further examples
Find the interval of convergence of the following series.

(a) $\displaystyle\sum_{n=0}^\infty\frac{n(x+2)^n}{3^{n+1}}$ $\qquad$ (b) $\displaystyle\sum_{n=1}^\infty\frac{(4x+1)^n}{n}$

**Solution**

(a) $\displaystyle\sum_{n=0}^\infty\frac{n(x+2)^n}{3^{n+1}}$

- Ratio of coefficients: $R_n=\displaystyle\frac{n+1}{3n}\longrightarrow\frac{1}{3}$.
- So the $R=3$, center is $x=-2$, and the preliminary interval is $(-2-3,-2+3)=(-5,1)$.
- Check endpoints: $\displaystyle\sum\frac{n(-3)^n}{3^{n+1}}$ diverges and $\displaystyle\sum\frac{n(3)^n}{3^{n+1}}$ also diverges. Final interval is $(-5,1)$.

(b) $\displaystyle\sum_{n=1}^\infty\frac{(4x+1)^n}{n}$

- Ratio of coefficients: $R_n=\displaystyle\frac{n+1}{n}\longrightarrow 1$.
- So $R=1$, and the series converges when $|4x+1|<1$.
- Extract preliminary interval.
    - Divide by $4$: $$|4x+1|<1\quad \overset{\div 4}{⨠⨠} \quad |x+1/4|<1/4\quad ⨠⨠ \quad x\in (0,1/2)$$
- Check endpoints: $\displaystyle\sum\frac{(4\cdot\frac{-1}{2}+1)^n}{n}$ converges but $\displaystyle\sum\frac{1}{n}$ diverges.
- Final interval of convergence: $\;[-1/2,0)$

