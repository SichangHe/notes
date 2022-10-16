# Abstract Algebra

# integer

$$
\Z:=\{\cdots,-2,-1,0,-1,-2,\cdots\}
$$

## natural number

$$
\N:=\{0,1,2,\cdots\}
$$

## well-ordering axiom

$∀\ R ⊆ \N,R ≠ ∅,∃\ a\in R$ s.t. $\min(R)=a$

## division algorithm

$∀\ a,b\in\Z,b>0,∃!\ q,r\in\Z$, s.t.

$$
a=bq+r
,\qquad
0≤r<b
$$

### divisibility

$b|a$, or $b$ divide $a ⇔ ∃\ c\in\Z$, s.t. $a=bc$

- $b\not|a$, or $b$ do not divide $a$
- $b|a ⇔ b|(-a)$
- $a≠0,b|a ⇒ b≤|a|$

### greatest common divisor

$a,b\in\Z\backslash\{0\},∃!\ d:=\gcd(a,b)$, s.t.

1. $d|a,d|b$
1. $c|a,c|b ⇒ c≤d$

or

1. $d|a,d|b$
1. $c|a,c|b ⇒ c|d$

#### Euclidean algorithm

$a,b\in\Z\backslash\{0\}$

1. let $r_{-2}=a,r_{-1}=b$
1. apply division algorithm on $r_{i-1},r_i$ until $r_{n+1}=0$

    $$
    r_{i-1}=q_{i+1}r_i+r_{i+1}
    $$

1. $r_n=\gcd(a,b)$

- $a,b,q,r\in\Z,b>0,a=bq+ ⇒ \gcd(a,b)=\gcd(b,r)$

#### Bézout's identity

$a,b\in\Z\backslash\{0\},∃\ u,v$ s.t.

$$
\gcd(a,b)=au+bv
$$

- $\gcd(a,b)=\min(\{ax+by|x,y\in\Z\})$
- $x,y\in\Z,c=ax+by ⇒ \gcd(a,b)|c$
- find $u,v$: substitute $\gcd(a,b)$
    from the last equation in Euclidean algorithm up

#### relatively prime

$a,b$ are relatively prime $⇔ \gcd(a,b)=1$

- $\gcd(a,b)=1⇔ ∃\ x,y\in\Z,ax+by=1$
- $a|bc,\gcd(a,b)=1 ⇒ a|c$

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

