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
\lim_{(x,y) → (x_0,y_0)}u(x,y)+i\lim_{(x,y) → (x_0,y_0)}v(x,y)
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
positively oriented contour $C$,
negatively oriented simple closed contour $C_i$,\
$C_i$ inside of and disjoint from $C$,\
$f:D → \mathbb C$ holomorphic on $D$ and on the region between $C,C_i$

$$
⇒ ∫_Cf(z)\ dz+∫_{C_i}f(z)\ dz=0
$$

### path deformation principle

for the following case, deformation of contour integral persist its value

positively oriented contour $C_1,C_2$,\
$f$ holomorphic between $C_1,C_2$

$$
⇒ ∫_{C_1}f(z)\ dz=∫_{C_2}f(z)\ dz
$$

## Cauchy's integral formula (Cauchy's formula)

$C$ positively oriented contour,\
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

### evaluating integral with Cauchy's integral formula

on positively oriented contour $C$,
evaluate integral

$$
I=∫_Cg(z)\ dz
$$

1. find $f(z),z_0$ s.t. $z_0$ inside $C$ and

    $$
    g(z)=\frac{f(z)}{(z-z_0)^n}
    $$

1. calculate $f^{(n-1)}(z_0)$
1. apply Cauchy's integral formula

    $$
    I=\frac{2\pi i}{(n-1)!}f^{(n-1)}(z_0)
    $$

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

# analyticity

$f:U_\varepsilon(z_0) → \mathbb C$ analytic $⇔$

$$
∀\ z\in U_\varepsilon(z_0),\quad
f(z)=∑_{n=0}^∞ a_n(z-z_0)^n
$$

# Laurent series

annual domain $D$, $R_0<|z-z_0|<R_1$,\
any closed contour $C$ in $D$,\
function $f$ holomorphic in $D ⇒$

$$
f(z)=∑_{n=-∞}^∞ c_n(z-z_0)^n\\[12pt]
c_n=\frac{1}{2\pi i}∫_C \frac{f(z)\ dz}{(z-z_0)^{n+1}}
$$

- punctured disk, $R_0=0$
- unique

## residue

$$
res\ f(z_0)=c_{-1}=\frac{1}{2\pi i}∫_Cf(z)\ dz\\[12pt] ⇒
∫_Cf(z)\ dz=2\pi i\ res\ f(z_0)
$$

### Cauchy residue theorem

positively oriented contour $C$,\
$f$ analytic on and within $C$ *except* on finite number of singularities
$z_k,k\in\{1,2,\cdots,n\}$

$$
∫_Cf(z)\ dz=2\pi i∑_{k=1}^n res\ f(z_k)
$$

### residue at infinity

all singularity are inside negatively oriented contour $C$

$$
∫_Cf(z)\ dz=2\pi i\ res\ f(∞)
$$

- Cauchy residue theorem can be rewritten as

    $$
    ∑_{k=1}^n res\ f(z_k)+res\ f(∞)=0
    $$

- by replacing $z$ with $\frac{1}{z}$

    $$
    res \left(
        \frac{1}{z^2}f \left(
            \frac{1}{z}
        \right)
    \right)(0)=-res\ f(∞)
    $$

# singularity

## isolated singularity

$f$ analytic in deleted neighborhood $\hat U(z_0)$

$z_0$ is isolated singularity

- $f$ has Laurent series about $z_0$
- not branch point
- isolated singular at infinity $\Leftarrow ∃\ R>0$ s.t.
    $f$ analytic for $R<|z|<∞$

### essential isolated singularity

$\not ∃\ m\in\N^+$ s.t. $∀\ n<-m,\ c_n=0$

$z_0$ is essential isolated singularity

- Casorati-Weierstrass theorem

    $∀\ \varepsilon,R>0,w\in\mathbb C,∃\ z\in|z-z_0|<R$ s.t
    $|f(z)-w|<\varepsilon$

### pole

$∃\ m\in\N^+$ s.t. $∀\ n<-m,\ c_n=0$

pole of order $m$ at $z_0$

- simple pole $\Leftarrow m=1$
    - $$
        res\ f(z_0)=[(z-z_0)f(z)](z_0)
        $$

- removable singularity $\Leftarrow m=0$
    - removed by setting $f(z_0)=c_0$
