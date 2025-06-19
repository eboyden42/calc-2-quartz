## Simple divergence test
#### Simple divergence test: examples
Consider: $\;\displaystyle\sum_{n=1}^\infty\frac{n}{4n+1}$
- This diverges by the SDT because $a_n\to\frac{1}{4}$ and not $0$.

Consider: $\;\displaystyle\sum_{n=1}^\infty (-1)^{n-1}\frac{n}{n+1}$
- This diverges by the SDT because $\lim_{n\to\infty} a_n=\text{DNE}$.
- We can say the terms “converge to the pattern $+1,\;-1,\;+1,\;-1,\;\dots\;$,” but that is not a limit value.

## Positive series
#### $p$-series examples
By finding $p$ and applying the $p$-series convergence properties: 

We see that $\sum_{n=1}^\infty\frac{1}{n^{1.1}}$ converges: $p=1.1$ so $p>1$

But $\sum_{n=1}^\infty\frac{1}{\sqrt{n}}$ diverges: $p=1/2$ so $p\leq 1$

#### Integral test - pushing the envelope of convergence
Does $\displaystyle\sum_{n=2}^\infty\frac{1}{n\ln n}$ converge?

Does $\displaystyle\sum_{n=2}^\infty\frac{1}{n(\ln n)^2}$ converge?

Notice that $\ln n$ grows *very slowly* with $n$, so $\frac{1}{n \ln n}$ is just a *little* smaller than $\frac{1}{n}$ for large $n$, and similarly $\frac{1}{n(\ln n)^2}$ is just a little smaller still.

**Solution**
1. & The two series lead to the two functions $f(x)=\frac{1}{x\ln x}$ and $g(x)=\frac{1}{x(\ln x)^2}$.
2. & Check applicability.
    - Clearly $f(x)$ and $g(x)$ are both continuous, positive, decreasing functions on $x\in[2,\infty]$.
3. && Apply the integral test to $f(x)$.
    - Integrate $f(x)$: $$\begin{align*}\int_2^\infty \frac{1}{x\ln x}\;dx \quad &⨠⨠ \quad   \int_{u=\ln 2}^\infty\frac{1}{u}\,du \\\\ &⨠⨠ \quad  \lim_{R\to\infty}\ln u\Big|_{\ln 1}^R \quad ⨠⨠ \quad  \infty\end{align*}$$
4. & Conclude: $\sum_{n=2}^\infty \frac{1}{n\ln n}$ *diverges*.
5. && Apply the integral test to $g(x)$.
    - Integrate $g(x)$: $$\begin{align*}\int_2^\infty \frac{1}{x(\ln x)^2}\,dx \quad &⨠⨠ \quad  \int_{u=\ln 2}^\infty \frac{1}{u^2}\;du \\\\ &⨠⨠ \quad  \lim_{R\to\infty}-u^{-1}\Big|_{\ln 2}^R \quad ⨠⨠ \quad  \frac{1}{\ln 2}\end{align*}$$
6. & Conclude: $\sum_{n=2}^\infty \frac{1}{n(\ln n)^2}$ *converges*.

#### Direct comparison test: rational functions
The series $\displaystyle\sum_{n=1}^\infty\frac{1}{\sqrt{n}\,3^n}$ *converges* by the DCT.
- Choose: $a_n=\frac{1}{\sqrt{n}\,3^n}$ and $b_n=\frac{1}{3^n}$
- Check: $0< \frac{1}{\sqrt{n}\,3^n}\leq \frac{1}{3^n}$
- Observe: $\sum \frac{1}{3^n}$ is a convergent geometric series

The series $\displaystyle\sum_{n=1}^\infty\frac{\cos^2 n}{n^3}$ *converges* by the DCT.
- Choose: $a_n=\frac{\cos^2 n}{n^3}$ and $b_n=\frac{1}{n^3}$.
- Check: $0\leq\frac{\cos^2 n}{n^3}\leq\frac{1}{n^3}$
- Observe: $\sum\frac{1}{n^3}$ is a convergent $p$-series

The series $\displaystyle\sum_{n=1}^\infty\frac{n}{n^3+1}$ *converges* by the DCT.
- Choose: $a_n=\frac{n}{n^3+1}$ and $b_n=\frac{1}{n^2}$
- Check: $0\leq \frac{n}{n^3+1}\leq \frac{1}{n^2}$ (notice that $\frac{n}{n^3+1}\leq\frac{n}{n^3}$)
- Observe: $\sum \frac{1}{n^2}$ is a convergent $p$-series

The series $\displaystyle\sum_{n=2}^\infty\frac{1}{n-1}$ *diverges* by the DCT.
- Choose: $a_n=\frac{1}{n}$ and $b_n=\frac{1}{n-1}$
- Check: $0\leq \frac{1}{n}\leq\frac{1}{n-1}$
- Observe: $\sum \frac{1}{n}$ is a divergent $p$-series

