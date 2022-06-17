# Sequence and Series

# sequence $\{a_n\}$

list of number in definite order

## sequence convergence

$$
\lim_{n → ∞}a_n=L
$$

$⇒ \{a_n\}$ converge

- $⇔ ∀\ \varepsilon>0,\ ∃\ N,\ ∀\ n>N$

    $$
    |a_n-L|<\varepsilon
    $$

- otherwise, $\{a_n\}$ diverge

### prove sequence convergence by function

sequence converge if corresponding function converge

$$
\lim_{x → ∞}f(x)=L
\qquad
f(n)=a_n
\quad
(n\in\N)
\\[12pt]
⇒ \lim_{n → ∞}a_n=L
$$

- all limit law on function can be applied on sequence

### sequence convergence preserve by chaining continuous function

$$
\lim_{n → ∞}a_n=L
\qquad
f\text{ continuous at }L
\\[12pt]
⇒ \lim_{x → ∞}f(a_n)=f(L)
$$

### convergence of $\{r^n\}$

$$
\lim_{n → ∞}r^n=\begin{cases}
    0&r\in(-1,1)
    \\
    1&r=1
    \\\text{DNE}&\text{otherwise}
\end{cases}
$$

## sequence monotonicity

increasing sequence

$$
∀\ n≥1,
\quad
a_n<a_{n+1}
$$

- the opposite is decreasing sequence

## bounded sequence

$\{a_n\}$ bounded above

$$
⇔ ∃\ M,
\quad ∀\ n≥1,
\quad
a_n<M
$$

- the opposite is bounded below
- bounded sequence: both bounded above and below

### monotonic sequence theorem

monotonic bounded sequence converge

# series (infinite series)

$$
\sum a_n
$$

or

$$
\sum_{n-1}^\infty a_n
$$

## $n$th partial sum $s_n$

$$
s_n=\sum_{i=1}^n
$$

## series convergence

$$
\lim_{n → ∞}s_n=s
$$

$⇒\sum a_n$ convergent

- $s$ sum of series
- the opposite is divergent
- linear combination of convergent series is convergent

## example series

### geometric series

$$
a_n=ar^{n-1}
\\[12pt]
s_n=\frac{a(1-r^n)}{1-r}
\\[12pt]
\sum a_n=\begin{cases}
    \displaystyle\frac{a}{1-r}&-1<r<1
    \\
    \text{DNE}&\text{otherwise}
\end{cases}
$$

#### power series

$$
\sum_{n=0}^∞ x^n=\frac{1}{1-x}
$$

### harmonic series

$$
a_n=\frac{1}{n}
$$

- divergent

### $p$-series

$$
\sum\frac{1}{n^p}\begin{cases}
    \text{converge}&p>1
    \\
    \text{diverge}&p≤1
\end{cases}
$$

## divergence test

$\sum a_n$ converge $⇒ \displaystyle\lim_{n → ∞}a_n=0$

$\displaystyle\lim_{n → ∞}a_n≠0\text{ or DNE} ⇒ \sum a_n$ diverge

## integral test

$∃\ N≥1\in\N^+,\ f(n)=a_n$ continuous decreasing positive on $[N,∞)$

$∫_1^∞ f(x)\ dx$ converge $⇔ \sum a_n$ converge

### remainder estimate for integral test

$f$ decreasing on $[n,∞)$
$$
R_n=s-s_n
\\[12pt]
∫_{n+1}^∞ f(x)\ dx≤R_n≤∫_n^∞ f(x)\ dx
$$

## comparison test

$\sum b_n$ converge, $∀\ n,a_n≤b_n$\
$⇒ a_n$ converge

$\sum b_n$ diverge, $∀\ n,b_n≤a_n$\
$⇒ a_n$ diverge

## limit comparison test

$$
\lim_{n → ∞}\frac{a_n}{b_n}=C>0
$$

$⇒ a_n,b_n$ have same convergence

## alternating series

$$
∀\ n≥1\in\N,
\qquad
a_n\cdot a_{n+1}<0
$$

### alternating series test

alternating series $a_n$

$$
\begin{rcases}
    ∀\ n≥1\in\N,
    \quad
    |a_n|≤|a_{n+1}|
    \\[12pt]
    \displaystyle\lim_{a_n → ∞}=0
\end{rcases}
⇒ a_n\text{ converge}
$$

### alternating series estimation theorem

$a_n$ satisfy alternating series test

$$
|R_n|=|s-s_n|≤|a_{n+1}|
$$

## absolute convergence

$$
\sum|a_n|\text{ converge}
$$

$ ⇒ \sum a_n$ absolutely converge

- $ ⇒ \sum a_n$ converge

### conditional convergence

$\sum a_n$ converge but not absolutely converge

$ ⇒ \sum a_n$ conditionally converge

### ratio test

$$
\left|
    \lim_{n → ∞}\frac{a_{n+1}}{a_n}
\right|
=\begin{cases}
    L<1 ⇒ \sum a_n\text{ absolutely converge}
    \\[12pt]
    L>1\text{ or } ∞ ⇒ \sum a_n\text{ diverge}
\end{cases}
$$

### root test

$$
\left|
    \lim_{n → ∞}\sqrt[n]{|a_n|}
\right|
=\begin{cases}
    L<1 ⇒ \sum a_n\text{ absolutely converge}
    \\[12pt]
    L>1\text{ or } ∞ ⇒ \sum a_n\text{ diverge}
\end{cases}
$$

## convergence test strategy

1. special series
    1. $p$-series
    1. geometric series
1. similar form to special series\
    $⇒$ (limit) comparison test
1. divergence test
1. alternating series test
1. absolute convergence
    1. ratio test
    1. $(b_n)^n ⇒ $ root test
1. integral test
