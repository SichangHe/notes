# Machine Learning

## general problem format

given input $A$, want output $y\in Y$

$$
f:A\rightarrow Y
,\qquad
y=f(a)\in Y
\quad\text{for }a\in A
$$

- traditional approach\
    hand-craft the function $f$
- machine learning\
    build another function $\lambda$ and use it to generate
    an approximation $f$

## machine learning is about building a function

- training data $L=\{(a_1,y_1),\cdots,(a_n,y_n)\}$
- class of allowed function $\mathcal F$

use a predefined algorithm to compute $f\in\mathcal F$ with the goal:

$$
y\approx f(x)
$$

### simplification using feature vector

convert input into a 1d vector, making machine learning generally applicable

- feature vector $\vec x\in X\subseteq\R^d$
- $\phi:A\rightarrow X$
- training set $T_a=\{(\vec x_1,y_1),\cdots,(\vec x_n,y_n)\}\subset\R^d\times\R^e$
- hypothesis space $\mathcal H$
- $Y\subseteq\R^e$

predefined algorithm produce $h\in\mathcal H$ so that

$$
f(a)=h(\phi(a))
$$

## loss

estimation of the error of $h$

$$
\ell:Y\times Y\rightarrow\R^+
\\[12pt]
\ell(y_n,h(\vec x_n))
$$

### empirical risk

average lost based on the training set

$$
L_T(h):=\frac{1}{N}\sum_{n=1}^N\ell(y_n,h(\vec x_n))
$$
