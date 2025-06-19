---
title: Examples - Unit 01
---
## Volume using cylindrical shells

#### 01 - Revolution of a triangle
A rotation-symmetric 3D body has cross section given by the region between $y=3x+2$, $y=6-x$, $x=0$, and is rotated around the $y$-axis. Find the volume of this 3D body.

**Solution**
1. & Define the cross section region.
    - Bounded above-right by $y=6-x$.
    - Bounded below-right by $y=3x+2$.
    - ! These intersect at $x=1$.
    - Bounded at left by $x=0$.
2. && Define range of integration variable.
    - Rotated around $y$-axis, therefore use $x$ for integration variable (shells!).
    - Integral over $x\in [0,1]$: 
      $$V=\int_0^1 2\pi Rh\,dr$$
3. & Interpret $R$.
    - Radius of shell-cylinder equals distance along $x$: $$R(x)=x$$
4. & Interpret $h$.
    - Height of shell-cylinder equals distance from lower to upper bounding lines: $$\begin{align*}h(x)&= (6-x)-(3x+2)\\ &= 4-4x\end{align*}$$
5. & Interpret $dr$.
    - $dr$ is limit of $\Delta r$ which equals $\Delta x$ here so $dr=dx$.
6. & Plug data in volume formula.
    - Insert data and compute integral: $$\begin{align*}V&= \int_0^1 2\pi Rh\,dr\\\\&= \int_0^1 2\pi\cdot x(4-4x)\,dx\\\\&=\left.2\pi\left(2x^2-\frac{4x^3}{3}\right)\right|_0^1 = \frac{4\pi}{3}\end{align*}$$

#### 02 - Revolution of a sinusoid
Consider the region given by revolving the first hump of $y=\sin(x)$ about the $y$-axis. Set up an integral that gives the volume of this region using the method of shells.

