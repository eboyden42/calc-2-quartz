#### 01 - Modifying a known power series
Consider the power series $\frac{1}{1-x} = 1 + x + x^{2} + x^{3} + \cdots = \sum_{n = 0}^{\infty}x^{n}$ for $|x| < 1$. 

(a) By modifying the series $\frac{1}{1-x}$, write $\frac{1}{5-x}$ as a power series centered at $a = 0$ and determine its radius of convergence.

(b) By modifying the series $\frac{1}{1-x}$, write $\frac{1}{16+2x^{3}}$ as a power series centered at $a = 0$ and determine its radius of convergence.

**Solution**

**(a)**
1. & Rewrite in the form $a\cdot\frac{1}{1-bx}$.  $$\frac{1}{5-x} = \frac{1}{5\left(1-\frac{1}{5}x\right)} = \frac{1}{5}\cdot\frac{1}{1-\frac{1}{5}x}$$
2. && Expand out power series. $$\frac{1}{5-x}=\frac{1}{5}\left(1+\left(\frac{x}{5}\right)+\left(\frac{x}{5}\right)^{2}+\cdots\right)=\sum_{n = 0}^{\infty}\frac{1}{5}\left(\frac{x}{5}\right)^{n}$$
3. & Determine radius of convergence. $$R_{n}=\left|\frac{a_{n+1}}{a_{n}}\right|=\frac{1}{5}|x| \quad⨠⨠  \quad R_{n} = 5$$

**(b)**
1. & Rewrite in the form $a \cdot \frac{1}{1-bx^{c}}$. $$\frac{1}{16+2x^{3}}=\frac{1}{16}\cdot\frac{1}{1-\left(-\frac{1}{8}x^{3}\right)}$$
2. && Expand out power series. $$\frac{1}{16+2x^{3}} = \frac{1}{16}\left(1+\left(-\frac{1}{8}x^{3}\right)+\left(-\frac{1}{8}x^{3}\right)^{2} + \cdots \right)=\sum_{n=0}^{\infty}\frac{1}{16}\left(-\frac{1}{8}x^{3}\right)^{n}$$
3. & Determine radius of convergence. $$R_{n} = \left|\frac{a_{n+1}}{a_{n}}\right| = \frac{1}{8}\left|x^{3}\right| \quad ⨠⨠ \quad |x^{3}| < 8 \quad ⨠⨠ \quad R_{n} = 2$$


#### 03 - Approximating $1/e$
Using the series representation of $e^{x}$, show that: $$\frac{1}{e} = \frac{1}{2!}-\frac{1}{3!}+\frac{1}{4!}-\cdots$$
Now use the alternating series error bound to approximate $\frac{1}{e}$ to within $10^{-3}$.

**Solution**

1. &&& Write the down series representation of $e^{x}$. $$e^{x} = \sum_{n = 0}^{\infty}\frac{x^{n}}{n!}$$
2. & Substitute $x$ for $-x$ to find the series representation for $e^{-x} = \frac{1}{e^{x}}$. $$e^{-x}=\sum_{n=0}^{\infty}\frac{(-x)^{n}}{n!}$$
3. & Plug in $x = 1$ to find the series for $e^{-1}$. $$e^{-1}=\sum_{n=0}^{\infty}\frac{(-1)^{n}}{n!}=1-1+\frac{1}{2!}-\frac{1}{3!}+\cdots$$
4. && Use the alternating series error bound. 
    - $$\begin{align*}|a_{n+1}| &< 10^{-3} \\ \frac{1}{(n+1)!} &< 10^{-3} \quad ⨠⨠ \quad n = 6 \end{align*}$$
    - Therefore $\frac{1}{e} = \frac{1}{2!}-\frac{1}{3!}+\frac{1}{4!}-\frac{1}{5!}+\frac{1}{6!}$ is an estimate accurate with $10^{-3}$.


#### 04 - Power series of a derivative
Suppose that a function $f(x)$ has power series given by: $$f(x) = x^{2}-\frac{x^{4}}{2}+\frac{x^{6}}{3}-\frac{x^{8}}{4}+\cdots=\sum_{n = 0}^{\infty}(-1)^{n}\frac{x^{2n+2}}{n+1}$$
The radius of convergence of this series is $R = 1$.
What is the power series of $f'(x)$ and what is its radius of convergence?

**Solution**

1. && Take the derivative of the sum. $$f'(x)=\sum_{n=0}^{\infty}(-1)^{n}(2(n+1))\frac{x^{2n+1}}{n+1}=\sum_{n=0}^{\infty}2(-1)^{n}x^{2n+1}$$
2. & Determine radius of convergence.
    - Since the radius of convergence of $f(x)$ is 1, we conclude the radius of convergence of $f'(x) = 1$. 


#### 05 - Finding a power series
Find a power series representation of these functions:

(a) $f(x) = \frac{x^{2}}{x^{4}+81}$

