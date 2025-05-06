# Chapter 1. Vector spaces

## Definitions

### Complex numbers

$ \mathbb{C} $ is set of complex numbers

$$ \mathbb{C} = \{ \alpha: \quad \exist! \ a_r, a_i \in \R, \quad \alpha = a_r + a_i \, i \} $$

$$ i^2 = -1 $$

$ \forall \alpha, \beta \in \mathbb{C} $

$$
\begin{aligned}

\alpha + \beta &= (a_r + b_r) + (a_i + b_i) \, i \\

\alpha \beta &= (a_r b_r - a_i b_i) + (a_r b_i + a_i b_r) \, i

\end{aligned}
$$

### Coordinate vectors $ F^n $

Let $ F $ be a field of numbers

$ F^n $ is set of coordinate vectors over field $ F $

$$ F^n = \{ x: \quad \exist! \ x_1, x_2, \ldots, x_n \in F, \quad x = (x_1, x_2, \ldots, x_n) \} $$

$ \forall x, y \in F^n $ and $ \forall \lambda \in F $

$$
\begin{aligned}

x + y &= (x_1 + y_1, x_2 + y_2, \ldots, x_n + y_n) \\

\lambda x &= (\lambda x_1, \lambda x_2, \ldots, \lambda x_n)

\end{aligned}
$$

### Function vectors $ F^S $

Let $ F $ be a field of numbers

Let $ S $ be a set of arbitrary elements

$ F^S $ is set of functions

$$ F^S = \{ S \rightarrow F \} $$

$ \forall f, g \in F^S $, $ \ \forall x \in S $ and $ \forall \lambda \in F $

$$
\begin{aligned}

(f + g)(x) &= f(x) + g(x) \\

(\lambda f)(x) &= \lambda f(x)

\end{aligned}
$$

### Vector space $ V $

Let $ F $ be a field of numbers

Let $ V $ be a vector space over field $ F $ with operations of addition and scalar multiplication which satisfy well-defined properties 1.20 on page 12

## Exercise 1A

page 10

### Exercise 1A.1. Addition commutativity of complex numbers

Also page 3

$ \forall \alpha, \beta \in \mathbb{C} $

$$ \alpha + \beta = \beta + \alpha $$

---

$$
\begin{aligned}

\alpha + \beta &= (a_r + b_r) + (a_i + b_i) \, i \\

&= (b_r + a_r) + (b_i + a_i) \, i \\

&= \beta + \alpha

\end{aligned}
$$

### Exercise 1A.2. Associativity of addition of complex numbers

Also page 3

$ \forall \alpha, \beta, \lambda \in \mathbb{C} $

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


### Exercise 1A.3. Associativity of multiplication of complex numbers

Also page 3

$ \forall \alpha, \beta, \lambda \in \mathbb{C} $

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

### Exercise 1A.4. Distributivity of multiplication over addition of complex numbers

Also page 3

$ \forall \alpha, \beta, \lambda \in \mathbb{C} $

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

Also page 3

$$ \forall \alpha \in \mathbb{C}, \quad \exist \  \beta \in \mathbb{C} : \quad \alpha + \beta = 0 $$

$  $

---

$$ \alpha + \beta = (a_r + b_r) + (a_i + b_i) \, i = 0 $$

One complex number equation leads to two real number equations

$$ a_r + b_r = 0 \\  a_i + b_i = 0 $$

Resolving

$$ b_r = -a_r, \quad b_i = -a_i $$

$$ \beta = (-a_r) + (-a_i) \, i $$

### Exercise 1A.6. Multiplicative inverse of complex numbers

Also page 3

$$ \forall \alpha \in \mathbb{C}, \quad \exist \  \beta \in \mathbb{C} : \quad \alpha \, \beta = 1 $$

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

Solve for  $ \alpha \in \mathbb{C} $

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
|a_r| = |a_i|
$$

Second one leads to

$$
a_r a_i > 0 \\
2 |a_r| |a_i| = 1
$$

Thus

$$ |a_r| = |a_i| = \frac{1}{\sqrt2} \\ $$

And finally

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

Solve for $ x \in {\R}^4 $

$$ (4, -3, 1, 7) + 2x = (5, 9, -6, 8) $$

---
$$
\begin{aligned}

(4, -3, 1, 7) + 2x &= (5, 9, -6, 8) \\

2x &= (1, 12, -7, 1) \\

x &= \left( \frac{1}{2}, 6, -\frac{7}{2}, \frac{1}{2} \right)

\end{aligned}
$$

### Exercise 1A.10

Explain why there doesn't exist $ \lambda \in \mathbb{C} $ such that

