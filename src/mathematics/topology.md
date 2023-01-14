# Topology

set $M$

set $\mathcal O ⊆ \mathcal P(M)$ with all its element open

- point, $p\in M$

## open

1. $∅ \in\mathcal O,M\in\mathcal O$
1. $∀\ U_i,U_j\in\mathcal O,\ U_i\cap U_j\in\mathcal O$
1. $∀\ U_i,U_j\in\mathcal O,\ U_i\cup U_j\in\mathcal O$

- closed, $V ⊆ M$ where $V^C\in\mathcal O$
    - $∅, M$ are both open and closed

## topological space $(M,\mathcal O)$

set $M$ and choice of set of open subset $\mathcal O$

- chaotic topology, $\mathcal O_c=\{∅, M\}$
- discrete topology, $\mathcal O_d=P(M)$

## neighborhood

neighborhood of $p$:
$U\in\mathcal O,p\in U$

- deleted neighborhood, $\hat U=U\setminus\{p\}$

## closure

$S ⊆ M$

closure of $S$, $\bar S=S\cup ∂S$

### interior point

point $p$

$∃\ U\ni p$ s.t. $U\cap S=U$

- interior of $S$, set of all interior point of $S$

### exterior point

point $p$

$∃\ U\ni p$ s.t. $U\cap S= ∅$

- exterior of $S$, set of all exterior point of $S$

### boundary point

neither interior nor exterior of $S$

- $∂S$, boundary of $S$, set of all boundary point of $S$

## limit point

limit point $p$ of $S ⇔$

$∀\ \hat U,\hat U\cap S≠ ∅$

### sequence convergence

$∀\ U\ni p,∃\ m\in\N$ s.t. $n>m ⇒ s(n)\in U$

- in chaotic topology, every sequence converge to every point
