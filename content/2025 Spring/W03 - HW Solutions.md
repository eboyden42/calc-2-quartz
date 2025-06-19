#### 04
The chart above shows a record of ambient temperatures measured each 15 minutes over 3 hours. Compute the approximate average temperature using Simpson's Rule. You may use a calculator to resolve the arithmetic in your final expression.

**Solution**
- & Recall formula for average value.
    - $$f_{avg} = \frac{1}{b-a}\int_{a}^{b}f(x)dx$$
- & Interpret $a$ and $b$ in the context of the problem.
    - The chart starts at $x = 0$ and goes to $x = 180$. So, we can set $b = 180$ and $a = 0$.
    - $$\frac{1}{b-a}\int_{a}^{b}f(x)dx = \frac{1}{180}\int_{0}^{180}f(x)dx$$
- &&& Use Simpson's Rule to approximate integral. Use the given table, and note that $\Delta x = 15$.
    - $$\begin{align*}\int_{0}^{180}f(x)dx\approx S_{180}  &= \frac{1}{3}(15)\left(21+4(21.3)+2(21.5)+\cdots+4(21.3)+21.2)\right) \\ &= 5\left(21+4(21.3)+2(21.5)+\cdots+4(21.3)+21.2)\right)\end{align*}$$
- && Plug in expression into average value formula.
    - $$\begin{align*}f_{avg}&=\frac{1}{180}\int_{0}^{180}f(x)dx \approx \frac{S_{180}}{180} \\&= \frac{1}{36}\left(21+4(21.3)+2(21.5)+\cdots+4(21.3)+21.2)\right) \\ &= 21.2\end{align*}$$
#### 05
Compute the integral:
$$\int \frac{x^{2}}{x^{2}+9}dx$$

**Solution**
- &&& Rewrite $\frac{x^{2}}{x^{2} + 9}$ as a difference of two fractions.
    - $$ \frac{x^{2}+9}{x^{2}+9} - \frac{x^{2}}{x^{2}+9} = \frac{9}{x^{2}+9} \quad ⨠⨠ \quad \int\frac{x^{2}}{x^{2}+9}dx = \int1-\frac{9}{x^{2}+9}dx$$
- & Split integral into difference of two integrals.
    - $$\int 1 - \frac{9}{x^{2}+9}dx = \int dx - 9\int\frac{dx}{x^{2}+9}$$
- !! Evaluate leftmost integral directly and use the formula $\int\frac{dx}{x^{2}+h^{2}} = \frac{1}{h}\tan^{-1}{\left(\frac{x}{h}\right)} + C$.
    - $$\int dx - 9 \int\frac{dx}{x^{2}+9} = x - 3\tan^{-1}\left(\frac{x}{3}\right) + C, \quad C \in \mathbb{R}$$
#### 06
Compute the integral:
$$\int \frac{x^{2}-x+1}{x^{2}+x}dx$$

**Solution**
- &&& Note that the degree of the denominator is not greater than that of the numerator. Proceed by long division and rewrite integrand.
    - $$\frac{x^{2}-x+1}{x^{2}+x} = 1 \text{ remainder } -2x+1$$
    - $$\int \frac{x^{2}-x+1}{x^{2}+x}dx = \int 1 + \frac{-2x+1}{x^{2}+x}dx$$
- & Perform partial fraction decomposition on $\frac{-2x+1}{x^{2}+x}$. Factor the denominator.
    - $$\frac{-2x+1}{x^{2}+x} = \frac{-2x+1}{x(x+1)}$$
- && Write out generic PFD. Note that there are two linear factors each repeated once in the denominator.
    - $$\frac{-2x+1}{x(x+1)} = \frac{A}{x} + \frac{B}{x+1}$$
- & Multiply out both sides by $x(x+1)$.
    - $$\begin{align*}
- -2x+1 &= A(x+1)+Bx
- \end{align*}$$
- && To solve for $A$, plug in $x = 0$. To solve for $B$, plug in $x = -1$.
    - $x = 0$:$$1 = A$$
    - $x = -1$: $$-2(-1)+1 = -B \quad ⨠⨠\quad B = -3$$
    - Therefore $\frac{-2x+1}{x^{2}+x} = \frac{1}{x} + \frac{-3}{x+1}$
