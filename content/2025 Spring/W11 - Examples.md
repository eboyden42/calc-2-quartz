## Power series as functions

#### Geometric series: algebra meets calculus
Consider the geometric series as a power series functions: 
$$\frac{1}{1-x}\quad=\quad 1+x+x^2+x^3+\cdots$$

Take the derivative of both sides of the *function*: $$\frac{d}{dx}\left(\frac{1}{1-x}\right)\quad ⨠⨠ \quad \frac{1}{(1-x)^2}\quad ⨠⨠ \quad \left(\frac{1}{1-x}\right)^2$$

This means $f$ satisfies the identity: $$f'=f^2$$

Now compute the derivative of the *series*: $$1+x+x^2+x^3+\cdots \quad \overset{\frac{d}{dx}}{⨠⨠} \quad 1+2x+3x^2+4x^3+\cdots$$
On the other hand, compute the square of the series: $$\left(1+x+x^2+x^3+\cdots\;\right)^2\quad ⨠⨠ \quad 1+2x+3x^2+4x^3+\cdots$$

So we find that the *same relationship holds*, namely $f'=f^2$, for the closed formula and the series formula for this function.

#### Manipulating geometric series: algebra
Find power series that represent the following functions: 

(a) $\displaystyle\frac{1}{1+x}$ $\quad$ (b) $\displaystyle\frac{1}{1+x^2}$ $\quad$ (c) $\displaystyle\frac{x^3}{x+2}$ $\quad$ (d) $\displaystyle\frac{3x}{2-5x}$

**Solution**

(a) $\displaystyle\frac{1}{1+x}$

1. & Rewrite in format $\frac{1}{1-u}$.
    - Introduce double negative: $$\frac{1}{1+x}=\frac{1}{1-(-x)}$$
    - Choose $u=-x$.
2. && Plug $u=-x$ into geometric series.
    - Geometric series in $u$: $$1+u+u^2+u^3+\cdots$$
    - Plug in $u=-x$: $$\qquad ⨠⨠ \qquad 1+(-x)+(-x)^2+(-x)^3+\cdots$$
    - Simplify: $$\qquad ⨠⨠ \qquad 1-x+x^2-x^3+\cdots$$
    - Final answer: $$\frac{1}{1+x}=1-x+x^2-x^3+\cdots$$

(b) $\displaystyle\frac{1}{1+x^2}$

1. & Rewrite in format $\frac{1}{1-u}$.
    - Rewrite: $$\frac{1}{1+x^2}=\frac{1}{1-(-x^2)}$$
    - Choose $u=-x^2$.
2. && Plug $u=-x^2$ into geometric series.
    - Geometric series in $u$: $$1+u+u^2+u^3+\cdots$$
    - Plug in $u=-x^2$: $$\begin{gather*}⨠⨠ \quad 1+(-x^2)+(-x^2)^2+(-x^2)^3+\cdots\\\\ ⨠⨠ \quad 1-x^2+x^4-x^6+\cdots\end{gather*}$$
    - Final answer: $$\frac{1}{1+x}=1-x^2+x^4-x^6+\cdots$$

(c) $\displaystyle\frac{x^3}{x+2}$

1. && Rewrite in format $Ax^3\cdot\frac{1}{1-u}$.
    - Rewrite: $$\begin{gather*}\frac{x^3}{x+2}\qquad ⨠⨠ \qquad x^3\cdot\frac{1}{2+x}\qquad ⨠⨠ \qquad x^3\cdot\frac{1}{2\left(1+\frac{x}{2}\right)}\\\\ ⨠⨠ \qquad \frac{1}{2}x^3\cdot\frac{1}{1+\frac{x}{2}}\qquad ⨠⨠ \qquad \frac{1}{2}x^3\cdot\frac{1}{1-\left(-\frac{x}{2}\right)}\end{gather*}$$
    - Choose $u=-\frac{x}{2}$. Here $Ax^3=\frac{1}{2}x^3$.
