<!-- toc -->
# Complex Analysis

# complex number $\mathbb C$

$z=(x,y)$ in complex plane where $x,y\in\R$

- real part, $x=\text{Re}z$
- imaginary part, $y=\text{Im}z$

## complex plane

- real axis/ imaginary axis
- $(0,y)$ pure imaginary number, $y≠0$

## binary operation of complex number

- addition, $(x_1,y_1)+(x_2,y_2)=(x_1+x_2,y_1+y_2)$
- multiplication, $(x_1,y_1)\cdot(x_2,y_2)=(x_1x_2-y_1y_2,x_1y_2+x_2y_1)$

## complex number short syntax

$(x,y)=(x,0)+(0,y)=(x,0)+(0,1)\cdot(y,0)=:x+iy$

where $i:=(0,1)$

## Argand diagram

diagram in $\R^2$ given by

$$
x+iy\mapsto x\vec i+y\vec j
$$

- modulus, $=$ Euclidean length in Argand diagram

    $$
    |z|=\sqrt{x^2+y^2}
    $$

- triangle inequality hold

## complex conjugation

$\bar z=x-iy$

- $\bar{\bar z}=z$
- $|\bar z|=|z|$
- $\overline{z_1+z_2}=\bar z_1+\bar z_2$
- $\overline{z_1z_2}=\bar z_1\bar z_2$
- $x=\frac{z+\bar z}{2},\quad y=\frac{z-\bar z}{2i}$
- $|z|^2=z\bar z$

## Euler's formula

$$
e^{i\theta}=\cos\theta+i\sin\theta\\[12pt] ⇒
x+iy=re^{i\theta}
$$

- $r=|z|$
- $\theta=\arg z$, argument of $z$
    - $-\pi<\text{Arg }z≤\pi$, principal argument of $z$
- $z_1z_2=r_1r_2e^{i(\theta_1+\theta_2)}$
    - $\arg(z_1z_2)=\arg z_1+\arg z_2$
- $z^{-1}=\frac{1}{r}e^{-i\theta}$
- $\bar z=re^{-i\theta}$

### de Moivre's formula

$$
(\cos\theta+i\sin\theta)^n=e^{in\theta}=\cos n\theta+i\sin n\theta
$$

## complex root

$z_0=r_0e^{i\theta_0}$

$n$th root of $z_0$

$$
z^n=z_0\\[12pt] ⇒
z_k=\sqrt[n]{r_0}e^{i \left(
    \frac{\theta_0+2\pi k}{n}
\right)},\qquad
k\in\{0,1,\cdots,n-1\}
$$

- $n$ distinct root
- principal root, when $\theta_0=\text{Arg }z_0,k=0$

## standard topology $\mathcal O_s$

see context in [Topology](topology.md)

$\varepsilon>0$

open $\varepsilon$-neighborhood

$$
U_\varepsilon(z_0)=\{z\in\mathbb C:|z=z_0|<\varepsilon\}
\in\mathcal O_s
$$

## region

nonempty connected set

- domain, open region

### connectedness

$D ⊆ \mathbb C$ is connected $⇔$

$∀\ z_1,z_2\in D,∃$ polygonal line with finitely many segment
between $z_1$, $z_2$

### bounded

$∃$ circle of finite radius containing the set

## complex infinity

$x → ∞$ or $y → ∞$

## Riemann sphere $\mathbb S$

$$
x^2+y^2+z^2=1
$$

intersection of the sphere with line through north poll and complex number

- north poll: $(0,0,1)$, correspond to complex infinity
- Argand plane $(x,y,0)$

# limit

$$
\lim_{z → z_0}f(z)=w_0
$$

$⇔ ∀\ \varepsilon>0,\ ∃\ \delta>0$ s.t.

$$
|f(z)-w_0|<\varepsilon\text{ whenever }|z-z_0|<\delta
$$

- unique if exist
- independent of direction of approach

## connection between complex limit and real limit

$f(z)=u(x,y)+iv(x,y)$

$$
\lim_{z → z_0}f(z)=
\lim_{(x,y) → (x_0,y_0)}u(x,y)+\lim_{(x,y) → (x_0,y_0)}v(x,y)
$$

$⇔$ limit on the RHS exist

# continuity

$f$ is continuous at $z_0 ⇔$

1. $f$ exist
1. $\lim_{z → z_0}f(z)$ exist
1. $$
    \lim_{z → z_0}f(z)=f(z_0)
    $$

# differentiation

$f:D → \mathbb C,U_\varepsilon(z_0) ⊆ D$

$f$ differentiable at $z_0 ⇔$

$$
\lim_{z → z_0}\frac{f(z)-f(z_0)}{z-z_0}
$$

exist

- $f(z)$ depend on $\bar z ⇒ f$ not differentiable
- $u,v$ differentiable $\not ⇒ f$ differentiable

## Cauchy-Riemann equations

$f'(z)$ exist at $z_0 ⇒$

$$
u_x=v_y,\qquad
u_y=-v_x\\[12pt]
f'=u_x+iv_x
$$

### Cauchy-Riemann equations in polar coordinate

$f(r,\theta)=u(r,\theta)+iv(r,\theta)$

$$
ru_r=v_\theta,\qquad
u_\theta=-rv_r\\[12pt]
f'=e^{-i\theta}(u_r+iv_r)
$$

### differentiability from Cauchy-Riemann equations

at $z_0$

1. $u_x,u_y,v_x,v_y$ are continuous
1. satisfy Cauchy-Riemann equations

$$
⇒ f'=u_x+iv_x
$$

exist

## holomorphicity

$f:D → \mathbb C$ holomorphic at $z_0 ⇔$

$f$ differentiable at each point in $U_\varepsilon(z_0) ⊆ D$

- a.k.a. analytic/ regular
- $u,v\in C^∞(D)$ and are harmonic function in $D$

### entire function

holomorphic at every finite point

### singularity

$z_0$ is singularity $⇔$

$f$ holomorphic in $\hat U_\varepsilon(z_0)$ and not at $z_0$

### constancy from holomorphicity

$f$ holomorphic, in $D$

$f$ is constant

$⇔ f'=0$

$⇔ \bar f$ holomorphic in $D$

$⇔ |f|$ is constant

# harmonic function

$h:D ⊆ \R^2 → \R$ with continuous second partial derivative

$$
h_{xx}+h_{yy}=0
$$
