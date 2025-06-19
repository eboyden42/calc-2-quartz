#### 03 - Limit Comparison Test
Use the Limit Comparison Test to determine whether the series converges: $$\displaystyle\sum_{n=1}^\infty\frac{1}{\sqrt{n}+\ln n}$$

Show your work. You must check that the test is applicable.

**Solution**
1. && Find appropriate $\sum b_{n}$ for comparison.
    - A good $\sum b_{n}$ would be $\sum \frac{1}{\sqrt{n}}$.
2. & Verify applicability of the limit comparison test.
    - $a_{n} \geq 0$ since $\sqrt{n} > 0$ for all $n > 1$ and $\ln{n} \geq 0$ for all $n > 1$. 
    - $b_{n} > 0$ since $\sqrt{n} > 0$ for all $n > 1$.
3. && Apply limit comparison test. $$\begin{align*}\lim_{n \to \infty}\frac{\frac{1}{\sqrt{n} + \ln{n}}}{\frac{1}{\sqrt{n}}} &= \lim_{n \to \infty}\frac{\sqrt{n}}{\sqrt{n} + \ln{n}} \\ &= 1\end{align*}$$
4. & Interpret results.
    - Since $0 < 1 < \infty$ and $\sum b_{n}$ diverges via the $p$-series test, we conclude that $\sum a_{n}$ also diverges.


#### 05 - Integral Test
Determine whether the series is convergent by using the Integral Test. Show your work. You must check that the test is applicable.

(a) $\displaystyle\sum_{n = 1}^{\infty}\frac{1}{n^{1.1}}$ $\qquad$ (b) $\displaystyle\sum_{n = 1}^{\infty}ne^{-n^{2}}$ $\qquad$ (c) $\displaystyle\sum_{n=1}^\infty \frac{1}{\sqrt[3]{n^2}}$

**Solution**

**(a)**
1. && Verify applicability of the integral test.
    - $f(x) \geq 0$ since $x^{1.1} \geq 0$ for all $x \geq 1$.
    - $f(x)$ is continuous for all $x \geq 1$. (only discontinuity is at $x = 0$, but the series starts at $x = 1$).
    - $f(x)$ is monotone decreasing, since as $x$ increases, the denominator increases, and the term decreases.
2. && Apply the integral test. $$\begin{align*}\int_{ 1}^{\infty}\frac{dx}{x^{1.1}} &= \lim_{b \to \infty}\int_{1}^{b}\frac{dx}{x^{1.1}} \\ &= \lim_{b \to \infty}\left.\left[-10x^{-0.1}\right]\right|_{1}^{b} \\ &= 0+10 = 0 \end{align*}$$
3. & Interpret results.
     - Since $\int_{1}^{\infty}f(x)dx$ converges, so must $\sum_{n = 1}^{\infty}a_{n}$.

**(b)**
1. &&& Verify applicability of the integral test.
    - $f(x) \geq 0$ since $x \geq 1$ and $e^{-x^{2}} \geq 0$ for all $x \in \mathbb{R}$.
    - $f(x)$ is continuous for all $x \in \mathbb{R}$.
    - $f'(x) = e^{-x^{2}}-2x^{2}e^{-x^{2}}$ has critical points at $x = \pm \frac{1}{\sqrt{2}}$. When $x > \frac{1}{\sqrt{2}}$, $f'(x) < 0$, so $f(x)$ is monotone decreasing.
2. && Apply the integral test. $$\begin{align*}\int_{1}^{\infty}xe^{-x^{2}}dx &= \lim_{b \to \infty}\int_{1}^{b}xe^{-x^{2}}dx \\ &= \lim_{b \to \infty}\left.\left[-\frac{e^{-x^{2}}}{2}\right]\right|^{b}_{1} \\ &= 0+\frac{e^{-1}}{2} = \frac{e^{-1}}{2}\end{align*}$$
3. & Interpret results.
    - Since $\int_{1}^{\infty}f(x)dx$ converges, so must $\sum_{n = 1}^{\infty}a_{n}$.

**(c)**
1. && Verify applicability of the integral test.
    - $f(x) \geq 0$ since $x^{-2/3} \geq 0$ for all $x \geq 1$.
    - $f(x)$ is continuous for all $x \geq 1$. (The only discontinuity is at $x = 0$, but the series starts at $n = 1$.)
    - $f(x)$ is monotone decreasing, since as $x$ increases, the denominator increases, and the term decreases.
2. && Apply the integral test. $$\begin{align*}\int_{ 1}^{\infty}\frac{dx}{x^{2/3}} &= \lim_{b \to \infty}\int_{1}^{b}\frac{dx}{x^{2/3}} \\ &= \lim_{b \to \infty}\left.\left[-\frac{2}{3}x^{-5/3}\right]\right|_{1}^{b} \\ &= 0+\frac{2}{3} = \frac{2}{3} \end{align*}$$
3. & Interpret results.
     - Since $\int_{1}^{\infty}f(x)dx$ converges, so must $\sum_{n = 1}^{\infty}a_{n}$.


