---
cssclasses:
  - hide-embedded-header
title: W08 Notes
---
## Simple divergence test
Videos, Math Dr. Bob
- [Geometric series and SDT, again](https://www.youtube.com/watch?v=h84pokHK-JU): Geometric series, Simple Divergence Test (aka “Limit Test”)
- [Integral test](https://www.youtube.com/watch?v=F2R5hXXMP24): Basics
- [Integral test](https://www.youtube.com/watch?v=DaE9WrsEmDw): $p$-series
    - Extra: [Integral test](https://www.youtube.com/watch?v=m53wTpmiRmw): Further examples
    - Extra: [Integral test](https://www.youtube.com/watch?v=qj0SoBqazIA): Estimations

### 01 Theory

> [!concept] Simple Divergence Test (SDT)
> **Applicability:** *Any* series.
> 
> **Test Statement:** $$\lim_{n\to\infty}a_n\neq 0 \qquad \implies\qquad \sum_{n=1}^\infty a_n \quad\text{diverges}$$

- !! The *converse is not valid*. For example, $\sum_{n=1}^\infty \frac{1}{n}$ diverges even though $\lim_{n\to\infty}\frac{1}{n}=0$.

### 02 Illustration

> [!mexample] Simple Divergence Test: examples
> ![Simple divergence test: examples](Calculus/2025%20Spring/W08%20-%20Examples.md#Simple%20divergence%20test%20examples)

## Positive series

- [Direct Comparison Test](https://www.youtube.com/watch?v=lkHi2IZAJig): Theory and basic examples
- [Direct Comparison Test](https://www.youtube.com/watch?v=zThp_EGKDAo): Series $\frac{1}{\ln n}$
- [Limit Comparison Test](https://www.youtube.com/watch?v=Q4_ntBBtCsU): Theory and basic examples
- [Limit Comparison Test](https://www.youtube.com/watch?v=uZ4PRMxdV5o): Further examples

### 03 Theory

> [!concept] Positive series
> A series is called **positive** when its individual terms are positive, i.e. $a_n>0$ for all $n$.

The partial sum sequence $S_N$ is *monotone increasing* for a positive series.

By the monotonicity test for convergence of sequences, $S_N$ therefore converges whenever it is *bounded above*. If $S_N$ is not bounded above, then $\sum_{n=1}^\infty a_n$ diverges to $+\infty$.

---

Another test, called the **integral test**, studies the terms of a series as if they represent rectangles with upper corner pinned to the graph of a continuous function.

To apply the test, we must convert the integer index variable $n$ in $a_n$ into a continuous variable $x$. This is easy when we have a formula for $a_n$ (provided it doesn’t contain factorials or other elements dependent on integrality).

> [!concept] Integral Test (IT)
> **Applicability:**
> - (i) $f(x)> 0$
> - (ii) $f(x)$ is continuous
> - (iii) $f(x)$ is *monotone decreasing*
> 
> **Test Statement:** $$\sum_{n=1}^\infty a_n\quad\frac{\text{converges}}{\text{diverges}}\qquad\iff\qquad \int_1^\infty f(x)\,dx\quad\frac{\text{converges}}{\text{diverges}}$$

> [!extra] Extra - Integral test: explanation
> To show that *integral convergence implies series convergence*, consider the diagram:
> 
> ![200](Pasted%20image%2020241015174203.png)
> 
> This shows that $\sum_{n=2}^N a_n\leq \int_1^N f(x)\,dx$ for any $N$. Therefore, if $\int_1^\infty f(x)\,dx$ converges, then $\int_1^N f(x)\,dx$ is bounded (independent of $N$) and so $\sum_{n=2}^N a_n$ is bounded by that inequality. But $\sum_{n=2}^N a_n=S_N-a_1$; so by adding $a_1$ to the bound, we see that $S_N$ itself is bounded, which implies that $\sum_{n=1}^\infty a_n$ converges.
> 
> To show that *integral divergence implies series divergence*, consider a similar diagram: 
> 
> ![200](Pasted%20image%2020241015174216.png)
> 
> This shows that $\sum_{n=1}^{N-1} a_n \geq \int_1^N f(x)\,dx$ for any $N$. Therefore, if $\int_1^\infty f(x)\,dx$ diverges, then $\int_1^N f(x)\,dx$ goes to $+\infty$ as $N\to\infty$, and so $\sum_{n=1}^{N-1} a_n$ goes to $+\infty$ as well. So $\sum_{n=1}^\infty a_n$ diverges.
> 
> - ! Notice: the picture shows $f(x)$ entirely above (or below) the rectangles.
>     - This depends upon $f(x)$ being *monotone decreasing*, as well as $f(x)> 0$.
>     - This explains the applicability conditions.

---

Next we use the integral test to evaluate the family of **$p$-series**, and later we can use $p$-series in comparison tests without repeating the work of the integral test.

> [!concept] $p$-series
> A **$p$-series** is a series of this form: $\quad\displaystyle\sum_{n=1}^\infty \frac{1}{n^p}$
> 
> Convergence properties: 
> $$p>1: \text{series converges} \hspace{3cm} p\leq 1: \text{series diverges}$$

> [!extra] Extra - Proof of $p$-series convergence
> To verify the convergence properties of $p$-series, apply the integral test:
> 1. & Applicability: verify it’s continuous, positive, decreasing.
>     - Convert $n$ to $x$ to obtain the function $f(x)=\frac{1}{x^p}$.
>     - Indeed $\frac{1}{x^p}$ is continuous and positive and decreasing as $x$ increases.
> 2. &&& Apply the integral test.
>     - Integrate, assuming $p\neq 1$: $$\begin{align*}\int_1^\infty\frac{1}{x^p}\;dx\quad &⨠⨠ \quad  \lim_{R\to\infty}\;\left.\frac{x^{p-1}}{p-1}\right|^R_1 \\\\ &⨠⨠ \quad  \lim_{R\to\infty}\;\left(\frac{R^{-p+1}}{-p+1}-\frac{1^{-p+1}}{-p+1}\right)\end{align*}$$
>     - When $p>1$ we have $\lim_{R\to\infty}\;\frac{R^{-p+1}}{-p+1}=0$
>     - When $p<1$ we have $\lim_{R\to\infty}\;\frac{R^{-p+1}}{-p+1}=\infty$
>     - When $p=1$, integrate a second time: $$\begin{align*}\int_1^\infty\frac{1}{x}\,dx \quad &⨠⨠ \quad  \lim_{R\to\infty}\;\ln x\Big|_1^R \\\\ &⨠⨠ \quad  \lim_{R\to\infty}\; \ln R - \ln 1 \quad ⨠⨠ \quad  \infty\end{align*}$$
> 1. & Conclude: the integral converges when $p>1$ and diverges when $p\leq 1$.
> - ! Supplement: we could instead immediately refer to the convergence results for *$p$-integrals* instead of reproving them here.

### 04 Illustration

> [!mexample] $p$-series examples
> ![$p$-series examples](Calculus/2025%20Spring/W08%20-%20Examples.md#$p$-series%20examples)

> [!mexample] Integral test - pushing the envelope of convergence
> ![Integral test - pushing the envelope of convergence](Calculus/2025%20Spring/W08%20-%20Examples.md#Integral%20test%20-%20pushing%20the%20envelope%20of%20convergence)

### 05 Theory

> [!concept] Direct Comparison Test (DCT)
> **Applicability:** Both series are positive: $\;a_n>0$ and $b_n>0$.
> 
> **Test Statement:** Suppose $a_n\leq b_n$ for large enough $n$.
> (Meaning: for $n\geq N$ with some given $N$.) Then: 
> - Smaller pushes up bigger: $$\sum_{n=1}^\infty a_n\quad \text{diverges}\qquad \implies \qquad \sum_{n=1}^\infty b_n \quad \text{diverges}$$
> - Bigger controls smaller: $$\sum_{n=1}^\infty b_n\quad \text{converges}\qquad \implies \qquad \sum_{n=1}^\infty a_n \quad \text{converges}$$

### 06 Illustration

> [!mexample] Direct comparison test: rational functions
> ![Direct comparison test: rational functions](Calculus/2025%20Spring/W08%20-%20Examples.md#Direct%20comparison%20test%20rational%20functions)

### 07 Theory

Some series can be compared using the DCT after applying certain manipulations and tricks.

For example, consider the series $\sum_{n=2}^\infty\frac{1}{n^2-1}$. We suspect convergence because $a_n\approx \frac{1}{n^2}$ for *large* $n$. But unfortunately, $a_n>\frac{1}{n^2}$ always, so we cannot apply the DCT.

We could make some *ad hoc* arguments that do use the DCT, eventually:
- Trick Method 1:
    - Observe that for $n>1$ we have $\frac{1}{n^2-1}\leq\frac{10}{n^2}$. (Check it!)
    - But $\sum \frac{10}{n^2}$ converges, indeed its value is $10\cdot\sum\frac{1}{n^2}$, which is $\frac{10\pi^2}{6}$.
    - So the series $\sum\frac{1}{n^2-1}$ converges.
- Trick Method 2:
    - Observe that we can change the letter $n$ to $n+1$ by starting the new $n$ at $n=1$.
    - Then we have: $$\sum_{n=2}^\infty\frac{1}{n^2-1}\quad =\quad \sum_{n=1}^\infty\frac{1}{(n+1)^2-1}\quad =\quad \sum_{n=1}^\infty\frac{1}{n^2+2n}$$
    - This last series has terms smaller than $\frac{1}{n^2}$ so the DCT with $b_n=\frac{1}{n^2}$ (a convergent $p$-series) shows that the original series converges too.

These convoluted arguments suggest that a more general version of Comparison is possible.

Indeed, it is sufficient to compare the *limiting behavior* of two series. The limit of *ratios* (limit of ‘comparison’) links up the convergence / divergence of $\sum a_n$ and $\sum b_n$.

> [!concept] Limit Comparison Test (LCT) - “Limiting Ratio Test”
> **Applicability:** Both series are positive: $\;a_n>0$ and $b_n>0$.
> 
> **Test Statement:** Suppose that $\lim_{n\to\infty}\displaystyle\frac{a_n}{b_n}=L$. Then: 
> - If $0<L<\infty$: $$\sum a_n\quad\frac{\text{converges}}{\text{diverges}}\qquad \iff \qquad \sum b_n \quad\frac{\text{converges}}{\text{diverges}}$$
> 
> If $L=0$ or $L=\infty$, we can still draw an inference, but in only one direction:
> - If $L=0$: $$\sum b_n\quad\text{converges}\qquad \implies \qquad \sum a_n \quad\text{converges}$$
> - If $L=\infty$: $$\sum b_n\quad\text{diverges}\qquad \implies \qquad \sum a_n \quad\text{diverges}$$

> [!extra] Extra - Limit Comparison Test: Theory
> Suppose $a_n/b_n\to L$ and $0<L<\infty$. Then for $n$ sufficiently large, we know $a_n/b_n<L+1$.
> 
> Doing some algebra, we get $a_n<(L+1)b_n$ for $n$ large.
> 
> If $\sum b_n$ converges, then $\sum (L+1)b_n$ also converges (constant multiple), and then the DCT implies that $\sum a_n$ converges.
> 
> Conversely: we also know that $b_n/a_n\to 1/L$, so $b_n<(1/L+1)a_n$ for all $n$ sufficiently large. Thus if $\sum a_n$ converges, $\sum (1/L+1)a_n$ also converges, and by the DCT again $\sum b_n$ converges too.
> 
> The cases with $L=0$ or $L=\infty$ are handled similarly.

### 08 Illustration

> [!mexample] Limit Comparison Test examples
> ![Limit comparison test examples](Calculus/2025%20Spring/W08%20-%20Examples.md#Limit%20comparison%20test%20examples)

## Alternating series
Videos, Math Dr. Bob:
- [Alternating Series Test](https://www.youtube.com/watch?v=bwUxyxqUU8A): Theory and basic examples
- [Alternating Series Test](https://www.youtube.com/watch?v=MbAqIj3nrgU): Remainder estimates
- [Alternating Series Test](https://www.youtube.com/watch?v=CTJ-_DpZhmw): Further remainder estimates

### 09 Theory

Consider these series:
$$\begin{align*}1&+\frac{1}{2}+\frac{1}{3}+\frac{1}{4}+\frac{1}{5}+\frac{1}{6}+\frac{1}{7}+\cdots\quad=\quad\infty\\\\ -1&-\frac{1}{2}-\frac{1}{3}-\frac{1}{4}-\frac{1}{5}-\frac{1}{6}-\frac{1}{7}-\cdots\quad=\quad-\infty\\\\ 1&-\frac{1}{2}+\frac{1}{3}-\frac{1}{4}+\frac{1}{5}-\frac{1}{6}+\frac{1}{7}-\cdots\quad=\quad\ln 2\\\\ 1&+\frac{1}{2}-\frac{1}{3}+\frac{1}{4}-\frac{1}{5}-\frac{1}{6}+\frac{1}{7}+\cdots\quad=\quad\;?\end{align*}$$

The absolute values of terms are the same between these series, only the signs of terms change.

The first is a **positive series** because there are no negative terms.

The second series is the negation of a positive series – the study of such series is equivalent to that of positive series, just add a negative sign everywhere. These signs can be factored out of the series. (For example $\sum -\frac{1}{n}=-\sum \frac{1}{n}$.)

The third series is an **alternating series** because the signs alternate in a strict pattern, every other sign being negative.

The fourth series is *not* alternating, nor is it positive, nor negative: it has a mysterious or unknown pattern of signs.

A series with any negative signs present, call it $\sum_{n=1}^\infty a_n$, **converges absolutely** when the positive series of absolute values of terms, namely $\sum_{n=1}^\infty |a_n|$, converges.

> [!abstract] THEOREM: Absolute implies ordinary
> If a series $\sum_{n=1}^\infty a_n$ converges absolutely, then it also converges as it stands.

A series might converge due to the presence of negative terms and yet *not* converge absolutely: 

A series $\sum_{n=1}^\infty a_n$ is said to be **converge conditionally** when the series converges as it stands, but the series produced by inserting absolute values, namely $\sum_{n=1}^\infty |a_n|$, diverges.

The alternating harmonic series above, $1-\frac{1}{2}+\frac{1}{3}-\frac{1}{4}+\cdots\;=\;\ln 2$, is therefore conditionally convergent. Let us see why it converges. We can group the terms to create new sequences of *pairs*, each pair being a positive term. This can be done in two ways. The first creates an increasing sequence, the second a decreasing sequence: 

$$\begin{align*}\text{increasing from $0$:}\qquad & \left(1-\frac{1}{2}\right)+\left(\frac{1}{3}-\frac{1}{4}\right)+\left(\frac{1}{5}-\frac{1}{6}\right)+\left(\frac{1}{7}-\frac{1}{8}\right)+\cdots\\\\ \text{decreasing from $1$:}\qquad & 1-\left(\frac{1}{2}-\frac{1}{3}\right)-\left(\frac{1}{4}-\frac{1}{5}\right)-\left(\frac{1}{6}-\frac{1}{7}\right)-\cdots\end{align*}$$

Suppose $S_N$ gives the sequence of partial sums of the original series. Then $S_{2N}$ gives the first sequence of pairs, namely $S_2$, $S_4$, $S_6$, $\dots$ . And $S_{2N-1}$ gives the second sequence of pairs, namely $S_1$, $S_3$, $S_5$, $\dots$ .

The second sequence shows that $S_N$ is bounded above by $1$, so $S_{2N}$ is monotone increasing and bounded above, so it converges. Similarly $S_{2N-1}$ is monotone decreasing and bounded below, so it converges too, and of course they must converge to the same thing.

The fact that the terms were *decreasing in magnitude* was an essential ingredient of the argument for convergence. This fact ensured that the parenthetical pairs were positive numbers.

> [!concept] Alternating Series Test (AST) - “Leibniz Test”
> **Applicability:** Alternating series only: $\;\sum_{n=1}^\infty (-1)^{n-1}a_n$ with $a_n>0$
> 
> **Test Statement:**
> If:
>  - (1) $a_n$ are *decreasing*, so $a_1> a_2> a_3> a_4>\dots>0$
>  - (2) $a_n\to 0$ as $n\to\infty$ (i.e. it passes the SDT)
> 
> Then: $$\sum_{n=1}^\infty (-1)^{n-1}a_n\quad\text{converges}$$
> 
> Furthermore, partial sum *errors* are bounded by “subsequent terms”: $$|S-S_N|\leq a_{N+1}$$

> [!extra] Extra - Alternating Series Test: Theory
> Just as for the alternating harmonic series, we can form *positive* paired-up series because the terms are decreasing: $$\begin{align*}\left(a_1-a_2\right)+\left(a_3-a_4\right)+\left(a_5-a_6\right)+\cdots\\\\ a_1-\left(a_2-a_3\right)-\left(a_4-a_5\right)-\left(a_6-a_7\right)-\cdots\end{align*}$$
> 
> The first sequence $S_{2N}$ is monotone increasing from $0$, and the second $S_{2N-1}$ is decreasing from $a_1$. The first is therefore also bounded above by $a_1$. So it converges. Similarly, the second converges. Their difference at any point is $S_{2N}-S_{2N-1}$ which is equal to $-a_{2N}$, and this goes to zero. So the two sequences must converge to the same thing.
> 
> By considering these paired-up sequences and the effect of adding each new term one after the other, we obtain the following order relations: $$0<S_2<S_4<S_6<\;\cdots\;<S<\;\cdots\;<S_5<S_3<S_1=a_1$$
> 
> Thus, for *any even $2N$* and *any odd $2M-1$*: $$S_{2N}<S<S_{2M-1}$$
> 
> Now set $M=N$ and subtract $S_{2N-1}$ from both sides: $$\begin{aligned}S_{2N}-S_{2N-1}&<S-S_{2N-1}<0\\\\ ⨠⨠ \quad -a_{2N}&<S-S_{2N-1}<0\end{aligned}$$
> 
> Now set $M=N+1$ and subtract $S_{2N}$ from both sides: $$\begin{aligned}0<S-S_{2N}&<S_{2N+1}-S_{2N}\\\\ ⨠⨠ \quad 0<S-S_{2N}&<a_{2N+1}\end{aligned}$$
> 
> This covers both even cases ($n=2N$) and odd cases ($n=2N-1$). In either case, we have: $$|S-S_n|<a_{n+1}$$

### 10 Illustration

> [!mexample] Alternating Series Test: Basic illustration
> ![Alternating series test: basic illustration](Calculus/2025%20Spring/W08%20-%20Examples.md#Alternating%20series%20test%20basic%20illustration)

> [!mexample] Approximating $\pi$
> ![Approximating $\pi$](Calculus/2025%20Spring/W08%20-%20Examples.md#Approximating%20$%20pi$)

