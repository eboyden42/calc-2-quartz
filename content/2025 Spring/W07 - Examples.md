## Sequences

#### Geometric sequence: revealing the format
Find $a_0$ and $r$ and $a_n$ (written in the geometric sequence format) for the following geometric sequences:

(a) $\; a_n=\left(-\displaystyle\frac{1}{2}\right)^n$ $\qquad$ (b) $\; b_n= -3\left( \displaystyle \frac{2^{n+1}}{5^n} \right)$ $\qquad$  (c) $\; c_n=e^{5+7n}$

**Solution**
(a)
Plug in $n=0$ to obtain $a_0=1$. Notice that $a_{n+1}/a_n=-1/2$ and so therefore $r=-1/2$. Then the ‘general term’ is $a_n=a_0\cdot r^n=1\cdot(-1/2)^n$.

(b)
Rewrite the fraction: $$\frac{2^{n+1}}{5^n}\quad ⨠⨠ \quad 2\cdot\left(\frac{2}{5}\right)^n$$
Plug that in and observe $b_n=-6\cdot(2/5)^n$. From this format we can *read off* $b_0=-6$ and $r=2/5$.

(c)
Rewrite: $$c_n\quad ⨠⨠ \quad e^5\cdot e^{7n}\quad ⨠⨠ \quad e^5\cdot\left(e^7\right)^n$$
From this format we can *read off* $c_0=e^5$ and $r=e^7$.

#### L’Hopital’s Rule for sequence limits
(a) What is the limit of $a_n=\displaystyle\frac{\ln n}{n}$?
(b) What is the limit of $b_n=\displaystyle\frac{(\ln n)^2}{n}$?
(c) What is the limit of $c_n=n\left(\sqrt{n^2+1}-\sqrt{n}\right)$?

**Solution**
(a)
Identify indeterminate form $\frac{\infty}{\infty}$. Change from $n$ to $x$ and apply L’Hopital: $$\lim_{x\to\infty}\frac{\ln x}{x}\qquad \overset{\frac{d}{dx}}{⨠⨠} \qquad \lim_{x\to\infty}\frac{1/x}{1}=0 $$

(b)
Identify indeterminate form $\frac{\infty}{\infty}$. Change from $n$ to $x$ and apply L’Hopital: $$\lim_{x\to\infty}\frac{(\ln x)^2}{x}\qquad \overset{\frac{d}{dx}}{⨠⨠} \qquad \lim_{x\to\infty}\frac{2\ln x \cdot \frac{1}{x}}{1}=2\lim_{x\to\infty}\frac{\ln x}{x}\quad\overset{\text{(by $a_n$ result)}}{=}\quad 0 $$

(c)
Identify form $\infty\cdot 0$ and rewrite as $\frac{\infty}{\infty}$: $$n\left(\sqrt{n^2+1}-\sqrt{n}\right)\qquad ⨠⨠ \qquad \frac{\sqrt{n^2+1}-\sqrt{n}}{1/n} $$
Change from $n$ to $x$ and apply L’Hopital: $$\lim_{x\to\infty}\frac{\sqrt{x^2+1}-\sqrt{x}}{1/x}\qquad ⨠⨠ \qquad \frac{\frac{1}{2}\left(x^2+1\right)^{-1/2}(2x)-\frac{1}{2}x^{-1/2}}{-1/x^2}$$

Simplify: $$\qquad ⨠⨠ \qquad \frac{-2x^3}{\sqrt{x^2+1}}+x^{3/2}=\frac{-2x^3+x^{3/2}\sqrt{x^2+1}}{\sqrt{x^2+1}}$$
Consider the limit: $$\frac{-2x^3+x^{3/2}\sqrt{x^2+1}}{\sqrt{x^2+1}} \quad\overset{x\to\infty}{\longrightarrow}\quad \frac{-2x^3+x^{3/2}x}{x}\longrightarrow \frac{-2x^3}{x}\longrightarrow -\infty$$

#### Squeeze theorem
Use the squeeze theorem to show that $\frac{4^n}{n!}\to 0$ as $n\to\infty$.

