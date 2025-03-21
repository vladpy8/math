# Chapter 1. Vector spaces

## Definitions

### Complex numbers

$ C $ is set of complex numbers

$$ C = \{ \alpha: \quad \exist! \ a_r, a_i \in \R, \quad \alpha = a_r + a_i \, i \} $$

$$ i^2 = -1 $$

$ \forall \alpha, \beta \in C $

$$
\begin{aligned}

\alpha + \beta &= (a_r + b_r) + (a_i + b_i) \, i \\

\alpha \beta &= (a_r b_r - a_i b_i) + (a_r b_i + a_i b_r) \, i

\end{aligned}
$$

### Vectors

$ F^n $ is set of vectors over field $ F $

$$ F^n = \{ x: \quad \exist! \ x_1, x_2, \ldots, x_n \in F, \quad x = (x_1, x_2, \ldots, x_n) \} $$

$ \forall x, y \in F^n $ and $ \lambda \in F $

$$
\begin{aligned}

x + y &= (x_1 + y_1, x_2 + y_2, \ldots, x_n + y_n) \\

\lambda x &= (\lambda x_1, \lambda x_2, \ldots, \lambda x_n)

\end{aligned}
$$


## Exercises 1A

page 10

### Exercise 1A.1. Commutativity of complex numbers

page 3

$ \forall \alpha, \beta \in C $

$$ \alpha + \beta = \beta + \alpha $$

---

$$
\begin{aligned}

\alpha + \beta &= (a_r + b_r) + (a_i + b_i) \, i \\

&= (b_r + a_r) + (b_i + a_i) \, i \\

&= \beta + \alpha

\end{aligned}
$$

### Exercise 1A.2. Additive associativity of complex numbers

page 3

$ \forall \alpha, \beta, \lambda \in C $

$$ (\alpha + \beta) + \lambda = \alpha + (\beta + \lambda) $$

---

$$
\begin{aligned}

(\alpha + \beta) + \lambda &= ((a_r + b_r) + (a_i + b_i) \, i) + (l_r + l_i \, i) \\

&= ((a_r + b_r) + l_r) + ((a_i + b_i) + l_i) \, i \\

&= (a_r + (b_r + l_r)) + (a_i + (b_i + l_i)) \, i \\

&= \alpha + (\beta + \lambda)

\end{aligned}
$$


### Exercise 1A.3. Multiplicative associativity of complex numbers

page 3

$ \forall \alpha, \beta, \lambda \in C $

$$ (\alpha \beta) \lambda = \alpha (\beta \lambda) $$

---
$$
\begin{aligned}

(\alpha \beta) \lambda &= ((a_r + a_i \, i)(b_r + b_i \, i))(l_r + l_i \, i) \\

&= ((a_r b_r - a_i b_i) + (a_r b_i + a_i b_r) \, i)(l_r + l_i \, i) \\

&= ((a_r b_r - a_i b_i) l_r - (a_r b_i + a_i b_r) l_i) + ((a_r b_r - a_i b_i) l_i + (a_r b_i + a_i b_r) l_r) \, i \\

&= (a_r b_r l_r - a_i b_i l_r - a_r b_i l_i - a_i b_r l_i) + (a_r b_r l_i - a_i b_i l_i + a_r b_i l_r + a_i b_r l_r) \, i \\

&= (a_r(b_r l_r - b_i l_i) - a_i(b_r l_i + b_i l_r)) + (a_r(b_r l_i + b_i l_r) + a_i(b_r l_r - b_i l_i)) \, i \\

&= (a_r + a_i \, i)((b_r l_r - b_i l_i) + (b_r l_i + b_i l_r) \, i) \\

&= (a_r + a_i \, i)((b_r + b_i \, i)(l_r + l_i \, i)) \\

&= \alpha (\beta \lambda)

\end{aligned}
$$

### Exercise 1A.4. Distributivity of addition and multiplication of complex numbers

page 3

$ \forall \alpha, \beta, \lambda \in C $

$$\lambda  (\alpha + \beta) = \lambda \alpha + \lambda \beta $$