$$ \lambda (2 - 3 \, i, 5 + 4 \, i, -6 + 7 \, i) = (12 - 5 \, i, 7 + 22 \, i, -32 - 9 \, i) $$

---

One complex vector equation leads to three complex number equations

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

### Exercise 1A.11. Associativity of addition of vectors

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

### Exercise 1A.12. Associativity of scalar multiplication of vectors

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

### Exercise 1A.14. Distributivity of scalar multiplication over addition of vectors

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

### Exercise 1A.15. Distributivity of addition over scalar multiplication of vectors

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

## 1B Definitions of vector spaces

### Proof of $ F^n $ being vector space

[Definition of $ F^n $](#coordinate-vectors)

#### 1. Commutativity of addition

$ \forall x, y \in F^n $

$$ x + y = y + x $$

---

$$
\begin{aligned}

x + y &= (x_1 + y_1, x_2 + y_2, \ldots, x_n + y_n) \\

&= (y_1 + x_1, y_2 + x_2, \ldots, y_n + x_n) \\

&= y + x

\end{aligned}
$$

#### 2. [Associativity of addition](#exercise-1a11-associativity-of-addition-of-vectors)

#### 3. [Associativity of scalar multiplication](#exercise-1a12-associativity-of-scalar-multiplication-of-vectors)

#### 4. Additive identity

Let $ 0 \in F^n $

$$ 0 = (0, 0, \ldots, 0) $$

$ \forall x \in F^n $

$$ x + 0 = x $$

---

$$
\begin{aligned}

x + 0 &= (x_1 + 0, x_2 + 0, \ldots, x_n + 0) \\

&= (x_1, x_2, \ldots, x_n) \\

&= x

\end{aligned}
$$

#### 5. Additive inverse

$$ \forall x \in F^n, \quad \exist y \in F^n, \quad x + y = 0 $$

---

Let

$$ y = (-x_1, -x_2, \ldots, -x_n) $$

Then

$$
\begin{aligned}

x + y &= (x_1 + (-x_1), x_2 + (-x_2), \ldots, x_n + (-x_n)) \\

&= (0, 0, \ldots, 0) \\

&= 0

\end{aligned}
$$

#### 6. [Multiplicative identity](#exercise-1a13-multiplicative-identity-of-vectors)

#### 7. [Distributivity of scalar multiplication over addition](#exercise-1a14-distributivity-of-scalar-multiplication-over-addition-of-vectors)

#### 8. [Distributivity of addition over scalar multiplication](#exercise-1a15-distributivity-of-addition-over-scalar-multiplication-of-vectors)

### Proof of $ F^∞ $ being vector space

Repeat proofs for $ F^n $ being vector space omitting the last element which comes after "$ \ldots $" everywhere explicit form of vector is used

### Proof of $ F^S $ being vector space

[Definition of $ F^S $](#function-vectors)

#### 1. Commutativity of addition

$ \forall f, g \in F^S $

$$ f + g = g + f $$

---

$ \forall x \in S $

$$
\begin{aligned}

(f + g)(x) &= f(x) + g(x) \\

&= g(x) + f(x) \\

&= (g + f)(x)

\end{aligned}
$$

#### 2. Associativity of addition

$ \forall f, g, h \in F^S $

$$ (f + g) + h = f + (g + h) $$

---

$ \forall x \in S $

$$
\begin{aligned}

((f + g) + h)(x) &= (f + g)(x) + h(x) \\
&= (f(x) + g(x)) + h(x) \\
&= f(x) + (g(x) + h(x)) \\
&= f(x) + (g + h)(x) \\
&= (f + (g + h))(x) \\

\end{aligned}
$$

#### 3. Associativity of scalar multiplication

$ \forall f \in F^S $ and $ \forall a, b \in F $

$$ (a b) f = a (b f) $$

---

$ \forall x \in S $

$$
\begin{aligned}

((a b) f)(x) &= (a b) f(x) \\

&= a (b f(x)) \\

&= (a (b f))(x)

\end{aligned}
$$

#### 4. Additive identity

Let $ 0 \in F^S $

$$ 0(x) = 0, \quad \forall x \in S $$

$ \forall f \in F^S $

$$ f + 0 = f $$

---

$ \forall x \in S $

$$
\begin{aligned}

(f + 0)(x) &= f(x) + 0(x) \\

&= f(x) + 0 \\

&= f(x)

\end{aligned}
$$

#### 5. Additive inverse

$$ \forall f \in F^S, \quad \exist g \in F^S, \quad f + g = 0 $$

---

Let $ g \in F^S $

$$ g(x) = -f(x), \quad \forall x \in S $$

Then

$$
\begin{aligned}

(f + g)(x) &= f(x) + g(x) \\

&= f(x) + (-f(x)) \\

&= 0 \\

\end{aligned}
$$

Thus, $ f + g = 0 $.

#### 6. Multiplicative identity

$ \forall f \in F^S $

$$ 1 f = f $$

---

$ \forall x \in S $

$$
\begin{aligned}

(1 f)(x) &= 1 \cdot f(x) \\

&= f(x)

\end{aligned}
$$

#### 7. Distributivity of scalar multiplication over addition

$ \forall f, g \in F^S $ and $ \forall a \in F $

$$ a (f + g) = a f + a g $$

---

$ \forall x \in S $

$$
\begin{aligned}

(a (f + g))(x) &= a (f + g)(x) \\

&= a (f(x) + g(x)) \\

&= a f(x) + a g(x) \\

&= (a f + a g)(x)

\end{aligned}
$$

#### 8. Distributivity of addition over scalar multiplication

$ \forall f \in F^S $ and $ \forall a, b \in F $

$$ (a + b) f = a f + b f $$

---

$ \forall x \in S $

$$
\begin{aligned}

((a + b) f)(x) &= (a + b) f(x) \\

&= a f(x) + b f(x) \\

&= (a f + b f)(x)

\end{aligned}
$$

## Exercise 1B

### Exercise 1B.1 Inverse of inverse

Let $ x \in V $

$$ -(-x) = x $$

---

$$
\begin{aligned}

-(-x) &= -(-x) + 0 \\

&= -(-x) + (x + (-x)) \\

&= (-(-x) + (-x)) + x \\

&= 0 + x \\

&= x

\end{aligned}
$$

### Exercise 1B.2

Let $ v \in V $ and $ a \in F $

If $ a v = 0 $ then either $ a = 0 $ or $ v = 0 $ (or both)

---

When $ a = 0 $, then according to page 15 (1.30)

$$ \forall v \in V, \quad a v = 0 $$

When $ a \ne 0 $, then according to page 15 (1.31)

$$
\begin{aligned}

0 &= \frac{1}{a} \, 0 = \frac{1}{a} \, (a v) = (\frac{1}{a} \, a) \ v = 1 v \\
&= v

\end{aligned}
$$

### Scalar multiplier equality

Let $ V $ be a vector space over field $ F $ which is not identical to $ \{0 \} $

$$ \forall u \in V, \ u \neq 0, \quad a, b \in F, \quad a u = b u \implies a = b $$

---

$$ 0 = a u + (-(b u)) = (a + (-b)) u $$

Which according to [Exercise 1B.2](#exercise-1b2) leads to

$$
a + (-b) = 0 \\
a = b
$$


### Exercise 1B.3

Let $ v, w \in V $

$$ \exist ! \ x \in V : \quad v + 3 x = w $$

---

Let $ y \in V $

$$ v + 3 y = w $$

Then

$$
\begin{aligned}

0 &= w - w = (v + 3 x) - (v + 3 y) = 3 x - 3 y \\
&= 3 (x - y) \\

\end{aligned}
$$

Which according to [Exercise 1B.2](#exercise-1b2) means

$$
x - y = 0 \\
x = y
$$

### Exercise 1B.4

Let $ V_{\empty} = \{ \} $

Then $ V_{\empty} $ couldn't be a vector space because it doesn't contain an additive identity

### Exercise 1B.5

Let $ V_m \subseteq V $

Let $ V_m $ satisfy a modified property *instead* of well-defined additive identity as stated in 1.20 on page 12

$$ \forall v \in V_m \quad 0 v = 0 $$

Then

$$ V_m = V $$

---

### Exercise 1B.6



Let $ \infty $ and $ -\infty $ denote two distinct objects, neither of which is in $ \R $. Define an addition and scalar multiplication on $ \R \cup \{\infty, -\infty\} $ as you could guess from the notation. Specifically, the sum and product of two real numbers is as usual, and for $ t \in \R $ define
$$t \infty = \begin{cases} -\infty & \text{if } t < 0, \\ 0 & \text{if } t = 0, \\ \infty & \text{if } t > 0, \end{cases} \quad t (-\infty) = \begin{cases} \infty & \text{if } t < 0, \\ 0 & \text{if } t = 0, \\ -\infty & \text{if } t > 0, \end{cases}$$
and
$$t + \infty = \infty + t = \infty + \infty = \infty,$$
$$t + (-\infty) = (-\infty) + t = (-\infty) + (-\infty) = -\infty,$$
$$\infty + (-\infty) = (-\infty) + \infty = 0.$$
With these operations of addition and scalar multiplication, is $ \R \cup \{\infty, -\infty\} $ a vector space over $ \R $? Explain.



Let $ R_{∞} = R \cup \{ \infty, -\infty \} $

---
