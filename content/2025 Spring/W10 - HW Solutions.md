#### 01 - Ratio and root tests
Apply the ratio test or the root test to determine whether each of the following series are absolutely convergent, conditionally convergent, or divergent.

(a) $\displaystyle\sum_{k = 0}^{\infty}\left(\frac{k}{3k+1}\right)^{k}$ $\qquad$ (b) $\displaystyle\sum_{n = 1}^{\infty}(-1)^{n}\frac{e^{n}}{n!}$ $\qquad$ (c) $\displaystyle\sum_{n = 1}^{\infty}\frac{1}{(2n)!}$

**Solution**

**(a)**
1. & Apply the root test. $$\sqrt[k]{|a_{k}|} = \frac{k}{3k + 1} $$
2. & Compute limit  $$\lim_{n \to \infty}\sqrt[k]{|a_{k}|} = \frac{1}{3} < 1$$
3. & State conclusions.
    - Since the limit is less than 1, we conclude that the series converges absolutely.

**(b)**
1. & Apply the ratio test. $$\left|\frac{a_{n+1}}{a_{n}}\right| = \frac{e^{n + 1}}{(n + 1)!}\cdot\frac{n!}{e^{n}} = \frac{e}{n + 1}$$
2. & Compute limit. $$\lim_{n \to \infty}\left|\frac{a_{n + 1}}{a_{n}}\right| = 0 < 1$$
3. & State conclusions. 
    - Since the limit is less than 1, we conclude that the series is absolutely convergent.

**(c)**
1. & Apply the ratio test. $$\left|\frac{a_{n+1}}{a_{n}}\right| = \frac{1}{\left(2(n+1)\right)!}\cdot(2n)! = \frac{1}{(2n+1)(2n+2)}$$
2. & Compute limit. $$\lim_{n \to \infty}\left|\frac{a_{n + 1}}{a_{n}}\right| = 0 < 1$$
3. & State conclusions.
    - Since the limit is less than 1, we conclude that the series is absolutely convergent.

#### 03 - Ratio and root tests
Apply the ratio test or the root test to determine whether each of the following series is absolutely convergent, conditionally convergent, or divergent.

(a) $\displaystyle\sum_{n = 1}^{\infty}\frac{(-2)^{n}}{n^{100}}$ $\qquad$ (b) $\displaystyle\sum_{n = 0}^{\infty}\left(\frac{5n}{10n+4}\right)^{n}$ $\qquad$ (c) $\displaystyle\sum_{n = 1}^{\infty}\frac{\sqrt{n}}{3^{n}}$

**Solution**

**(a)**
1. & Apply ratio test. $$\left|\frac{a_{n+1}}{a_{n}}\right| = \frac{2^{n + 1}}{(n+1)^{100}} \cdot \frac{n^{100}}{2^{n}} = 2\left(\frac{n}{n+1}\right)^{100}$$
2. & Compute limit. $$\lim_{n \to \infty}\left|\frac{a_{n+1}}{a_{n}}\right| = 2 > 1$$
3. & State conclusions.
    - Since the limit is greater than 1, we conclude that the series is divergent.

**(b)**
1. & Apply root test. $$\sqrt[n]{|a_{n}|} = \frac{5n}{10n+4}$$
2. & Compute limit. $$\lim_{n \to\infty}\sqrt[n]{|a_{n}|} = \frac{1}{2} < 1$$
3. & State conclusions.
    - Since the limit is less than 1, we conclude that the series is absolutely convergent.

**(c)**
1. & Apply ratio test. $$\left|\frac{a_{n+1}}{a_{n}}\right| = \frac{\sqrt{n+1}}{3^{n+1}}\cdot\frac{3^{n}}{\sqrt{n}} = \frac{1}{3}\sqrt{\frac{n+1}{n}}$$
2. & Compute limit. $$\lim_{n \to \infty}\left|\frac{a_{n+1}}{a_{n}}\right|=\frac{1}{3} < 1$$
3. & State conclusions.
    - Since the limit is 1, we conclude that the series is absolutely convergent.

#### 04 - Various limits, Part I
Find the limits. You may use $+\infty$ or $-\infty$ or $\mathrm{DNE}$ as appropriate. Braces indicate sequences.
- C = Convergent
- AC = Absolutely Convergent
- CC = Conditionally Convergent
- D = Divergent