---
$$
\begin{aligned}

\lambda  (\alpha + \beta) &= (l_r + l_i \, i)((a_r + b_r) + (a_i + b_i) \, i) \\

&= (l_r(a_r + b_r) - l_i(a_i + b_i)) + (l_r(a_i + b_i) + l_i(a_r + b_r)) \, i \\

&= (l_r a_r - l_i a_i + l_r b_r - l_i b_i) + (l_r a_i + l_i a_r + l_r b_i + l_i b_r) \, i \\

&= (l_r a_r - l_i a_i) + (l_r b_r - l_i b_i) + (l_r a_i + l_i a_r) \, i + (l_r b_i + l_i b_r) \, i \\

&= ((l_r a_r - l_i a_i) + (l_r a_i + l_i a_r) \, i) + ((l_r b_r - l_i b_i) + (l_r b_i + l_i b_r) \, i) \\

&= \lambda \alpha + \lambda \beta

\end{aligned}
$$

### Exercise 1A.5. Additive inverse of complex numbers

page 3

$$ \forall \alpha \in C, \quad \exist \  \beta \in C : \quad \alpha + \beta = 0 $$

$  $

---

$$ \alpha + \beta = (a_r + b_r) + (a_i + b_i) \, i = 0 $$

One complex number equation leads to two real number equations

$$ a_r + b_r = 0 \\  a_i + b_i = 0 $$

Resolving

$$ b_r = -a_r, \quad b_i = -a_i $$

$$ \beta = (-a_r) + (-a_i) \, i $$

Verification is redundant

### Exercise 1A.6. Multiplicative inverse of complex numbers

page 3

$$ \forall \alpha \in C, \quad \exist \  \beta \in C : \quad \alpha \, \beta = 1 $$

---

$$ \alpha \beta = a_r b_r - a_i b_i + (a_r b_i + a_i b_r) \, i = 1 + 0 \, i $$

One complex number equation leads to two real number equations

$$
a_r b_r - a_i b_i = 1 \\
a_r b_i + a_i b_r = 0
$$

Adding this equations together after multiplication of the first one by $ a_r $ and the second one by $ a_i $

$$ a_r^2 b_r - a_r a_i b_i + a_i a_r b_i + a_i^2 b_r = a_r $$

Resolving $ b_r $ and $ b_i $

$$
b_r = \frac{a_r}{a_r^2 + a_i^2} \\
b_i = -\frac{a_i}{a_r^2 + a_i^2}
$$

Verifying

$$
\begin{aligned}

\alpha \beta &= ( a_r + a_i \, i ) \left( \frac{a_r}{a_r^2 + a_i^2} - \frac{a_i}{a_r^2 + a_i^2} \, i \right) \\

&= \left( a_r \cdot \frac{a_r}{a_r^2 + a_i^2} - a_r \cdot \frac{a_i}{a_r^2 + a_i^2} \, i + a_i \cdot \frac{a_r}{a_r^2 + a_i^2} \, i + a_i \cdot \frac{a_i}{a_r^2 + a_i^2} \, i^2 \right) \\

&= \left( \frac{a_r^2}{a_r^2 + a_i^2} - \frac{a_r a_i}{a_r^2 + a_i^2} \, i + \frac{a_r a_i}{a_r^2 + a_i^2} \, i - \frac{a_i^2}{a_r^2 + a_i^2} \right) \\

&= \left( \frac{a_r^2 - a_i^2}{a_r^2 + a_i^2} + \frac{a_r a_i - a_r a_i}{a_r^2 + a_i^2} \, i \right) \\

&= \left( \frac{a_r^2 - a_i^2}{a_r^2 + a_i^2} \right) \\

&= 1

\end{aligned}
$$

### Exercise 1A.7

$ \alpha = \frac{-1 + \sqrt{3} \, i}{2} $

Prove that $ \alpha ^3  = 1 $

---

$$
\begin{aligned}

\alpha^2 &= \left( \frac{-1 + \sqrt{3} \, i}{2} \right) \left( \frac{-1 + \sqrt{3} \, i}{2} \right) \\

