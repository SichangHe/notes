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

## complex infinity

$x → ∞$ or $y → ∞$

## Riemann sphere

$$
x^2+y^2+z^2=1
$$

intersection of the sphere with line through north poll and complex number

- north poll: $(0,0,1)$, correspond to complex infinity

# limit

$$
\lim_{z → z_0}f(z)=w_0
$$

$⇔ ∀\ \varepsilon>0,\ ∃\ \delta>0$ s.t.

$$
|f(z)-w_0|<\varepsilon\text{ whenever }|z-z_0|<\delta
$$
