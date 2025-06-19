---
cssclasses:
  - hide-embedded-header
title: W11 Notes
---
## Power series as functions
Videos, Math Dr. Bob
- [Power series functions](https://www.youtube.com/watch?v=aiI2tiTFOcg): Derivative/Antiderivative - Basics
- [Power series functions](https://www.youtube.com/watch?v=j22XJ0-lzsM): Derivative/Antiderivative - Interval of Convergence
- [Power series functions](https://www.youtube.com/watch?v=HiGkS4KXHuk): Derivative/Antiderivative - More examples
- [Power series functions](https://www.youtube.com/watch?v=gGw1NUUSn30): Geometric Power Series

### 01 Theory
Given a numerical value for $x$ within the interval of convergence of a power series, the series sum may be considered as the output $f(x)$ of a function $f$.

Many techniques from algebra and calculus can be applied to such power series functions.

**Addition and Subtraction:** 
$$\begin{align*}f \;&= \;  a_0+a_1x+a_2x^2+a_3x^3+\cdots\\ g \;&= \;  b_0+b_1x+b_2x^2+b_3x^3+\cdots\\ \hline\\ f+g \;&= \;  (a_0+b_0)+(a_1+b_1)\,x+(a_2+b_2)\,x^2+\cdots\end{align*}$$

Summation notation: $$\sum_{n=0}^\infty a_nx^n + \sum_{n=0}^\infty b_nx^n \quad=\quad \sum_{n=0}^\infty(a_n+b_n)x^n$$

**Scaling:** 
$$cf \;=\; ca_0+(ca_1)\,x+(ca_2)\,x^2+\cdots$$

Summation notation: $$c\sum_{n=0}^\infty a_nx^n\quad=\quad \sum_{n=0}^\infty (ca_n)\,x^n$$

> [!extra] Extra - Multiplication and composition
> **Multiplication:**
> $$\begin{align*}f\cdot g &= \left(a_0+a_1x+a_2x^2+\cdots\right)\cdot\left(b_0+b_1x+b_2x^2+\cdots\right)\\\\ &= a_0b_0+\left(a_0b_1+a_1b_0\right)\,x+\left(a_0b_2+a_1b_1+a_2b_0\right)\,x^2+\cdots\end{align*}$$
> 
> For example, suppose that the geometric power series $f(x)=1+x+x^2+x^3+\cdots$ converges, so $|x|<1$. Then we have for its square: 
> $$\begin{align*}f\cdot f\;=\; f(x)^2 \;&= \;  (1+x+x^2+\cdots)\cdot (1+x+x^2+\cdots)\\&= \;  1+(1+1)x+(1+1+1)x^2+\cdots\\&= \;  1+2x+3x^2+4x^3+\cdots \\&=\; \sum_{n=0}^\infty (n+1)x^n\end{align*}$$
> 
> **Composition:**
> $$\begin{align*}f(-x)\;&= \;  1-x+x^2-x^3+x^4-\cdots\\\\ f(2x^3) \;&= \;  1+2x^3+(2x^3)^2+\cdots\\ \;&= \;  1+2x^3+4x^6+8x^9+\cdots\end{align*}$$

---

Assume:  $$f \;=\; a_0+a_1x+a_2x^2+a_3x^3+\cdots\;=\; \sum_{n=0}^\infty a_n x^n$$
Then:

**Differentiation:**
$$\frac{df}{dx}\;=\; a_1+(2a_2)\,x+(3a_3)\,x^2+\cdots\quad=\quad \sum_{n=1}^\infty na_nx^{n-1}$$

**Antidifferentiation:**
$$\int f(x)\,dx\;=\; C+a_0x+\frac{a_1}{2}x^2+\frac{a_2}{3}x^3+\cdots \quad=\quad  C+\sum_{n=0}^\infty\frac{a_n}{n+1}x^{n+1}$$

For example, for the geometric series we have: 
$$\begin{align*}f&\;=\;  1+x+x^2+x^3+x^4+\cdots\\\\ \frac{df}{dx}&\;=\;  1+2x+3x^2+4x^3+5x^4+\cdots\\\\ \int f\,dx&\;=\;  C+x+\frac{1}{2}x^2+\frac{1}{3}x^3+\frac{1}{4}x^4+\cdots\end{align*}$$

---

Do the series created with sums, products, derivatives etc., all converge? On what interval?

For the algebraic operations, the resulting power series will converge wherever both of the original series converge.

For calculus operations, the *radius* is preserved, but the *endpoints* are not necessarily:

> [!abstract] Power series calculus - Radius preserved
> If the power series $f(x)$ has radius of convergence $R$, then the power series $f'(x)$ and $\int f\,dx$ also have the same radius of convergence $R$.

> [!warning] Power series calculus - Endpoints not preserved
> It is possible that a power series $f(x)$ converges at and endpoint $a$ of its interval of convergence, yet $f'$ and $\int f\,dx$ do *not* converge at $a$.

> [!extra] Extra - Proof of radius for derivative and integral series
> Suppose $f(x)$ has radius of convergence $R=L^{-1}$: $$\left|\frac{a_{n+1}}{a_n}\right|\cdot|x|\longrightarrow L\cdot|x|\quad\text{ as }\;n\to\infty$$
> 
> Consider now the derivative $f'$ and its ratios of successive terms: 
> $$\left|\frac{(n+1)a_{n+1}x^{n}}{na_nx^{n-1}}\right|=\left(\frac{n+1}{n}\right)\cdot\left|\frac{a_{n+1}}{a_n}\right|\cdot|x|\quad\overset{n\to\infty}{\longrightarrow}\quad 1\cdot L\cdot |x|=L\cdot|x|$$
> 
> Consider instead the antiderivative $\int f\,dx$ and its ratios of successive terms: 
> $$\left|\frac{\left(\frac{1}{n+1}\right)a_{n}x^{n+1}}{\left(\frac{1}{n}\right)a_{n-1}x^{n}}\right|=\left(\frac{n}{n+1}\right)\cdot\left|\frac{a_{n}}{a_{n-1}}\right|\cdot|x|\quad\overset{n\to\infty}{\longrightarrow}\quad 1\cdot L\cdot |x|=L\cdot|x|$$
> 
> In both these cases the ratio test provides that the series converges when $|x|<L^{-1}$.

### 02 Illustration

> [!mexample] Example - Geometric series: algebra meets calculus
> ![Geometric series: algebra meets calculus](Calculus/2025%20Spring/W11%20-%20Examples.md#Geometric%20series%20algebra%20meets%20calculus)

> [!mexample] Example - Manipulating geometric series: algebra
> ![Manipulating geometric series: algebra](Calculus/2025%20Spring/W11%20-%20Examples.md#Manipulating%20geometric%20series%20algebra)

> [!mexample] Example - Manipulating geometric series: calculus
> ![Manipulating geometric series: calculus](Calculus/2025%20Spring/W11%20-%20Examples.md#Manipulating%20geometric%20series%20calculus)

> [!mexample] Example - Recognizing and manipulating geometric series: Part I
> ![Recognizing and manipulating geometric series: Part I](Calculus/2025%20Spring/W11%20-%20Examples.md#Recognizing%20and%20manipulating%20geometric%20series%20Part%20I)

> [!mexample] Example - Recognizing and manipulating geometric series: Part II
> ![Recognizing and manipulating geometric series: Part II](Calculus/2025%20Spring/W11%20-%20Examples.md#Recognizing%20and%20manipulating%20geometric%20series%20Part%20II)


## Taylor and Maclaurin series
Videos, Math Dr. Bob
- [Maclaurin series](https://www.youtube.com/watch?v=xsuTDV26hp0): $f(x)=\frac{1}{(1-x)^2}$
- [Maclaurin series](https://www.youtube.com/watch?v=ebPmGeTom-c): $f(x)=e^x$
- [Maclaurin series](https://www.youtube.com/watch?v=43QNY-edoys): $f(x)=\sin x,\, \cos x,\,\tan x$
- [Taylor series](https://www.youtube.com/watch?v=8XDxDMcgh0g): $f(x)=\ln x$ at $x=1$

### 03 Theory

Suppose that we have a power series function: $$f(x)=a_0+a_1x+a_2x^2+a_3x^3+\cdots$$

Consider the *successive derivatives* of $f$: 
$$
\begin{array}{r}f(x)&=&a_0&+&a_1x&+&a_2x^2&+&a_3x^3&+&a_4x^4&+&\cdots\\ f'(x)&=&0&+&a_1&+&2\cdot a_2x^1&+&3\cdot a_3x^2&+&4\cdot a_4x^3&+&\cdots\\ f''(x)&=&0&+&0&+&2\cdot a_2&+&3\cdot2\cdot a_3x^1&+&4\cdot3\cdot a_4x^2&+&\cdots\\ f'''(x)&=&0&+&0&+&0&+&3\cdot2\cdot1\cdot a_3&+&4\cdot3\cdot2\cdot a_4x^1&+&\dots\\ \vdots&&&\vdots&&&\vdots&&&\vdots\\ f^{(n)}(x)&=&0&+&0&+&0&+&0&+&\dots+n!\cdot a_n&+&\cdots\end{array}
$$

When these functions are evaluated at $x=0$, all terms with a positive $x$-power become zero: 
$$
\begin{array}{r}f(0)&=&a_0&=&a_0\\ f'(0)&=&a_1&=&a_1\\ f''(0)&=&2\cdot a_2 &=& 2!\cdot a_2\\ f'''(0)&=&3\cdot2\cdot a_3&=&3!\cdot a_3\\\vdots&=&\vdots&=&\vdots\\ f^{(n)}(0)&=&n\cdot(n-1)\cdots2\cdot1\cdot a_n&=&n!\cdot a_n\end{array}
$$

This last formula is the basis for Taylor and Maclaurin series: 

> [!abstract] Power series: Derivative-Coefficient Identity
> $$f^{(n)}(0)\quad=\quad n!\cdot a_n$$
> 
> This identity holds for a power series function $f(x)=a_0+a_1x+a_2x^2+a_3x^3+\cdots$ which has a nonzero radius of convergence.

We can apply the identity in both directions: 
- Know $f(x)$? $\quad\rightsquigarrow\quad$ Calculate $a_n$ for any $n$.
- Know $a_n$? $\quad\rightsquigarrow\quad$ Calculate $f^{(n)}(0)$ for any $n$.

---

Many functions can be ‘expressed’ or ‘represented’ near $x=c$ (i.e. for small enough $|x-c|$) as convergent power series. (This is true for almost all the functions encountered in pre-calculus and calculus.)

Such a power series representation is called a **Taylor series**.
When $c=0$, the Taylor series is also called the **Maclaurin series**.

One power series representation we have already studied: 

$$\frac{1}{1-x}\quad=\quad 1+x+x^2+x^3+\cdots$$

---

Whenever a function has a power series (Taylor or Maclaurin), the Derivative-Coefficient Identity may be applied to *calculate the coefficients* of that series.

Conversely, sometimes a series can be interpreted as an *evaluated power series* coming from $x=c$ for some $c$. If the closed form function format can be obtained for this power series, the *total sum of the original series may be discovered* by putting $x=c$ in the argument of the function.

%% 
> [!warning] YES $a_n\rightsquigarrow f^{(n)}(0)$ , but... MAYBE NOT $f^{(n)}(0)\rightsquigarrow a_n$
> The reasoning might not work backwards:
> 
> Given a function $f(x)$ that is differentiable (all derivatives), we can produce a series using the formula $a_n=\frac{f^{(n)}(0)}{n!}$, namely: $$f(0)+\frac{f'(0)}{1!}x+\frac{f''(0)}{2!}x^2+\cdots+\frac{f^{(n)}(0)}{n!}x^n+\cdots$$ But this series might **NOT** converge, or it might converge and **NOT** equal with the original function $f(x)$. It could be a different function.
> 
> - ! For example, $f(x)=e^{-1/x^2}$ generates the series with $a_n=0$ for all $n$, yet $f(x)$ is not the zero function.
> 
> However, the forward reasoning is still interesting for given functions:
> 
> IF a function equals some converging power series, THEN the coefficients are uniquely determined and may be computed using the formula $a_n=\frac{f^{(n)}(0)}{n!}$.

> [!abstract] Theorem: Validity of power series representation
> Suppose that there is a constant $K>0$ such that $|f^{(n)}(x)|\leq K$ for all $x\in(-R,R)$.
> 
> (In other words: the derivatives $f^{(n)}$ do not “grow too quickly”, rather they are “controlled by $K$.”) 
> 
> Then: $$f(x) = \sum_{n=0}^\infty \frac{f^{(n)}(0)}{n!}x^n$$
> 
> and the series converges on the interval.

> [!mexample] Example - The function $f(x)=e^x$ equals its power series for any $x\in(-\infty,+\infty)$
> First observe that $f^{(n)}(x)=e^x$ because $\frac{d}{dx}e^x=e^x$.
> 
> Now suppose $R>0$ is any number. Then $|f^{(n)}(x)|=|e^x|$ satisfies $|e^x|\leq e^R$ on $x\in(-R,R)$. Therefore if we let $K=e^R$ we see that $|f^{(n)}(x)|\leq K$ for any $x\in(-R,R)$. By the theorem, the series must converge and equal $e^x$ as functions *on the interval* $(-R,R)$.
> 
> Since that is true for all possible $R>0$, in fact we know that the series for $e^x$ converges and equals $e^x$ *everywhere*.
> 
> Now let us compute the series. Since $f^{(n)}(x)=e^x$ we see that $f^{(n)}(0)=e^0=1$ for any $n$. So $a_n=\frac{1}{n!}$ for any $n$. In conclusion we have: 
> $$
> e^x = 1+\frac{1}{1!}x+\frac{1}{2!}x^2+\frac{1}{3!}x^3+\cdots
> $$

%%

### 04 Illustration

> [!mexample] Example - Maclaurin series of $e^x$
> ![Maclaurin series of $e^x$](Calculus/2025%20Spring/W11%20-%20Examples.md#Maclaurin%20series%20of%20$e%20x$)

> [!mexample] Example - Maclaurin series of $\cos x$
> ![Maclaurin series of $\cos x$](Calculus/2025%20Spring/W11%20-%20Examples.md#Maclaurin%20series%20of%20$%20cos%20x$)

> [!mexample] Maclaurin series from other Maclaurin series
> ![Maclaurin series from other Maclaurin series](Calculus/2025%20Spring/W11%20-%20Examples.md#Maclaurin%20series%20from%20other%20Maclaurin%20series)

> [!mexample] Computing a Taylor series
> ![Computing a Taylor series](Calculus/2025%20Spring/W11%20-%20Examples.md#Computing%20a%20Taylor%20series)

### 05 Theory

> [!warning] Study these!
> - Memorize all of these series!
> - Recognize all of these series!
> - Recognize all of these summation formulas!

$$
\begin{align*}
\frac{1}{1-x}&=1+x+x^2+\cdots &=\quad & \sum_{n=0}^{\infty} x^n, \quad R=1, \quad \text{interval: }\;(-1,1) \\
\ln (1-x)&=-\frac{x}{1}-\frac{x^2}{2}-\frac{x^3}{3}-\cdots &=\quad &\sum_{n=0}^{\infty}-\frac{x^{n+1}}{n+1}, \quad R=1, \quad\text{interval: }\;[-1,1) \\
\tan ^{-1} x&=x-\frac{x^3}{3}+\frac{x^5}{5}-\cdots &=\quad &\sum_{n=0}^{\infty}(-1)^n \frac{x^{2 n+1}}{2 n+1}, \quad R=1, \quad\text{interval: }\;[-1,1] \\
e^x&=1+\frac{x}{1!}+\frac{x^2}{2!}+\cdots &=\quad &\sum_{n=0}^{\infty} \frac{x^n}{n!}, \quad R=\infty \\
\cos x&=1-\frac{x^2}{2!}+\frac{x^4}{4!}-\cdots &=\quad &\sum_{n=0}^{\infty}(-1)^n \frac{x^{2 n}}{(2 n)!}, \quad R=\infty \\
\sin x&=x-\frac{x^3}{3!}+\frac{x^5}{5!}+\cdots &=\quad &\sum_{n=0}^{\infty}(-1)^n \frac{x^{2 n+1}}{(2 n+1)!}, \quad R=\infty
\end{align*}
$$


## Applications of Taylor series
Videos, Math Dr. Bob
- [Approximating with Maclaurin polynomials](https://www.youtube.com/watch?v=7_5yc4IIcbw): $f(x)=\ln(1-x)$ to find $\ln(1.1)$
- [Approximating with Taylor polynomials](https://www.youtube.com/watch?v=8jXynT202wg): $f(x)=\frac{1}{x+1}$ at $x=1$ to find $1/2.1$

### 06 Theory reminder

**Linear approximation** is the technique of approximating a specific value of a function, say $f(x_1)$, at a point $x_1$ that is close to another point $x_0$ where we *know* the exact value $f(x_0)$. We write $\Delta x$ for $x_1-x_0$, and $y_0=f(x_0)$, and $y_1=f(x_1)$. Then we write $dy=f'(x_0)\cdot\Delta x$ and use the fact that: $$y_1\approx y_0+dy=y_0+f'(x_0)\cdot\Delta x$$

> [!mexample] Computing a linear approximation
> For example, to approximate the value of $\sqrt{4.01}$, set $f(x)=\sqrt{x}$, set $x_0=4$ and $y_0=2$, and set $x_1=4.01$ so $\Delta x=0.01$.
> 
> Then compute: $f'(x)=\frac{1}{2\sqrt{x}}$
> So $f'(x_0)=1/4$.
> 
> Finally: $$y_1\approx y_0+f'(x_0)\cdot\Delta x\qquad ⨠⨠ \qquad y_1\approx 2+\frac{1}{4}\cdot 0.01=2.0025$$

---

Now recall the **linearization** of a function, which is itself another function:

Given a function $f(x)$, the linearization $L(x)$ at the basepoint $x=c$ is: 
$$L(x)=f(c)+f'(c)(x-c)$$

The graph of this linearization $L(x)$ is the tangent line to the curve $y=f(x)$ at the point $(c,f(c))$.

The linearization $L(x)$ may be used as a replacement for $f(x)$ for values of $x$ near $c$. The closer $x$ is to $c$, the more accurate the approximation $L(x)$ is for $f(x)$.

> [!mexample] Computing a linearization
> We set $f(x)=\sqrt{x}$, and we let $c=4$.
> 
> We compute $f(c)=2$, and $f'(x)=\frac{1}{2\sqrt{x}}$ so $f'(c)=\frac{1}{4}$.
> 
> Plug everything in to find $L(x)$: $$L(x)=f(c)+f'(c)(x-c)\qquad ⨠⨠ \qquad L(x)=2+\frac{1}{4}(x-4)$$
> Now approximate $f(4.01)\approx L(4.01)$: $$L(4.01)=2+\frac{1}{4}(4.01-4)=2.0025$$

### 07 Theory

> [!concept] Taylor polynomials
> The **Taylor polynomials $T_n(x)$** of a function $f(x)$ are the partial sums of the Taylor series of $f(x)$: 
> $$T_N(x)=\sum_{n=0}^N \frac{f^{(n)}(c)}{n!}(x-c)^n=f(c)+\frac{f'(c)}{1!}(x-c)+\frac{f''(c)}{2!}(x-c)^2+\cdots$$

These polynomials are *generalizations of linearization*.
Specifically, $f(c)=T_0(x)$, and $L(x)=T_1(x)$.

The Taylor series $T_n(x)$ is a better approximation of $f(x)$ than $T_i(x)$ for any $i<n$.

![200](Pasted%20image%2020241109175743.png)

![400](Pasted%20image%2020241109175818.png)

> [!Extra] Facts about Taylor series
> The series $T_n(x)$ has the same derivatives as $f(x)$ at the point $x=c$. This fact can be verified by visual inspection of the series: apply the power rule and chain rule, then plug in $x=c$ and all factors left with $(x-c)$ will become zero.
> 
> The difference $f(x)-T_n(x)$ vanishes to order $n$ at $x=c$: $$\begin{align*}f(x)-T_n(x)\quad&= \quad\frac{f^{(n)}(c)}{n!}(x-c)^n+\frac{f^{(n+1)}(c)}{(n+1)!}(x-c)^{n+1}+\cdots\\\\ &= \quad (x-c)^n\left(\frac{f^{(n)}(c)}{n!}+\frac{f^{(n+1)}(c)}{(n+1)!}(x-c)+\cdots\quad\right)\end{align*}$$
> 
> The factor $(x-c)^n$ drives the whole function to zero with order $n$ as $x\to c$.
> 
> If we only considered orders up to $n$, we might say that $f(x)$ and $T_n(x)$ are the same near $c$.

### 08 Illustration

> [!mexample] Taylor polynomial approximations
> ![Taylor polynomial approximations](Calculus/2025%20Spring/W11%20-%20Examples.md#Taylor%20polynomial%20approximations)

> [!mexample] Taylor polynomials to approximate a definite integral
> ![Taylor polynomials to approximate a definite integral](Calculus/2025%20Spring/W11%20-%20Examples.md#Taylor%20polynomials%20to%20approximate%20a%20definite%20integral)