&= \frac{1 - 2 \sqrt{3} \, i + 3 i^2}{4} \\

&= \frac{-1 - \sqrt{3} \, i}{2}

\end{aligned}
$$

$$
\begin{aligned}
\alpha^3 &= \left( \frac{-1 - \sqrt{3} \, i}{2} \right) \left( \frac{-1 + \sqrt{3} \, i}{2} \right) \\

&= \frac{(-1 - \sqrt{3} \, i)(-1 + \sqrt{3} \, i)}{4} \\

&= \frac{1 - (\sqrt{3} \, i)^2}{4} \\

&= \frac{1 - 3 i^2}{4} \\

&= 1

\end{aligned}
$$

### Exercise 1A.8. Square roots of $ i $

Solve for  $ \alpha \in C $

$$ \alpha^2 = i $$

---

$$
\begin{aligned}

(a_r + a_i \, i)^2 = i \\

a_r^2 - a_i^2 + 2 a_r a_i \, i = i \\

\end{aligned}
$$

One complex number equation leads to two real number equations

$$
a_r^2 - a_i^2 = 0 \\
2 a_r a_i \, i = i
$$

From the first equation follows

$$
|a_r| = |a_i| \\
a_r a_i > 0
$$

Second one leads to

$$ 2 |a_r| |a_i| = 1 $$

Thus

$$ |a_r| = |a_i| = \frac{1}{\sqrt2} \\ $$

$$ a_r = a_i = \frac{1}{\sqrt2} \quad \text{or} \quad a_r = a_i = - \frac{1}{\sqrt2} $$

The square roots of $ i $ are

$$ \frac{1}{\sqrt2} + \frac{1}{\sqrt2} \, i \quad \ \text{or} \quad -\frac{1}{\sqrt2} - \frac{1}{\sqrt2} \, i $$

Verifying

$$
\begin{aligned}

\left( \frac{1}{\sqrt2} + \frac{1}{\sqrt2} \, i \right)^2 &= \left( \frac{1}{\sqrt2} \right)^2 + 2 \left( \frac{1}{\sqrt2} \right) \left( \frac{1}{\sqrt2} \, i \right) + \left( \frac{1}{\sqrt2} \, i \right)^2 \\

&= \frac{1}{2} + \frac{2}{2} \, i - \frac{1}{2} \\

&= i

\end{aligned}
$$


$$
\begin{aligned}

\left( -\frac{1}{\sqrt2} - \frac{1}{\sqrt2} \, i \right)^2 &= \left( -\frac{1}{\sqrt2} \right)^2 + 2 \left( -\frac{1}{\sqrt2} \right) \left( -\frac{1}{\sqrt2} \, i \right) + \left( -\frac{1}{\sqrt2} \, i \right)^2 \\

&= \frac{1}{2} + \frac{2}{2} \, i - \frac{1}{2} \\

&= i

\end{aligned}
$$

### Exercise 1A.9

Solve for $ x \in F^4 $

$ (4, -3, 1, 7) + 2x = (5, 9, -6, 8) $

---
$$
\begin{aligned}

(4, -3, 1, 7) + 2x &= (5, 9, -6, 8) \\

2x &= (1, 12, -7, 1) \\

x &= \left( \frac{1}{2}, 6, -\frac{7}{2}, \frac{1}{2} \right)

\end{aligned}
$$

### Exercise 1A.10

Explain why there doesn't exist $ \lambda \in C $ such that

$ \lambda (2 - 3 \, i, 5 + 4 \, i, -6 + 7 \, i) = (12 - 5 \, i, 7 + 22 \, i, -32 - 9 \, i) $

---

One complex number equation leads to two real number equations

$$
\begin{aligned}

\lambda (2 - 3 \, i) &= 12 - 5 \, i \\

\lambda (5 + 4 \, i) &= 7 + 22 \, i \\

\lambda (-6 + 7 \, i) &= -32 - 9 \, i \\

\end{aligned}
$$

Adding first and second equations together:

$$
\begin{aligned}

