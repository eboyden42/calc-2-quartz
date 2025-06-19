#### List 1
**Problem**
Determine whether each of the series is absolutely convergent, conditionally convergent, or divergent, using any convergence test.
- (1) $\sum_{n=1}^{\infty}\left(1+\frac{1}{n}\right)2^{-n}$ 
- (2) $\sum_{n = 1}^{\infty}\sin{\left(\left(\frac{2n+1}{2}\right)\pi\right)n^{-\frac{1}{2}}}$
- (3) $\sum_{n=1}^{\infty}\frac{\ln{n}}{n + 2}$ 
- (4) $\sum_{n = 1}^{\infty}(-1)^{n}\ln{\left(\frac{n}{3n+1}\right)}$
- (5) $\sum_{n = 1}^{\infty}\frac{(-2)^{n}}{n^{2}}$
- (6) $\sum_{n = 1}^{\infty}\frac{1}{9^{n}}(2n)!$ 
- (7) $\sum_{n  = 1}^{\infty}\frac{1\cdot 3 \cdot 5 \cdots (2n - 1)}{5^{n}n!}$  
- (8) $\sum_{n = 1}^{\infty}(-1)^{n}\frac{1}{3n}$
- (9) $\sum_{n = 1}^{\infty}\left(-\frac{1}{3n}\right)^{n}$
- (10) $\sum_{n = 1}^{\infty} (-1)^{n}\frac{n^{2n}}{\left(1+2n^{2}\right)^{n}}$
- (11) $\sum_{n = 1}^{\infty}(-1)^{n}\frac{n}{n^{4} + 1}$
- (12) $\sum_{n = 1}^{\infty}(-1)^{n}\frac{\ln{n}}{\sqrt{n}}$
- (13) $\sum_{n = 1}^{\infty}\frac{\ln{n}}{n^{2}}$ 


**Solution**
**(1)**
1. && Use ratio test to determine convergence.
    - $a_{n} = \left(\frac{n + 1}{n}\right)\frac{1}{2^{n}}$
    - $a_{n + 1} = \left(\frac{n + 2}{n+1}\right)\frac{1}{2^{n + 1}}$
    $$\begin{align*}
    \left|\frac{a_{n + 1}}{a_{n}}\right| &= \left(\frac{n + 2}{n + 1}\right)\frac{1}{2^{n + 1}}\cdot \left(\frac{n}{n + 1}\right)2^{n} \\
    &= \left(\frac{n(n+2)}{2(n+1)^{2}}\right) \\
    \lim_{n \to \infty}\left|\frac{a_{n + 1}}{a_{n}}\right| &= \frac{1}{2}
    \end{align*}$$
2. & Derive conclusion.
    - Since $\frac{1}{2} < 1$, the series absolutely converges.

**(2)**
1. && Simplify series. $$\sum_{n = 1}^{\infty}\sin{\left(\left(\frac{2n + 1}{2}\right)\pi\right)}n^{-\frac{1}{2}} = \sum_{n = 1}^{\infty}(-1)^{n}n^{-\frac{1}{2}}$$
2. & Use alternating series test to determine convergence. $$\lim_{n \to \infty}\left|a_{n}\right| = \lim_{n \to \infty}n^{-\frac{1}{2}} = 0$$
3. & Derive conclusion.
    - Since $\lim_{n \to \infty}|a_{n}| = 0$ and $\left\{|a_{n}|\right\}$ is a decreasing sequence, $\sum a_{n}$ converges.
4. & Determine absolute convergence. 
    - Since $\sum |a_{n}| = \sum_{n = 1}^{\infty}n^{-\frac{1}{2}}$, is a divergent $p$-series, $\sum a_{n}$ is conditionally convergent. 

**(3)**
1. & Set up limit comparison test to determine convergence. Compare series with $\sum{\frac{\ln{n}}{n}}$
2. & Determine comparison of $\sum \frac{\ln{n}}{n}$ using comparison test with $\sum \frac{1}{n}$.
    - Note that $\frac{\ln {n}}{n} > \frac{1}{n}$.
    - Since $\frac{1}{n}$ is a divergent $p$-series, we conclude $\frac{\ln{n}}{n}$ also diverges.
3. && Perform limit comparison test. $$\begin{align*}\lim_{n \to \infty}\frac{\ln{n}}{n + 2} \cdot \frac{n}{\ln{n}} &= 1 \neq 0\end{align*}$$
4. & Derive conclusion.
    - Since the above limit does not evaluate to zero, and our comparison series diverges, our given series diverges as well.

**(4)**
1. & Use alternating-series test to determine convergence. $$\begin{align*} \lim_{n \to \infty}\left|(-1)^{n}\ln{\left(\frac{n}{3n + 1}\right)}\right| &= \lim_{n \to \infty}\ln{\left(\frac{n}{3n + 1}\right)} \\ &= \ln{\left(\frac{1}{3}\right)}\end{align*}$$
 2. & Derive conclusion.
    - Since the above limit does not evaluate to zero, we conclude our series diverges.

