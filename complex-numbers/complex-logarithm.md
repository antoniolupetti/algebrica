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
## Definition

The [real exponential](../exponential-function/) is a [bijection](../functions/) from $\mathbb{R}$ to $(0,\infty),$ and its [inverse function](../inverse-function/) is the real logarithm. The [complex exponential](../eulers-formula/) has period $2\pi i,$ so it is not injective on $\mathbb{C}.$ For every $w\in\mathbb{C}$ and every [integer](../integers/) $k\in\mathbb{Z},$ we have:

$$e^{w+2k\pi i}=e^w$$

Two complex numbers that differ by an integer multiple of $2\pi i$ have the same exponential. Fix a nonzero [complex number](../complex-numbers/) $z.$ Every solution $w\in\mathbb{C}$ of the following equation is called a complex logarithm of $z:$

$$e^w=z$$

To solve this equation, write $w=u+iv$ with $u,v\in\mathbb{R},$ and write $z$ in [exponential form](../complex-numbers-exponential-form/) as $z=re^{i\theta},$ where $r=|z|>0$ and $\theta$ is one argument of $z.$ The exponential of $w$ is:

$$e^w=e^{u+iv}=e^u(\cos v+i\sin v)$$

The equality $e^w=z$ holds exactly when $e^u=r$ and $v=\theta+2k\pi$ for some $k\in\mathbb{Z}.$ Since $e^u=r,$ we have $u=\ln r.$ The complete [set](../sets/) of logarithms of $z$ is:

$$\log z:=\{\ \ln|z|+i(\theta+2k\pi)\mid k\in\mathbb{Z}\ \}$$

Choosing another argument $\theta+2m\pi$ does not change this set, because the index $k$ then shifts by the integer $m.$ All logarithms of a fixed $z$ have real part $\ln|z|,$ and their imaginary parts differ by integer multiples of $2\pi.$ In the complex plane they lie on the vertical line whose real coordinate is $\ln|z|,$ equally spaced at distance $2\pi.$

For every finite $u,$ the [modulus](../complex-numbers/) $|e^{u+iv}|=e^u$ is positive. The complex exponential never vanishes, so the number $0$ has no complex logarithm.

## The principal logarithm

A standard single-valued choice uses the [principal argument](../complex-numbers/). For $z\neq0,$ the number $\mathrm{Arg}(z)$ is the unique argument in the interval $(-\pi,\pi].$ The principal logarithm is:

$$\mathrm{Log}(z):=\ln|z|+i\mathrm{Arg}(z)$$

The capitalized notation $\mathrm{Log}$ is the selected value, while the lowercase notation $\log z$ is the full set. On the positive real axis the definition agrees with the real [natural logarithm](../logarithms/). If $x>0,$ then $\mathrm{Arg}(x)=0$ and $\mathrm{Arg}(-x)=\pi,$ so the corresponding principal values are:

$$\mathrm{Log}(x)=\ln x,\qquad \mathrm{Log}(-x)=\ln x+i\pi$$

The number $z=-\sqrt{3}-i$ is in the third quadrant. Its modulus and principal argument are:

$$
\begin{align}
|z|&=\sqrt{(-\sqrt{3})^2+(-1)^2}=2\\[6pt]
\mathrm{Arg}(z)&=-\frac{5\pi}{6}
\end{align}
$$

Its principal logarithm is:

$$\mathrm{Log}(-\sqrt{3}-i)=\ln 2-\frac{5\pi i}{6}$$

All logarithms of $-\sqrt{3}-i$ are:

$$\log(-\sqrt{3}-i)=\left\{\ \ln 2+i\left(-\frac{5\pi}{6}+2k\pi\right)\mid k\in\mathbb{Z}\ \right\}$$

The value for $k=0$ is principal, and every other value differs from it by $2k\pi i.$

- - -

The principal logarithm is a right inverse of the exponential on nonzero complex numbers:

$$e^{\mathrm{Log}(z)}=z$$

The inverse identity in the other order holds only on a horizontal strip. If $w=x+iy,$ let $k$ be the unique integer for which $-\pi<y-2k\pi\leq\pi.$ Then:

$$\mathrm{Log}(e^w)=w-2k\pi i$$