2. && Plug $u=-x^2$ into geometric series.
    - Geometric series in $u$: $$1+u+u^2+u^3+\cdots$$
    - Plug in $u=-\frac{x}{2}$: $$\begin{align*}\qquad ⨠⨠& \qquad 1+(-\tfrac{x}{2})+(-\tfrac{x}{2})^2+(-\tfrac{x}{2})^3+\cdots\\\\ \qquad ⨠⨠& \qquad 1-\frac{1}{2}x+\frac{1}{4}x^2-\frac{1}{8}x^3+\cdots\end{align*}$$
    - Obtain: $$\frac{1}{1-\left(-\frac{x}{2}\right)}=1-\frac{1}{2}x+\frac{1}{4}x^2-\frac{1}{8}x^3+\cdots$$
3. & Multiply by $\frac{1}{2}x^3$.
    - Distribute: $$\frac{1}{2}x^3\cdot \frac{1}{1-\left(-\frac{x}{2}\right)}\qquad ⨠⨠ \qquad \frac{1}{2}x^3-\frac{1}{4}x^4+\frac{1}{8}x^5-\frac{1}{16}x^6+\cdots$$
    - Final answer: $$\frac{x^3}{x+2}=\frac{1}{2}x^3-\frac{1}{4}x^4+\frac{1}{8}x^5-\frac{1}{16}x^6+\cdots$$

(d) $\displaystyle\frac{3x}{2-5x}$

1. && Rewrite in format $Ax\cdot\frac{1}{1-u}$.
    - Rewrite: $$\begin{align*}\frac{3x}{2-5x}\qquad ⨠⨠ \qquad 3x\cdot\frac{1}{2-5x}\\\\ \qquad ⨠⨠ \qquad 3x\cdot\frac{1}{2\left(1-\frac{5x}{2}\right)} \qquad ⨠⨠ \qquad& \frac{3}{2}x\cdot\frac{1}{1-\frac{5x}{2}}\end{align*}$$
    - Choose $u=\frac{5x}{2}$. Here $Ax=\frac{3}{2}x$.
2. && Plug $u=\frac{5x}{2}$ into geometric series.
    - Geometric series in $u$: $$1+u+u^2+u^3+\cdots$$
    - Plug in $u=\frac{5x}{2}$: $$\begin{align*}\qquad ⨠⨠& \qquad 1+(\tfrac{5x}{2})+(\tfrac{5x}{2})^2+(\tfrac{5x}{2})^3+\cdots\\\\ \qquad ⨠⨠& \qquad 1+\frac{5}{2}x+\frac{25}{4}x^2+\frac{125}{8}x^3+\cdots\end{align*}$$
    - Obtain: $$\frac{1}{1-\frac{5x}{2}}=1+\frac{5}{2}x+\frac{25}{4}x^2+\frac{125}{8}x^3+\cdots$$
3. & Multiply by $\frac{3}{2}x$.
    - Distribute: $$\frac{3}{2}x\cdot \frac{1}{1-\frac{5x}{2}}\qquad ⨠⨠ \qquad \frac{3}{2}x+\frac{15}{4}x^2+\frac{75}{8}x^3+\frac{375}{16}x^4+\cdots$$
    - Final answer: $$\frac{3x}{2-5x}=\frac{3}{2}x+\frac{15}{4}x^2+\frac{75}{8}x^3+\frac{375}{16}x^4+\cdots$$

#### Manipulating geometric series: calculus
Find a power series that represents $\ln(1+x)$.

**Solution**

1. & Differentiate to obtain similarity to geometric sum formula.
    - Differentiate $\ln(1+x)$: $$\frac{d}{dx}\ln(1+x)=\frac{1}{1+x}\qquad ⨠⨠ \qquad \frac{1}{1-(-x)}$$
2. & Find power series of differentiated function.
    - Power series by modifying $\frac{1}{1-u}$ with $u=-x$: $$\frac{1}{1-(-x)}=1-x+x^2-x^3+x^4-\cdots$$