**(5)**
1. && Use the ratio test to determine convergence. 
    - $a_{n} = \frac{(-2)^{n}}{n^{2}}$
    - $a_{n + 1} = \frac{(-2)^{n+1}}{(n+1)^{2}}$
    $$\begin{align*} \left|\frac{a_{n + 1}}{a_{n}}\right| &= \frac{2^{n + 1}}{(n+1)^{2}}\cdot\frac{n^{2}}{2^{n}} \\ &= \frac{2n^{2}}{(n+1)^{2}} \\ \lim_{n \to \infty}\left|\frac{a_{n+1}}{a_{n}}\right| &= 2 > 1\end{align*}$$
2. & Derive conclusion.
    - Since the above limit is greater than 1, the series diverges.
**(6)**
1. && Use ratio test to determine convergence. 
    - $a_{n} = \frac{1}{9^{n}}(2n)!$
    - $a_{n + 1} = \frac{1}{9^{n+1}}\left(2n + 2)\right)!$
    $$\begin{align*}\left|\frac{a_{n + 1}}{a_{n}}\right|&= \frac{(2n + 2)!}{9^{n + 1}}\cdot \frac{9^{n}}{(2n)!} \\ &= \frac{(2n+2)(2n + 1)}{9} \\ \lim_{n \to \infty}\left|\frac{a_{n + 1}}{a_{n}} \right| &= \infty > 1\end{align*}$$
2. & Derive conclusion.
    - Since the above limit is greater than 1, the series diverges.

**(7)**
1. && Use ratio test to determine convergence.
    - $a_{n} = \frac{1\cdot 3 \cdot 5 \cdots (2n - 1)}{5^{n}n!}$
    - $a_{n + 1} = \frac{1\cdot 3\cdot 5 \cdots (2n + 1)}{5^{n+1}(n+1)!}$ 
    $$\begin{align*} \left|\frac{a_{n + 1}}{a_{n}}\right| &= \frac{1\cdot3\cdot5\cdots(2n + 1)}{5^{n + 1}(n+1)!}\cdot \frac{5^{n}n!}{1\cdot 3\cdot 5\cdots (2n-1)} \\ &= \frac{2n + 1}{5(n+1)} \\ \lim_{n \to \infty}\left|\frac{a_{n + 1}}{a_{n}}\right| &= \frac{2}{5}\end{align*}$$
2. & Derive conclusion.
    - Since the above limit is less than 1, the series absolutely converges.

**(8)**
1. & Use alternating series test to determine convergence. $$\lim_{n \to \infty}\left|(-1)^{n}\frac{1}{3n}\right|=\lim_{n \to \infty}\frac{1}{3n} = 0$$
2. & Derive conclusion.
    - Since the above limit evaluates to 0 and $\left\{|a_{n}|\right\}$ is a decreasing sequence, the given series converges.
3. & Determine absolute convergence.
    - Since $\sum |a_{n}|$ is a divergent $p$-series, we concluded our given series is conditionally convergent.

**(9)**
1. & Use root test to determine convergence. $$\begin{align*}\lim_{n\to\infty}{\sqrt[n]{\left|a_{n}\right|}} &= \lim_{n \to \infty}\frac{1}{3n} = 0\end{align*}$$
2. & Derive conclusion.
    - Since the above limit is less than 1, the given series converges absolutely.

**(10)**
1. & Use root test to determine convergence. $$\begin{align*} \lim_{n \to \infty}{\sqrt[n]{\left|a_{n}\right|}} &= \lim_{n \to \infty}\frac{n^{2}}{\left(1+2n^{2}\right)} = \frac{1}{2}\end{align*}$$
2. & Derive conclusion.
    - Since the above limit is less than 1, the given series converges absolutely.

**(11)**
1. & Set up alternating-series test to determine convergence. $$\lim_{n \to \infty}|a_{n}| = \lim_{n \to \infty}\frac{n}{n^{4}+1} = 0$$
2. & Derive conclusion.
    - Since the above limit evaluates to 0 and $\left\{|a_{n}|\right\}$ is a decreasing sequence, the series converges.
3. && Determine absolute convergence using limit comparison test.
    - Compare $\sum|a_{n}|$ with $\sum \frac{1}{n^{3}}$ .
    $$\lim_{n \to \infty}\frac{n}{n^{4}+1}\cdot n^{3} = \lim_{n\to\infty}\frac{n^{4}}{n^{4}+1} = 1$$
    - Since $\sum \frac{1}{n^{3}}$ is a converging $p$-series, $\sum |a_{n}|$ also converges.
4. & Derive conclusion.
    - Since $\sum |a_{n}|$ converges, our given series is absolutely convergent.

