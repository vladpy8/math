# Solving equations cheat sheet

## Definitions

$ F $ is field

$ F^n $ is n-dimensional coordinate vector space

$ B $ is set of functions $ F^n \rightarrow F $

Let $ Sol $ denote a function for set of solutions of equation

$$
Sol(f) = \{ x \in F^n: f(x) = 0 \} \\
f \in B
$$

## Equations addition

Let $ (f + g)(x) = f(x) + g(x) $

Let $ f, g, (f + g) \in B $

Then

$$
(Sol(f) \cap Sol(g)) \subseteq Sol(f + g)
$$

---

For $ \forall x \in (Sol(f) \cap Sol(g)) $

$$
f(x) = 0 \\
g(x) = 0
$$

Adding this equations together

$$
\begin{aligned}

f(x) + g(x) = 0 + 0 &= 0 \\

(f+g)(x) & = 0

\end{aligned}
$$

Which leads to $ x \in Sol(f + g) $

---

Opposite might not be true due to the counterexample below

### Counterexample of equations addition having bigger set of solutions

Given the $ x, y, \alpha, \beta \in F $, $ \alpha \neq 0, \beta \neq 0 $ and  system of two equations:

$$
x \, y - \beta = 0 \\
\alpha \, y - \beta = 0 \\
$$

Adding equations together results in one equation

$$
\begin{aligned}

(x \, y - \beta) - (\alpha \, y - \beta) &= 0 \\
(x - \alpha) \, y &= 0

\end{aligned}
$$

This equation produces new solution $ y = 0 $, which clearly doesn't satisfy none of the original equations above
