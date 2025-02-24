# Chapter 1. Vector spaces

## Standing assumptions

$ C $ is set of complex numbers

$$ C = \{ \alpha: \exist \ a_r, a_i \in \R \ \ \alpha = a_r + a_i \ i \} $$

For each $ \alpha, \beta \in C $ there are defined addition and multiplication operations, as by the book

$ F^n $ is set of vectors over field $ F $

$$ F^n = \{ x: \exist \ x_1, x_2, \ldots, x_n \in F, \ \ \ x = (x_1, x_2, \ldots, x_n) \} $$

For each $ x, y \in F^n $ there are defined addition and multiplication operations, as by the book


## Exercises 1A

page 10

### Exercise 1A.1

Commutativity, page 3

$ \alpha, \beta \in C $

$ \alpha + \beta = \beta + \alpha $

---

$ \alpha + \beta = (a_r + b_r) + (a_i + b_i) \ i $

$ = (b_r + a_r) + (b_i + a_i) \ i $

$ = \beta + \alpha $


### Exercise 1A.2

Additive Associativity, page 3

$ \alpha, \beta, \lambda \in C $

$ (\alpha + \beta) + \lambda = \alpha + (\beta + \lambda) $

---

$ (\alpha + \beta) + \lambda = ((a_r + b_r) + (a_i + b_i) \ i) + (l_r + l_i \ i) $

$ = ((a_r + b_r) + l_r) + ((a_i + b_i) + l_i) \ i $

$ = (a_r + (b_r + l_r)) + (a_i + (b_i + l_i)) \ i $

$ = \alpha + (\beta + \lambda) $


### Exercise 1A.3

Multiplicative Associativity, page 3

$ \alpha, \beta, \lambda \in C $

$ (\alpha \beta) \lambda = \alpha (\beta \lambda) $

---

$ (\alpha \beta) \lambda = ((a_r + a_i \ i)(b_r + b_i \ i))(l_r + l_i \ i) $


$ = ((a_r b_r - a_i b_i) + (a_r b_i + a_i b_r) \ i)(l_r + l_i \ i) $

$ = ((a_r b_r - a_i b_i) l_r - (a_r b_i + a_i b_r) l_i) + ((a_r b_r - a_i b_i) l_i + (a_r b_i + a_i b_r) l_r) \ i $

$ = (a_r b_r l_r - a_i b_i l_r - a_r b_i l_i - a_i b_r l_i) + (a_r b_r l_i - a_i b_i l_i + a_r b_i l_r + a_i b_r l_r) \ i $

$ = (a_r(b_r l_r - b_i l_i) - a_i(b_r l_i + b_i l_r)) + (a_r(b_r l_i + b_i l_r) + a_i(b_r l_r - b_i l_i)) \ i $

$ = (a_r + a_i \ i)((b_r l_r - b_i l_i) + (b_r l_i + b_i l_r) \ i) $

$ = (a_r + a_i \ i)((b_r + b_i \ i)(l_r + l_i \ i)) $

$ = \alpha (\beta \lambda) $

### Exercise 1A.4

Distributivity, page 3

$ \alpha, \beta, \lambda \in C $

$ \lambda  (\alpha + \beta) = \lambda \alpha + \lambda \beta $

---

$ \lambda  (\alpha + \beta) = (l_r + l_i \ i)((a_r + b_r) + (a_i + b_i) \ i) $

$ = (l_r(a_r + b_r) - l_i(a_i + b_i)) + (l_r(a_i + b_i) + l_i(a_r + b_r)) \ i $

$ = (l_r a_r - l_i a_i + l_r b_r - l_i b_i) + (l_r a_i + l_i a_r + l_r b_i + l_i b_r) \ i $

$ = (l_r a_r - l_i a_i) + (l_r b_r - l_i b_i) + (l_r a_i + l_i a_r) \ i + (l_r b_i + l_i b_r) \ i $

$ = ((l_r a_r - l_i a_i) + (l_r a_i + l_i a_r) \ i) + ((l_r b_r - l_i b_i) + (l_r b_i + l_i b_r) \ i) $

$ = \lambda \alpha + \lambda \beta $

### Exercise 1A.5

Additive Inverse, page 3

$ \alpha, \beta \in C $

$ \alpha + \beta = 0 $

---

$ \alpha + \beta = (a_r + b_r) + (a_i + b_i) \ i = 0 $

