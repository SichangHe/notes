<!-- toc -->
# Multivariate Calculus

# multivariate function

$$
\{f(x_1,x_2,\cdots)|(x_1,x_2,\cdots)\in D\}
$$

## level curve (contour curve)/ level space

curve/ space with equation

$$
f(x_1,x_2,\cdots)=k
$$

- $k$ is constant

## limit of multivariate function

$$
\lim_{(x_1,x_2,\cdots)\rightarrow(a_1,a_2,\cdots)}f(x_1,x_2,\cdots)=L
$$

$\Leftrightarrow f(x_1,x_2,\cdots)$ approach $L$
as $(x_1,x_2,\cdots)$ approach $(a_1,a_2,\cdots)$
from any path within domain

- proof for the opposite using counterexample:\
    point out that the function approach different value from two different direction
- the squeeze theorem hold

## continuity of multivariate function

$$
\lim_{(x_1,x_2,\cdots)\rightarrow(a_1,a_2,\cdots)}f(x_1,x_2,\cdots)
=f(a_1,a_2,\cdots)
$$

$\Leftrightarrow f$ continuous

## partial derivative

$$
\frac{∂f}{∂x_n}\Bigr|_{x_1=a_1,\cdots,x_n=a_n,\cdots}
=f_{x_n}(a_1,a_2,\cdots)
=g'(a_n)
$$

where

$$
g(x_n)=f(a_1,\cdots,x_n,a_{n+1},\cdots)
$$

### higher partial derivative

$$
(f_{x_m})_{x_n}
=f_{x_mx_n}
$$

#### Clairaut's theorem

$f$ defined on $D$ containing $(a,b)$,
$f_{xy},f_{yx}$ continuous

$$
\Rightarrow f_{xy}(a,b)=f_{yx}(a,b)
$$

## tangent plane

$$
z-z_0=f_x(x_0,y_0)(x-x_0)+f_y(x_0,y_0)(y-y_0)
$$

### line approximation

$$
f(x,y)\approx f_x(a,b)(x-a)+f_y(a,b)(y-b)+f(a,b)
$$

## increment

$$
\Delta z=f(a+\Delta x,b+\Delta y)-f(a,b)
$$

### differentiable function

$$
\lim_{\Delta x → 0,\Delta y → 0}\Delta z=
\lim_{\Delta x → 0,\Delta y → 0}\left(
    \frac{∂z}{∂x}+\varepsilon_1
\right)\Delta x+\left(
    \frac{∂z}{∂y}+\varepsilon_2
\right)\Delta y\\[12pt]=
\lim_{\Delta x → 0,\Delta y → 0}\frac{∂z}{∂x}\Delta x+\frac{∂z}{∂y}\Delta y
$$

### differential

for differentiable function

$$
dz=\frac{∂z}{∂x}dx+\frac{∂z}{∂y}dy
$$

## implicit function

$$
F(x,y)=0
$$

### implicit function theorem

given

1. $F$ differentiable by $x$ and $y$
1. $\frac{∂F}{∂y}≠0$

take derivative of both side

$$
\frac{∂F}{∂x}\frac{dx}{dx}+\frac{∂F}{∂y}\frac{dy}{dx}=0 ⇒
\frac{dy}{dx}=-\frac{\frac{∂F}{∂x}}{\frac{∂F}{∂y}}
$$

## gradient

$$
\nabla f(x_1,\cdots,x_n)=\langle f_{x_1},\cdots,f_{x_n} \rangle
$$

- product rule, $\nabla(fg)=(\nabla f)g+f(\nabla g)$

### directional derivative

$\vec u$ is unit vector

$$
D_{\vec u}=\lim_{h → 0}\frac{
    f(x_1+u_1h,\cdots,x_n+u_nh)-f(x_1,\cdots,x_n)
}{h}\\[12pt]=\nabla f(x_1,\cdots,x_n)\cdot\vec u
$$

$\max(D_{\vec u}f)=|\nabla f|$ only when
$\vec u,\nabla f(x_1,\cdots,x_n)$ have the same direction

### level surface

level surface $F(x,y,z)=k$

line curve $\vec r(t)$ on the surface of the level surface

$$
\nabla F\cdot\vec r'=0
$$

$⇒ \nabla F$ is normal vector of tangent plane

- for level curve, $\nabla F$ is perpendicular to the curve

#### tangent plane of level surface

$$
F_x(x-x_0)+F_y(y-y_0)+F_z(z-z_0)=0
$$

## extrema

point $(a,b)$

$$
\begin{cases}
f_x(a,b)=0\\
f_y(a,b)=0
\end{cases}
$$

$⇒$ maximum or minimum or saddle point

$$
D(a,b)=f_{xx}(a,b)f_{yy}(a,b)-f_{xy}^2(a,b)
$$

- $D>0 ⇒$
    - $f_{xx}>0 ⇒$ local minimum
    - $f_{xx}<0 ⇒$ local maximum
- $D<0 ⇒$ saddle point

### extrema subject to constraint

constraint $g(x,y,z)=k$

$$
\nabla f\parallel\nabla g ⇒ \nabla f(x,y,z)=\lambda\nabla g(x,y,z)
$$

- Lagrange multiplier $\lambda$

for additional constraint $h(x,y,z)=c$

two constraint's intersection curve $C$

$$
\nabla f,\nabla g,\nabla h\perp C ⇒
\nabla f(x,y,z)=\lambda\nabla g(x,y,z)+\mu\nabla h(x,y,z)
$$
