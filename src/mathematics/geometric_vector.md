# Geometric Vector

# vector

$$
\vec v=\overrightarrow{AB}
$$

- $\vec v$ displacement vector
- $A$ initial point
- $B$ terminal point
- $\vec0$ zero vector
- $\frac{\vec v}{|\vec v|}$ unit vector

## vector addition

- triangle law
- parallelogram law

## scalar multiplication

$$
c\vec v
$$

## component of vector

$$
\vec a=\langle a_1,a_2,a_3 \rangle
$$

## standard basis vector

$$
\vec j=\langle 1,0,0 \rangle
\qquad
\vec k=\langle 0,1,0 \rangle
\qquad
\vec l=\langle 0,0,1 \rangle
$$

## dot product (scalar product, inner product)

$$
\vec a\cdot\vec b
=\sum_ia_ib_i
\\[12pt]
=|\vec a||\vec b|\cos\theta
$$

### angle between $\vec a,\vec b$, $\theta$

$$
\cos\theta=\frac{\vec a\cdot\vec b}{|\vec a||\vec b|}
$$

#### perpendicular vector

$$
\vec a\perp\vec b
⇔ \vec a\cdot\vec b=0
$$

### direction angle

$$
\cos\alpha=\frac{a_1}{|\vec a|}
\qquad
\cos\beta=\frac{a_2}{|\vec a|}
\qquad
\cos\gamma=\frac{a_3}{|\vec a|}
$$

- relation

    $$
    \cos^2\alpha+\cos^2\beta+\cos^2\gamma=1
    $$

- conclusion

    $$
    \frac{\vec a}{|\vec a|}
    =\langle \cos\alpha,\cos\beta,\cos\gamma \rangle
    $$

### projection

$$
\text{comp}_{\vec a}\vec b
=\frac{\vec a\cdot\vec b}{|\vec a|}
\\[12pt]
\text{proj}_{\vec a}\vec b
=\frac{\vec a\cdot\vec b}{|\vec a|^2}\vec a
$$

## cross product

$$
\vec a\times\vec b
=\langle a_2b_3-a_3b_2,a_3b_1-a_1b_3,a_1b_2-a_2b_1 \rangle
\\[12pt]
=\begin{vmatrix}
    \vec i&\vec j&\vec k
    \\
    a_1&a_2&a_3
    \\
    b_1&b_2&b_3
\end{vmatrix}
$$

- $\vec a\times\vec b\perp\vec a$
- $\vec a\times\vec b\perp\vec b$
- right hand rule determine direction of $\vec a\times\vec b$

### magnitude of cross product

$$
|\vec a\times\vec b|=|\vec a||\vec b|\sin\theta
$$

- equal to area of parallelogram by $\vec a,\vec b$

### parallel vector

$$
\vec a\parallel\vec b
⇔ \vec a\times\vec b=\vec0
$$

### property of cross product

- $\vec a\times\vec b=-\vec b\times\vec a$
- linear
- $\vec a\cdot(\vec b\times\vec c)
    =(\vec a\times\vec b)\cdot\vec c$
- $\vec a\times(\vec b\times\vec c)
    =(\vec a\cdot\vec c)b-(\vec a\cdot\vec b)\vec c$

### triple product

#### scalar triple product

$$
\vec a\cdot(\vec b\times\vec c)
$$

- volume of parallelepiped by $\vec a,\vec b,\vec c$

    $$
    V=|\vec a\cdot(\vec b\times\vec c)|
    $$

- $V=0 ⇔ \vec a,\vec b,\vec c$ coplanar

#### vector triple product

$$
\vec a\times(\vec b\times\vec c)
$$

# line $L$

- vector equation

    $$
    \vec r=\vec r_0+t\vec v
    $$

- parametric equation

    $$
    x=x_0+at
    \qquad
    y=y_0+bt
    \qquad
    z=z_0+ct
    $$

    where

    $$
    \vec r=\langle x,y,z \rangle
    \qquad
    \vec r_0=\langle x_0,y_0,z_0 \rangle
    \qquad
    \vec v=\langle a,b,c \rangle
    $$

- symmetric equation

    $$
    \frac{x-x_0}{a}
    =\frac{y-y_0}{b}
    =\frac{z-z_0}{c}
    $$