The equality $\mathrm{Log}(e^w)=w$ holds exactly when $-\pi<\mathrm{Im}(w)\leq\pi.$ On this half-open horizontal strip, the principal logarithm is the inverse of the exponential.

## Logarithmic branches and branch cuts

Let $U$ be a connected open subset of $\mathbb{C}^{*}:=\mathbb{C}\setminus\{\ 0\ \}.$ A logarithmic branch on $U$ is a [continuous function](../continuous-functions/) $L:U\to\mathbb{C}$ such that the following identity holds for every $z\in U:$

$$e^{L(z)}=z$$

No logarithmic branch exists on the whole punctured plane $\mathbb{C}^{*}.$ If such a branch $L$ existed, the parametrization of the [unit circle](../unit-circle/) by $z=e^{it},$ with $0\leq t\leq2\pi,$ would define the continuous function:

$$h(t):=L(e^{it})-it$$

For every $t,$ one has $e^{h(t)}=1,$ so $h(t)$ belongs to the discrete set $2\pi i\mathbb{Z}.$ A continuous function from an interval into a discrete set is constant. Both endpoints of the path are the point $1,$ because $e^0=e^{2\pi i}=1,$ but:

$$h(0)=L(1),\qquad h(2\pi)=L(1)-2\pi i$$

The two values differ by $2\pi i,$ which contradicts constancy. Along one circuit of the unit circle, a continuous argument changes by $2\pi,$ although the starting and ending point are both $1.$

- - -

A branch cut is a deleted curve that prevents such a circuit. After a ray from the origin to infinity has been removed, the remaining plane has a continuous choice of argument. Fix an angle $\beta$ and remove the ray:

$$R_{\beta}:=\{\ re^{i\beta}\mid r\geq0\ \}$$

Every point of $\mathbb{C}\setminus R_{\beta}$ has a unique argument $\mathrm{Arg}_{\beta}(z)$ in the interval $(\beta,\beta+2\pi).$ The branch for this interval is:

$$L_{\beta}(z):=\ln|z|+i\mathrm{Arg}_{\beta}(z)$$

For $\beta=-\pi,$ the removed ray is the non-positive real axis and the selected angles are in $(-\pi,\pi).$ This branch is the principal branch on:

$$\mathbb{C}\setminus(-\infty,0]$$

The principal value $\mathrm{Log}(z)$ is defined pointwise on every $z\neq0,$ including negative real numbers. Its restriction to the cut plane is continuous and complex differentiable, so this restriction is the principal branch. On the whole punctured plane $\mathbb{C}^{*},$ the principal value is not a logarithmic branch.

For a fixed $x<0,$ the values on opposite sides of the cut have the limits:

$$
\begin{align}
\lim_{y\to0^+}\mathrm{Log}(x+iy)&=\ln|x|+i\pi\\[6pt]
\lim_{y\to0^-}\mathrm{Log}(x+iy)&=\ln|x|-i\pi
\end{align}
$$

The jump across the negative real axis is $2\pi i.$ With a different branch cut, the jump is on a different curve. No [domain](../determining-the-domain-of-a-function/) of a single-valued branch can contain a closed path that winds a nonzero number of times around the origin.

If $L_1$ and $L_2$ are two branches on the same connected domain, their difference has values in $2\pi i\mathbb{Z},$ because $e^{L_1(z)-L_2(z)}=1.$ The difference is continuous, and the domain is connected, so it is constant. This constant has the form $2m\pi i$ for some fixed integer $m:$

$$L_1(z)-L_2(z)=2m\pi i$$

## Logarithmic identities and their restrictions

For the multivalued logarithm, the product law is an equality of sets. For nonzero $z_1$ and $z_2,$ one has:

$$\log(z_1z_2)=\log z_1+\log z_2$$

The right-hand side is the set of all sums of one logarithm of each factor. If $\theta_1$ and $\theta_2$ are arguments of $z_1$ and $z_2,$ these sums have the form:

$$\ln|z_1|+\ln|z_2|+i(\theta_1+\theta_2+2k\pi)$$

Since $|z_1z_2|=|z_1||z_2|$ and $\theta_1+\theta_2$ is an argument of $z_1z_2,$ these are exactly the logarithms of the product.

