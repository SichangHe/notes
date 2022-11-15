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

# integral

## partition

partition $P$ of $[a,b]$ is any finite collection of point

$$
x_0<x_1<\cdots<x_N
$$

where

$$
x_0=a,\quad x_N=b
$$

## upper sum/ lower sum

for subinterval $[x_{i-1},x_i]$ of partition $P$

$$
M_i:=\sup_x\{f(x)|x_{i-1}≤x≤x_i\}\\[12pt]
m_i:=\inf\{f(x)|x_{i-1}≤x≤x_i\}
$$

lower sum

$$
L_P(f):=\sum_{i=1}^Nm_i(x_i-x_{i-1})
$$

upper sum

$$
U_P(f):=\sum_{i=1}^NM_i(x_i-x_{i-1})
$$

- $L_P(f)≤U_P(f)$
- for any partition $Q$

    $$
    L_P(f)≤U_Q(f)
    $$

- for partition $Q$ that contain all point of $P$ and additional point

    $$
    L_P(f)≤L_Q(f),\quad
    U_Q(f)≤U_P(f)
    $$

## Riemann integrability

$f$ on $[a,b]$ is Riemann integrable $⇔$

$$
\sup_P\{L_P(f)\}=\inf\{U_P(f)\}
$$

- $∀\ \varepsilon>0,∃$ partition $P$ s.t.

    $$
    U_P(f)-L_P(f)≤\varepsilon
    $$

    $⇒ f$ is Riemann integrable

- $f$ continuous on $[a,b] ⇒ f$ Riemann integrable

## Riemann integral

$f$ Riemann integrable on $[a,b]$

Riemann integral

$$
\int_a^bf(x)\ dx:=\inf\{U_P(f)\}
$$

- $∀\ x\in[a,b],\ f(x)≤g(x) ⇒$

    $$
    \int_a^bf(x)\ dx≤\int_a^bg(x)\ dx
    $$

- $f\in C[a,b] ⇒$

    $$
    \left|\int_a^bf(x)\ dx\right|≤\int_a^b|f(x)|\ dx\\[12pt]
    \left|\int_a^bf(x)\ dx\right|≤(b-a)\sup_{[a,b]}|f(x)|
    $$

## Riemann sum

$$
\sum_{i=1}^Nf(x_i^*)(x_i-x_{i-1})
$$

where $x_i^*\in[x_{i-1},x_i]$

- $f$ continuous on $[a,b]$,
    $\{P_k\}$ is sequence of partition s.t.
    maximum length of subinterval $→ 0$ as $k → ∞$,
    $S_k$ is any Riemann sum corresponding to $P_k ⇒$

    $$
    S_k → \int_a^bf(x)\ dx
    \quad\text{as}\quad
    k → ∞
    $$

# differentiation

## continuously differentiable

$f$ differentiable on $[a,b]$
and $f'$ continuous on $[a,b]$,
or $f\in C^{(1)}[a,b]$

- $f$ continuous on $\R$ is denoted as $f\in C(\R)$

## Rolle's theorem

$f\in C[a,b]$ differentiable on $(a,b)$,
$f(a)=0=f(b) ⇒$

$$
∃\ c\in(a,b)
,\text{ s.t. }
f'(c)=0
$$

## mean value theorem

$f\in C[a,b]$ differentiable on $(a,b)$, $⇒$

$$
∃\ c\in(a,b)
,\text{ s.t. }
f'(c)=\frac{f(b)-f(a)}{b-a}
$$

## Taylor's theorem

$f\in C^{(n)}[a,b]$,
$f^{(n+1)}$ exist on $(a,b)$,
$x_0\in[a,b] ⇒$

$$
∀\ x\in[a,b],x≠x_0,∃\ \xi\text{ between }x,x_0
\text{ s.t.}\\[12pt]
f(x)=T^{(n)}(x,x_0)+\frac{f^{(n+1)}(\xi)}{(n+1)!}(x-x_0)^{n+1}
$$

where $T^{(n)}$ is define in
[Sequence and Series](sequence_series.md#n-th-degree-taylor-polynomial-tn)

- proof

    fix $x$, let $\alpha$ s.t.

    $$
    f(x)=T^{(n)}(x,x_0)+\frac{f^{(n+1)}(\xi)}{(n+1)!}(x-x_0)^{n+1}
    +\alpha(x-x_0)^{n+1}\\[12pt]
    g(t)=f(t)-T^{(n)}(t,x_0)-\alpha(t-x_0)^{n+1}
    $$

    apply Rolle's theorem $n$ time to show $∃\ \xi$ between $x,x_0$ s.t.

    $$
    g^{(n+1)}(x_{n+1})=0
    $$