**Solution**
We will squeeze the given general term above $0$ and below a sequence $b_n$ that we must devise: $$0\leq \frac{4^n}{n!}\leq b_n$$
We need $b_n$ to satisfy $b_n\to 0$ and $\frac{4^n}{n!}\leq b_n$. Let us study $\frac{4^n}{n!}$. $$\frac{4^n}{n!}=\frac{\;\;\,4\cdot4\cdot\;\cdots\;\cdot4\cdot4\cdot4\cdot4\cdot4\cdot4\cdot 4}{n(n-1)\cdots7\cdot6\cdot5\cdot4\cdot3\cdot2\cdot1}$$
Now for the trick. Collect factors in the middle bunch: $$\frac{4^n}{n!}=\frac{4}{n}\left(\frac{4}{n-1}\cdot\frac{4}{n-2}\cdot\;\cdots\;\cdot\frac{4}{7}\cdot\frac{4}{6}\cdot\frac{4}{5}\right)\frac{4\cdot4\cdot4\cdot4}{4\cdot3\cdot2\cdot1}$$
Each factor in the middle bunch is $< 1$ so the entire middle bunch is $< 1$. Therefore: $$\frac{4^n}{n!}<\frac{4}{n}\cdot \frac{4^4}{4!}=\frac{1024}{24n}$$
Now we can easily see that $1024/24n\to0$  as $n\to\infty$, so we set $b_n=1024/24n$ and we are done.

#### Monotonicity
Show that $a_n=\sqrt{n+1}-\sqrt{n}$ converges.

**Solution**
1. & Observe that $a_n> 0$ for all $n$.
    - Because $n+1>n$, we know $\sqrt{n+1}>\sqrt{n}$.
    - Therefore $\sqrt{n+1}-\sqrt{n}>0$
2. &&& Change $n$ to $x$ and show $a_x$ is decreasing.
    - New formula: $a_x=\sqrt{x+1}-\sqrt{x}$ considered as a *differentiable* function.
    - !! Take derivative to show decreasing.
        - Derivative of $a_x$: $$\frac{d}{dx}a_x=\frac{1}{2\sqrt{x+1}}-\frac{1}{2\sqrt{x}}$$
    - Simplify: $$\qquad ⨠⨠ \qquad \frac{2\left(\sqrt{x}-\sqrt{x+1}\right)}{4\sqrt{x}\sqrt{x+1}}$$
    - Denominator is $>0$. Numerator is $<0$. So $\frac{d}{dx}a_x<0$ and $a_x$ is monotone decreasing.
3. & Therefore $a_n$ is monotone decreasing as $n\to\infty$.

## Series

#### Geometric series - total sum and partial sums
The geometric series *total sum $S$* can be calculated using a *“shift technique”* as follows: 
1. Compare $S$ and $rS$: $$\begin{align*}S\quad =\quad & a_0+a_0r+a_0r^2+a_0r^3+\cdots\\ \qquad \overset{\times r}{ ⨠⨠ } \qquad rS\quad =\quad & a_0r+a_0r^2+a_0r^3+a_0r^4+\cdots\end{align*}$$
2. Subtract second line from first line, many cancellations: $$\begin{align*}S&\quad =\quad  a_0+a_0r+a_0r^2+a_0r^3+\cdots\\ -\Big(rS&\quad =\quad  a_0r+a_0r^2+a_0r^3+a_0r^4+\cdots\Big)\\———&———————————————\\ S-rS&\quad=\quad a_0\end{align*}$$
3. Solve to find $S$: $$S\quad=\quad\frac{a_0}{1-r}$$
- !! Note: this calculation *assumes* that $S$ exists, i.e. that the series *converges*.

The geometric series *partial sums* can be calculated similarly, as follows: 
1. Compare $S$ and $rS$: $$\begin{align*}S_N\quad =\quad & a_0+a_0r+a_0r^2+\cdots+a_0r^N\\ \qquad \overset{\times r}{ ⨠⨠ } \qquad rS_N\quad =\quad & a_0r+a_0r^2+\cdots+a_0r^N+a_0r^{N+1}\end{align*}$$
2. Subtract second line from first line, many cancellations: $$\begin{align*}S_N\quad =\quad & a_0+a_0r+a_0r^2+\cdots+a_0r^N\\ -\Big(rS_N\quad =\quad & a_0r+a_0r^2+\cdots+a_0r^N+a_0r^{N+1}\Big)\\———&———————————————\\ S_N-rS_N&\quad =\quad  a_0-a_0r^{N+1}\end{align*}$$
3. Solve to find $S_N$: $$\begin{gather*}S_N\quad =\quad a_0\frac{1-r^{N+1}}{1-r}\\\\ =\quad \frac{a_0}{1-r}-\frac{a_0}{1-r}r^{N+1}\quad=\quad S-Sr^{N+1}\end{gather*}$$
- The last formula is revealing in its own way. Here is what it means in terms of terms: $$\begin{aligned}a_0+a_0r+\dots+a_0r^N= \\\\& \begin{aligned}a_0+a_0r+a_0r^2+\cdots&\\\quad &-\Big(a_0r^{N+1}+a_0r^{N+2}+\cdots \Big) \end{aligned}\end{aligned}$$
