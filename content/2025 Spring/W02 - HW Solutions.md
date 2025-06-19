#### 04
Compute the definite integral: $$\int_{0}^{\frac{1}{2}}\frac{x^{2}}{\sqrt{1-x^{2}}}dx$$

**Solution**
1. &&& Perform substitution $x = \sin{\theta}$. Draw right triangle with the length of the hypotenuse being 1 and that of the opposite being $x$ for reference.
    - $dx = \cos{\theta}d\theta$
    - Adjust the bounds:
    $$\begin{align*}x &= 0 \quad ⨠⨠ \quad \theta = 0 \\ x &= \frac{1}{2} \quad ⨠⨠ \quad \theta = \frac{\pi}{6}  \end{align*}$$
    - Rewrite integral
    $$\int_{0}^{\frac{1}{2}} \frac{x^{2}}{\sqrt{1-x^{2}}}dx=\int_{0}^{\frac{\pi}{6}}\frac{\sin^{2}{\theta}\cos{\theta}}{\sqrt{1-\sin^{2}{\theta}}}d\theta$$

2. && Simplify integral using Pythagorean identity $1- \sin^{2}{\theta} = \cos^{2}{\theta}$
$$\begin{align*}
\int_{0}^{\frac{\pi}{6}}\frac{\sin^{2}{\theta}\cos{\theta}}{\sqrt{1-\sin^{2}{\theta}}}d\theta &= \int_{0}^{\frac{\pi}{6}}\frac{\sin^{2}{\theta}\cos{\theta}}{\sqrt{\cos^{2}{\theta}}}d\theta \\ &= \int_{0}^{\frac{\pi}{6}}\frac{\sin^{2}{\theta}\cos{\theta}}{\cos{\theta}}d\theta \\ &= \int_{0}^{\frac{\pi}{6}}\sin^{2}\theta d\theta
\end{align*}$$
3. && Use trigonometric identity $\sin^{2}{\theta} = \frac{1}{2} - \frac{\cos{2\theta}}{2}$ to rewrite integrand.  
$$\int_{0}^{\frac{\pi}{6}}\sin^{2}{\theta}d\theta = \int_{0}^{\frac{\pi}{6}}\frac{1}{2}-\frac{\cos{2\theta}}{2}d\theta$$ 
4. && Evaluate definite integral.
$$\begin{align*}
\int_{0}^{\frac{\pi}{6}} \frac{1}{2}-\frac{\cos{2\theta}}{2}d\theta &= \left.\left[\frac{\theta}{2}-\frac{\sin{2\theta}}{4}\right]\right|^{\frac{\pi}{6}}_{0} \\
&= \frac{\pi}{12}-\frac{\sin{\frac{\pi}{3}}}{4} \\ &= \frac{\pi}{12}-\frac{\sqrt{3}}{8}
\end{align*}$$

#### 07
Compute the integral: $$\int \tan^{3}{x}\sec^{2}{x}dx$$
- (a) Using $du = \sec^{2}xdx$
- (b) Using $du = \sec{x}\tan{x}dx$ 

**Solution**
(a)
1. & Identify $u$ given $du$.
$$ du = \sec^{2}{x}dx \quad ⨠⨠\quad u = \tan{x}$$
2. & Perform $u$-substitution
$$\int \tan^{3}x\sec^{2}{x}dx = \int u^{3}du$$
3. & Compute integral using power rule.
$$\int u^{3}du = \frac{u^{4}}{4}+C, \quad C \in \mathbb{R}$$
4. & Substitute back $u = \tan{x}$
$$\frac{u^{4}}{4} + C = \frac{\tan^{4}{x}}{4}+C, \quad C \in \mathbb{R}$$
(b)
1. & Identify $u$ given $du$
$$du = \sec{x}\tan{x}dx \quad ⨠⨠ \quad u = \sec{x}$$
2. && Rewrite integrand as product of $du$.
$$ \int \tan^{3}{x}\sec^{2}xdx = \int \tan^{2}{x}\sec{x}(\sec{x}\tan{x})dx$$
3. && Rewrite $\tan^{2}{x}$ as $\sec^{2}{x}-1$ using the Pythagorean trigonometric identity.
$$\int \tan^{2}{x}\sec{x}(\sec{x}\tan{x})dx = \int \left(\sec^{2}{x}-1\right)\sec{x}(\sec{x}\tan{x})dx$$
4. & Perform $u$-substitution.
$$\int \left(\sec^{2}{x}-1\right)\sec{x}(\sec{x}\tan{x})dx = \int\left(u^{2}-1\right)udu$$
5. & Compute integral.
$$\begin{align*}
\int \left(u^{2}-1\right)udu &= \int u^{3}-udu \\ &= \frac{u^{4}}{4}-\frac{u^{2}}{2}+C, \quad C \in \mathbb{R}
\end{align*}$$
6. & Substitute back $u = \sec{x}$
$$\frac{u^{4}}{4}-\frac{u^{2}}{2} +C = \frac{\sec^{4}{x}}{4}-\frac{\sec^{2}{x}}{2}+C, \quad C \in \mathbb{R}$$