3. && Integrate series to find original function.
    - Integrate both sides: $$\begin{align*}\int\frac{1}{1-(-x)}\,dx &= \int 1-x+x^2-x^3+x^4-\cdots\,dx\\\\ \ln(1+x)&= D+x-\frac{1}{2}x^2+\frac{1}{3}x^3-\frac{1}{4}x^4+\cdots\end{align*}$$
    - Use known point to solve for $D$: $$\ln(1+0)=D+0+0+\cdots\qquad ⨠⨠ \qquad 0=D$$
    - Final answer: $$\ln(1+x)= x-\frac{1}{2}x^2+\frac{1}{3}x^3-\frac{1}{4}x^4+\cdots$$

#### Recognizing and manipulating geometric series: Part I
(a) Evaluate $\displaystyle\sum_{n=1}^\infty(-1)^{n-1}\frac{1}{n}$.
(Hint: consider the series of $\ln(1-x)$.)

(b) Find a series approximation for $\ln(2/3)$.

**Solution**

(a) Evaluate $\displaystyle\sum_{n=1}^\infty(-1)^{n-1}\frac{1}{n}$. (Hint: consider the series of $\ln(1-x)$.)

1. &&& Find the series representation of $\ln(1-x)$ following the hint.
    - ! Notice that $\frac{d}{dx}\ln(1-x)=\frac{-1}{1-x}$.
    - We know the series of $\frac{-1}{1-x}$: $$\frac{-1}{1-x}=-(1+x+x^2+\cdots)=-1-x-x^2-\cdots$$
    - Notice that $\int\frac{-1}{1-x}\,dx=\ln(1-x)+C$; this is the desired function when $C=0$.
    - Integrate the series term-by-term: $$\begin{gather*}\int\frac{-1}{1-x}\,dx=\int -1-x-x^2-\cdots\,dx\\\\ ⨠⨠ \quad \ln(1-x)=D-x-\frac{x^2}{2}-\frac{x^3}{3}-\cdots\end{gather*}$$
    - Solve for $D$ using $\ln(1-0)=0$, so $0=D-0-0-\cdots$ and thus $D=0$. So: $$\ln(1-x)=-x-\frac{x^2}{2}-\frac{x^3}{3}-\cdots\quad=\quad\sum_{n=1}^\infty-\frac{x^n}{n!}$$
2. ! Notice the similar formula.
    - The series formula $\sum_{n=1}^\infty -\frac{x^n}{n!}$ looks similar to the formula $\sum_{n=1}^\infty (-1)^{n-1}\frac{1}{n}$.
3. & Choose $x=-1$ to recreate the desired series.
    - We obtain equality by setting $x=-1$ because $-(-1)^n=(-1)^{n+1}=(-1)^{n-1}$.
4. & Final answer is $\ln(1--1)=\ln 2$.

(b) Find a series approximation for $\ln(2/3)$.

1. & Observe that $\ln(2/3)=\ln(1-1/3)$.
    - Therefore we can use the series $\ln(1-x)=-x-\frac{x^2}{2}-\frac{x^3}{3}-\cdots$
2. & Plug $x=1/3$ into the series for $\ln(1-x)$.
    - Plug in and simplify: $$\begin{align*}\ln(2/3)=\ln(1-1/3) &= -1/3-\frac{(1/3)^2}{2}-\frac{(1/3)^3}{3}-\cdots\\ &= -\frac{1}{3}-\frac{1}{3^2\cdot 2}-\frac{1}{3^3\cdot 3}-\cdots\end{align*}$$


#### Recognizing and manipulating geometric series: Part II
(a) Find a series representing $\tan^{-1}(x)$ using differentiation.

(b) Find a series representing $\displaystyle\int\frac{dx}{1+x^4}$.

**Solution**

(a) Find a series representing $\tan^{-1}(x)$.

1. !! Notice that $\frac{d}{dx}\tan^{-1}(x)=\frac{1}{1+x^2}$.
2. && Obtain the series for $\frac{1}{1+x^2}$.
    - Let $u=-x^2$: $$\begin{gather*}\frac{1}{1+x^2}\qquad ⨠⨠ \qquad \frac{1}{1-u}=1+u+u^2+\cdots \\\\ ⨠⨠ \qquad 1-x^2+x^4-x^6+x^8-\cdots\end{gather*}$$
