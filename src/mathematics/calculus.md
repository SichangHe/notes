# Calculus

# function

## piecewise defined function

different formula for different part of domain

- step function

## composite function $f\circ g$

# mathematical model

## empirical model

model based entirely on data

# limit

$f$ is defined on interval containing $a$ except possibly $a$

$$
\lim_{x → a}f(x)=L
\\\\[12pt]
⇔ ∀\ \varepsilon>0,\ ∃\ \delta>0,
\\\\[12pt]
\text{if}\quad
0<|x-a|<\delta
\quad\text{then}\quad
|f(x)-L|<\varepsilon
$$

- limit exist iff limit from both side exist

    $$
    \lim_{x → a}f(x)=L
    \quad\text{iff }
    \lim_{x → a^-}f(x)=L
    \text{ and }
    \lim_{x → a^+}f(x)=L
    $$

## limit law

- linear: sum law, difference law, constant multiplication law
- product law, power law
- quotient law

    $$
    \lim_{x → a}\frac{f(x)}{g(x)}
    =\frac{\lim_{x → a}f(x)}{\lim_{x → a}g(x)}
    \quad\lim_{x → a}g(x)≠0
    $$

derivative rule

- $∀\ r>0$ rational

    $$
    \lim_{x → ∞}\frac{1}{x^r}=0
    $$

    - limit calculation technique\
        divide numerator and denominator by highest power of $x$

## direct substitution property

polynomial limit can be pulled out

$$
\lim_{h → 0}\frac{b^h-1}{h}=\ln b
$$

## limit comparison

$f(x)≤g(x)$ near $a$

$$
⇒ \lim_{x → a}f(x)
≤ \lim_{x → a}g(x)
$$

### squeeze theorem (sandwich theorem)

$f(x)≤g(x)≤h(x)$ near $a$,

$$
\lim_{x → a}f(x)=\lim_{x → a}h(x)=L
\\\\[12pt]
⇒ \lim_{x → a}g(x)=L
$$

e.g.

$$
\lim_{h → 0}\frac{\sin h}{h}=1
$$

## continuity

$f$ is continuous at $a$

$$
⇔ \lim_{x → a}f(x)=f(a)
$$

- continuous from the left/ right
- continuous on an interval $⇔$ continuous at every point in interval
- continuous function after operation in limit law are still continuous
- function continuous in domain
    - polynomial
    - rational
    - (inverse) trigonometric
    - exponential
    - logarithmic

### discontinuity

- removable\
    redefining $f$ at single point remove discontinuity
- unremovable
    - infinite discontinuity
    - jump discontinuity

### intermediate value theorem

$f$ continuous on $[a,b],f(a)≠f(b)$,\
$⇒ ∀\ N\in(f(a),f(b)),
\quad ∃\ c\in(a,b),f(c)=N$

# derivative $f'(a)$

derivative of $f$ at $a$

$$
f'(a)=\lim_{h → 0}\frac{f(a+h)-f(a)}{h}
\\\\[12pt]
=\lim_{x → a}\frac{f(x)-f(a)}{x-a}
$$

## derivative function $f'(x)$

$$
f'(x)=\lim_{h → 0}\frac{f(x+h)-f(x)}{h}
\\\\[12pt]
=y'
=\frac{dy}{dx}
=\frac{df}{dx}
=\frac{d}{dx}f(x)
=Df(x)
=D_xf(x)
$$

differential operator $D$, $\frac{d}{dx}$

$$
f'(a)=\frac{dy}{dx}\Bigr|_{x=a}
=\left.\frac{dy}{dx}\right] _{x=a}
$$

## differentiability

$f$ is differentiable at $a$\
$⇔ f'(x)$ exist

$f$ is differentiable on interval\
$⇔ f$ is differentiable at every point in the interval

- $f$ differentiable at $a ⇒ f$ continuous at $a$

## second derivative

$$
f''(x)=\frac{d}{dx}\left(
    \frac{dy}{dx}
\right)
=\frac{d^2y}{dx^2}
$$

## derivative rule

- linear: constant multiplication, sum, difference rule
- definition of $e$

    $$
    \lim_{h → 0}\frac{e^h-1}{h}=1
    $$

- product rule

    $$
    \frac{d}{dx}(uv)=u \frac{dv}{dx}+v \frac{du}{dx}
    $$

- quotient rule

    $$
    \frac{d}{dx}\left(
        \frac{u}{v}
    \right)
    =\frac{v \frac{du}{dx}-u \frac{dv}{dx}}{v^2}
    $$

- chain rule

    $$
    \frac{dy}{dx}=\frac{dy}{du}\frac{du}{dx}
    $$

## implicit differentiation

differentiate both side of equation

### derivative of (inverse) trigonometric function

$$
\frac{d}{dx}(\tan x)=\sec^2\\!x
\\\\[12pt]
\frac{d}{dx}(\csc x)=-\csc x\cot x
\\\\[12pt]
\frac{d}{dx}(\sec x)=\sec x\tan x
\\\\[12pt]
\frac{d}{dx}(\cot x)=-\csc^2\\!x
\\\\[12pt]
\frac{d}{dx}(\sin^{-1}\\!x)=\frac{1}{\sqrt{1-x^2}}
\\\\[12pt]
\frac{d}{dx}(\cos^{-1}\\!x)=-\frac{1}{\sqrt{1-x^2}}
\\\\[12pt]
\frac{d}{dx}(\tan^{-1}\\!x)=\frac{1}{1+x^2}
\\\\[12pt]
\frac{d}{dx}(\cot^{-1}\\!x)=-\frac{1}{1+x^2}
\\\\[12pt]
\frac{d}{dx}(\sec^{-1}\\!x)=\frac{1}{x\sqrt{x^2-1}}
\\\\[12pt]
\frac{d}{dx}(\csc^{-1}\\!x)=-\frac{1}{x\sqrt{x^2-1}}
$$

### derivative of logarithmic function

$$
\frac{d}{dx}(\ln u)=\frac{du}{udx}
\\\\[12pt]
\frac{d}{dx}\ln|x|=\frac{1}{x}
$$

## logarithmic differentiation

take the logarithm of both side of equation and differentiate

## differential $dy$

$$
dy=\frac{dy}{dx}dx
$$

## hyperbolic function

$$
\sinh x=\frac{e^x-e^{-x}}{2}
\\\\[12pt]
\cosh x=\frac{e^x+e^{-x}}{2}
$$

- hyperbolic identity similar to trigonometric identity
- inverse hyperbolic function composed of logarithm
- derivative of hyperbolic function compose of hyperbolic functions
- derivative of inverse hyperbolic function have similar form
    like that of trigonometric function