- & Rewrite integrand with partial fraction decomposition.
    - $$\int 1 + \frac{-2x+1}{x^{2}+x}dx = \int1 + \frac{1}{x}-\frac{3}{x+1}dx$$
- & Compute integral.
    - $$\int 1 + \frac{1}{x}-\frac{3}{x+1}dx = x + \ln{|x|}-3\ln{|x+1|}+C, \quad C \in \mathbb{R}$$


#### 07
Give the *generic* partial fraction decomposition (no need to solve for the constants):
$$\frac{x+2}{\left(x^{2}+2\right)(x-1)^{3}\left(x^{2}-9\right)}$$

**Solution**
- && Note that the factor $\left(x^{2}-9\right)$ is a difference of squares, and thus can be simplified further.
    - $$\frac{x+2}{\left(x^{2}+2\right)(x-1)^{3}\left(x^{2}-9\right)} = \frac{x+2}{\left(x^{2}+2\right)(x-1)^{3}(x-3)(x+3)}$$
- &&& Write generic PFD.
    - $x^{2}+2$ is a quadratic factor repeated once. The corresponding PFD term would be $\frac{Ax+B}{x^{2}+2}$.
    - $(x-1)^{3}$ is a linear factor repeated thrice. The corresponding PFD terms would then be $\frac{C}{x-1} + \frac{D}{(x-1)^{2}} + \frac{E}{(x-1)^{3}}$.
    - $(x-3)$ is a linear factor repeated once. The corresponding PFD term would be $\frac{F}{x-3}$.
    - $(x+3)$ is a linear factor repeated once. The corresponding PFD term would be $\frac{G}{x+3}$.
    - Putting it all together, we get $$\frac{x+2}{\left(x^{2}+2\right)(x-1)^{3}\left(x^{2}-9\right)} = \frac{Ax+B}{x^{2}+2}+\frac{C}{x-1}+\frac{D}{(x-1)^{2}}+\frac{E}{(x-1)^{3}} + \frac{F}{x-3} + \frac{G}{x+3}$$

#### 08
Compute the integral:
$$\int \frac{5x^{2}-5x+14}{(x-2)\left(x^{2}+4\right)}dx$$

**Solution**
- &&& Begin by rewriting integrand as a partial fraction. Write out generic PFD.
    - Note that $x - 2$ is a linear factor repeated once and $x^{2}+4$ is a quadratic factor repeated once.
    - $$\frac{5x^{2}-5x+14}{(x-2)(x^{2}+4)} = \frac{A}{x-2} + \frac{Bx+C}{x^{2}+4}$$
- & Multiply both sides by $(x-2)\left(x^{2}+4\right)$
    - $$5x^{2}-5x+14=A\left(x^{2}+4\right)+(Bx+C)(x-2)$$
- && Expand out right hand side and group like terms.
    - $$\begin{align*}