(b) $g(x) = x^{2}\ln{(1+x)}$

**Solution**

1. && Rewrite in format $Ax \cdot \frac{1}{1-u}$. $$\frac{x^{2}}{x^{4}+81} = \frac{x^{2}}{81}\cdot\frac{1}{1-\left(-\frac{1}{81}x^{4}\right)}$$
2. && Plug $u = -\frac{1}{81}x^{4}$ into geometric series.
    - Geometric series in $u$. $$1+u+u^{2}+u^{3}+\cdots$$
    - Plug in $u = -\frac{1}{81}x^{4}$. $$1-\frac{x^{4}}{81}+\left(-\frac{x^{4}}{81}\right)^{2}+\left(-\frac{x^{4}}{81}\right)^{3}+\cdots$$
3. & Multiply by $\frac{x^{2}}{81}$ $$\frac{x^{2}}{x^{4}+81}=\frac{x^{2}}{81}-\frac{x^{6}}{81^{2}}-\frac{x^{10}}{81^{3}}+\cdots = \sum_{n = 0}^{\infty}\frac{x^{2}}{81}\left(-\frac{x^{4}}{81}\right)^{n}$$

**(b)**

1. && Find the power series of $\ln(1+x)$ (see example 10-05). $$\ln(1+x) = x-\frac{x^{2}}{2}+\frac{x^{3}}{3}-\frac{x^{4}}{4}+\cdots=\sum_{n= 1}^{\infty}\frac{(-1)^{n-1}x^{n}}{n}$$
2. & Multiply by $x^{2}$ to find the power series of $g(x)$. $$g(x)=x^{3}-\frac{x^{4}}{2}+\frac{x^{5}}{3}-\frac{x^{6}}{4}+\cdots=\sum_{n=1}^{\infty}\frac{(-1)^{n-1}x^{2n+1}}{n}$$


#### 06 - Modifying and integrating a power series

(a) Modify the power series $\frac{1}{1-x} = 1 + x + x^{2} + x^{3} + \cdots = \sum_{n = 0}^{\infty}x^{n}$ for $|x| < 1$ to obtain the power series for $f(x) = \frac{1}{1+ x^{4}}$.

(b) Now integrate this series to find the power series for $\int f(x) dx$.

**Solution**

**(a)**
1. & Rewrite $\frac{1}{1+x^{4}}$ as $\frac{1}{1-\left(-x^{4}\right)}$ and find the power series. $$\frac{1}{1+x^{4}}=1-x^{4}+x^{8}-x^{12}+\cdots=\sum_{n=0}^{\infty}\left(-x^{4}\right)^{n}$$

**(b)**
1. && Integrating term by term, we get $$\int f(x)dx = x-\frac{x^{5}}{5}+\frac{x^{9}}{9}-\frac{x^{13}}{13}+\cdots+C=C+\sum_{n=0}^{\infty}\frac{\left(-x^{4}\right)^{n+1}}{n+1}$$



#### 11 - Summing a Maclaurin series by guessing its function
For each of these series, identify the function of which it is the Maclaurin series:

(a) $\sum_{n = 0}^{\infty}(-1)^{n}\frac{5x^{4n+2}}{(2n+1)!}$

(b) $\sum_{n = 0}^{\infty}\frac{(-5x)^{n+1}}{n+1}$

Now find the total sums of these series:

(c) $\sum_{n = 0}^{\infty}\frac{(-5)^{n}}{n!}$

(d) $\sum_{n = 0}^{\infty}\frac{(-1)^{n}\pi^{2n}}{9^{n}(2n)!}$

**Solution**

**(a)**
1. && Write in the form of known Maclaurin series. $$\sum_{n = 0}^{\infty}(-1)^{n}\frac{5x^{4n+2}}{(2n+1)!} = 5\sum_{n = 0}^{\infty}(-1)^{n}\frac{\left(x^{2}\right)^{2n+1}}{(2n+1)!}=5\sin{x^{2}}$$

**(b)**
1. && Write in the form of known Maclaurin series. $$\sum_{n = 0}^{\infty}\frac{(-5x)^{n +1}}{n+1}=-\sum_{n=0}^{\infty}-\frac{(-5x)^{n+1}}{n+1}=-\ln\left(1-(-5x)\right)=-\ln(1+5x)$$

**(c)**
1. && Write in the form of known Maclaurin series, where $x = -5$. $$\sum_{n=0}^{\infty}\frac{(-5)^{n}}{n!}=e^{-5}$$

**(d)**
1. &&& Write as a product of two Maclaurin series. $$\sum_{n=0}^{\infty}\frac{(-1)^{n}\pi^{2n}}{9^{n}(2n)!}=\left(\sum_{n=0}^{\infty}(-1)^{n}\frac{\pi^{2n}}{(2n)!}\right)\left(\sum_{n=0}^{\infty}\left(\frac{1}{9}\right)^{n}\right)$$
2. && Evaluate series. $$\left(\sum_{n=0}^{\infty}(-1)^{n}\frac{\pi^{2n}}{(2n)!}\right)\left(\sum_{n=0}^{\infty}\left(\frac{1}{9}\right)^{n}\right) = \frac{1}{1-\frac{1}{9}}\cos{\pi}=-\frac{9}{8}$$