|             $a_n$              | $\lim _{n \rightarrow \infty} a_n$ | $\left\{a_n\right\}$<br>C or D | $\lim _{n \rightarrow \infty}(-1)^n a_n$ | $\left\{(-1)^n a_n\right\}$<br>C or D | $\sum a_n$<br>AC, CC, or D | $\sum(-1)^n a_n$<br>AC, CC, or D |
|:------------------------------:|:----------------------------------:|:------------------------------:|:----------------------------------------:|:-------------------------------------:|:--------------------------:|:--------------------------------:|
|  $\displaystyle\frac{1}{n+2}$  |                 0                  |              $C$               |                    0                     |                  $C$                  |            $D$             |              $C C$               |
|  $\displaystyle\frac{n}{n+2}$  |                 1                  |              $C$               |                 $D N E$                  |                  $D$                  |            $D$             |               $D$                |
| $\displaystyle\frac{1}{n^2+2}$ |                 0                  |              $C$               |                    0                     |                  $C$                  |           $A C$            |              $A C$               |
|  $\displaystyle\frac{4}{2^n}$  |                 0                  |              $C$               |                    0                     |                  $C$                  |           $A C$            |              $A C$               |
| $\displaystyle\frac{4 n}{2^n}$ |                 0                  |              $C$               |                    0                     |                  $C$                  |           $A C$            |              $A C$               |

#### 05 - Various limits, Part II
Find the limits. You may use $+\infty$ or $-\infty$ or $\mathrm{DNE}$ as appropriate. Braces indicate sequences.
- C = Convergent
- AC = Absolutely Convergent
- CC = Conditionally Convergent
- D = Divergent

|                $a_n$                | $\lim _{n \rightarrow \infty} a_n$ | $\left\{a_n\right\}$<br>C or D | $\lim _{n \rightarrow \infty}(-1)^n a_n$ | $\left\{(-1)^n a_n\right\}$<br>C or D | $\sum a_n$<br>AC, CC, or D | $\sum(-1)^n a_n$<br>AC, CC, or D |
| :---------------------------------: | :--------------------------------: | :----------------------------: | :--------------------------------------: | :-----------------------------------: | :------------------------: | :------------------------------: |
|   $\displaystyle\frac{4 n!}{2^n}$   |              $\infty$              |              $D$               |                 $D N E$                  |                  $D$                  |            $D$             |               $D$                |
| $\displaystyle\frac{(n+2) 3^n}{n!}$ |                 0                  |              $C$               |                    0                     |                  $C$                  |           $A C$            |              $A C$               |
| $\displaystyle\frac{4^n}{(3 n)^n}$  |                 0                  |              $C$               |                    0                     |                  $C$                  |           $A C$            |              $A C$               |
|  $\displaystyle\frac{1}{(2n+1)!}$   |                 0                  |              $C$               |                    0                     |                  $C$                  |           $A C$            |              $A C$               |

#### 07 - Power series - interval of convergence
Find the radius and interval of convergence for these power series:
- (a) $\sum_{n = 0}^{\infty}\frac{(x-8)^{n}}{n^{4}+1}$
- (b) $\sum_{n = 1}^{\infty}\frac{x^{n}}{3\cdot7\cdot11\cdots(4n-1)}$

**Solution**

**(a)**
1. & Apply the ratio test. $$R_{n} = \lim_{n \to \infty}\left|\frac{(x-8)^{n+1}}{(n+1)^{4}+1}\cdot\frac{n^{4}+1}{(x-8)^{n}}\right|=\lim_{n\to\infty}\left|\frac{(x-8)\left(n^{4}+1\right)}{(n+1)^{4}+1}\right|=|x-8|$$
2. && Find interval of convergence. $$|x-8|< 1 \quad ⨠⨠ \quad -1<x-8<1 \quad ⨠⨠\quad 7<x<9$$
3. & Check endpoints and state final answer
    - at $x = 7$, we have $\sum_{n=0}^{\infty}\frac{(-1)^{n}}{n^{4}+1}$, which converges absolutely by the alternating series test.
    - at $x = 9$, we have $\sum_{n = 0}\frac{1}{n^{4}+1}$, which converges by the DCT.
    - Therefore, the radius of convergence is $1$ and our interval of convergence is $[7, 9]$.

**(b)**
1. && Apply the ratio test. $$R_{n} = \lim_{n \to \infty}\left|\frac{x^{n+1}}{3\cdot7\cdot11\cdots(4n-1)(4n+3)}\cdot\frac{3\cdot7\cdot11\cdots(4n-1)}{x^{n}}\right|=\lim_{n\to\infty}\left|\frac{x}{4n+3}\right| = 0$$
2. & Derive conclusions. 
    - Since the ratio test evaluates to 0, the series converges for all $x$, so the radius of convergence is $\infty$ and the interval of convergence is $(-\infty, \infty)$.