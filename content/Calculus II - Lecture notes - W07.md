---
cssclasses:
  - hide-embedded-header
title: W07 Notes
---
## Sequences

Videos, Math Dr. Bob: 
- [Infinite sequences](https://www.youtube.com/watch?v=BsgL0-iOU3o): Definition; Squeeze Theorem
    - Extra: [Infinite sequences](https://www.youtube.com/watch?v=JURgCWoxFEQ): Various examples, arithmetic and geometric
    - Extra: [Infinite sequences](https://www.youtube.com/watch?v=yAW8MHIyUJw): Recursive sequences (like Fibonacci)

### 01 Theory

A **sequence** is a rule that defines a **term** for each natural number $n\in\mathbb{N}$: $$a_0,\;a_1,\;a_2,\;a_3,\;a_4,\;\dots$$
So a sequence is a function from $\mathbb{N}$ to $\mathbb{R}$.

> [!concept] Geometric sequence
> A sequence is called **geometric** if the *ratio of consecutive terms is some constant $r$*, independent of $n$: $$\frac{a_{n+1}}{a_n}=r\quad \text{for every}\;n$$

The defining relation of a geometric sequence is equivalent to $a_{n+1}=a_n\cdot r$.

By plugging $a_1=a_0\cdot r$ into $a_2=a_1\cdot r$, we have $a_2=(a_0\cdot r)\cdot r=a_0\cdot r^2$. This plugging can be repeated $n$-times to get a formula for the $n^\text{th}$ term: $$a_n=a_{n-1}\cdot r=a_{n-2}\cdot r^2=a_{n-3}\cdot r^3=\dots=a_1\cdot r^{n-1}=a_0\cdot r^n$$
Therefore $a_n=a_0\cdot r^n$, and we have a formula for the **general term** of the sequence (the term with index $n$).

![center|250](Pasted%20image%2020241009080349.png)

> [!notation] Starting point of a sequence
> Note that sometimes the index (variable) of a sequence starts somewhere other than $0$. Most common is $1$ but any other starting point is allowed, even negative numbers.
> 
> Sometimes $c$ is used instead of $a_0$ in the formula for the general term of a sequence, thus $a_n=cr^n$. The ‘$c$’ notation is useful when the sequence starts from $n\neq 0$.

> [!extra] Extra - Fibonacci sequence
> The **Fibonacci** sequence goes like this:
> $$0,\; 1,\; 1,\; 2,\; 3,\; 5,\; 8,\; 13,\; 21,\; 34,\; 55,\; 89,\; 144,\; \dots$$
> The pattern is: $$F_{n}=F_{n-1}+F_{n-2}$$ This formula is a **recursion relation**, which means that terms are defined using the values of prior terms.
> 
> The Fibonacci sequence is perhaps the most famous sequence of all time. It is related to the Golden Ratio and the Golden Spiral:
> 
> ![center|300](Pasted%20image%2020241008210315.png)

### 02 Illustration

> [!mexample] Geometric sequence: revealing the format
> ![Geometric sequence: revealing the format](Calculus/2025%20Spring/W07%20-%20Examples.md#Geometric%20sequence%20revealing%20the%20format)

## Series
Videos, Math Dr. Bob:
- [Infinite series](https://www.youtube.com/watch?v=B5B347sw3ok): Definitions, basic examples
- [Geometric series and SDT](https://www.youtube.com/watch?v=h84pokHK-JU): Geometric series, Simple Divergence Test (aka “Limit Test”)
- [Infinite series](https://www.youtube.com/watch?v=T-qSECuTi2Y): Various examples
    - Extra: [Infinite series convergence](https://www.youtube.com/watch?v=pWshnk-dZ9w): Telescoping series

### 03 Theory

A **series** is an infinite sum that is created by successive additions without end. The terms are not added up “all at once” but rather they are added up “as $n$ increases” or “as $n\to\infty$.”
$$a_0+a_1+a_2+a_3+\dots\qquad =\quad\sum_{n=0}^\infty a_n$$
Three of the most famous series are the Leibniz series and the geometric series:
$$\begin{align*}\text{Leibniz series:}& \qquad 1-\frac{1}{3}+\frac{1}{5}-\frac{1}{7}+\cdots+\frac{(-1)^n}{2n+1}+\cdots &=&\quad\frac{\pi}{4} \\\\ \text{Geometric series:}& \qquad 1+\frac{1}{2}+\frac{1}{4}+\frac{1}{8}+\cdots+\left(\frac{1}{2}\right)^n+\cdots &=&\quad 2\end{align*}$$

---

> [!concept] Partial sum sequence of a series
> The **partial sum sequence** of a series is the *sequence* whose terms are the sums up to the given index: 
> $$S_N=a_0+a_1+\dots+a_N\qquad =\quad \sum_{n=0}^N a_n$$
> These $S_N$ terms themselves form a sequence: 
> $$S_0,\;S_1,\;S_2,\;S_3,\;\dots$$

### 04 Illustration

> [!mexample] Example - Geometric series
> ![Geometric series - total sum and partial sums](Calculus/2025%20Spring/W07%20-%20Examples.md#Geometric%20series%20-%20total%20sum%20and%20partial%20sums)

## Convergence
Videos, Math Dr. Bob:
- [Infinite sequences convergence](https://www.youtube.com/watch?v=EkbPeM6kfp4): Squeeze; Monotone Bounded
- [Infinite sequences convergence](https://www.youtube.com/watch?v=JKiwztS6e_s): Examples sequences: convergent, monotonic, bounded

### 05 Theory

A sequence has a **limit** if its terms tend toward a specific number, or toward $\pm\infty$.
![center|600](Pasted%20image%2020241009080939.png)

When this happens we can write “$\lim_{n\to\infty}a_n=L$” with some number $L\in\mathbb{R}$ or $L=\pm\infty$.
We can also write “$a_n\to L$ as $n\to\infty$”.

The sequence is said to **converge** if it has a *finite limit* $L\in\mathbb{R}$.

Some sequences don’t have a limit at all, like $a_n=\cos n$:
![center|300](Pasted%20image%2020241009081114.png)

Or $a_n=e^n$: 
![center|300](Pasted%20image%2020241009081153.png)

These sequences **diverge**.
In the second case, there is a limit $L=\infty$, so we say it **diverges to $+\infty$**.

- %& The difference between *converging* and *having a limit* is that a limit could ‘exist’, namely at $+\infty$ or $-\infty$, yet we still say the sequence diverges.

> [!extra] Extra - Convergence definition
> The precise meaning of convergence is this. We have $a_n\to L$ as $n\to\infty$ if, given any proposed error $\varepsilon>0$, it is possible to find $N$ such that for all $n>N$ we have $|a_n-L|<\varepsilon$.
> 
> When $L=\infty$, convergence means that given any $B>0$, we can find $N$ such that for all $n>N$ we have $a_n>B$.
> 
> Similarly for $L=-\infty$.

---

If the general term $a_n$ is a continuous function of $n$, we can replace $n$ with the continuous variable $x$ and compute the continuous limit instead: $$\lim_{n\to\infty}a_n\quad=\quad\lim_{x\to\infty}a_x$$

If $a_x$ would be a *differentiable* function, and we discover an *indeterminate form*, then we can apply L’Hopital’s Rule to find the limit value. For example, if the indeterminate form is $0\cdot\infty$, we can convert it to $\frac{\infty}{1/0}=\frac{\infty}{\infty}$ and apply L’Hopital.

### 06 Illustration

> [!mexample] L’Hopital’s Rule for sequence limits
> ![L’Hopital’s Rule for sequence limits](Calculus/2025%20Spring/W07%20-%20Examples.md#L’Hopital’s%20Rule%20for%20sequence%20limits)

> [!extra] Extra - Squeeze theorem
> ![Squeeze theorem](Calculus/2025%20Spring/W07%20-%20Examples.md#Squeeze%20theorem)

### 07 Theory

> [!concept] Monotone sequences
> A sequence is called **monotone increasing** if $a_{n+1}\geq a_n$ for every $n$.
> 
> A sequence is called **monotone decreasing** if $a_{n+1}\leq a_n$ for every $n$.

In this context, ‘monotone’ just means it preserves the increasing or decreasing modality for *all* terms.

> [!abstract] Monotonicity Theorem
> If a sequence is monotone increasing, and **bounded above** by $B$, then it *must converge* to some limit $L$, and $L\leq B$.
> 
> If a sequence is monotone decreasing, and **bounded below** by $B$, then it *must converge* to some limit $L$, and $L\geq B$.

Terminology: 
- *Bounded above by $B$* means that $a_n\leq B$ for every $n$
- *Bounded below by $B$* means that $B\leq a_n$ for every $n$

Notice!
- !!! The Monotonicity Theorem says that a limit $L$ *exists*, but it does not *provide* the limit value.

### 08 Illustration

> [!mexample] Monotonicity theorem
> ![Monotonicity](Calculus/2025%20Spring/W07%20-%20Examples.md#Monotonicity)

### 09 Theory

> [!concept] Series convergence
> We say that a *series* converges when its *partial sum sequence converges*: 
> $$\text{“}\sum_{n=0}^\infty a_n\quad\text{converges}\text{”}\qquad \text{MEANS:}\qquad \text{“}S_N\quad\text{converges as $N\to\infty$”}$$

Let us apply this to the geometric series. Recall our formula for the partial sums: 
$$S_N=a_0\frac{1-r^{N+1}}{1-r}$$
Rewrite this formula: $$\qquad ⨠⨠ \qquad S_N = \frac{a_0}{1-r}-\frac{a_0}{1-r}r^{N+1}$$
Now take the limit as $N\to\infty$: $$\lim_{N\to\infty}S_N\quad =\quad \text{“}\;\frac{a_0}{1-r}-\frac{a_0}{1-r}r^{\infty+1}\;\text{”}\quad=\quad \frac{a_0}{1-r}$$

- !! So we see that $S_N$ converges exactly when $|r|< 1$. It converges to $\frac{a_0}{1-r}$.

(If $|r|=1$ then the denominator is $0$, and if $|r|>1$ then the factor $r^{\infty+1}$ does not converge.)

Furthermore, we have the limit value: 
$$\sum_{n=0}^\infty a_n\quad =\quad \lim_{N\to\infty} S_N = \frac{a_0}{1-r}=S$$

This result confirms the formula we derived for the total $S$ for a geometric series. This time we did not start by assuming $S$ exists, on the contrary we *proved* that $S$ exists. (Provided that $|r|<1$.)

> [!extra] Extra - Aspects of $S$ and $S_N$ from the geometric series
> Notice that we always have the rule: $$\begin{align*}S_N&= S-r^{N+1}S\\\\ S_N &= \frac{a_0}{1-r}-\frac{a_0}{1-r}r^{N+1}\end{align*}$$
> This rule can be viewed as coming from partitioning the full series into a finite part $S_N$ and the remaining infinite part: $$\begin{align*}S&= \underbrace{a_0+a_0r+\dots+a_0r^N}_{S_N}+\underbrace{a_0r^{N+1}+a_0r^{N+2}+\dots}_{S-S_N}\end{align*}$$
> We can remove a factor $r^{N+1}$ from the infinite part: $$S-S_N=r^{N+1}\left(a_0+a_0r+a_0r^2\;\dots\;\right)$$
> The parenthetical expression is equal to $S$, so we have the formula $S_N=S-r^{N+1}S$ given above.