$ \Rightarrow a_r + b_r = 0 \ \text{ and } \ a_i + b_i = 0 $

$ \Rightarrow b_r = -a_r \ \text{and} \ b_i = -a_i $

$ \Rightarrow \beta = -\alpha $

Is unique

### Exercise 1A.6

Multiplicative inverse, page 3

$ \alpha, \beta \in C $

$ \alpha \ \beta = 1 $

---

$ a_r b_r - a_i b_i + (a_r b_i + a_i b_r) \ i = 1 + 0 \ i $

$ a_r b_r - a_i b_i = 1 $ and $ a_r b_i + a_i b_r = 0 $

$ a_r^2 b_r - a_r a_i b_i + a_i a_r b_i + a_i^2 b_r = a_r$

$ b_r = \frac{a_r}{a_r^2 + a_i^2} $ and $ b_i = -\frac{a_i}{a_r^2 + a_i^2} $

$ \alpha \ \beta = ( a_r + a_i \ i ) ( \frac{a_r}{a_r^2 + a_i^2} - \frac{a_i}{a_r^2 + a_i^2} \ i) $

$ = \left( a_r \cdot \frac{a_r}{a_r^2 + a_i^2} - a_r \cdot \frac{a_i}{a_r^2 + a_i^2} \ i + a_i \cdot \frac{a_r}{a_r^2 + a_i^2} \ i + a_i \cdot \frac{a_i}{a_r^2 + a_i^2} \ i^2 \right) $

$ = \left( \frac{a_r^2}{a_r^2 + a_i^2} - \frac{a_r a_i}{a_r^2 + a_i^2} \ i + \frac{a_r a_i}{a_r^2 + a_i^2} \ i - \frac{a_i^2}{a_r^2 + a_i^2} \right) $

$ = \left( \frac{a_r^2 - a_i^2}{a_r^2 + a_i^2} + \frac{a_r a_i - a_r a_i}{a_r^2 + a_i^2} \ i \right) $

$ = \left( \frac{a_r^2 - a_i^2}{a_r^2 + a_i^2} \right) $

$ = 1 $

### Exercise 1A.7

$ \alpha = \frac{-1 + \sqrt{3} \ i}{2} $

Show that $ \alpha ^3  = 1 $

----

$ \alpha^2 = \left( \frac{-1 + \sqrt{3} \ i}{2} \right) \left( \frac{-1 + \sqrt{3} \ i}{2} \right) $

$ = \frac{1 - 2 \sqrt{3} \ i + 3 i^2}{4} $

$ = \frac{-1 - \sqrt{3} \ i}{2} $

$ \alpha^3 = \left( \frac{-1 - \sqrt{3} \ i}{2} \right) \left( \frac{-1 + \sqrt{3} \ i}{2} \right) $

$ = \frac{(-1 - \sqrt{3} \ i)(-1 + \sqrt{3} \ i)}{4} $

$ = \frac{1 - (\sqrt{3} \ i)^2}{4} $

$ = \frac{1 - 3 i^2}{4} $

$ = 1 $

### Exercise 1A.8

Find square roots of $ i $

---

$ \alpha ^ 2 = i $ and $ \alpha \in C $

$ (a_r + a_i \ i)^2 =  i$

$ a_r ^ 2 - a_i ^2 + 2 a_r a_i \ i  = i $

$ a_r ^ 2 - a_i ^ 2 = 0 $

$ 2 a_r a_i \ i = i $

$ |a_r| = |a_i| $

$ 2 |a_r| |a_i| = 1 $

$ |a_r| = |a_i| = \frac{1}{\sqrt2} $

$ a_r a_i > 0 $

$ a_r = a_i = \frac{1}{\sqrt2} $

or

$ a_r = a_i = - \frac{1}{\sqrt2} $

The square roots of $ i $ are $\frac{1}{\sqrt2} + \frac{1}{\sqrt2} i$ and $-\frac{1}{\sqrt2} - \frac{1}{\sqrt2} i$.


### Exercise 1A.9

Solve for $ x \in F^4 $

$ (4, -3, 1, 7) + 2x = (5, 9, -6, 8) $

---

$ ((-4, 3, -1, -7) + (4, -3, 1, 7)) + 2x = (-4, 3, -1, -7) + (5, 9 -6, 8) $

$ 0 + 2x = (1, 12, -7, 1) $

$ \frac{1}{2} \ 2 x = \frac{1}{2} \ (1, 12, -7, 1) $

