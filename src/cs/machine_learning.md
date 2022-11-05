<!-- toc -->
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

## three types of machine learning problems

### classification problem

label given data

- classifier (predictor) $h$: the produced function

#### all possible training set

$$
\mathcal T:=2^{X\times Y}
$$

#### signature of machine learning function $\lambda$

$$
\lambda:\mathcal T\rightarrow\mathcal H
\quad\text{such that}\quad
\lambda(T)=h
$$

- $\lambda$ learn (or train) classifier $h$ from training set $T$
- inference: apply classifier $h$ on any data
    - testing: apply classifier $h$ on unseen data

#### classifier $h$ define a partition of $X$

### regression problem

given data, return a vector

### clustering problem

group given data

## supervised/ unsupervised machine learning

supervised learning: classification, regression

unsupervised learning: clustering

# k-nearest neighbors predictor

remember the whole training set

$$
T=\{(\vec x_i,y_i)|i=1,\cdots,N\}
$$

return average of $y_n$s corresponding to
the $k$ closest $\vec x_n$s to $\vec x$

- useful for both classification and regression
- smaller $k$ results in worse overfitting
- good interpolation and poor extrapolation

## Voronoi diagram

![example of a Voronoi diagram](https://www.baeldung.com/wp-content/uploads/sites/4/2021/11/plotcrop-768x768.png)

