<!-- toc -->
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

$a,b\in\Z\setminus\{0\},∃!\ d:=\gcd(a,b)$, s.t.

1. $d|a,d|b$
1. $c|a,c|b ⇒ c≤d$

or

1. $d|a,d|b$
1. $c|a,c|b ⇒ c|d$

#### Euclidean algorithm

$a,b\in\Z\setminus\{0\}$

1. let $r_{-2}=a,r_{-1}=b$
1. apply division algorithm on $r_{i-1},r_i$ until $r_{n+1}=0$

    $$
    r_{i-1}=q_{i+1}r_i+r_{i+1}
    $$

1. $r_n=\gcd(a,b)$

- $a,b,q,r\in\Z,b>0,a=bq+r ⇒ \gcd(a,b)=\gcd(b,r)$

#### Bézout's identity

$a,b\in\Z\setminus\{0\},∃\ u,v$ s.t.

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

### prime number

$p\in\Z$, then $p$ is prime $⇔ p≠0,p≠±1$, the only divisor of $p$ are $±1,±p$

- composite number: not prime

#### Euclid's lemma

$p$ prime, $p|ab ⇒ p|a$ or $p|b$

- $p\in\Z\setminus\{0,±1\}$,
    then $p$ prime $⇔$ if $p|ab$, then $p|a$ or $p|b$
- $p$ prime, $p|a_1a_2\cdots a_n ⇒ ∃\ i,p|a_i$

#### fundamental theorem of arithmetic

$∀\ n\in\Z\setminus\{0,±1\},n$ can be factored uniquely into product of primes

# relation

relation $R$ on $A$ is a subset $R ⊆ A × A$

$aRb$ or $a$ is related to $b ⇔ (a,b)\in R$

- $a\not Rb$ or $a$ is not related to $b$

## partition of set

$A$ is a non-empty set, partition of $A$

$$
\mathcal P:\ \{A_i|i=1,2,\cdots\}
$$

s.t.

1. $∀\ i≠j,A_i\cap A_j= ∅$
1. $A=\displaystyle\bigcup_iA_i$

- $R_\mathcal P:=\{(a,b)|∃\ A_i,a\in A_i,b\in A_i\}$
    is equivalence relation

## equivalence relation

1. reflexive: $aRa$
1. symmetric: $aRb ⇒ bRa$
1. transitive: $aRb,bRc ⇒ aRc$

### equivalence class

equivalence class of representative $a$

$$
[a] :=\{x\in A|xRa\}
$$

- $aRb ⇔ [a]=[b]$
- $[a],[b]$ are either disjoint or identical
- quotient set of $A$ by $R$

    $$
    A/R:=\{[a]|a\in A\}
    $$

    is partition of $R$

## modular arithmetic

$a,b,n\in\Z,n>0$, then

$a\equiv_n b$
or $a\equiv b$ (mod $n$)
or $a$ is congruent to $b$ modulo $n ⇔ n|(a-b)$

### congruence module $n$

$\Z/n$ ($\Z$ mod $n$) or quotient set of $\Z$ by $\equiv_n$

- $\Z/n$ is equivalence relation on $\Z$

### congruence class

equivalence class of $a$ modulo $n$

$$
[a]_n:=\{x\in\Z|x\equiv_na\}\\[12pt]=
\{a+nk|k\in\Z\}
$$

- there are $n$ distinct congruence classes

### addition and multiplication in modular arithmetic

$$
[a]+[b]=[a+b]\\[12pt]
[a] [b]=[ab]
$$

- addition and multiplication are well-defined
- $∀\ [a]\in\Z/n,∃!$ additive inverse
- $[a]≠[0]$ either has unique multiplicative inverse or it has not

#### unit

$∃\ x\in\Z/n,[a]x=[1]$

- $[a]$ is unit $⇔ \gcd(a,n)=1$

#### zero divisor

$∃\ x≠[0],[a]x=[0]$

- $p\in\N\setminus\{0,1\}$, then

    $p$ is prime

    $⇔ ∀\ [a]≠[0]$, $[a]$ is unit

    $⇔ [b] [c]=[0] ⇒ [b]=[0]$ or $[c]=[0]$,
    or no zero divisor

# group

ordered pair $(G,*)$

- set $G$
- binary operation $*$

axiom group satisfy:

1. $*$ is associative
1. identity: $∃\ e\in G,\ ∀\ a\in G,\ a*e=e*a=a$
1. inverse: $∀\ a\in G,\ ∃\ a^{-1}\in G,\ a*a^{-1}=a^{-1}*a=e$

property

1. $e$ is unique
1. $∀\ a\in G$, $a$ has unique inverse
1. $a*x=b$ and $y*a=b$ has unique solution,
    cancellation law work

- $(a^{-1})^{-1}=a$
- $(a*b)^{-1}=b^{-1}*a^{-1}$
- value of $a_1*a_2*\cdots*a_n$ is independent of the bracketing

## abelian group (commutative group)

$*$ is commutative

- $\Z,\mathbb Q,\R,\mathbb C,\Z/n,\R^{m × n}$ under $+$
- $\mathbb Q\setminus\{0\},\R\setminus\{0\},\mathbb C\setminus\{0\},(\Z/n)^×$
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