#### 14 - Large derivative using pattern of Maclaurin series
Consider the function $f(x)=x^{2}\sin{\left(5x^{3}\right)}$. Find the value of $f^{(35)}(0)$.

(Hint: find the rule for coefficients of the Maclaurin series of $f(x)$ and then plug in 0.) 

**Solution**

1. && Find series for $\sin\left(5x^{3}\right)$ using our known series and plugging in $u =5x^{3}$. $$\sin\left(5x^{3}\right)=\sum_{n=0}^{\infty}(-1)^{n}\frac{\left(5x^{3}\right)^{2n+1}}{(2n+1)!} = \sum_{n=0}^{\infty}(-1)^{n}\frac{5^{2n+1}x^{6n+3}}{(2n+1)!}$$
2. & Multiply series by $x^{2}$ to obtain the series for $f(x)$. $$x^{2}\sum_{n=0}^{\infty}(-1)^{n}\frac{5^{2n+1}x^{6n+3}}{(2n+1)!}=\sum_{n=0}^{\infty}(-1)^{n}\frac{5^{2n+1}x^{6n+5}}{(2n+1)!}$$.
3. !! Note that MacLaurin series of $f$ have the form $\sum_{n = 0}^{\infty}a_{n}x^{n}$, where $a_{n}=\frac{f^{(n)}(0)}{n!}$. So, $f^{(n)}(0) = n!\cdot a_{n}$.
4. && Compute $a_{35}$.  $$a_{6n+5}=(-1)^{n}\frac{5^{2n+1}}{(2n+1)!}\quad ⨠⨠ \quad a_{35}=(-1)^{5}\frac{5^{11}}{11!}=-\frac{5^{11}}{11!}$$
5. & Compute $f^{(35)}(0)$. $$f^{(35)}(0)=35!\cdot a_{35}=5^{11}\cdot \frac{35!}{11!}$$

#### 15 - Estimates with alternating series error bound
Without a calculator, estimate $\cos(0.02)$ (the angle in radians) with an error below $1\times10^{-6}$.

(Use the error bound formula for alternating series.)

**Solution**

1. & Write the Maclaurin series of $\cos(x)$. $$\cos(x)=\sum_{n=0}^{\infty}(-1)^{n}\frac{x^{2n}}{(2n)!}$$
2. && Implement error bound to set up question for $n$.
    - Find $n$ such that $a_{n+1}\leq 10^{-6}$, and therefore $$|E_{n}| \leq a_{n+1}\leq10^{-6}$$
    - Plug in $x = 0.02$.  $$a_{2n}=\frac{0.02^{2n}}{(2n)!}$$
3. & Find when $a_{2n} \leq 10^{-6}$.
    - The first time $a_{2n}$ is below $10^{-6}$ is when $2n = 4$.
4. && Derive conclusions.
    - The sum of prior terms equals $T_{3}(0.02)$.
    - For $\cos(x)$, there is no $x^{3}$ term, so $T_{3}(0.02) = T_{2}(0.02)$, so $n = 2$.


#### 16 - Estimates with alternating series error bound
Find an infinite series representation of $\int_{0}^{1}\sin\left(x^{2}\right)dx$ and then use your series to estimate this integral to within an error of $10^{-3}$.

(Use the error bound formula for alternating series.)

**Solution**

1. & Write the series of the integrand. Note that $u = x^{2}$. $$\sin\left(x^{2}\right)=\sum_{n=0}^{\infty}(-1)^{n}\frac{\left(x^{2}\right)^{2n+1}}{(2n+1)!}=\sum_{n=0}^{\infty}(-1)^{n}\frac{x^{4n+2}}{(2n+1)!}$$
2. && Compute integral of series. $$\int_{0}^{1} \sum_{n=0}^{\infty}(-1)^{n}\frac{x^{4n+2}}{(2n+1)!}dx=\left.\left[\sum_{n=0}^{\infty}(-1)^{n}\frac{x^{4n+3}}{(4n+3)(2n+1)!}\right]\right|_{0}^{1}=\sum_{n=0}^{\infty}\frac{(-1)^{n}}{(4n+3)(2n+1)!}$$
3. & Compute terms until coefficient is below $10^{-3}$.
    - The first coefficient that is below $10^{-3}$ is $\frac{1}{\left(4(2)+3\right)\left(2(2)+1\right)!}$. So, the sum of the terms before this will give you an appropriate estimate.
4. & Final answer is $\frac{1}{3}-\frac{1}{42} \approx 0.3095$.