For principal values, the same formula can fail because the sum of two principal arguments can leave $(-\pi,\pi].$ The correct formula is:

$$\mathrm{Log}(z_1z_2)=\mathrm{Log}(z_1)+\mathrm{Log}(z_2)-2m\pi i$$

The integer $m$ is the unique member of $\{\ -1,0,1\ \}$ for which $\mathrm{Arg}(z_1)+\mathrm{Arg}(z_2)-2m\pi$ is in $(-\pi,\pi].$ The product law has no correction when:

$$-\pi<\mathrm{Arg}(z_1)+\mathrm{Arg}(z_2)\leq\pi$$

For example, $\mathrm{Log}(-1)=i\pi$ and $(-1)(-1)=1.$ The two sides are:

$$
\begin{align}
\mathrm{Log}((-1)(-1))&=\mathrm{Log}(1)=0\\[6pt]
\mathrm{Log}(-1)+\mathrm{Log}(-1)&=2\pi i
\end{align}
$$

The two expressions differ by $2\pi i.$ The [quotient law](../complex-number-operations/) and the formula for the principal logarithm of an [integer power](../de-moivre-theorem/) have analogous correction terms in $2\pi i\mathbb{Z}.$ Before applying a real logarithm law to principal complex logarithms, one must check whether the selected arguments cross the branch cut.

## Derivative and local power series

Every logarithmic branch on an open domain is complex differentiable. Fix a point $z_0$ in the domain of $L.$ The [derivative](../derivatives/) of the exponential at $L(z_0)$ is $e^{L(z_0)}=z_0\neq0.$ By the local [inverse function theorem](../inverse-function/), the exponential is injective on some neighborhood $V$ of $L(z_0),$ and its inverse on the image of $V$ is complex differentiable. Since $L$ is continuous, a sufficiently small neighborhood $W$ of $z_0$ is contained in this image and has $L(W)\subseteq V.$ For each $z\in W,$ both $L(z)$ and the local inverse are in $V$ and have exponential $z,$ so they are equal. Hence $L$ is complex differentiable near every point of its domain.

Differentiating the identity $e^{L(z)}=z$ with the [chain rule](../chain-rule/), we have:

$$
\begin{align}
e^{L(z)}L'(z)&=1\\[6pt]
zL'(z)&=1\\[6pt]
L'(z)&=\frac{1}{z}
\end{align}
$$

The derivative is independent of the branch because two branches on a connected domain differ by a constant multiple of $2\pi i.$

Near $z=1,$ the principal branch has a [power series](../power-series/). For $|u|<1,$ the [geometric series](../geometric-series/) for $1/(1+u)$ converges. Its termwise antiderivative with value $0$ at $u=0$ is $\mathrm{Log}(1+u):$

$$\mathrm{Log}(1+u)=\sum_{n=1}^{\infty}(-1)^{n+1}\frac{u^n}{n}=u-\frac{u^2}{2}+\frac{u^3}{3}-\frac{u^4}{4}+\cdots$$

The condition $|u|<1$ means that $1+u$ is in the open disk centered at $1$ with radius $1.$ This disk contains neither the origin nor any point of the branch cut, so the sum of the series is $\mathrm{Log}(1+u)$ throughout the disk.

## Connection with complex powers

Once a logarithmic branch $L$ has been fixed on a domain $U,$ the corresponding [power](../powers/) for $a\in\mathbb{C}$ and $z\in U$ is:

$$z^a:=e^{aL(z)}$$

If $L$ is replaced by the branch $L+2k\pi i,$ the value is multiplied by $e^{2k\pi ia}.$ When $a$ is an integer, this factor is $1,$ so the value is independent of the branch. For a general complex exponent, the power can have different values on different branches.

For $i^i,$ all logarithms of $i$ are:

$$\log i=\left\{\ i\left(\frac{\pi}{2}+2k\pi\right)\mid k\in\mathbb{Z}\ \right\}$$

The corresponding values of $i^i$ are:

$$i^i=\left\{\ e^{-\pi/2-2k\pi}\mid k\in\mathbb{Z}\ \right\}$$

Every value in this set is a positive real number. For the principal logarithm, $k=0,$ so the principal value of $i^i$ is $e^{-\pi/2}.$
