---
title: Complex Logarithm
source: https://algebrica.org/complex-logarithm/
license: CC BY-NC 4.0
tags:
  - branch-cut
  - complex-argument
  - complex-exponential
  - complex-logarithm
  - complex-numbers
  - principal-logarithm
---
## Definition and properties

A complex logarithm of a [complex number](../complex-numbers/) $z \neq 0$ is a number $w\in\mathbb{C}$ that satisfies the equation:

$$e^w=z \tag{1}$$

Recall that over the [real numbers](../real-numbers/), the [natural logarithm](../logarithms/) is the [inverse](../inverse-function/) of the [exponential function](../exponential-function/), which is a bijection from $\mathbb{R}$ to $(0,\infty).$ Thus every positive real number has a unique real logarithm. The situation is more complicated over the complex numbers because the complex exponential is [periodic](../functions/) and the following identity holds for every $w\in\mathbb{C}$ and every $k\in\mathbb{Z}$:

$$e^{w+2k\pi i}=e^w \tag{2}$$

It follows from $(2)$ that if $w$ is a solution of $(1),$ then so is $w+2k\pi i$ for every $k\in\mathbb{Z}.$ To find all the solutions of $(1),$ we therefore write $w=u+iv$ with $u,v\in\mathbb{R}$ and $z=re^{i\theta},$ where $r=|z|$ and $\theta$ is an argument of $z.$ [Euler's formula](../eulers-formula/) gives:

$$e^w=e^{u+iv}=e^u(\cos v+i\sin v) \tag{3}$$

Comparing $(3)$ with the [exponential form](../complex-numbers-exponential-form/) of $z$ shows that $(1)$ holds if and only if the moduli are equal, so that $e^u=r,$ and the arguments differ by an integer multiple of $2\pi,$ so that $v=\theta+2k\pi$ for some $k\in\mathbb{Z}.$ Since $r>0,$ the real equation $e^u=r$ gives $u=\ln r.$ The set of complex logarithms of $z$ is therefore given by:

$$\log z:=\{\ \ln|z|+i(\theta+2k\pi)\mid k\in\mathbb{Z}\ \} \tag{4}$$

Geometrically, the logarithms in $(4)$ all lie on the vertical line in the complex plane with real coordinate $\ln|z|,$ and consecutive values are $2\pi$ apart.

- - -

For $z\neq0,$ the principal logarithm $\mathrm{Log}(z)$ is the value in $(4)$ obtained by choosing $\mathrm{Arg}(z),$ the unique argument of $z$ in $(-\pi,\pi]:$

$$\mathrm{Log}(z):=\ln|z|+i\mathrm{Arg}(z) \tag{5}$$

Equation $(5)$ gives a single value, while $\log z$ denotes the set of all logarithms of $z.$ For $x>0$ we have $\mathrm{Arg}(x)=0$ and $\mathrm{Arg}(-x)=\pi,$ so:

$$
\begin{align}
\mathrm{Log}(x)&=\ln x \notag\\[6pt]
\mathrm{Log}(-x)&=\ln x+i\pi \tag{6}
\end{align}
$$

By $(6),$ the principal logarithm agrees with the natural logarithm on the positive real axis. For example, the complex number $z=-\sqrt{3}-i$ lies in the third quadrant and has the following modulus and principal argument:

$$
\begin{aligned}
|z|&=\sqrt{(-\sqrt{3})^2+(-1)^2}=2\\[6pt]
\mathrm{Arg}(z)&=-\frac{5\pi}{6}
\end{aligned} \tag{7}
$$

Substituting the values from $(7)$ into $(5)$ gives:

$$\mathrm{Log}(-\sqrt{3}-i)=\ln 2-\frac{5\pi i}{6} \tag{8}$$

Using $(4),$ we obtain the full set of complex logarithms:

$$\log(-\sqrt{3}-i)=\left\{\ \ln 2+i\left(-\frac{5\pi}{6}+2k\pi\right)\mid k\in\mathbb{Z}\ \right\} \tag{9}$$

Setting $k=0$ in $(9)$ gives the principal logarithm in $(8).$ For every $z\neq0,$ the principal logarithm is a solution of $(1),$ so:

$$e^{\mathrm{Log}(z)}=z \tag{10}$$

If we reverse the order of the operations in $(10),$ then $(5)$ selects the logarithm whose imaginary part lies in $(-\pi,\pi].$ We therefore recover $w$ exactly when its imaginary part already lies in that interval:

$$\mathrm{Log}(e^w)=w \quad\Longleftrightarrow\quad -\pi<\mathrm{Im}(w)\leq\pi \tag{11}$$

The restriction in $(11)$ can be seen by taking $w=2\pi i,$ for which $e^w=1$ and $\mathrm{Log}(1)=0.$

- - -

We now look at the main properties of the complex logarithm, beginning with the logarithm of a [product](../complex-number-operations/). For two nonzero complex numbers $z_1$ and $z_2,$ the following relation holds:

$$\log(z_1z_2)=\log z_1+\log z_2 \tag{12}$$

Equation $(12)$ is an equality of [sets](../sets/), so the right-hand side contains every sum formed by adding a logarithm of $z_1$ to a logarithm of $z_2.$ If $\theta_1$ and $\theta_2$ are arguments of the two factors, then $(4)$ gives all sums of the following form as $k$ ranges over $\mathbb{Z}:$

$$\ln|z_1|+\ln|z_2|+i(\theta_1+\theta_2+2k\pi) \tag{13}$$

For the principal logarithm, we have instead:

$$\mathrm{Log}(z_1z_2)=\mathrm{Log}(z_1)+\mathrm{Log}(z_2)-2m\pi i \tag{14}$$

In $(14),$ the [integer](../integers/) $m$ is determined by requiring $\mathrm{Arg}(z_1)+\mathrm{Arg}(z_2)-2m\pi$ to lie in $(-\pi,\pi].$
