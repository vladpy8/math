# Solving equations cheat sheet

## Definitions

Let $ F $ be a field

Let $ S $ be an arbitrary set

Let $ F^S $ be a set of functions $ S \rightarrow F $

Let $ Sol $ denote a function for a set of solutions of an equation

$$
Sol(f) = \{ x \in S: f(x) = 0 \} \\
f \in F^S
$$

## Equations addition

Let $ f, g, (f + g) \in F^S $

Let $ (f + g)(x) = f(x) + g(x) $

Then

$$
(Sol(f) \cap Sol(g)) \subseteq Sol(f + g)
$$

---

$ \forall x \in (Sol(f) \cap Sol(g)) $

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

Which leads to

$$ x \in (Sol(f) \cap Sol(g)) \implies x \in Sol(f + g) $$

Opposite might not be true due to the counterexample below

---

### Counterexample. Equations addition having bigger set of solutions

Let $ \alpha, \beta \in F, \ \alpha \neq 0, \beta \neq 0 $ be two constants

Let $ x, y \in F $ be two variables

Given the system of two equations:

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