#### Limit comparison test examples
The series $\displaystyle\sum_{n=1}^\infty\frac{1}{2^n-1}$ *converges* by the LCT.
- Choose: $a_n=\frac{1}{2^n-1}$ and $b_n=\frac{1}{2^n}$.
- Compare in the limit: $$\lim_{n\to\infty}\frac{a_n}{b_n}\quad ⨠⨠ \quad \lim_{n\to\infty}\frac{2^n}{2^n-1}\quad ⨠⨠ \quad 1\;=:\; L$$
- Observe: $\sum\frac{1}{2^n}$ is a convergent geometric series

The series $\displaystyle\sum_{n=1}^\infty\frac{2n^2+3n}{\sqrt{5+n^5}}$ *diverges* by the LCT.
- Choose: $a_n=\frac{2n^2+3n}{\sqrt{5+n^5}}$, $b_n=n^{-1/2}$
- Compare in the limit: $$\lim_{n\to\infty}\frac{a_n}{b_n}\quad ⨠⨠ \quad \lim_{n\to\infty}\frac{(2n^2+3n)\sqrt{n}}{\sqrt{5+n^5}}$$ $$\frac{(2n^2+3n)\sqrt{n}}{\sqrt{5+n^5}}\quad\overset{n\to\infty}{\longrightarrow}\quad\frac{2n^{5/2}}{n^{5/2}}\to 2\;=:\;L$$
- Observe: $\sum n^{-1/2}$ is a divergent $p$-series

The series $\displaystyle\sum_{n=2}^\infty\frac{n^2}{n^4-n-1}$ *converges* by the LCT.
- Choose: $a_n=\frac{n^2}{n^4-n-1}$ and $b_n=n^{-2}$
- Compare in the limit: $$\lim_{n\to\infty}\frac{a_n}{b_n}\quad ⨠⨠ \quad \lim_{n\to\infty}\frac{n^4}{n^4-n-1}\quad ⨠⨠ \quad 1\;=:\;L$$
- Observe: $\sum_{n=2}^\infty n^{-2}$ is a converging $p$-series

## Alternating series
#### Alternating series test: basic illustration
(a) $\displaystyle\sum_{n=1}^\infty\frac{(-1)^{n-1}}{\sqrt{n}}$ converges by the AST.
- Notice that $\sum\frac{1}{\sqrt{n}}$ diverges as a $p$-series with $p=1/2<1$.
- Therefore the first series converges *conditionally*.

(b) $\displaystyle\sum_{n=1}^\infty\frac{\cos n\pi}{n^2}$ converges by the AST.
- Notice the funny notation: $\cos n\pi=(-1)^n$.
- This series converges *absolutely* because $\left|\frac{\cos n\pi}{n^2}\right|=\frac{1}{n^2}$, which is a $p$-series with $p=2>1$.

#### Approximating $\pi$
The Taylor series for $\tan^{-1} x$ is given by: $$\tan^{-1} x=x-\frac{x^3}{3}+\frac{x^5}{5}-\frac{x^7}{7}+\cdots$$

Use this series to approximate $\pi$ with an error less than $0.001$.

**Solution**
The main idea is to use $\tan\frac{\pi}{4}=1$ and thus $\tan^{-1} 1=\frac{\pi}{4}$. Therefore: $$\frac{\pi}{4}=1-\frac{1}{3}+\frac{1}{5}-\frac{1}{7}+\cdots$$ and thus: $$\pi=4-\frac{4}{3}+\frac{4}{5}-\frac{4}{7}+\cdots$$

Write $E_n$ for the error of the approximation, meaning $E_n=S-S_n$.

By the AST error formula, we have $|E_n|<a_{n+1}$.

We desire $n$ such that $|E_n|<0.001$. Therefore, calculate $n$ such that $a_{n+1}<0.001$, and then we will know: $$|E_n|<a_{n+1}<0.001$$

The general term is $a_n=\frac{4}{2n-1}$. Plug in $n+1$ in place of $n$ to find $a_{n+1}=\frac{4}{2n+1}$. Now solve: $$\begin{align*}\quad & a_{n+1}= \frac{4}{2n+1}< 0.001\\\\  \qquad ⨠⨠& \qquad  \frac{4}{0.001}< 2n+1\\\\  \qquad ⨠⨠& \qquad  3999< 2n\\\\  \qquad ⨠⨠& \qquad  2000\leq n\end{align*}$$

We conclude that at least $2000$ terms are necessary to be confident (by the error formula) that the approximation of $\pi$ is accurate to within $0.001$.