$ x = ( \frac{1}{2}, 6, -\frac{7}{2}, \frac{1}{2} ) $

### Exercise 1A.10

Explain why there doesn't exist $ \lambda \in C $ such that

$ \lambda (2 - 3 \ i, 5 + 4 \ i, -6 + 7 \ i) = (12 - 5 \ i, 7 + 22 \ i, -32 - 9 \ i) $

---

$ \lambda (2 - 3 \ i) = 12 - 5 \ i $

$ \lambda (5 + 4 \ i) = 7 + 22 \ i $

$ \lambda (-6 + 7 \ i) = -32 - 9 \ i $

Adding first and second equations together

$ 4 \lambda (2 - 3 \ i) + 3 \lambda (5 + 4 \ i) = 4 (12 - 5 \ i) + 3 (7 + 22 \ i) $

$ \lambda (8 - 12 \ i + 15 + 12 \ i) = 48 - 20 \ i + 21 + 66 \ i $

$ \lambda (23) = 69 + 46 \ i $

$ \lambda = \frac{69 + 46 \ i}{23} $

$ \lambda = 3 + 2 \ i $

Substituting $\lambda = 3 + 2 \ i$ in the third equation:

$ (3 + 2 \ i)(-6 + 7 \ i) = -32 - 9 \ i $

$ = -18 + 21 \ i - 12 \ i - 14 $

$ = -32 + 9 \ i $

$ \ne -32 - 9 \ i $

### Exercise 1A.11

Additive associativity of vectors

$ x, y, z \in F^n $

$ (x + y) + z = x + (y + z) $

---

$ (x + y) + z = ((x_1 + y_1, x_2 + y_2, \ldots, x_n + y_n) + (z_1, z_2, \ldots, z_n)) $

$ = ((x_1 + y_1) + z_1, (x_2 + y_2) + z_2, \ldots, (x_n + y_n) + z_n) $

$ = (x_1 + (y_1 + z_1), x_2 + (y_2 + z_2), \ldots, x_n + (y_n + z_n)) $

$ = (x_1, x_2, \ldots, x_n) + (y_1 + z_1, y_2 + z_2, \ldots, y_n + z_n) $

$ = x + (y + z) $

### Exercise 1A.12

Multiplicative associativity of vectors

$ x \in F^n $ and $ a, b \in F $

$ (a b) x = a (bx) $

---

$ (a b) x = ((a b) x_1, (a b) x_2, \ldots, (a b) x_n) $

$ = (a (b x_1), a (b x_2), \ldots, a (b x_n)) $

$ = a (b x_1, b x_2, \ldots, b x_n) $

$ = a (b x) $

### Exercise 1A.13

Multiplicative identity for vectors

$ x \in F^n $

$ 1 x = x $

---

$ 1 x = (1 x_1, 1 x_2, \ldots, 1 x_n) $

$ = (x_1, x_2, \ldots, x_n) $

$ = x $

### Exercise 1A.14

Distributivity for vectors

$ \lambda \in F $ and $ x, y \in F^n $

$ \lambda (x + y) = \lambda x + \lambda y $

---

$ \lambda (x + y) = \lambda (x_1 + y_1, x_2 + y_2, \ldots, x_n + y_n) $

$ = (\lambda (x_1 + y_1), \lambda (x_2 + y_2), \ldots, \lambda (x_n + y_n)) $

$ = (\lambda x_1 + \lambda y_1, \lambda x_2 + \lambda y_2, \ldots, \lambda x_n + \lambda y_n) $

$ = (\lambda x_1, \lambda x_2, \ldots, \lambda x_n) + (\lambda y_1, \lambda y_2, \ldots, \lambda y_n) $

$ = \lambda x + \lambda y $

### Exercise 1A.15

Distributivity for vectors

$ a, b \in F $ and $ x \in F^n $

$ (a + b) x = ax + bx $

---
$ (a + b) x = ((a + b) x_1, (a + b) x_2, \ldots, (a + b) x_n) $

$ = (a x_1 + b x_1, a x_2 + b x_2, \ldots, a x_n + b x_n) $

$ = (a x_1, a x_2, \ldots, a x_n) + (b x_1, b x_2, \ldots, b x_n) $

$ = a (x_1, x_2, \ldots, x_n) + b (x_1, x_2, \ldots, x_n) $

$ = a x + b x $