## order of group

$|G|$, or order of $G$, is the number of distinct elements in $G$

### order of element in group

$|a|$, or order of $a$, is the smallest $n\in\Z_+$ s.t.

$$
a^n=e
$$

or $∞$ if $n$ DNE

- $e,a,a^2,\cdots,a^{n-1}$ are distinct
- $a^m=1 ⇔ n|m$
- $∀\ m\in\Z_+,|a^m|=\frac{n}{\gcd(m,n)}$

## Torsion group

$G$ is a Torsion group, then
$∀\ a\in G,|a|$ is finite

- Torsion-free group: $∀\ a\in G,a≠e,|a|= ∞$
- Torsion subgroup of $G$: for abelian group $G$,

    $$
    \text{Tor}(G):=\{a\in G||a|\text{ is finite}\}
    $$

- $ab=ba,\gcd(|a|,|b|)=1 ⇒ |ab|=|a||b|$
- $G$ is abelian Torsion group,
    then $c$ has largest order $⇒ ∀\ a\in G,|a|\big||c|$

## dihedral group $D_{2n}$

rotation ($r$) and reflection ($s$) of n-gon

$$
\{1,s,r,sr,r^2,sr^2,\cdots,r^{n-1},sr^{n-1}\}
\qquad n≥3
\\[12pt]
(r^i)(k)=i+k\mod n
$$

- order $2n$
- degree $n$
- $|s|=2$
- $|r|=n$
- $∀\ 0≤i≠j≤n-1,sr^i≠sr^j$
- $∀\ 0≤i≤n,r^is=sr^{-i}$

### permutation of set

permutation of $X$: bijection

$$
\sigma:X → X
$$

## symmetric group on set

set $\Omega≠ ∅$

$S_\Omega$, the set of permutation of $\Omega$

$(S_\Omega,\circ)$, symmetric group on $\Omega$

- $n≥1,\Omega=X_n ⇒ (S_n,\circ)$, symmetric group of degree $n$
- $|S_\Omega|=n!$
- $n≥3 ⇒ (S_n,\circ)$ nonabelian

### array notation of permutation

$α$ is permutation on $X_n$

$$
α=\begin{pmatrix}
    1&2&\cdots&n
    \\
    α(1)&α(2)&\cdots&α(n)
\end{pmatrix}
$$

### cycle notation of permutation

cyclically permute and fix the rest

$$
(a_1\ a_2\ \cdots\ a_m)=
\begin{pmatrix}
    a_1&a_2&\cdots&a_m
    \\
    a_2&a_3&\cdots&a_1
\end{pmatrix}
$$

- $m$-cycle (or cycle of length $m$)

#### transposition

$2$-cycle

- $∀\ \sigma\in S_n,\sigma$ can be expressed as product of transposition
    - not unique
    - even permutation: length of such transposition is even
    - odd permutation

#### disjoint cycle

no common number

- $α,\beta\in S_n$ disjoint $⇒ α\beta=\beta α$
- $∀\ \pi\in S_n,\pi≠1,\pi$ can be
    uniquely expressed as product of disjoint cycle of length at least 2

## subgroup

$H≤G$, or $H ⊆ G$ is a subgroup of $G$

1. $H≠ ∅$
1. $∀\ x,y\in H,xy\in H$
1. $∀\ x\in H,x^{-1}\in H$

- $H<G$, or $H$ is a proper subgroup of $G$

### subgroup test

1. $H≤G ⇔$
    1. $H≠ ∅$
    1. $∀\ x,y\in H,xy^{-1}\in H$
1. $|G|< ∞,H≤G ⇔$
    1. $H≠ ∅$
    1. $∀\ x,y\in H,xy\in H$

### centralizer of group

$$
C_G(A):=\{g\in G| ∀\ a\in A,ga=ag\}
$$

- $C_G(a)$ if $A=\{a\}$

#### center of group

$$
Z(G):=\{g\in G| ∀\ a\in G,ga=ag\}
$$

### normalizer of group

$$
N_G(A):=\{g\in G|gAg^{-1}=A\}
$$

where

$$
gAg^{-1}:=\{gag^{-1}|a\in A\}
$$

for group $G$ and subset $A ⊆ G$

- $C_G(A)≤N_G(A)≤G$
- $G$ abelian $⇒ Z(G)=G,C_G(A)=N_G(A)$

## cyclic group

$$
G=\langle x \rangle=\{x^n|n\in\Z\}
$$

- generator $x$
- cyclic group are abelian
- $|G|=|x|$

### fundamental theorem of cyclic group

1. $H≤G ⇒ ∃!\ k\in\N,k=\min_k\{x^k\in H\},\ H=\langle x^k \rangle$
1. $|G|=n ⇒$
    - $∀\ a\in\N,a|n,∃!\ A,|A|=a$
        - $A=\langle x^d\rangle$
        - $d=\frac{n}{a}$
    - $∀\ m\in\Z,\langle x^m \rangle=\langle x^{\gcd(m,n)} \rangle$
    - $∀\ i,j,x^i=x^j ⇔ i\equiv j\mod n$
1. $|G|=∞ ⇒ ∀\ m\in\Z,\langle x^m \rangle=\langle x^{|m|} \rangle$