3. &&& Integrate the series for $\frac{1}{1+x^2}$ by terms.
    - Set up the strategy. We know: $$\int\frac{1}{1+x^2}\,dx= \tan^{-1}(x)+C$$ and: $$\frac{1}{1+x^2}=1-x^2+x^4-x^6+x^8-\cdots$$
    - Integrate term-by-term: $$\begin{gather*}⨠⨠ \quad \int 1-x^2+x^4-x^6+x^8-\cdots\,dx \\\\ ⨠⨠ \quad D + x-\frac{x^3}{3}+\frac{x^5}{5}-\frac{x^7}{7}+\cdots\end{gather*}$$
    - Conclude that: $$\tan^{-1}(x)+C=D + x-\frac{x^3}{3}+\frac{x^5}{5}-\frac{x^7}{7}+\cdots$$
4. & Solve for $D-C$ by testing at $\tan^{-1}(0)=0$.
    - Plugging in, obtain: $$\tan^{-1}(0)=D-C+0+\cdots+0$$ so $D-C=0$.
5. & Final answer is $\tan^{-1}(x)=x-\frac{x^3}{3}+\frac{x^5}{5}-\frac{x^7}{7}+\cdots$.

(b) Find a series representing $\displaystyle\int\frac{dx}{1+x^4}$.

1. && Find a series representing the integrand.
    - Integrand is $\frac{1}{1+x^4}$.
    - Rewrite integrand in format of geometric series sum: $$\frac{1}{1+x^4}\qquad ⨠⨠ \qquad \frac{1}{1-(-x^4)}\qquad ⨠⨠ \qquad \frac{1}{1-u},\quad u=-x^4$$
    - Write the series: $$\begin{gather*}\frac{1}{1-u}=1+u+u^2+u^3+\cdots\\\\ ⨠⨠ \quad 1-x^4+x^8-x^{12}+x^{16}-\cdots\quad=\sum_{n=0}^\infty(-1)^n x^{4n}\end{gather*}$$
2. & Integrate the integrand series by terms.
    - Integrate term-by-term: $$\int 1-x^4+x^8-x^{12}+x^{16}-\cdots\,dx\qquad ⨠⨠ \qquad C+x-\frac{x^5}{5}+\frac{x^9}{9}-\frac{x^{13}}{13}+\frac{x^{17}}{17}-\cdots$$
    - This is our final answer.


## Taylor and Maclaurin series

#### Maclaurin series of $e^x$
What is the Maclaurin series of $f(x)=e^x$?

**Solution**
Because $\displaystyle\frac{d}{dx}e^x=e^x$, we find that $f^{(n)}(x)=e^x$ for all $n$.

So $f^{(n)}(0)=e^0=1$ for all $n$. Therefore $a_n=\displaystyle\frac{1}{n!}$ for all $n$ by the Derivative-Coefficient identity.

Thus: 
$$e^x = 1+\frac{x}{1!}+\frac{x^2}{2!}+\frac{x^3}{3!}+\cdots\;=\; \sum_{n=0}^\infty \frac{x^n}{n!}$$

#### Maclaurin series of $\cos x$
Find the Maclaurin series representation of $\cos x$.

**Solution**
Use the Derivative-Coefficient Identity to solve for the coefficients: $$a_n \quad=\quad \frac{f^{(n)}(0)}{n!}$$

|   $n$    | $f^{(n)}(x)$ | $f^{(n)}(0)$ |    $a_n$ |
| :------: | -----------: | -----------: | -------: |
|    0     |     $\cos x$ |          $1$ |      $1$ |
|    1     |    $-\sin x$ |          $0$ |      $0$ |
|    2     |    $-\cos x$ |         $-1$ |   $-1/2$ |
|    3     |     $\sin x$ |          $0$ |      $0$ |
|    4     |     $\cos x$ |          $1$ |   $1/24$ |
|    5     |    $-\sin x$ |          $0$ |      $0$ |
| $\vdots$ |     $\vdots$ |     $\vdots$ | $\vdots$ |