- 5x^{2}-5x+14&= Ax^{2}+4A+Bx^{2}-2Bx+Cx-2C \\
- &= (A+B)x^{2}+(-2B+C)x+(4A-2C)
- \end{align*}$$
- &&& Set up and solve system of equations. (If you can do linear algebra, it's easier to set up a matrix and solve, but that is beyond the scope of this class).
    - $$\begin{align*}
- A + B &= 5 \\
- -2B + C &= -5 \\
- 4A - 2C &= 14 \quad ⨠⨠ \quad 2A - C = 7
- \end{align*}$$
    - Note that $A = 5 - B$ from the first equation and $C = -5 + 2B$ from the second equation. Plug these expressions into the last equation to solve for $B$
    - $$\begin{align*}
    - 4A - 2C &= 14 \\
    - 4(5-B)-2(-5+2B) &= 14  \\
    - 20 -4B + 10-4B &= 14 \\
    - -8B &= -16 \\
    - B &= 2
    - \end{align*}$$
    - Plug $B = 2$ in the first equation to get $A = 3$.
    - Plug $B = 2$ in the second equation to get $C = -1$.
- & Rewrite integrand in partial fractions.
    - $$\int \frac{5x^{2}-5x+14}{(x-2)\left(x^{2}+4\right)}dx = \int\frac{3}{x-2}+\frac{2x-1}{x^{2}+4}dx$$
- & Expand out second fraction.
    - $$\int \frac{3}{x-2}+\frac{2x-1}{x^{2}+4}dx=\int\frac{3}{x-2}+\frac{2x}{x^{2}+4}-\frac{1}{x^{2}+4}dx$$
- !! Evaluate integral. Note that for the second fraction, $2x = \frac{d}{dx}(x^{2}+4)$ . For the third fraction, use the formula $\frac{dx}{x^{2}+h^{2}} = \frac{1}{h}\tan^{-1}{\left(\frac{x}{h}\right)} + C$ .
$$\int \frac{3}{x-2}+\frac{2x}{x^{2}+4} - \frac{1}{x^{2}+4}dx = 3\ln{|x-2|}+\ln{\left|x^{2}+4\right|}-\frac{1}{2}\tan^{-1}{\left(\frac{x}{2}\right)} + C, \quad C \in \mathbb{R}$$

#### 09
Compute the integral:
$$\int \frac{1}{x(x-1)^{3}}dx$$

**Solution**
- &&& Rewrite integrand in terms of partial fractions. Write out generic PFD form.
    - Note that $x$ is a linear factor repeated once.
    - $(x-1)^{3}$ is a linear factor repeated thrice.
    - $$\frac{1}{x(x-1)^{3}} = \frac{A}{x}+\frac{B}{x-1}+\frac{C}{(x-1)^{2}} + \frac{D}{(x-1)^{3}}$$
- & Multiply both sides by $x(x-1)^{3}$.
    - $$1 = A(x-1)^{3}+Bx(x-1)^{2}+Cx(x-1)+Dx$$
- && Expand and collect like terms.
    - $$\begin{align*}
- 1&= A\left(x^{3}-3x^{2}+3x-1\right) + Bx\left(x^{2}-2x+1\right) + Cx(x-1)+Dx \\
- &= (A+B)x^{3}+(-3A-2B+C)x^{2} + (3A + B-C +D)x+(-A)
- \end{align*}$$
- &&& Solve system of equations:
    - $$\begin{align*}
- A +B &= 0 \\ -3A -2B + C &= 0 \\ 3A + B-C+D &= 0 \\ -A &= 1
- \end{align*}$$
    - Since $A = -1$, we can use this value to obtain $B = 1$.
    - Thus,
    - $$-3(-1)-2(1)+C = 0 \quad ⨠⨠ \quad C = -1$$$$ 3(-1)+(1)-(-1)+D = 0 \quad ⨠⨠ \quad D = 1$$
- & Rewrite integrand in terms of partial fractions.
    - $$\int\frac{dx}{x(x-1)^{3}} = \int -\frac{1}{x}+\frac{1}{x-1}-\frac{1}{(x-1)^{2}}+\frac{1}{(x-1)^{3}}dx$$
- &&& Evaluate integral, use $u = x-1$ to evaluate the integral of the last three fractions.
    - $$\int -\frac{1}{x}+\frac{1}{x-1}-\frac{1}{(x-1)^{2}}+\frac{1}{(x-1)^{3}}dx = -\ln{|x|}+\ln{|x-1|}+\frac{1}{x-1}-\frac{1}{2(x-1)^{2}}+C, \quad C \in \mathbb{R}$$

%%
#### 03-07 - Partial fractions - rationalize first
For each of these integrals, make a $u$-substitution that changes the integrand into a rational function. Write the integral in terms of $u$ for your answer. You do not have to compute the $u$-integral.
- (a) $\int \frac{1}{e^{x}-1}dx$
- (b) $\int \frac{\sqrt{x}}{x-1}dx$

**Solution**
**(a)**
- && Rewrite integrand as a difference of fractions.
    - $$\begin{align*}\int \frac{1}{e^{x}-1}dx &= \int \frac{1+e^{x}-e^{x}}{e^{x}-1}dx \\ &= -\int\frac{e^{x}-1-e^{x}}{e^{x}-1}dx \\ &= -\int \frac{e^{x}-1}{e^{x}-1}-\frac{e^{x}}{e^{x}-1} \\ &= -\int1-\frac{e^{x}}{e^{x}-1}dx \\ &= \int \frac{e^{x}}{e^{x}-1}dx-\int dx \\&= \int \frac{e^{x}}{e^{x}-1}dx-x+C, \quad C \in \mathbb{R}\end{align*} $$

- && Use $u$-substitution $u = e^{x} - 1$ for the first integral. 
    - $du = e^{x}dx$
    - $$\int \frac{e^{x}}{e^{x}-1}dx-x+C = \int\frac{du}{u}-x+C. \quad C \in \mathbb{R}$$

- **(b)**
- && Being by multiplying integral by $\frac{\sqrt{x}}{\sqrt{x}}$.
    - $$\begin{align*}\int \frac{\sqrt{x}}{x-1}dx &= \int \frac{\sqrt{x}}{x-1}\cdot\frac{\sqrt{x}}{\sqrt{x}}dx \\ &= \int \frac{x}{(x-1)\sqrt{x}}dx\end{align*}$$
- && Use $u$-substitution $u = \sqrt{x}$.
    - $du = \frac{dx}{2\sqrt{x}}$
    - Note that $x = u^{2}$
$$ \int \frac{x}{(x-1)\sqrt{x}}dx = 2\int \frac{u^{2}}{u^{2}-1}du$$

%%

#### 10
Use Simpson's Rule with $n = 6$ to compute the volume of the solid obtained by revolving the pictured region about the $y$-axis. Can you do it without using a calculator?

- && Recall formula for volume by shells rotated around line parallel to $y$-axis.
    - $$V = \int_{a}^{b}2\pi Rhdx$$
- & Interpret $R$, the radius of the shells/cylinders.
    - $$R = x$$
- & Interpret $h$, the height of the shells/cylinders.
    - $$h = f(x)$$
- & Interpret cross section region.
    - Bound above by $f(x)$.
    - Bound left by $x = 2$.
    - Bound right by $x = 8$.
    - Bound below by $x$-axis.
- & Put together integral to approximate.
    - $$V = 2\pi\int_{2}^{8} xf(x)dx$$
- &&& Create table for Simpson's rule. Your columns should have at least $x_{i}$ and $x_{i}f(x_{i})$. Note that the integrand is not just $f(x_{i})$!
    - $$\begin{align*}
- x_{i} &\qquad f(x_{i}) &\qquad x_{i}f(x_{i}) \\ \\
- x_{0} =  2&\qquad f(x_{0}) = 0 &\qquad x_{0}f(x_{0}) = 0 \\
- x_{1} =  3&\qquad f(x_{1}) = 1 &\qquad x_{1}f(x_{1}) = 3 \\
- x_{2} =  4&\qquad f(x_{2}) = 3 &\qquad x_{2}f(x_{2}) = 12 \\
- x_{3} =  5&\qquad f(x_{3}) = 3 &\qquad x_{3}f(x_{3}) = 15\\
- x_{4} =  6&\qquad f(x_{4}) = 2 &\qquad x_{4}f(x_{4}) = 12 \\
- x_{5} =  7&\qquad f(x_{5}) = 3 &\qquad x_{5}f(x_{5}) = 21 \\
- x_{6} =  8&\qquad f(x_{6}) = 0 &\qquad x_{6}f(x_{6}) = 0 \\
- \end{align*}$$
- &&& Use Simpson's Rule formula $S_{n}= \frac{1}{3}\Delta x\left(y_{0} + 4y_{1}+2y_{2} + \cdots + 2y_{n-2}+4y_{n-1}+y_{n}\right)$ to approximate integral $\int_{2}^{8}xf(x)dx$. Note that $\Delta x$ here is 1 and the $y_{i}$ values are the rightmost column $x_{i}f(x_{i})$.
    - $$\begin{align*}S_{n} &= \frac{1}{3}\left(x_{0}f(x_{0}) + 4x_{1}f(x_{1}) + 2x_{2}f(x_{2}) + \cdots + 4x_{5}f(x_{5}) + x_{6}f(x_{6})\right) \\ &= \frac{1}{3}\left(0+4(3)+2(12)+4(15)+2(12)+4(21)+0\right) \\ &= \frac{1}{3}(12 + 24 + 60 + 24 + 84) \\ &= 4 + 8 + 20 + 8 + 28 \\ &= 68
- \end{align*}$$
- && Use obtained value to approximate volume.
$$V = 2\pi\int_{2}^{8}xf(x)dx \approx 2\pi(68) = 136\pi$$