#### 06 - Integral Test, Direct Comparison, Limit Comparison
Determine whether the series converges by checking applicability and then applying the designated convergence test.

(a) Integral Test: $\displaystyle\sum_{n = 1}^{\infty}\frac{\ln{n}}{n^{2}}$

(b) Direct Comparison Test: $\displaystyle\sum_{n = 1}^{\infty}\frac{n^{3}}{n^{5}+4n+1}$

(c) Limit Comparison Test: $\;\displaystyle\sum_{n=2}^\infty\frac{n^2}{n^4-1}$

**Solution**

**(a)**
1. &&& Verify applicability of the integral test.
    - $f(x) \geq 0$ since $\ln{x} \geq 0$ for all $x \geq 1$, and $n^{2} > 0$ for all $x \geq 1$.
    - $f(x)$ is only discontinuous at $x = 0$, but since the series starts at $x = 1$, this discontinuity is not relevant.
    - $f'(x) = \frac{1-2\ln{x}}{x^{3}}$. The critical point is at $x = e^{\frac{1}{2}}$. For $x > e^{\frac{1}{2}}$, $f'(x) < 0$, so the function is decreasing. 
2. && Apply the integral test. $$\begin{align*}\int_{1}^{\infty}\frac{\ln{x}}{x^{2}}dx &= \lim_{b \to \infty}\int_{1}^{b}\frac{\ln{x}}{x^{2}}dx \\  &= \lim_{b \to \infty}\left.\left[-\frac{\ln{x}}{x}-\frac{1}{x}\right]\right|_{1}^{b} \\ &= (0-0)-(0-1) \\ &= 1 \end{align*}$$
3. & Derive conclusions.
    - Since $\int_{1}^{\infty}f(x)dx$ converges, so must $\sum_{n = 1}^{\infty}a_{n}$.

**(b)**
1. && Find appropriate $\sum b_{n}$ for comparison.
    - A good $\sum b_{n}$ would be $\sum \frac{n^{3}}{n^{5}} = \sum\frac{1}{n^{2}}$.

2. & Verify applicability of the direct comparison test.
    - Since $a_{n} \leq b_{n}$ for large $n$ because the denominator for $a_{n}$ is always larger, the DCT can be applied.
3. && Apply the direct comparison test.
    - Since $\sum b_{n}$ converges by the $p$-series test, we conclude that $\sum a_{n}$ must converge as well.

**(c)**
1. && Find appropriate $\sum b_{n}$ for comparison.
    - A good $\sum b_{n}$ would be $\sum \frac{n^{2}}{n^{4}} = \sum \frac{1}{n^{2}}$.
2. & Verify applicability of the limit comparison test.
    - $a_{n} > 0$ since the numerator is always positive and $n^{4} - 1 > 0$ for all $n > 2$.
    - $b_{n}$ is always positive since $n^{2} > 0$ for all $n > 2$.
3. && Apply limit comparison test. $$\begin{align*}\lim_{n \to \infty}\frac{\frac{n^{2}}{n^{4}-1}}{\frac{1}{n^{2}}} = \lim_{n \to \infty}\frac{n^{4}}{n^{4}-1} &= 1\end{align*}$$
4. & Interpret results.
    - Since $0 < 1 < \infty$ and $\sum b_{n}$ converges via the $p$-series test, we conclude that $\sum a_{n}$ also converges.


#### 07 - Limit Comparison Test
Use the Limit Comparison Test to determine whether the series converges: $$\displaystyle\sum_{n = 1}^{\infty}\frac{e^{n}+n}{e^{2n}-n^{2}}$$

Show your work. You must check that the test is applicable.

**Solution**

1. && Find appropriate $\sum b_{n}$ for comparison.
    - A good $\sum b_{n}$ would be $\sum \frac{e^{n}}{e^{2n}} = \sum \frac{1}{e^{n}}$.
2. & Verify applicability of the limit comparison test.
    - Since $a_{n} \geq 0$ for all $n > 1$ (note that $e^{2n}$ grows faster than $n^{2}$) and $b_{n} > 0$ for all $n > 1$, the test is applicable.
3. && Apply the limit comparison test. $$\lim_{n \to \infty}\frac{\frac{e^{n}+n}{e^{2n}-n^{2}}}{\frac{1}{e^{n}}} = \lim_{n \to \infty}\frac{e^{2n}+ne^{n}}{e^{2n}-n^{2}} = 1$$
4. & Determine convergence of $\sum b^{n}$ using the integral test. $$\int_{1}^{\infty}\frac{dx}{e^{x}} = \lim_{b\to\infty}\left.\left[-e^{-x}\right]\right|^{b}_{1}=0+e^{-1}=e^{-1}$$
5. & Derive conclusions about $\sum b_{n}$ and $\sum a_{n}$.
    - Since $\sum b_{n}$ converges by the integral test and $0 < 1 < \infty$, we conclude that $\sum a_{n}$ also converges.

