---
cssclasses:
  - hide-embedded-header
title: W01 Notes
---
## Volume using cylindrical shells

**Review**
- [Volume using cross-sectional area](https://www.youtube.com/watch?v=exSD4NNAlmM)
- [Disk/washer method - 01](https://www.youtube.com/watch?v=vUV9loPJVN0)
- [Disk/washer method - 02](https://www.youtube.com/watch?v=Y_f8XQ-rReM)
- [Disk/washer method - 03](https://www.youtube.com/watch?v=wXxa2qijuZQ)

**Shells**
- [Shell method - 01](https://www.youtube.com/watch?v=ow8oayo4Z48)
- [Shell method - 02](https://www.youtube.com/watch?v=LuMt_uCdydU)
- [Shell method - 03](https://www.youtube.com/watch?v=5gLkhQztXJ0)

### 01 Theory

Take a graph $y=f(x)$ in the first quadrant of the $xy$-plane. Rotate this about the $y$-axis. The resulting 3D body is symmetric around the axis. We can find the volume of this body by using an integral to add up the volumes of infinitesimal **shells**, where each shell is a *thin cylinder*.

![700](Pasted%20image%2020240827225049.png)

The volume of each cylindrical shell is $2\pi\,R\,h\,\Delta r$:
![300](Pasted%20image%2020240827225029.png)

In the limit as $\Delta r\to dr$ and the number of shells becomes infinite, their total volume is given by an integral.

> [!concept] Volume by shells - general formula
> $$V=\int_a^b 2\pi Rh\,dr$$

In any concrete volume calculation, we simply interpret each factor, ‘$R$’ and ‘$h$’ and ‘$dr$’, and determine $a$ and $b$ in terms of the variable of integration that is set for $r$.

> [!tip] Shells vs. washers
> Can you see why shells are sometimes easier to use than washers?
> ![500](Pasted%20image%2020240827225152.png)
> 
> ![200](Pasted%20image%2020240827225302.png)

### 02 Illustration

> [!mexample] Example - Revolution of a triangle
> ![01 - Revolution of a triangle](Calculus%20II%20-%20Examples%20-%20Unit%2001.md#01%20-%20Revolution%20of%20a%20triangle)

%%  %%
> [!exercise] Exercise - Revolution of a sinusoid
> ![02 - Revolution of a sinusoid](Calculus%20II%20-%20Examples%20-%20Unit%2001.md#02%20-%20Revolution%20of%20a%20sinusoid)

## Integration by substitution

\[Note: this section is non-examinable. It is included for comparison to IBP.]

- [Integration by Substitution 1](https://www.youtube.com/watch?v=B3EyBCRXNDw): $\int\frac{-x}{(x+1)-\sqrt{x+1}}\,dx$
- [Integration by Substitution 2](https://www.youtube.com/watch?v=n2e-LkjK_B0): $\int\frac{x^5}{(1-x^3)^3}\,dx$
- [Integration by Substitution 3](https://www.youtube.com/watch?v=vBavjIHTQ2Y): $\int_0^1 x^2(1+x)^4\,dx$
- [Integration by Substitution 4](https://www.youtube.com/watch?v=ugK4id8qJ0M): $\int\frac{2x+3}{\sqrt{2x+1}}\,dx$
- [Integration by Substitution 5](https://www.youtube.com/watch?v=H7kjfK_m6sI): $\int\frac{\sin x}{\cos^3x}\,dx$
- [Integration by Substitution](https://www.youtube.com/watch?v=i58TAqPUgN0): Definite integrals, various examples

### 03 Theory

The method of **$u$-substitution** is applicable when the integrand is a *product*, with one factor a composite whose *inner function’s derivative* is the other factor.

> [!concept] Substitution
> Suppose the integral has this format, for some functions $f$ and $u$: $$\int f(u(x))\cdot u'(x)\,dx$$
> 
> Then the rule says we may convert the integral into terms of $u$ considered as a variable, like this: $$\int f(u(x))\cdot u'(x)\,dx\quad ⨠⨠ \quad \int f(u)\,du$$

The technique of $u$-substitution comes from the **chain rule for derivatives**: 
$$\frac{d}{dx}F\big(u(x)\big)=f(u(x))\cdot u'(x)$$
Here we let $F'=f$. Thus $\displaystyle\int f(x)\,dx = F(x) + C$ for some $C$.

Now, if we *integrate both sides* of this equation, we find: 
$$F\big(u(x)\big) = \int f(u(x))\cdot u'(x)\,dx$$
And of course $F\big(u\big)=\displaystyle\int f(u)\,du -C$.

> [!extra] Extra - Full explanation of $u$-substitution
> The substitution method comes from the **chain rule for derivatives**. The rule simply comes from *integrating on both sides* of the chain rule.
> 
> 1. && Setup: functions $F'=f$ and $u(x)$.
>     - Let $F$ and $f$ be any functions satisfying $F'=f$, so $F$ is an antiderivative of $f$.
>     - Let $u$ be another *function* and take $x$ for its independent variable, so we can write $u(x)$.
> 2. ! The chain rule for derivatives.
>     - Using primes notation: $$\big(F\circ u\big)'=(F'\circ u)\cdot u'$$
>     - Using differentials in variables: $$\frac{d}{dx}F\big(u(x)\big)=f(u(x))\cdot u'(x)$$
> 3. !!! Integrate both sides of chain rule.
>     - Integrate with respect to $x$: $$\begin{align*}\frac{d}{dx}F\big(u(x)\big)=f(u(x))\cdot u'(x) \qquad &\overset{\int}{⨠⨠} \qquad \int \frac{d}{dx}F\big(u(x)\big)=\int f(u(x))\cdot u'(x)\\\\ &\overset{\text{FTC}}{⨠⨠} \qquad F(u(x))=\int f(u(x))\cdot u'(x)\end{align*}$$
> 4. &&& Introduce ‘variable’ $u$ from the $u$-format of the integral.
>     - Treating $u$ as a variable, the definition of $F$ gives: $$F(u)=\int f(u)\,du+C$$
>     - Set the ‘variable’ $u$ to the ‘function’ $u$ output: $$F(u)\,\Big|_{u=u(x)}=F(u(x))$$
>     - Combining these: $$\begin{align*}F(u(x))&= F(u)\,\Big|_{u=u(x)}\\\\ &= \left.\int f(u)\,du\;\right|_{u=u(x)}+C\end{align*}$$
> 5. && Substitute for $F(u(x))$ in the integrated chain rule.
>     - Reverse the equality and plug in:  $$\int f(u(x))\cdot u'(x)\,dx=F(u(x))=\left.\int f(u)\,du\;\right|_{u=u(x)}+C$$
> 6. & This is “$u$-substitution” in final form.

## Integration by parts
Videos:
- [Integration by Parts 1](https://www.youtube.com/watch?v=F6RlYgZODyU): $\int e^x\,dx$ and $\int\ln x\,dx$
- [Integration by Parts 2](https://www.youtube.com/watch?v=EKht9hlok5k): $\int\tan^{-1}x\,dx$ and $\int x\sec x\,dx$
- [Integration by Parts 3](https://www.youtube.com/watch?v=btaQ-J4hCew): Definite integrals
- Example: $\int e^{3x}\cos 4x\,dx$, two methods:
    - [Double IBP](https://www.youtube.com/watch?v=BDZ0cLEpHlU)
    - [Fast Solution](https://www.youtube.com/watch?v=0YiaapQxdBE)
- [Integration by Parts 6](https://www.youtube.com/watch?v=gr3sNouGBww): $\int\sec^5x\,dx$

### 04 Theory

The method of **integration by parts** (abbreviated IBP) is applicable when the integrand is a *product* for which one factor is easily integrated while the other *becomes simpler* when differentiated.

> [!concept] Integration by parts
> Suppose the integral has this format, for some functions $u$ and $v$: $$\int u\cdot v'\,dx$$
> 
> Then the rule says we may convert the integral like this: $$\int u\cdot v'\,dx\quad ⨠⨠ \quad u\cdot v - \int u'\cdot v\,dx$$

This technique comes from the **product rule for derivatives**: 
$$\big(u\cdot v\big)'=u'\cdot v + u\cdot v'$$

Now, if we *integrate both sides* of this equation, we find: 
$$u\cdot v = \int u'\cdot v\,dx + \int u\cdot v'\,dx$$
and the IBP rule follows by algebra.

> [!extra] Extra - Full explanation of integration by parts
> 1. && Setup: functions $u$ and $v'$ are established.
>     - Recognize functions $u(x)$ and $v'(x)$ in the integrand: $$\int u\cdot v'\,dx$$
> 
> 2. ! Product rule for derivatives.
>     - Using primes notation: $$\big(u\cdot v\big)'=u'\cdot v + u\cdot v'$$
> 
> 3. !!! Integrate both sides of product rule.
>     - Integrate with respect to an input variable labeled ‘$x$’: $$\begin{align*}\big(u\cdot v\big)'=u'\cdot v + u\cdot v' \qquad &\overset{\int}{⨠⨠} \qquad \int \big(u\cdot v\big)'\,dx= \int u'\cdot v\,dx + \int u\cdot v'\,dx\\\\ \qquad &\overset{\text{FTC}}{⨠⨠} \qquad u\cdot v= \int u'\cdot v\,dx + \int u\cdot v'\,dx \end{align*}$$
> 
>     - Rearrange with algebra: $$\int u\cdot v'\,dx=u\cdot v-\int u'\cdot v$$
> 4. & This is “integration by parts” in final form.
> 
> **Addendum:** *definite* integration by parts
> 
> 3. ! Definite version of FTC.
>     - Apply FTC to $u\cdot v$: $$\int_a^b \big(u\cdot v\big)'\,dx = u\cdot v\,\Big|_a^b$$
> 
> 4. && Integrate the derivative product rule using specified bounds.
>     - Perform definite integral on both sides, plug in definite FTC, then rearrange: $$\int_a^b u\cdot v'\,dx = u\cdot v\,\Big|_a^b-\int_a^b u'\cdot v$$

> [!tip] Choosing factors well
> IBP is symmetrical. How do we know which factor to choose for $u$ and which for $v$?
> 
> Here is a trick: the acronym “LIATE” spells out the order of choices – to the left for $u$ and to the right for $v$: $$\begin{gather*}\text{LIATE}:\\\\ u\;\leftarrow\text{Logarithmic – Inverse\_trig – Algebraic – Trig – Exponential}\rightarrow v\end{gather*}$$

### 05 Illustration
> [!mexample] Example - A and T factors
> ![03 - A and T factors](Calculus%20II%20-%20Examples%20-%20Unit%2001.md#03%20-%20A%20and%20T%20factors)

%%  %%
> [!exercise] Exercise - Hidden A
> ![04 - Hidden A](Calculus%20II%20-%20Examples%20-%20Unit%2001.md#04%20-%20Hidden%20A)
