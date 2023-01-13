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