By studying the generating pattern of the coefficients, we find for the series: 
$$\cos x \quad=\quad 1-\frac{x^2}{2!}+\frac{x^4}{4!}-\frac{x^6}{6!}+\cdots\;=\; \sum_{n=0}^\infty (-1)^n\frac{x^{2n}}{(2n)!}$$

%% To check the equality we verify the conditions of the theorem. The derivative values for *any* $x\in\mathbb{R}$ are in the range $[-1,+1]$, so if we set $K=2$ we certainly have that $|f^{(n)}(x)|\leq K$ for all $x$ in any given interval. So the theorem implies that the series converges and equals $\cos x$ as we hoped. %%

#### Maclaurin series from other Maclaurin series
(a) Find the Maclaurin series of $\sin x$ using the Maclaurin series of $\cos x$.

(b) Find the Maclaurin series of $f(x)=x^2e^{-5x}$ using the Maclaurin series of $e^x$.

(c) Using (b), find the *value* of $f^{(22)}(0)$.

**Solution**

(a)

1. ! Remember that $\frac{d}{dx}\cos x=-\sin x$
2. && Differentiate $\cos x=1-\frac{x^2}{2!}+\frac{x^4}{4!}-\frac{x^6}{6!}+\cdots$
    - Differentiate term-by-term: $$\begin{align*}1-\frac{x^2}{2!}+\frac{x^4}{4!}-\frac{x^6}{6!}+\cdots\quad ⨠⨠& \quad 0-2\frac{x^1}{2!}+4\frac{x^3}{4!}-6\frac{x^5}{6!}+\cdots\\\\ &=\quad -\frac{x^1}{1!}+\frac{x^3}{3!}-\frac{x^5}{5!}-\cdots\end{align*}$$
    - Take negative because $\sin x=-\frac{d}{dx}\cos x$: $$\qquad ⨠⨠ \qquad x-\frac{x^3}{3!}+\frac{x^5}{5!}-\frac{x^7}{7!}+\cdots$$
3. & Final answer is $\sin x = x-\frac{x^3}{3!}+\frac{x^5}{5!}-\cdots$

(b)

1. ! Recall the series $e^u=1+\frac{u^1}{1!}+\frac{u^2}{2!}+\frac{u^3}{3!}+\cdots$
2. & Compute the series for $e^{-5x}$.
    - Set $u=-5x$: $$\begin{gather*}1+\frac{u^1}{1!}+\frac{u^2}{2!}+\frac{u^3}{3!}+\cdots\\\\ ⨠⨠ \quad 1+\frac{(-5x)}{1!}+\frac{(-5x)^2}{2!}+\frac{(-5x)^3}{3!}+\cdots\end{gather*}$$
3. & Compute the product.
    - Product of series: $$\begin{align*}x^2e^{-5x} \quad ⨠⨠& \quad   x^2\left(1+\frac{(-5x)}{1!}+\frac{(-5x)^2}{2!}+\frac{(-5x)^3}{3!}+\cdots\right)\\\\ ⨠⨠& \quad   x^2-5x^3+\frac{25}{2}x^4-\frac{125}{3!}x^5+\cdots\\\\ ⨠⨠& \quad  \sum_{n=0}^\infty (-1)^n\frac{5^nx^{n+2}}{n!}\end{align*}$$

(c)

1. !! Derivatives at $x=0$ are calculable from series coefficients.
    - Suppose we know the series $f(x)=a_0+a_1x+a_2x^2+a_3x^3+\cdots$
    - Then $f^{(n)}(0)=n!\cdot a_n$.
    - It may be easier to compute $a_n$ for a given $f(x)$ than to compute the derivative *functions* $f^{(n)}(x)$ and then evaluate them.