#### 08
Compute the integral: $$\int \sin{7x}\sec^{5}{7x}dx$$
1. & Perform $u$-substitution $u = 7x$.
    - $du = 7dx$
    $$\int \sin{7x}\sec^{5}{7x}dx = \frac{1}{7}\int\sin{u}\sec^{5}{u}du$$
2. && Rewrite integrand as product of $\tan{u}$
$$\begin{align*}
\frac{1}{7}\int \sin{u}\sec^{5}{u}du &= \frac{1}{7}\int \frac{\sin{u}}{\cos{u}}\sec^{4}{u}du \\ &= \frac{1}{7}\int \tan{u}\sec^{4}u du
\end{align*}$$
3. && Perform substitution $v = \sec{u}$
    - $dv = \sec{u}\tan{u}du$
    $$\frac{1}{7}\int \tan{u}\sec^{4}udu = \frac{1}{7}\int v^{3}dv$$
4. & Compute integral
$$\frac{1}{7}\int v^{3}dv = \frac{v^{4}}{28} + C, \quad C \in \mathbb{R}$$
5. & Substitute back $v = \sec{u} = \sec{7x}$
$$\frac{v^{4}}{28} + C = \frac{\sec^{4}{7x}}{28} + C, \quad C \in \mathbb{R}$$

#### 12
Compute the definite integral: $$\int_{0}^{\frac{\pi}{2}}\frac{\cos{x}}{\sqrt{1+\sin^{2}{x}}}dx$$

**Solution**
1. && Perform $u$-substitution $u = \sin{x}$.
    - $du = \cos{x}dx$
    - Adjust bounds:
    $$\begin{align*}
    x &= 0 \quad ⨠⨠ \quad u = 0 \\ x &= \frac{\pi}{2} \quad ⨠⨠ \quad u = 1
    \end{align*}$$
    - Rewrite integral:
    $$\int_{0}^{\frac{\pi}{2}}\frac{\cos{x}}{\sqrt{1+\sin^{2}{x}}}dx =\int_{0}^{1}\frac{1}{\sqrt{1+u^{2}}}du$$
2. &&& Perform substitution $u = \tan{\theta}$. Draw a right triangle with the length of the hypotenuse being $\sqrt{1+u^{2}}$ and opposite being $u$ for reference.
    - $du = \sec^{2}{\theta}d\theta$ 
    - Adjust bounds:
    $$\begin{align*}
    u &= 0 \quad ⨠⨠ \quad \theta = 0 \\ u &= 1 \quad ⨠⨠ \quad \theta =\frac{\pi}{4}
    \end{align*}$$
    - Rewrite integral:
    $$\int_{0}^{1}\frac{1}{\sqrt{1+u^{2}}}du = \int_{0}^{\frac{\pi}{4}}\frac{\sec^{2}{\theta}}{\sqrt{1+\tan^{2}{\theta}}}d\theta$$
