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

$f$ defined around $z_0$,\
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

# parametric curve

complex-valued function

$$
C:[a,b] ⊆ \R → \mathbb C,\\[6pt]
t\mapsto z(t)=x(t)+iy(t)
$$

- simple $⇔$ does not intersect self $⇔$ injection
    - simple closed (Jordan curve) $⇔$ simple except two end meet
- oriented
    - positively oriented $⇔$ simple closed counterclockwise
    - negatively oriented

## parametric derivative

$x'(t),y'(t)$ continuous

$⇒ C$ differentiable,

$$
z'(t)=x'(t)+iy'(t)
$$

- velocity
    - speed $|z'|$
- smooth $⇔$ differentiable and $z'≠0$
    - $C$ has unit tangent vector in Argand diagram

        $$
        T(t)=\frac{z'(t)}{|z'(t)|}
        $$

## parametric integral

$$
\int z(t)=\int x(t)+i\int y(t)
$$

- both real part and imaginary part commute
- antiderivative
- mean value theorem of integral fail

## reparametrization

$$
\tilde t\mapsto\phi(\tilde t)=t\\[6pt]
C:z(t)=\tilde z(\tilde t)
$$

- curve length persist

### parametric curve length

$$
L(C)=∫_a^b\sqrt{x'(t)^2+y'(t)^2}\ dt=∫_a^b|z'(t)|\ dt
$$

# contour

piecewise smooth curve $C$ joined from finite smooth parametric curve

- $z$ continuous
- $z'$ piecewise continuous
- vertex, point where $C$ not smooth
- length, orientation, simple closed like parametric curve

## Jordan curve theorem

simple closed contour separate $\mathbb C$ into

1. a bounded interior
1. an unbounded exterior

## contour integral

contour $C:z(t):[a,b] → \mathbb C$,\
function $f(z)$ piecewise continuous on $C$

$$
\int_Cf(z)\ dz=\int_a^bf(z(t))\ z'(t)\ dt
$$

- independent of parametrization
- linearity

    $$
    \int_C(cf(z)+g(z))\ dz=c\int_Cf(z)\ dz+\int_Cg(z)\ dz
    $$

    for contour $C=C_1\cup C_2$

    $$
    \int_Cf(z)\ dz=\int_{C_1}f(z)\ dz+\int_{C_2}f(z)\ dz
    $$

- traversed in opposite direction

    $$
    -C:t\mapsto z(-t):[-b,-a] → \mathbb C\\[12pt] ⇒
    \int_{-C}f(z)\ dz=-\int_Cf(z)\ dz
    $$

### upper bound theorem for contour integral (ML theorem)

contour $C$ of length $L$,\
$f(z)$ piecewise continuous on $C$,\
$f(z)$ bounded by $M$

$$
⇒ \left|
    \int_Cf(z)\ dz
\right|≤ML
$$

- proof using lemma

    $$
    \left|\int_a^bz(t)\ dt\right|≤\int_a^b|z(t)|\ dt
    $$

    <details>
    <summary>proof of lemma</summary>

    $$
    I:=∫_a^bw(t)\ dt=r_Ie^{i\theta_I}
    $$

    lemma hold for $I=0$.
    for $I≠0$

    $$
    r_I>0\\[12pt] ⇒
    r_I=\text{Re }\left(e^{-i\theta_I}∫_a^bw(t)\ dt\right)\\[12pt]=
    ∫_a^b\text{Re }\left(e^{-i\theta_I}w(t)\right)\ dt≤
    ∫_a^b\left|e^{-i\theta_I}w(t)\right|\ dt\\[12pt]=
    ∫_a^b|z(t)|\ dt
    $$
    </details>

### path independence of contour integral

$f:D ⊆ \mathbb C → \mathbb C$ continuous in $D$

$∃$ antiderivative $F$ s.t. $∀\ C$ in $D$ from $z_1$ to $z_2$