[Solution](Calculus%20II%20-%20Exercise%20solutions%20-%20Unit%2001.md#02%20-%20Revolution%20of%20a%20sinusoid)

## Integration by parts
#### 03 - A and T factors
Compute the integral: $\displaystyle\int x\cos x\,dx$

**Solution**
1. & Choose $u=x$. %% fold %% 
    - Set $u(x)=x$ because $x$ *simplifies* when differentiated.
      (By the trick: $x$ is *Algebraic*, i.e. more “$u$”, and $\cos x$ is *Trig*, more “$v$”.)
    - Remaining factor must be $v'$: $$v'(x)=\cos x$$
2. && Compute $u'$ and $v$. %% fold %% 
    - Derive $u$: $$u'=1$$
    - Antiderive $v'$: $$v=\sin x$$
    - Obtain chart: $$\begin{array}{c|c}u=x&v'=\cos x\\\hline u'=1&v=\sin x\end{array} \begin{array}{l}\quad\longrightarrow\quad\int u\cdot v'\qquad\text{original} \\ \quad\longrightarrow\quad\int u'\cdot v\qquad\text{final} \end{array}$$
3. && Plug into IBP formula. %% fold %% 
    - Plug in all data: $$\int x\cos x\,dx=x\sin x-\int 1\cdot\sin x\,dx$$
    - Compute integral on RHS: $$\int x\cos x\,dx = x\sin x+\cos x+C$$
      Note: the *point* of IBP is that this integral is easier than the first one!
4. & Final answer is: $\;x\sin x+\cos x + C$

#### 04 - Hidden A
Compute the integral: $$\int \ln x\,dx$$

[Solution](Calculus%20II%20-%20Exercise%20solutions%20-%20Unit%2001.md#04%20-%20Hidden%20A)

## Trig power products
#### 05 - Power product - odd power
Compute the integral: $$\int \cos^2x\cdot \sin^5 x\,dx$$
**Solution**
1. &&& Swap over the even bunch.
    - Max even bunch leaving power-one is $\sin^4x$: $$\sin^5x \qquad ⨠⨠ \qquad \sin x\,\big(\sin^2x\big)^2 \qquad ⨠⨠ \qquad \sin x\,\big(1-\cos^2x\big)^2$$
    - Apply to $\sin^5x$ in the integrand: $$\int \cos^2x\cdot\sin^5x\,dx \qquad ⨠⨠ \qquad \int \cos^2x\cdot\sin x\,\big(1-\cos^2x\big)^2\,dx$$
2. &&& Perform $u$-substitution on the power-one integrand.
    - Set $u=\cos x$.
    - Hence $du=\sin x\,dx$. Recognize this in the integrand.
    - Convert the integrand: $$\begin{align*}\int\cos^2x\cdot\sin x\big(1-\cos^2x\big)^2\,dx \qquad &⨠⨠ \qquad  \int \cos^2x\cdot\big(1-\cos^2x\big)^2\big(\sin x\,dx\big)\\\\ \qquad &⨠⨠ \qquad \int u^2\cdot(1-u^2)^2\,du \end{align*}$$
3. & Perform the integral.
    - Expand integrand and use power rule to obtain: $$\int u^2\cdot(1-u^2)^2\,du = \frac{1}{3}u^3 - \frac{2}{5}u^5 + \frac{1}{7}u^7 + C$$
    - Insert definition $u=\cos x$: $$\begin{gather*}\int \cos^2x\cdot\sin^5 x\,dx \quad ⨠⨠ \quad  \int u^2\cdot(1-u^2)^2\,du \\\\ ⨠⨠ \quad  \frac{1}{3}\cos^3 x - \frac{2}{5}\cos^5 x + \frac{1}{7}\cos^7 x + C\end{gather*}$$
4. & This is our final answer.

#### 06 - Power product - tan and sec
Compute the integral: $$\int \tan^5x\cdot\sec^3x\,dx$$

**Solution**
1. && Try $du=\sec^2x\,dx$.
    - Factor $du$ out of the integrand: $$\int \tan^5x\cdot\sec^3 x\,dx \qquad ⨠⨠ \qquad \int \tan^5x\cdot\sec x\,\big(\sec^2 x\,dx\big)$$
    - We then must swap over remaining $\sec x$ into the $\tan x$ type.
    - Cannot do this because $\sec x$ has odd power. Need even to swap.
2. && Try $du=\sec x\,\tan x\,dx$.
    - Factor $du$ out of the integrand: $$\int \tan^5x\cdot\sec^3 x\,dx \qquad ⨠⨠ \qquad \int \tan^4x\cdot\sec^2x\,\big(\sec x\,\tan x\,dx\big)$$
    - Swap remaining $\tan x$ into $\sec x$ type: $$\begin{gather*}\int (\tan^2x)^2\cdot\sec^2x\,\big(\sec x\,\tan x\,dx\big) \\\\ ⨠⨠ \quad \int \big(\sec^2x-1\big)^2\cdot\sec^2x\, \big(\sec x\,\tan x\,dx\big)\end{gather*}$$
    - Substitute $u=\sec x$ and $du=\sec x\,\tan x\,dx$: $$\qquad ⨠⨠ \qquad \int (u^2-1)^2\cdot u^2\,du$$
3. &&& Compute the integral in $u$ and convert back to $x$.
    - Expand the integrand: $$\qquad ⨠⨠ \qquad \int u^6-2u^4+u^2\,du$$
    - Apply power rule: $$\qquad ⨠⨠ \qquad \frac{u^7}{7}-2\frac{u^5}{5}+\frac{u^3}{3}+C$$
    - Plug back in, $u=\sec x$: $$\qquad ⨠⨠ \qquad \frac{\sec^7 x}{7}-2\frac{\sec^5 x}{5}+\frac{\sec^3 x}{3}+C$$
4. & This is our final answer.

#### 07 - Trig power product - differing frequencies
Compute the integral: $$\int \sin 4x\cdot\cos 5x\,dx$$

**Solution**
1. !! Convert product to sum using trig identity.
    - Use $\sin A\,\cos B = \frac{1}{2}\big(\sin(A-B)+\sin(A+B)\big)$ with $A=4x$ and $B=5x$: $$\sin 4x\cdot\cos 5x \qquad ⨠⨠ \qquad  \tfrac{1}{2}\big(\sin(-x)+\sin(9x)\big)$$
2. & Perform the integral.
    - Break up the sum: $$\int\sin 4x\cdot\cos 5x\,dx\quad ⨠⨠ \quad \frac{1}{2}\int\sin(-x)\,dx+\frac{1}{2}\int\sin(9x)\,dx$$
    - Observe chain rule backwards: $$\frac{1}{2}\int\sin(-x)\,dx+\frac{1}{2}\int\sin(9x)\quad ⨠⨠ \quad \frac{1}{2}\cos(-x) - \frac{1}{18}\cos(9x) + C$$
3. & This is our final answer.

## Trig substitution
#### 08 - Trig sub in quadratic - completing the square
Compute the integral: $$\int\frac{dx}{\sqrt{x^2-6x+11}}$$

**Solution**
1. ! Notice square root of a quadratic.
2. &&& Complete the square to obtain Pythagorean form.
    - Find constant term for a complete square: $$x^2-6x+\left(\frac{-6}{2}\right)^2=x^2-6x+9=(x-3)^2$$
    - Add and subtract desired constant term: $$x^2-6x+11\qquad ⨠⨠ \qquad x^2-6x+9-9+11$$
    - Simplify: $$x^2-6x+9-9+11\qquad ⨠⨠ \qquad (x-3)^2+2$$
3. && Perform shift substitution.
    - Set $u=x-3$ as inside the square: $$(x-3)^2+2=u^2+2$$
    - Infer $du=dx$.
    - Plug into integrand: $$\int\frac{dx}{\sqrt{x^2-6x+11}}\qquad ⨠⨠ \qquad \int \frac{du}{\sqrt{u^2+2}}$$
4. !! Trig sub with $\tan\theta$.
    - Identify triangle: ![200](Pasted%20image%2020240906214345.png)
    - Use substitution $u=\sqrt{2}\tan\theta$. (From triangle or memorized tip.)
    - Infer $du=\sqrt{2}\sec^2\theta\,d\theta$.
    - Plug in data: $$\int \frac{du}{\sqrt{u^2+2}}\qquad ⨠⨠ \qquad \int\frac{\sec^2\theta}{\sec\theta} \,d\theta= \int\sec\theta\,d\theta$$
5. & Compute trig integral.
    - Use ad hoc formula: $$\int\sec\theta\,d\theta = \ln|\tan\theta+\sec\theta|+C$$
6. && Convert trig back to $x$.
    - First in terms of $u$, referring to the triangle: $$\tan\theta=\frac{u}{\sqrt{2}},\qquad \sec\theta=\frac{\sqrt{u^2+2}}{\sqrt{2}}$$
    - Then in terms of $x$ using $u=x-3$.
    - Plug everything in: $$\ln|\tan\theta+\sec\theta|+C\qquad ⨠⨠ \qquad \ln\left|\frac{x-3}{\sqrt{2}} +\frac{\sqrt{(x-3)^2+2}}{\sqrt{2}}\right|+C$$
7. && Simplify using log rules.
    - Log rule for division gives us: $$\ln \frac{f(x)}{a}=\ln f(x)-\ln a$$
    - The common denominator $\frac{1}{\sqrt{2}}$ can be pulled outside as $-\ln \sqrt{2}$.
    - The new term $-\ln \sqrt{2}$ can be “absorbed into the constant” (redefine $C$).
    - So we write our final answer thus: $$\ln\left|x-3+\sqrt{(x-3)^2+2}\right|+C$$

## Partial fractions
#### 09 - Partial fractions with repeated factor
Find the partial fraction decomposition: $$\frac{3x-9}{x^3+3x^2-4}$$
**Solution**
1. & Check! Numerator is smaller than denominator (degree-wise).
2. && Factor the denominator.
    - Rational roots theorem: $x=1$ is a zero.
    - Divide by $x-1$: $$\frac{x^3+3x^2-4}{x-1}=x^2+4x+4$$
    - Factor again: $$x^2+4x+4=(x+2)^2$$
    - Final factored form: $$x^3+3x^2-4\qquad ⨠⨠ \qquad (x-1)(x+2)^2$$
3. & Write the generic PFD.
    - Allow all lower powers: $$\frac{3x-9}{(x-1)(x+2)^2}=\frac{A}{x-1}+\frac{B}{x+2}+\frac{C}{(x+2)^2}$$
4. &&& Solve for $A$, $B$, and $C$.
    - Multiply across by the common denominator: $$3x-9=A(x+2)^2+B(x-1)(x+2)+C(x-1)$$
    - For $A$, set $x=1$, obtain: $$\begin{align*}&&3\cdot 1-9&=A(1+2)^2+B\cdot 0+C\cdot 0\\\qquad ⨠⨠&& \qquad -6&= 9A \\  ⨠⨠&& \qquad A&= -2/3 \end{align*}$$
    - For $C$, set $x=-2$, obtain: $$\begin{align*}&&3\cdot (-2)-9&=A\cdot0+B\cdot 0+C\cdot (-3)\\\qquad ⨠⨠&& \qquad -15&= -3C \\  ⨠⨠&& \qquad C&= 5 \end{align*}$$
    - For $B$, insert prior results and solve. 
        - Plug in $A$ and $C$: $$3x-9=-\frac{2}{3}(x+2)^2+B(x-1)(x+2)+5(x-1)$$
        - Now plug in another convenient $x$, say $x=3$: $$\begin{align*}0&= -\frac{2}{3}\cdot5^2+B\cdot2\cdot5 +5\cdot2 \\ \frac{50}{3}-10&= 10B \qquad ⨠⨠ \qquad  B= \frac{2}{3}\end{align*}$$
5. & Plug in $A$, $B$, $C$ for the final answer.
    - Final answer: $$\frac{3x-9}{x^3+3x^2-4}=\frac{-2/3}{x-1}+\frac{2/3}{x+2}+\frac{5}{(x+2)^2}$$

#### 10 - Partial fractions - repeated quadratic, linear tops
Compute the integral: $$\int\frac{x^3+1}{(x^2+4)^2}\,dx$$

**Solution**
1. &&& Compute the partial fraction decomposition.
    - Check that numerator degree is lower than denominator. $\checkmark$
    - Factor denominator completely. $\checkmark$ (No real roots.)
    - Write generic PFD: $$\frac{x^3+1}{(x^2+4)^2}=\frac{Ax+B}{x^2+4}+\frac{Cx+D}{(x^2+4)^2}$$
    - ! Notice “linear over quadratic” in first term.
    - !! Notice repeated factor: sum with incrementing powers up to 2.
    - Common denominators and solve: $$\begin{gather*}x^3+1=(Ax+B)(x^2+4)+Cx+D\\\\ ⨠⨠ \quad x^3+1=Ax^3+Bx^2+(4A+C)x+4B+D\\\\ ⨠⨠ \quad A=1,\;B=0\\\\ ⨠⨠ \quad C=-4,\;D=1\end{gather*}$$
    - Therefore: $$\frac{x^3+1}{(x^2+4)^2}=\frac{x}{x^2+4}+\frac{-4x+1}{(x^2+4)^2}$$
2. &&& Integrate by terms.
    - Integrate the first term using $u=x^2+4$: $$\begin{gather*}\int\frac{x}{x^2+4}dx\quad \overset{u=x^2+4}{⨠⨠} \quad \frac{1}{2}\int\frac{du}{u}\\\\ ⨠⨠ \quad \frac{1}{2}\ln|u|+C\quad ⨠⨠ \quad \frac{1}{2}\ln\left|x^2+4\right|+C\end{gather*}$$
    - Break up the second term: $$\frac{-4x+1}{(x^2+4)^2}\quad ⨠⨠ \quad \frac{-4x}{(x^2+4)^2}+\frac{1}{(x^2+4)^2}$$
    - Integrate the first term of RHS: $$\begin{gather*}\int\frac{-4x}{(x^2+4)^2}\,dx\quad ⨠⨠ \quad -2\int\frac{du}{u^2}\\\\ ⨠⨠ \quad \frac{2}{u}+C\quad ⨠⨠ \quad \frac{2}{x^2+4}+C\end{gather*}$$
    - Integrate the second term of RHS: $$\begin{gather*}\int\frac{dx}{(x^2+4)^2}\quad \overset{x=2\tan\theta}{⨠⨠} \quad \int\frac{2\sec^2\theta\,d\theta}{16\sec^4\theta}\\\\ ⨠⨠ \quad \frac{1}{8}\int\cos^2\theta\,d\theta\quad ⨠⨠ \quad \frac{1}{16}\theta+\frac{1}{32}\sin(2\theta)+C\end{gather*}$$

## Simpson’s Rule
#### 11 - Simpson’s Rule on the Gaussian distribution
The function $e^{x^2}$ is very important for probability and statistics, but it cannot be integrated analytically.

Apply Simpson’s Rule to approximate the integral: $$\int_0^1 e^{x^2}\,dx$$ with $\Delta x=0.1$ and $n=10$. What error bound is guaranteed for this approximation?

**Solution**
We need a table of values of $x_i$ and $y_i=f(x_i)$: 

|    $x_i:$     |    $0.0$    |    $0.1$    | $0.2$       | $0.3$       | $0.4$       | $0.5$       | $0.6$       | $0.7$       | $0.8$       | $0.9$       | $1.0$       |
| ----------: | --------- | --------- | ----------- | ----------- | ----------- | ----------- | ----------- | ----------- | ----------- | ----------- | ----------- |
| $f(x_i):$ | $e^{0.0^2}$ | $e^{0.1^2}$ | $e^{0.2^2}$ | $e^{0.3^2}$ | $e^{0.4^2}$ | $e^{0.5^2}$ | $e^{0.6^2}$ | $e^{0.7^2}$ | $e^{0.8^2}$ | $e^{0.9^2}$ | $e^{1.0^2}$ |
|  $\approx$   |   $1.000$   |   $1.010$   | $1.041$     | $1.094$     | $1.174$     | $1.284$     | $1.433$     | $1.632$     | $1.896$     | $2.248$     | $2.718$     |
These can be plugged into the Simpson Rule formula to obtain our desired approximation: 
$$\begin{gather}S_{10} = \frac{1}{3}\cdot0.1\cdot\Big(1.000+4\cdot1.010+2\cdot1.041+4\cdot1.094+\cdots+2\cdot1.896+4\cdot2.248+2.718\Big)\\\\ \approx 1.463
\end{gather}$$
To find the error bound we need to find the smallest number we can manage for $K_4$.

Take four derivatives and simplify: $$f^{(4)}(x)=(12+48x^2+16x^4)e^{x^2}$$
On the interval $x\in[0,1]$, this function is maximized at $x=1$. Use that for the optimal $K_4$: $$f^{(4)}(1.000)=206.589$$
Finally we plug this into the error bound formula: 
$$\frac{K_4(b-a)^5}{180n^4}=\frac{206.589\cdot 1.000^5}{180\cdot10^4}\approx 0.0001$$
$$⨠⨠ \qquad \mathrm{Error}(S_{10})\leq 0.0001$$