- $$
    res\ f(z_0)=\frac{d^{m-1}}{(m-1)!\ dz^{m-1}}\left[
        (z-z_0)^{m-1}f(z)
    \right]\Bigr|_{z=z_0}
    $$

    - only usable for $m=1,2$
    - for $m=2$

        $$
        res\ f(z_0)=\frac{d}{dz}[(z-z_0)^2f(z)](z_0)
        $$

### zero of order $m$

$f$ analytic at $z_0$,\
$f(z_0)=0$,\
$∃\ m\in\N^+$ s.t.

$$
∀\ n<m,\quad f^{(n)}(z_0)=0
$$

- identically zero $\Leftarrow m=∞$
    - otherwise, the zero is isolated

#### zero and pole

$p,q$ analytic,\
$q$ has zero of order $m$ at at $z_0$\
$p(z_0)≠0$

$⇒ \frac{p}{q}$ has pole of order $m$ at $z_0$

- $m=1 ⇒ \frac{p}{q}$ has simple pole at $z_0$,

    $$
    res\ \left[
        \frac{p}{q}
    \right](z_0)=\frac{p(z_0)}{q'(z_0)}
    $$

# improper integral

## Cauchy principal value $CPV$

$$
CPV\ ∫_{-∞}^∞ f(x)\ dx=\lim_{R → ∞}∫_{-R}^R f(x)\ dx
$$

if RHS exist

- $f$ is even $⇒ ∫_{-∞}^∞ f(x)\ dx=CPV\ ∫_{-∞}^∞ f(x)\ dx$

## improper integral for even rational function

real, continuous, even, irreducible rational function $f=\frac{p}{q}$

$⇒ f$ has finitely many zeros $z_k$ *above* the real axis

let $C_R$ be upper half semicircle with $[-R,R]$ as its missing side

$$
∫_{-R}^R f(x)\ dx+∫_C f(x)\ dx=2\pi i∑_k res\ f(z_k)
$$

## Fourier integral

$k>0$

$$
∫_{-∞}^∞ f(s)\sin(kx)\ dx
$$

### Jordan's lemma

$f(z)$ analytic above the imaginary axis outside $|z|<R_0$

### Jordan's inequality

## indented path

### lemma

# Laplace transform

## Bromwich formula

# meromorphic

$f$ is analytic except possibly for poles

## theorem for meromorphic function

simple closed contour $C$,\
$f$ non-zero and analytic on $C$, meromorphic within $C$

$$
\frac{1}{2\pi i}∫_C \frac{f'(z)}{f(z)} dz=Z-P
$$

- $Z$, number of zero of $f$ within $C$ counted with order
- $P$, number of pole of $f$ within $C$ counted with order

## argument principle

$$
Z-P=\frac{1}{2\pi i}∫_C \frac{f'(z)}{f(z)} dz=
\frac{1}{2\pi}\Delta_C\arg f=\nu(\Gamma,0)
$$

## Rouché's theorem (dog on a leash theorem)

$f,g$ analytic on and within $C$

## Brouwer's fixed point theorem

$D:|z|≤1,int\ D:|z|<1$,\
$g:D → int\ D$ analytic

$⇒ ∃!\ z_0\in D$ s.t. $g(z_0)=z_0$ (fixed point)

## Hopf's theorem

closed curve $\Gamma,\tilde\Gamma$,\
one can be continuously deformed into another without crossing point $w$

$⇔ \nu(\Gamma,w)=\nu(\tilde\Gamma,w)$

# Möbius transformation

$$
f(z)=\frac{az+b}{cz+d}:\bar{\mathbb C} → \bar{\mathbb C},\qquad
ad-bc≠0
$$

- extended complex plane $\bar{\mathbb C}:=\mathbb C\cup\{∞\}$
- only singularity is simple pole $\frac{d}{c}$
- derivative non-zero

    $$
    f'(z)=\frac{ad-bc}{(cz+d)^2}≠0
    $$

- they are a group
- map circle to circle
    - line are circle of infinite radius through $∞$

## circle in Argand diagram

$$
Az\bar z+(B-iC)z+(B+iC)\bar z+D=0\\[12pt]
A,B,C,D\in\R
$$