4 \lambda (2 - 3 \, i) + 3 \lambda (5 + 4 \, i) &= 4 (12 - 5 \, i) + 3 (7 + 22 \, i) \\

\lambda (8 - 12 \, i + 15 + 12 \, i) &= 48 - 20 \, i + 21 + 66 \, i \\

\lambda (23) &= 69 + 46 \, i \\

\lambda &= \frac{69 + 46 \, i}{23} \\

\lambda &= 3 + 2 \, i \\

\end{aligned}
$$

Substituting $\lambda = 3 + 2 \, i$ in the left part of the third equation:

$$
\begin{aligned}

(3 + 2 \, i)(-6 + 7 \, i) &= -18 + 21 \, i - 12 \, i - 14 \\

&= -32 + 9 \, i \\

&\ne -32 - 9 \, i

\end{aligned}
$$

### Exercise 1A.11. Additive associativity of vectors

$ \forall x, y, z \in F^n $

$$ (x + y) + z = x + (y + z) $$

---

$$
\begin{aligned}

(x + y) + z &= ((x_1 + y_1, x_2 + y_2, \ldots, x_n + y_n) + (z_1, z_2, \ldots, z_n)) \\

&= ((x_1 + y_1) + z_1, (x_2 + y_2) + z_2, \ldots, (x_n + y_n) + z_n) \\

&= (x_1 + (y_1 + z_1), x_2 + (y_2 + z_2), \ldots, x_n + (y_n + z_n)) \\

&= (x_1, x_2, \ldots, x_n) + (y_1 + z_1, y_2 + z_2, \ldots, y_n + z_n) \\

&= x + (y + z)

\end{aligned}
$$

### Exercise 1A.12. Multiplicative associativity of vectors

$ \forall x \in F^n $ and $ \forall a, b \in F $

$$ (a b) x = a (bx) $$

---

$$
\begin{aligned}

(a b) x &= ((a b) x_1, (a b) x_2, \ldots, (a b) x_n) \\

&= (a (b x_1), a (b x_2), \ldots, a (b x_n)) \\

&= a (b x_1, b x_2, \ldots, b x_n) \\

&= a (b x)

\end{aligned}
$$

### Exercise 1A.13. Multiplicative identity of vectors

$ \forall x \in F^n $

$$ 1 x = x $$

---

$$
\begin{aligned}

1 x &= (1 x_1, 1 x_2, \ldots, 1 x_n) \\

&= (x_1, x_2, \ldots, x_n) \\

&= x

\end{aligned}
$$

### Exercise 1A.14. Distributivity of vectors

$ \forall \lambda \in F $ and $ \forall x, y \in F^n $

$$ \lambda (x + y) = \lambda x + \lambda y $$

---

$$
\begin{aligned}

\lambda (x + y) &= \lambda (x_1 + y_1, x_2 + y_2, \ldots, x_n + y_n) \\

&= (\lambda (x_1 + y_1), \lambda (x_2 + y_2), \lambda (x_n + y_n)) \\

&= (\lambda x_1 + \lambda y_1, \lambda x_2 + \lambda y_2, \ldots, \lambda x_n + \lambda y_n) \\

&= (\lambda x_1, \lambda x_2, \ldots, \lambda x_n) + (\lambda y_1, \lambda y_2, \ldots, \lambda y_n) \\

&= \lambda x + \lambda y

\end{aligned}
$$

### Exercise 1A.15. Distributivity of vectors

$ \forall a, b \in F $ and $ \forall x \in F^n $

$$ (a + b) x = ax + bx $$

---

$$
\begin{aligned}

(a + b) x &= ((a + b) x_1, (a + b) x_2, \ldots, (a + b) x_n) \\

&= (a x_1 + b x_1, a x_2 + b x_2, \ldots, a x_n + b x_n) \\

&= (a x_1, a x_2, \ldots, a x_n) + (b x_1, b x_2, \ldots, b x_n) \\

&= a (x_1, x_2, \ldots, x_n) + b (x_1, x_2, \ldots, x_n) \\

&= a x + b x

\end{aligned}
$$