2. && Compute $a_{22}$.
    - Write the series such that it reveals the coefficients: $$\begin{gather*}\sum_{n=0}^\infty (-1)^n\frac{5^nx^{n+2}}{n!}\qquad ⨠⨠ \qquad \sum_{n=0}^\infty \left((-1)^n\frac{5^n}{n!}\right)x^{n+2} \\\\\implies\qquad a_{n+2}=(-1)^n\frac{5^n}{n!}\end{gather*}$$
    - !!! Coefficient with $a_{n+2}$ corresponds to the term with $x^{n+2}$, *not necessarily* the $(n+2)^\text{th}$ term (e.g. if the first term is $x^2$ as here).
    - Compute $a_{22}$: $$a_{22}=(-1)^{20}\frac{5^{20}}{20!}\qquad ⨠⨠ \qquad 5^{20}\frac{1}{20!}$$
3. & Compute $f^{(22)}(0)$.
    - Use Derivative-Coefficient Identity: $$\begin{gather*}f^{(22)}(0)\quad=\quad  22!\cdot a_{22}\\\\⨠⨠ \quad 5^{20}\cdot\frac{22!}{20!}\quad ⨠⨠ \quad  5^{20}\cdot 22\cdot 21\end{gather*}$$

#### Computing a Taylor series
Find the first five terms of the Taylor series of $f(x)=\sqrt{x+1}$ centered at $c=3$.

**Solution**
A Taylor series is just a Maclaurin series that isn’t centered at $c=0$.

The general format looks like this: 
$$f(x) = a_0 + a_1(x-c) + a_2(x-c)^2 + a_3(x-c)^3 + \cdots$$

The coefficients satisfy $a_n=\frac{f^{(n)}(c)}{n!}$. (Notice the $c$.)

We find the coefficients by computing the derivatives and evaluating at $x=3$: 

$\begin{align*} f(x) & =(x+1)^{1 / 2}, & f(3) & =2 \\ f^{\prime}(x) & =\frac{1}{2}(x+1)^{-1 / 2}, & f^{\prime}(3) & =\frac{1}{4} \\ f^{\prime \prime}(x) & =-\frac{1}{4}(x+1)^{-3 / 2}, & f^{\prime \prime}(3) & =-\frac{1}{32} \\ f^{\prime \prime \prime}(x) & =\frac{3}{8}(x+1)^{-5 / 2}, & f^{\prime \prime \prime}(3) & =\frac{3}{256} \\ f^{(4)}(x) & =-\frac{15}{16}(x+1)^{-7 / 2}, & f^{(4)}(3) & =-\frac{15}{2048}\end{align*}$

By dividing by $n!$ we can write out the first terms of the series: 
$$\begin{gather*}f(x)\;=\; \sqrt{x+1}\\\\ =\;  2+\frac{1}{4}(x-3)-\frac{1}{64}(x-3)^2+\frac{1}{512}(x-3)^3-\frac{5}{16,384}(x-3)^4+\cdots\end{gather*}$$


## Applications of Taylor series

#### Taylor polynomial approximations
Let $f(x)=\sin x$ and let $T_n(x)$ be the Taylor polynomials expanded around $c=0$.

By considering the alternating series error bound, find the first $n$ for which $T_n(0.02)$ must have error less than $10^{-6}$.

**Solution**

1. & Write the Maclaurin series of $\sin x$ because we are expanding around $c=0$.
    - Alternating sign, odd function: $$\sin x\;=\; x-\frac{x^3}{3!}+\frac{x^5}{5!}-\frac{x^7}{7!}+\cdots\;=\; \sum_{n=0}^\infty (-1)^n\frac{x^{2n+1}}{(2n+1)!}$$
2. !! Notice this series is alternating, so AST error bound formula applies.
    - AST error bound formula is: $$|E_n|\leq a_{n+1}$$
    - Here the series is $S=a_0-a_1+a_2-a_3+\cdots\;$ and $E_n=S-S_n$ is the error.
    - ! Notice that $x=0.02$ is part of the terms $a_i$ in this formula.
