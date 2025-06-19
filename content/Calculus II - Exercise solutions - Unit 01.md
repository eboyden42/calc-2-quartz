---
title: Exercise solutions - Unit 01
---
## Volume using cylindrical shells
#### 02 - Revolution of a sinusoid
1. && Set up the integral for shells.
    - Integration variable: $r=x$, the distance of a shell to the $y$-axis.
    - Then $dr=dx$ and $h=\sin x$, the height of a shell.
    - Bounds: one hump is given by $x\in[0,\pi]$.
    - Thus: $$V=\int_0^\pi 2\pi x\sin x\,dx$$

2. &&& Perform the integral using IBP.
    - Choose $u=2\pi x$ and $v'=\sin x$ since $x$ is A and $\sin x$ is T.
    - Then $u'=2\pi$ and $v=-\cos x$.
    - ! Recall IBP formula: 
      $$\int uv'\,dx=uv-\int u'v\,dx$$
    - Insert data in IBP formula: $$\int_0^\pi 2\pi x\sin x\,dx\quad ⨠⨠ \quad (2\pi x)(-\cos x)\Big|_0^\pi - \int_0^\pi 2\pi(-\cos x)\,dx$$
    - Compute first term: $$-2\pi x\cos x\Big|_0^\pi\quad ⨠⨠ \quad -2\pi(\pi)(-1)--2\pi(0)(+1)\quad ⨠⨠ \quad 2\pi^2$$
    - Compute integral term: $$-\int_0^\pi 2\pi(-\cos x)\,dx\quad ⨠⨠ \quad 2\pi\sin\Big|_0^\pi\quad ⨠⨠ \quad 0$$
    - So the answer is $2\pi^2$.


## Integration by parts
#### 04 - Hidden A
1. & Choose $u=\ln x$.
    - Because Log is farthest right in LIATE.
    - It follows that we must choose $v'(x)=1$.

2. && Compute $u'$ and $v$.
    - We have $u'=\frac{1}{x}$ and $v=x$.
    - Obtain chart: $$\begin{array}{c|c}u=\ln x&v'=1\\\hline u'=1/x&v=x\end{array} \begin{array}{l}\quad\longrightarrow\quad\int u\cdot v'\qquad\text{original} \\ \quad\longrightarrow\quad\int u'\cdot v\qquad\text{final} \end{array}$$
3. && Plug into IBP formula.
    - Plug in all data: $$\int \ln x\cdot 1\,dx = x\ln x-\int \frac{1}{x}\cdot x\,dx$$
    - Integrate: $$-\int \frac{1}{x}\cdot x\,dx\quad ⨠⨠ \quad -\int 1\,dx\quad ⨠⨠ \quad -x+C$$
    - Final answer is: $\;x\ln x - x + C$