$$
\int_Cf(z)\ dz=F(z_2)-F(z_1)
$$

$⇔ ∀\ C$ closed,

$$
\oint_Cf(z)\ dz=0
$$

## Cauchy-Goursat theorem

on $D ⊆ \mathbb C$,\
simple closed contour $C$ in $D$,\
$f:D → \mathbb C$ holomorphic on and within $C$

$$
⇒ \int_Cf(z)\ dz=0
$$

### Cauchy's theorem

same as Cauchy-Goursat theorem, except $f'(z)$ continuous

<details>
<summary>proof using Green's theorem and Cauchy-Riemann equations</summary>

$$
∫_Cf(z)\ dz=∫_C(u+iv)(dx+idy)=∫_C(u+iv)dx+(-v+iu)dy\\[12pt]=
\iint_D \left(
    \frac{∂}{∂x}(-v+iu)-\frac{∂}{∂y}(u+iv)
\right)dA\\[12pt]=
\iint_D(-v_x+iu_x-u_y+iv_y)dA=0
$$
</details>

## Cauchy-Goursat theorem on simply connected domain

on simply connected domain $D ⊆ \mathbb C$,\
closed contour $C$ in $D$,\
$f:D → \mathbb C$ holomorphic on $D$

$$
⇒ \int_Cf(z)\ dz=0
$$

- simply connected domain:
    every simple closed contour enclose only point in $D$
    - multiply connected domain
- holomorphic function on simply connected domain has antiderivative
    - entire function has antiderivative

## adoption of Cauchy-Goursat theorem on multiply connected domain

on multiply connected domain $D ⊆ \mathbb C$,\
positively oriented simple closed contour $C$,
negatively oriented simple closed contour $C_i$,\
$C_i$ inside of and disjoint from $C$,\
$f:D → \mathbb C$ holomorphic on $D$ and on the region between $C,C_i$

$$
⇒ ∫_Cf(z)\ dz+∫_{C_i}f(z)\ dz=0
$$

### path deformation principle

for the following case, deformation of contour integral persist its value

positively oriented simple closed contour $C_1,C_2$,\
$f$ holomorphic between $C_1,C_2$

$$
⇒ ∫_{C_1}f(z)\ dz=∫_{C_2}f(z)\ dz
$$

## Cauchy's integral formula (Cauchy's formula)

$C$ positively oriented simple closed contour,\
$f$ holomorphic inside and on $C$

$∀\ z_0$ inside $C$

$$
f(z_0)=\frac{1}{2\pi i}∫_C \frac{f(z)\ dz}{z-z_0}
$$

- derivative

    $$
    f'(z_0)=\frac{1}{2\pi i}∫_C \frac{f(z)\ dz}{(z-z_0)^2}
    $$

- at $z_0$, $f$ holomorphic $⇒ ∀\ n\in\N,f^{(n)}$ exist and holomorphic

    $$
    f^{(n)}(z_0)=\frac{n!}{2\pi i}∫_C \frac{f(z)\ dz}{(z-z_0)^{(n+1)}}
    $$

- $f$ holomorphic $⇒ u,v$ have continuous partial derivative at all order

<details>
<summary>proof</summary>
show using upper bound theorem

$$
\left|∫_{C_R}\frac{f(z)-f(z_0)}{z-z_0}\ dz\right|=0
$$
</details>

## Morera's theorem

$f$ continuous on $D$

$∀$ closed contour $C$

$$
∫_Cf(z)\ dz=0
$$

$⇒ f$ holomorphic throughout $D$

## Liouville's theorem

bounded entire function is constant

## fundamental theorem of algebra

non-constant polynomial of degree $n$ has $n$ root

## maximum modulus principle

non-constant holomorphic function $f$ on open $D$\
$⇒ |f|$ has no maximum on $D$

- for $f$ on $D\cup ∂D$,
    $|f|$ reach maximum always on $∂D$,
    never on interior