3. && Implement error bound to set up equation for $n$.
    - Find $n$ such that $a_{n+1}\leq 10^{-6}$, and therefore by the AST error bound formula: $$|E_n|\leq a_{n+1}\leq 10^{-6}$$
    - Plug in $x=0.02$.
    - From the series of $\sin x$ we obtain for $a_{2n+1}$: $$a_{2n+1}=\frac{0.02^{2n+1}}{(2n+1)!}$$
    - We seek the first time it happens that $a_{2n+1}\leq 10^{-6}$.
4. && Solve for the first time $a_{2n+1}\leq 10^{-6}$.
    - Equations to solve: $$\frac{0.02^{2n+1}}{(2n+1)!}\leq 10^{-6}\qquad\text{but:}\quad\frac{0.02^{2(n-1)+1}}{(2(n-1)+1)!}\nleq 10^{-6}$$
    - Method: list the values: $$\begin{gather*}\frac{0.02^1}{1!}=0.02,\qquad \frac{0.02^3}{3!}\approx 1.33\times 10^{-6},\\\\ \frac{0.02^5}{5!}\approx 2.67\times 10^{-11},\qquad\dots\end{gather*}$$
    - The first time $a_{2n+1}$ is below $10^{-6}$ happens when $2n+1=5$.
5. && Interpret result and state the answer.
    - When $2n+1=5$, the term $\displaystyle\frac{x^{2n+1}}{(2n+1)!}$ at $x=0.02$ is less than $10^{-6}$.
    - Therefore the sum of prior terms is accurate to an error of less than $10^{-6}$.
    - The sum of prior terms equals $T_4(0.02)$.
    - Since $T_4(x)=T_3(x)$ because there is no $x^4$ term, the same sum is $T_3(0.02)$.
    - The final answer is $n=3$.
    - !!! It would be wrong to infer at the beginning that the answer is $5$, or to solve $2n+1=5$ to get $n=2$.


#### Taylor polynomials to approximate a definite integral
Approximate $\displaystyle\int_0^{0.3} e^{-x^2}\,dx$ using a Taylor polynomial with an error no greater than $10^{-5}$.

**Solution**

1. & Write the series of the integrand.
    - Plug $u=-x^2$ into the series of $e^u$: $$\begin{gather*}e^u=1+\frac{u}{1!}+\frac{u^2}{2!}+\cdots\\\\ ⨠⨠ \qquad e^{-x^2}=1-\frac{1}{2!}x^2+\frac{1}{4!}x^4-\frac{1}{6!}x^6+\cdots\end{gather*}$$
2. && Compute definite integral by terms.
    - Antiderivative by terms: $$\begin{gather*}\int1-\frac{1}{2!}x^2+\frac{1}{4!}x^4-\frac{1}{6!}x^6+\cdots\,dx\\\\ ⨠⨠ \quad x-\frac{1}{3!}x^3+\frac{1}{5!}x^5-\frac{1}{7!}x^7+\cdots\end{gather*}$$
    - Plug in bounds for definite integral: $$\begin{align*}\int_0^{0.3}e^{-x^2}\,dx \qquad ⨠⨠& \qquad  x-\frac{1}{3!}x^3+\frac{1}{5!}x^5-\frac{1}{7!}x^7+\cdots\;\Bigg|_0^{0.3}\\\\\qquad ⨠⨠& \qquad 0.3-\frac{0.3^3}{3!}+\frac{0.3^5}{5!}-\frac{0.3^7}{7!}+\cdots\end{align*}$$
3. & Notice AST, apply error formula.
    - Compute some terms: $$\frac{0.3^3}{3!}\approx 0.0045,\qquad \frac{0.3^5}{5!}\approx 2.0\times 10^{-5},\qquad \frac{0.3^7}{7!}\approx 4.34\times 10^{-8}$$
    - So we can guarantee an error less than $4.34\times 10^{-5}$ by summing the first terms through $\frac{0.3^5}{5!}$.
4. & Final answer is $\displaystyle 0.3-\frac{0.3^3}{3!}+\frac{0.3^5}{5!}\approx 0.291243$.
