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

Opposite might not be true due to counterexample below

### Example of set of solutions of equations addition being bigger

Given the $ x, y, \alpha, \beta \in F $ and  system of two equations:

$$
x \, y - \beta = 0 \\
\alpha \, y - \beta = 0 \\
$$

Adding equations together produces one equation

$$
\begin{aligned}

(x \, y - \beta) - (\alpha \, y - \beta) &= 0
(x - \alpha) \, y &= 0

\end{aligned}
$$


Produces new solution
