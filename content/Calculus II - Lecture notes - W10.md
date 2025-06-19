---
cssclasses:
  - hide-embedded-header
title: W10 Notes
---
## Ratio test and Root test
Videos, Math Dr. Bob
- [Ratio test](https://www.youtube.com/watch?v=IrTB5cA8HgQ): Basics
- [Ratio test](https://www.youtube.com/watch?v=ARtxUdTuFvA): Ratio test + DCT
- [Root test](https://www.youtube.com/watch?v=XI608axS5FM): Basics
- [Root test](https://www.youtube.com/watch?v=INLXzB2cW3U): for $\sum (1-1/n^2)^{n^3}$

### 01 Theory

> [!concept] Ratio Test (RaT)
> **Applicability:** Any series with nonzero terms.
> 
> **Test Statement:**
> 
> Suppose that $\displaystyle\left|\frac{a_{n+1}}{a_n}\right|\longrightarrow L$ as $n\to\infty$.
> 
> Then: $$\begin{align*}L<1:&&& \sum_{n=1}^\infty a_n\quad\text{converges absolutely}\\L>1:&&& \sum_{n=1}^\infty a_n\quad\text{diverges}\\\\L=1\;\text{or DNE}:&&& \text{test inconclusive}\end{align*}$$

> [!extra] Extra - Ratio test: explanation
> To understand the ratio test, consider this series: $$\sum_{n=0}^\infty\frac{2^n}{n!}\quad=\quad 1+\frac{2}{1!}+\frac{2^2}{2!}+\frac{2^3}{3!}+\cdots$$
> - The term $\frac{2^3}{3!}$ is given by multiplying the prior term by $\frac{2}{3}$.
> - The term $\frac{2^4}{4!}$ is given by multiplying the prior term by $\frac{2}{4}$.
> - The term $a_n$ is created by multiplying the prior term by $\frac{2}{n}$.
> 
> When $n>3$, the multiplication factor giving the next term is necessarily less than $\frac{2}{3}$. Therefore, when $n>3$, the terms shrink *faster than those of a geometric series* having $r=\frac{2}{3}$. Therefore this series converges.
> 
> Similarly, consider this series: $$\sum_{n=0}^\infty\frac{10^n}{n!}\quad=\quad 1+\frac{10}{1!}+\frac{10^2}{2!}+\frac{10^3}{3!}+\cdots$$
> 
> Write $R_n = \frac{a_n}{a_{n-1}}$ for the ratio from the prior term $a_{n-1}$ to the current term $a_n$. For this series, $R_n=\frac{10}{n}$.
> 
> This ratio falls below $\frac{10}{11}$ when $n>11$, after which the terms necessarily shrink faster than those of a geometric series with $r=\frac{10}{11}$. Therefore this series converges.
> 
> The main point of the discussion can be stated like this: 
> $$R_n\to L<1\quad\text{as}\;\; n\to\infty$$
> 
> Whenever this is the case, then *eventually* the ratios are bounded below some $r<1$, and the series terms are smaller than those of a converging geometric series.

> [!extra] Extra - Ratio test: proof
> Let us write $R_n=\left|\frac{a_{n+1}}{a_n}\right|$ for the ratio to the next term from term $n$.
> 
> Suppose that $R_n\to L$ as $n\to\infty$, and that $L<1$. This means: eventually the ratio of terms is close to $L$; so eventually it is less than $1$.
> 
> More specifically, let us define $r=\frac{L+1}{2}$. This is the point halfway between $L$ and $1$. Since $R_n\to L$, we know that eventually $R_n<r$.
> 
> Any geometric series with ratio $r$ converges. Set $c=a_N$ for $N$ big enough that $R_N<r$. Then the terms of our series satisfy $|a_{N+n}|\leq cr^n$, and the series starting from $a_N$ is absolutely convergent by comparison to this geometric series.
> 
> (Note that the terms $a_1,\,\dots,\,a_{N-1}$ do not affect convergence.)

### 02 Illustration

> [!mexample] Example - Ratio test
> ![Ratio test examples](Calculus/2025%20Spring/W10%20-%20Examples.md#Ratio%20test%20examples)

### 03 Theory

> [!concept] Root Test (RooT)
> **Applicability:** Any series.
> 
> **Test Statement:**
> 
> Suppose that $\sqrt[n]{|a_n|}\longrightarrow L$ as $n\to\infty$.
> 
> Then: $$\begin{align*}L<1:&&& \sum_{n=1}^\infty a_n\quad\text{converges absolutely}\\L>1:&&& \sum_{n=1}^\infty a_n\quad\text{diverges}\\\\L=1\;\text{or DNE}:&&& \text{test inconclusive}\end{align*}$$

> [!extra] Extra - Root test: explanation
> The fact that $\sqrt[n]{|a_n|}\to L$ and $L<1$ implies that eventually $\sqrt[n]{|a_n|}<r$ for all high enough $n$, where $r=\frac{L+1}{2}$ is the midpoint between $L$ and $1$.
> 
> Now, the equation $\sqrt[n]{|a_n|}<r$ is equivalent to the equation $|a_n|<r^n$.
> 
> Therefore, eventually the terms $|a_n|$ are each less than the corresponding terms of this convergent geometric series: $$\sum_{n=1}^\infty r^n\;=\; 1+r+r^2+r^3+\cdots$$

### 04 Illustration

> [!mexample] Root test examples
> ![Root test examples](Calculus/2025%20Spring/W10%20-%20Examples.md#Root%20test%20examples)

> [!mexample] Ratio test versus root test
> ![Ratio test versus root test](Calculus/2025%20Spring/W10%20-%20Examples.md#Ratio%20test%20versus%20root%20test)

## Series tests: strategy tips
Videos, Math Dr. Bob
- [Series test round-up](https://www.youtube.com/watch?v=INEvgmVI4q4): Part I
- [Series test round-up](https://www.youtube.com/watch?v=CxC74YuWf1Y): Part II
- [Series test round-up](https://www.youtube.com/watch?v=T8P9RdKHwNU): Part III

Videos, Trefor Bazett
- [How to choose a series convergence test](https://www.youtube.com/watch?v=0wefqjpQyKM)

### 05 Theory

It can help to associate certain “strategy tips” to find convergence tests based on certain patterns.

> [!tip] Matching powers → Simple Divergence Test
> $$\displaystyle\sum_{n=1}^\infty \frac{n-1}{2n+1}$$
> 
> Use the SDT because we see the highest power is the *same* ($=1$) in numerator and denominator.

> [!tip] Rational or Algebraic → Limit Comparison Test
> $$\sum_{n=1}^\infty\frac{\sqrt{n^3+1}}{3n^3+4n^2+2}$$
> 
> Use the LCT because we have a *rational or algebraic* function (positive terms).

> [!tip] Not rational, not factorials → Integral Test
> $$\sum_{n=1}^\infty ne^{-n^2}$$
> 
> Use the IT because we do *not* have a rational/algebraic function, and we do *not* see factorials.

> [!tip] Rational, alternating → AST, and LCT or DCT
> $$\sum_{n=1}^\infty (-1)^n\frac{n^2}{n^4+1}$$
> 
> Use the AST because it’s alternating. Then use the LCT (to find absolute convergence) because its a rational function.

> [!tip] Factorials → Ratio Test
> $$\sum_{n=1}^\infty\frac{2^n}{n!}$$
> 
> Use the RaT because we see a factorial. (In case of alternating + factorial, use RaT first.)

> [!tip] Recognize geometric → LCT or DCT
> $$\sum_{n=1}^\infty\frac{1}{2+3^n}$$
> 
> Use the LCT or DCT comparing to $\frac{1}{3^n}$ because we see similarity to $\frac{1}{3^n}$ (recognize geometric).

## Power series: Radius and Interval
Videos, Math Dr. Bob
- [Power series](https://www.youtube.com/watch?v=1alNQXbYJ-s): Interval and Radius of Convergence
- [Power series](https://www.youtube.com/watch?v=Nl_QMUaoecc): Interval of Convergence Using Ratio Test
    - [Further example](https://www.youtube.com/watch?v=aBhSIFyYNgI)
- [Power series](https://www.youtube.com/watch?v=nnUFDQRuZek): Interval of Convergence Using Root Test
- [Power series](https://www.youtube.com/watch?v=86NxxlveaqI): Finding the Center

### 06 Theory
A power series looks like this: 

$$f(x)\;=\;a_0+a_1x+a_2x^2+a_3x^3+\cdots$$

Power series are used to *build and study functions*. They allow a uniform “modeling framework” in which many functions can be described and compared. Power series are also convenient for *computers* because they provide a way to store and evaluate *differentiable* functions with numerical (approximate) values.

> [!warning] Small $x$ needed for power series
> The most important fact about power series is that they work for *small values of $x$*.
> 
> Many power series diverge for $|x|$ too big; but even when they converge, for big $|x|$ they converge more slowly, and partial sum approximations are less accurate.

The idea of a power series is a modification of the idea of a geometric series in which the common ratio $r$ becomes a variable $x$, and each term has an additional *coefficient parameter* $a_n$ controlling the relative contribution of different orders.

%% 
> [!tip] Thinking about power series: scale and order of magnitude
> It can be helpful to think about power series with a heuristic. Each power of $x$, such as $x^2$ or $x^4$, gives a function with a *sensitivity* to small inputs $x$ that *decreases* with the power. Consider that $0.1^2=0.01$ while $0.1^5=0.00001$.
> 
> The coefficients $a_n$ jointly control the response of $f(x)$ to $x$ at *different scales*. The “coarse-grained,” or most sensitive, response is controlled by $a_0$ and $a_1$. The “fine-grained,” or less sensitive, response is controlled by higher $a_n$ like $a_5$ or $a_{17}$.
> 
> The setup is like having coarse and fine controls on the focal length of a microscope. The large knob that moves over a large range is like $a_1$, and the small knob that gives fine control is like a higher coefficient such as $a_{10}$.
> 
> By combining these response controls $a_n$ at different size scales via the powers $x^n$, we build a function with any desired behavior for values of $x$ near $0$.

 %%
 
### 07 Theory

Every power series has a **radius of convergence** and an **interval of convergence**.

> [!concept] Radius of convergence
> Consider a power series centered at $x=0$:
> 
> $$f(x)=a_0+a_1x+a_2x^2+a_3x^3+\cdots$$
> 
> Define $L$ as the limit of coefficient ratios: 
> 
> $$L\;=\;\lim_{n\to\infty}\,\left|\frac{a_{n+1}}{a_n}\right|$$
> 
> Then reciprocal, $R=1/L$, is the **radius of convergence**; it can be anything in $[0,\infty]$ including either extreme.
> 
> The power series necessarily converges for $|x|<R$ and diverges for $|x|>R$.

> [!extra] Extra - Radius of convergence: explanatory proof
> Treat the variable $x$ in the power series $f(x)=a_0+a_1x+a_2x^2+\cdots$ as a constant.
> 
> Apply the ratio test to this series. The ratio function is: 
> 
> $$R_n=\displaystyle\left|\frac{a_{n+1}}{a_n}\right|\cdot|x|$$
> 
> Since $|x|$ is a constant here, we have: $$\lim_{n\to\infty}\,R_n \;=\; L|x|$$
> 
> Therefore, the ratio test says that the series converges absolutely when $|x|<1/L$, and diverges when $|x|>1/L$.

---

We can build **shifted power series** for $x$ near another value $c$. Just replace the variable $x$ with a shifted variable $u=x-c$: 

$$\begin{gather}a_0+a_1u+a_2u^2+a_3u^3+\cdots\\\\ ⨠⨠ \quad  a_0+a_1(x-c)+a_2(x-c)^2+a_3(x-c)^3+\cdots\end{gather}$$

The radius of convergence of a shifted series is calculated in the same way, using the coefficients: 

$$R=\frac{1}{\lim_{n\to\infty}\left|\frac{a_{n+1}}{a_n}\right|}$$

However, in the shifted setting, the radius of convergence concerns the *distance from $c$*: Such a power series converges when $|x-c|<R$ and diverges when $|x-c|>R$.

---

The **interval of convergence** of a power series is determined by:
- the radius of convergence
- the center point
- special consideration of endpoints

> [!concept] Interval of convergence
> The interval of convergence $I$ of a power series $f(x)=a_0+a_1x+a_2x^2+\cdots$ is the set of values of $x$ where the series converges.
> 
> The interval of convergence $I$ is:
> - centered at $x=c$
> - extending a distance $R$ to either side of $c$
> - including / excluding the endpoints where $|x-c|=R$ depending on the particular case

To calculate the interval of convergence, follow these steps: 
- Observe the center $c$ of the shifted series; $c=0$ corresponds to no shift.
- Take the limit to compute $R$.
- Write down the *preliminary interval* $(c-R,\,c+R)$.
- Plug each endpoint $c-R$ and $c-R$ into the original series
    - → check for convergence
- Add in the convergent endpoints. There are 4 total possibilities.

### 08 Illustration

> [!mexample] Example - Radius and interval for a few series
> ![Radius and interval for a few series](Calculus/2025%20Spring/W10%20-%20Examples.md#Radius%20and%20interval%20for%20a%20few%20series)

> [!mexample] Example - Radius of convergence
> ![Radius of convergence](Calculus/2025%20Spring/W10%20-%20Examples.md#Radius%20of%20convergence)

> [!mexample] Example - Interval of convergence
> ![Interval of convergence](Calculus/2025%20Spring/W10%20-%20Examples.md#Interval%20of%20convergence)

> [!mexample] Interval of convergence - further examples
> ![Interval of convergence - further examples](Calculus/2025%20Spring/W10%20-%20Examples.md#Interval%20of%20convergence%20-%20further%20examples)