**(12)**
1. & Set up alternating series test to determine convergence. $$\lim_{n\to\infty}|a_{n}| = \lim_{n \to \infty}\frac{\ln{n}}{\sqrt{n}} = \lim_{n \to \infty}\frac{1}{n}\cdot2\sqrt{n} = 0$$
2. & Derive conclusion.
    - Since the above limit evaluates to 0 and $\left\{|a_{n}|\right\}$ is a decreasing sequence, the series converges.
3. && Determine absolute convergence using comparison test.
    - Use $\sum \frac{1}{\sqrt{n}}$ for comparison, and not that $|a_{n}| > \frac{1}{\sqrt{n}}$.
    - Since $\sum \frac{1}{\sqrt{n}}$ is a divergent $p$-series, $\sum|a_{n}|$ also diverges.
4. & Derive conclusion.
    - Since $\sum|a_{n}|$ diverges, $\sum a_{n}$ conditionally converges.

**(13)**
1. && Use the integral test to determine convergence. $$\begin{align*}\int_{1}^{\infty}\frac{\ln{x}}{x^{2}}dx  &= \lim_{b \to \infty}\int_{1}^{b} \frac{\ln{x}}{x^{2}}dx \\ &= \lim_{b \to \infty}\left[\left.-\frac{\ln{x}}{x}\right|^{b}_{1} + \int_{1}^{b}\frac{dx}{x^{2}}\right] \\ &= \lim_{b \to \infty}\left[-\frac{\ln{b}}{b}-\frac{1}{b}+\ln{1}+1\right] \\ &= 1\end{align*}$$
2. & Derive conclusion.
    - Since the above integral converges, our given series is convergent.


#### List 2

**Problem**
For each series, state a convergence test that will show whether is converges or diverges. 
- (43) $\sum_{n = 1}^{\infty}\frac{2^{n}+4^{n}}{7^{n}}$
- (44) $\sum_{n = 1}^{\infty}\frac{n^{3}}{n!}$
- (45) $\sum_{n = 1}^{\infty}\frac{n^{3}}{5^{n}}$
- (46) $\sum_{n = 2}^{\infty}\frac{1}{n(\ln{n})^{3}}$ 
- (47) $\sum_{n = 2}^{\infty}\frac{1}{\sqrt{n^{3}-n^{2}}}$ 
- (48) $\sum_{n = 1}^{\infty}\frac{n^{2}+4n}{3n^{4}+9}$
- (49) $\sum_{n = 1}^{\infty}n^{-0.8}$
- (50) $\sum_{n = 1}^{\infty}(0.8)^{-n}n^{-0.8}$
- (51) $\sum_{n = 1}^{\infty}4^{-2n + 1}$
- (52) $\sum_{n = 1}^{\infty} \frac{(-1)^{n-1}}{\sqrt{n}}$
- (53) $\sum_{n = 1}^{\infty}\sin{\frac{1}{n^{2}}}$
- (54) $\sum_{n = 1}^{\infty}(-1)^{n}\cos{\frac{1}{n}}$
- (55) $\sum_{n = 1}^{\infty}\frac{(-2)^{n}}{\sqrt{n}}$
- (56) $\sum_{n = 1}^{\infty}\left(\frac{n}{n+ 12}\right)^{n}$


**Solution**
**(43)**
1. && Note that the series is a sum of two geometric series. Therefore, you can use the geometric series test.

**(44)**
1. & Since the series involves a factorial, you should use the ratio test.

**(45)**
1. & Since the series involves a polynomial over an $n^{\text{th}}$ power, the ratio test would be the best option.

**(46)**
1. & Since the function is easily integrated, positive, and decreasing, the integral test is a good option.

**(47)**
1. & The limit comparison test with $\sum\frac{1}{n^{\frac{3}{2}}}$ is a good option for determining convergence. Note that the direct comparison test would not work since our comparison series converges and the given series is greater.
2. & If you are comfortable with integrals involving trigonometric substitutions, the integral test can be used as well.

**(48)**
1. & The direct comparison test with $\sum \frac{1}{n^{2}}$ is an efficient way for determining convergence since the terms of the given series are less than those of the comparison series.

**(49)**
1. & The $p$-series test is the easiest way to determine convergence.

**(50)**
1. & The divergence test is the easiest way to tell the series diverges.

**(51)**
1. & This series can be rewritten as a geometric series, so the geometric series test can be applied.

**(52)**
1. & The presence of a $(-1)^{n-1}$ term implies using the alternating-series test along with the $p$-series test to analyze the absolute value of the series.

**(53)**
1. & The limit comparison test with $\sum \frac{1}{n^{2}}$ is the best option.

**(54)**
1. & The alternating-series test used with a limit comparison test with $\sum{\frac{1}{n}}$ is the best option.

**(55)**
1. & The ratio test is the best option since we have an $n^{\text{th}}$ power over a polynomial.

**(56)**
1. & The root test is the best option here since all terms are raised to the power of $n$.