3. && Use Pythagorean identity $1 + \tan^{2}{\theta} = \sec^{2}{\theta}$ to rewrite integrand.
$$\begin{align*}\int_{0}^{\frac{\pi}{4}}\frac{\sec^{2}{\theta}}{\sqrt{1+\tan^{2}{\theta}}}d\theta &= \int_{0}^{\frac{\pi}{4}}\frac{\sec^{2}{\theta}}{\sqrt{\sec^{2}{\theta}}}d\theta \\ &= \int_{0}^{\frac{\pi}{4}}\frac{\sec^{2}{\theta}}{\sec{\theta}}d\theta \\ &= \int_{0}^{\frac{\pi}{4}}\sec{\theta}d\theta\end{align*}$$
4. &&& Multiply integrand by $\frac{\sec{\theta} + \tan{\theta}}{\sec{\theta} + \tan{\theta}} = 1$
$$\begin{align*}
\int_{0}^{\frac{\pi}{4}}\sec{\theta}d\theta &= \int_{0}^{\frac{\pi}{4}}\sec{\theta}\left(\frac{\sec{\theta}+\tan{\theta}}{\sec{\theta} + \tan{\theta}}\right)d\theta \\
&= \int_{0}^{\frac{\pi}{4}}\frac{\sec^{2}{\theta+\sec{\theta}\tan{\theta}}}{\sec{\theta}+\tan{\theta}}d\theta
\end{align*}$$
5. &&& Use rule that $\int \frac{f'(x)}{f(x)} = \ln{\left|f(x)\right|} +C$. (If not immediately evident to you, use substitution $v = \sec{\theta} + \tan{\theta}$, same thing).
$$\int_{0}^{\frac{\pi}{4}}\frac{\sec^{2}{\theta}+\sec{\theta}\tan{\theta}}{\sec{\theta}+\tan{\theta}}d\theta = \left.\ln{\left|\sec{\theta}+\tan{\theta}\right|}\right|^{\frac{\pi}{4}}_{0}$$
6. & Evaluate expression.
$$\begin{align*}
\left.\ln{\left|\sec{\theta} + \tan{\theta}\right|}\right| &= \ln\left|\sec{\frac{\pi}{4}} + \tan{\frac{\pi}{4}}\right| - \ln{\left|\sec{0}+\tan{0}\right|} \\ &= \ln{\left|1+\sqrt{2}\right|} - \ln{\left|1\right|} \\ &= \ln{|1 + \sqrt{2}}|
\end{align*}$$


#### 13
A charged wire lies on the $x$-axis running from $x_{1}$ to $x_{2}$. The electric field at the point $p = (0, h)$ is given by: $$E = \int_{x_{1}}^{x_{2}}\frac{k\lambda h}{\left(x^{2}+h^{2}\right)^{\frac{3}{2}}}dx$$
Find the numerical value of $E$ assuming $\lambda = 6.0 \times 10^{-4}$ and $k = 8.99 \times 10^{9}$ and $h = 3$ and $\left(x_{1},x_{2}\right) = (-15, 15)$.  

**Solution**
1. & Take constants outside of integral.
$$\int_{x_{1}}^{x_{2}}\frac{k\lambda h}{\left(x^{2}+h^{2}\right)^{\frac{3}{2}}}dx = k\lambda h\int_{x_{1}}^{x_{2}}\frac{dx}{\left(x^{2}+h^{2}\right)^{\frac{3}{2}}}$$
2. & Substitute given values inside integral: $h = 3$, $\left(x_{1}, x_{2}\right) = (-15, 15)$
$$k\lambda h \int_{x_{1}}^{x_{2}}\frac{dx}{\left(x^{2}+h^{2}\right)^{\frac{3}{2}}} = k\lambda h\int_{-15}^{15}\frac{dx}{\left(x^{2}+9\right)^{\frac{3}{2}}}$$
3. &&& Use substitution $x = 3\tan{\theta}$. Draw right triangle with hypotenuse having length $x^{2} + 9$ and opposite having length $x$ for reference.
    - $dx = 3\sec^{2}{\theta}d\theta$
    - Adjust bounds: 
    $$\begin{align*}x &= -15 \quad ⨠⨠ \quad \theta = \tan^{-1}{\left(-5\right)} \\ x &= 15 \quad ⨠⨠ \quad \theta = \tan^{-1}(5)\end{align*} $$
    - Rewrite integral
    $$k\lambda h\int_{-15}^{15}\frac{dx}{\left(x^{2}+9\right)^{\frac{3}{2}}} = k\lambda h\int_{\tan^{-1}{(-5)}}^{\tan^{-1}{(5)}}\frac{3\sec^{2}\theta}{\left(9\tan^{2}\theta+9\right)^{\frac{3}{2}}}d\theta$$
4. && Use Pythagorean identity $\tan^{2}\theta + 1 = \sec^{2}{\theta}$ to simplify integral.
$$\begin{align*}k\lambda h\int_{\tan^{-1}{(-5)}}^{\tan^{-1}{(5)}}\frac{3\sec^{2}\theta}{\left(9\tan^{2}\theta+9\right)^{\frac{3}{2}}}d\theta &= k\lambda h \int_{\tan^{-1}{(-5)}}^{\tan^{-1}{(5)}}\frac{3\sec^{2}{\theta}}{\left(9\left(\tan^{2}{\theta}+1\right)^{\frac{3}{2}}\right)}d\theta \\ &= k\lambda h \int_{\tan^{-1}(-5)}^{\tan^{-1}{(5)}}\frac{3\sec^{2}\theta}{9^{\frac{3}{2}}\left(\sec^{2}{\theta}\right)^{\frac{3}{2}}}d\theta \\ &= k\lambda h \int_{\tan^{-1}{(-5)}}^{\tan^{-1}(5)} \frac{3\sec^{2}{\theta}}{27\sec^{3}{\theta}}d\theta \\ &= \frac{k\lambda h}{9} \int_{\tan^{-1}(-5)}^{\tan^{-1}(5)}\cos{\theta}d\theta\end{align*}$$
5. & Evaluate integral. Plug back in given values for $k$, $\lambda$, and $h$.
$$\begin{align*}\frac{k\lambda h}{9} \int_{\tan^{-1}(-5)}^{\tan^{-1}(5)}\cos{\theta}d\theta &= \left.\frac{k\lambda h}{9} \sin{\theta}\right|^{\tan^{-1}(5)}_{\tan^{-1}(-5)} \\ &= \frac{k\lambda h}{9}\left[\sin{\left(\tan^{-1}(5)\right)-\sin{\left(\tan^{-1}(-5)\right)}}\right] \\ &= \frac{k\lambda h}{9}\left[\sin{\left(\tan^{-1}(5)\right)+\sin{\left(\tan^{-1}(5)\right)}}\right] \\ &= \frac{\left(6\times10^{-4}\right)\left(8.99 \times 10^{9}\right)}{3}\left[2\sin{\left(\tan^{-1}(5)\right)}\right] \\ &= \frac{\left(6\times10^{-4}\right)\left(8.99 \times 10^{9}\right)}{3} \left(\frac{10}{\sqrt{26}}\right) \\ &= \frac{\left(6\times10^{-3}\right)\left(8.99 \times 10^{10}\right)}{3\sqrt{26}}\end{align*} $$ 
