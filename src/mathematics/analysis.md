# Real Analysis

# set

## complement of set $S$

$S ⊆ X$

$$
S^c:=\{x\in X|x\notin S\}
$$

## real number

- real number are complete\
    every Cauchy sequence in $\R$ converge to $\R$
- real number satisfy the Archimedian property

### Archimedian property

$a>0,b>0 ⇒ ∃\ n\in\Z,na>b$

## function

function $f$ from $S$ to $T$ is subset $F ⊆ S\times T$

$t$ is the value of $f$ at $s$:

$$
s\xrightarrow{f}t
$$

or

$$
t=f(s)
$$

- $Dom(f)$ domain
- $Ran(f)$ range
- onto: $Ran(f)=T$
- one-to-one: $∀\ t\in Ran(f),∃!\ s\in S,f(s)=t$
- one-to-one correspondence: onto and one-to-one

## inverse function

for one-to-one function $f$, inverse function $f^{-1}$ of $f\iff$

$$
f(f^{-1}(t))=t\qquad ∀\ t\in Dom(f)
\\[12pt]
f^{-1}(f(s))=s\qquad ∀\ s\in S
$$

## cardinality

$|S|=|T|\iff ∃\ f:S → T$ one-to-one correspondence

### finite set

empty or has cardinality of $\{1,2,\cdots,n\}$ for some $n$

### infinite set

#### countable set

has cardinality of $\N$

- $T$ countable, $S$ infinite and $S ⊆ T ⇒ S$ countable
- $S,T$ countable $⇒ S\times T$ countable

## fundamental theorem of arithmetic

every integer $N≥2$ can be written uniquely as
a finite product of positive integral power of primes:

$$
N=p_1^{s_1}p_2^{s_2}\cdots p_n^{s_n}
$$
