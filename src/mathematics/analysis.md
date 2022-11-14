<!-- toc -->
# Real Analysis

# set

## complement of set $S$

$S ⊆ X$

$$
S^c:=\{x\in X|x\notin S\}
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

# real number

- real number are complete\
    every Cauchy sequence in $\R$ converge to $\R$
- real number satisfy the Archimedian property

## Archimedian property

$a>0,b>0 ⇒ ∃\ n\in\Z,na>b$

# function

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

# sequence

$\{a_n\}_{n=1}^∞$ or $\{a_n\}$

$$
a_n:\N → \R
$$

see also [Sequence and Series](sequence_series.md)

## sequence convergence

$$
\lim_{n → ∞}a_n=a
\quad\text{or}\quad
a_n → a
$$

or $\{a_n\}$ converge to limit $a$ iff,

$∀\ \varepsilon>0,∃$ integer $N(\varepsilon)$, so that $∀\ n≥N$,

$$
|a_n-a|≤\varepsilon
$$

## sequence diverge to infinite

$∀\ M,∃\ N$, so that $∀\ n≥N$,

$$
a_n≥M
$$

## bounded sequence

$a_n$ is bounded iff

$∃\ M$ so that $∀\ n$

$$
|a_n|≤M
$$

- bounded monotone sequence converge

## limit theorem

- bounded sequence
- squeeze theorem
- limit are linear
- multiplication and division can be extracted

## Cauchy sequence

$∀\ \varepsilon>0,∃\ N$ so that, if $n≥N,m≥N$, then

$$
|a_n-a_m|≤\varepsilon
$$

- convergent sequence are Cauchy sequence
- axiom of completeness\
    Cauchy sequence in $\R$ converge to finite number in $\R$

## subsequence

$k\mapsto n(k):\N → \N$

$∀\ k\in\N,\quad n(k+1)>n(k)$

subsequence of $\{a_n\}_{n=1}^∞$,

$$
\{a_{n(k)}\}
_{k=1}^∞
\text{ or }\{a
_{n_k}\}
$$

## limit point

limit point $d$ of $\{a_n\} ⇔$

$$
∀\ \varepsilon>0,N\in\Z,
∃\ n≥N,\text{ s.t. }
|a_n-d|≤\varepsilon
$$

- $d$ is limit point $⇔ ∃$ subsequence $\{a_{n_k}\} → d$

## Bolzano-Weierstrass Theorem

$\{a_n\}$ bounded
$⇒ ∃\ \{a_{n_k}\},d$ s.t. $\{a_{n_k}\}→ d$

- proof: successively shrink interval by half
    and keep the half with infinite element
- $a_n\in[b,c] ⇒ ∃\ \{a_{n_k}\},d\in[b,c]$ s.t. $a_{n_k} → d$

# continuity

$f$ is continuous at $c\in Dom(f) ⇔$

$$
∀\text{ sequence }\{x_n\},x_n\in Dom(f),x_n → c,\\[12pt]
\lim_{n → ∞}f(x_n)=f(c)
$$

- $f$ is continuous at $c\in Dom(f) ⇔$

    $$
    ∀\ \varepsilon>0,∃\ \delta>0,\text{ s.t. }
    ∀\ x\in Dom(f),\\[12pt]
    |x-c|≤\delta ⇒ |f(x)-f(c)|≤\varepsilon
    $$

## continuous function on closed interval

$f$ is continuous on $S ⇒$
$f$ is bounded:

$$
∃\ B\in\R,\text{ s.t. }∀\ x\in S,\\[12pt]
|f(x)|≤B
$$

$f$ continuous on $[a,b] ⇒$

$$
∃\ c,d\in[a,b]\text{ s.t.}\\[12pt]
f(c)=\sup_{[a,b]}f,\quad
f(d)=\inf_{[a,b]}f
$$

and

$$
Range(f)=[\inf_{[a,b]}f,\sup_{[a,b]}f]
$$

and $f$ is uniformly continuous on $[a,b]$

- supremum

    $$
    \sup_Sf:=\sup\{f(x)|x\in S\}
    $$

- infimum

    $$
    \inf_Sf:=\inf\{f(x)|x\in S\}
    $$

### intermediate value theorem

$f$ continuous on $[a,b]$, $f(a)≠f(b)$,
$y\in\R$ is between $f(a),f(b) ⇒$

$$
∃\ c\in(a,b)\text{ s.t. }
f(c)=y
$$

## uniform continuity

$f$ is uniformly continuous $⇔$

$$
∀\ \varepsilon>0,∃\ \delta>0\text{ s.t. }
∀\ x,c\in Dom(f)\\[12pt]
|x-c|≤\delta ⇒ |f(x)-f(c)|≤\varepsilon
$$

## Lipschitz continuity

$f$ is Lipschitz continuous on $S ⇔$

$$
∃\ M\text{ s.t. }∀\ x,c\in S,x≠c,\quad
\frac{f(x)-f(c)}{x-c}≤M
$$
