# Abstract Algebra

# group

ordered pair $(G,*)$

- set $G$
- binary operation $*$

axiom group satisfy:

1. $*$ is associative
1. identity: $∃\ e\in G,\ ∀\ a\in G,\ a*e=e*a=a$
1. inverse: $∀\ a\in G,\ ∃\ a^{-1}\in G,\ a*a^{-1}=a^{-1}*a=e$

## abelian group (commutative group)

$*$ is commutative

- $\Z,\mathbb Q,\R,\mathbb C,\Z/n,\R^{m × n}$ under $+$
- $\mathbb Q\backslash\{0\},\R\backslash\{0\},\mathbb C\backslash\{0\},(\Z/n)^×$
    under $\cdot$

## nonabelian group

- dihedral group of order $2n$, $D_{2n}$
- $(GL(n,\R),\cdot)$

### general linear group of degree $n$ over $R$

$$
GL(n,R):=\{A\in R^{n × n}|A\text{ is invertible}\}
$$

#### special linear group of degree $n$ over $R$

$$
SL(n,R):=\{A\in GL(n,R)|\det A=1\}
$$

## binary operation

$$
*:G × G → G
$$

### associative binary operation

$$
(a*b)*c=a*(b*c)
$$

### commutative binary operation

$$
a*b=b*a
$$
