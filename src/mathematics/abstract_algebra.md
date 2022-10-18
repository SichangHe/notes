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

### prime number

$p\in\Z$, then $p$ is prime $⇔ p≠0,p≠±1$, the only divisor of $p$ are $±1,±p$

- composite number: not prime

#### Euclid's lemma

$p$ prime, $p|ab ⇒ p|a$ or $p|b$

- $p\in\Z\backslash\{0,±1\}$,
    then $p$ prime $⇔$ if $p|ab$, then $p|a$ or $p|b$
- $p$ prime, $p|a_1a_2\cdots a_n ⇒ ∃\ i,p|a_i$

#### fundamental theorem of arithmetic

$∀\ n\in\Z\backslash\{0,±1\},n$ can be factored uniquely into product of primes

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

- $p\in\N\backslash\{0,1\}$, then

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
