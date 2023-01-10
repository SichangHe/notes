<!-- toc -->
# Complex Analysis

# complex number

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

where

$$
r=|z|,\quad
\theta=\tan{\frac{y}{x}}
$$
