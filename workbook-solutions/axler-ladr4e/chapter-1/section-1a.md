# Chapter 1. Vector spaces

## Section 1A. $ \R^n $ and $ {\mathbb{C}}^n $

### Relevant definitions

#### Definition 1. Complex numbers

Page reference 2

$ \mathbb{C} $ is the set of complex numbers:
$$ \mathbb{C} = \{ \alpha : \quad \exist! \ a_r, a_i \in \R, \quad \alpha = a_r + a_i \, i \} $$

The imaginary unit $ i $ satisfies:
$$ i^2 = -1 $$

$ \forall \alpha, \beta \in \mathbb{C} $:
$$
\begin{aligned}
\alpha + \beta &= (a_r + b_r) + (a_i + b_i) \, i \\
\alpha \beta &= (a_r b_r - a_i b_i) + (a_r b_i + a_i b_r) \, i
\end{aligned}
$$

#### Definition 2. Coordinate vectors $ F^n $

Page reference 6

Let $ F $ be a field of numbers.

$ F^n $ is the set of coordinate vectors over field $ F $:
$$ F^n = \{ x : \quad \exist! \ x_1, x_2, \ldots, x_n \in F, \quad x = (x_1, x_2, \ldots, x_n) \} $$

$ \forall x, y \in F^n $ and $ \forall \lambda \in F $:
$$
\begin{aligned}
x + y &= (x_1 + y_1, x_2 + y_2, \ldots, x_n + y_n) \\
\lambda x &= (\lambda x_1, \lambda x_2, \ldots, \lambda x_n)
\end{aligned}
$$

### Exercises 1A

Page reference 10

#### Exercise 1A.1. Commutativity of addition of complex numbers

Page reference 10

$ \forall \alpha, \beta \in \mathbb{C} $:
$$ \alpha + \beta = \beta + \alpha $$

<details>
<summary>Proof</summary>

Let $ \alpha = a_r + a_i \, i $ and $ \beta = b_r + b_i \, i $.

$$
\begin{aligned}

\alpha + \beta &= (a_r + b_r) + (a_i + b_i) \, i \\

&= (b_r + a_r) + (b_i + a_i) \, i \\

&= \beta + \alpha

\end{aligned}
$$

</details>

#### Exercise 1A.2. Associativity of addition of complex numbers

Page reference 10

$ \forall \alpha, \beta, \lambda \in \mathbb{C} $:
$$ (\alpha + \beta) + \lambda = \alpha + (\beta + \lambda) $$

<details>
<summary>Proof</summary>

Let $ \alpha = a_r + a_i \, i $, $ \beta = b_r + b_i \, i $, and $ \lambda = l_r + l_i \, i $.

$$
\begin{aligned}

(\alpha + \beta) + \lambda &= ((a_r + b_r) + (a_i + b_i) \, i) + (l_r + l_i \, i) \\

&= ((a_r + b_r) + l_r) + ((a_i + b_i) + l_i) \, i \\

&= (a_r + (b_r + l_r)) + (a_i + (b_i + l_i)) \, i \\

&= (a_r + a_i \, i) + ((b_r + b_i \, i) + (l_r + l_i \, i)) \\

&= \alpha + (\beta + \lambda)

\end{aligned}
$$

</details>

#### Exercise 1A.3. Associativity of multiplication of complex numbers

Page reference 10

$ \forall \alpha, \beta, \lambda \in \mathbb{C} $:
$$ (\alpha \beta) \lambda = \alpha (\beta \lambda) $$

<details>
<summary>Proof</summary>

Let $ \alpha = a_r + a_i \, i $, $ \beta = b_r + b_i \, i $, and $ \lambda = l_r + l_i \, i $.

$$
\begin{aligned}

(\alpha \beta) \lambda &= ((a_r + a_i \, i)(b_r + b_i \, i))(l_r + l_i \, i) \\

&= ((a_r b_r - a_i b_i) + (a_r b_i + a_i b_r) \, i)(l_r + l_i \, i) \\

&= ((a_r b_r - a_i b_i) l_r - (a_r b_i + a_i b_r) l_i) + ((a_r b_r - a_i b_i) l_i + (a_r b_i + a_i b_r) l_r) \, i \\

&= (a_r b_r l_r - a_i b_i l_r - a_r b_i l_i - a_i b_r l_i) + (a_r b_r l_i - a_i b_i l_i + a_r b_i l_r + a_i b_r l_r) \, i \\

&= (a_r(b_r l_r - b_i l_i) - a_i(b_r l_i + b_i l_r)) + (a_r(b_r l_i + b_i l_r) + a_i(b_r l_r - b_i l_i)) \, i \\

&= (a_r + a_i \, i) ((b_r l_r - b_i l_i) + (b_r l_i + b_i l_r) \, i) \\

&= (a_r + a_i \, i) ((b_r + b_i \, i)(l_r + l_i \, i)) \\

&= \alpha (\beta \lambda)

\end{aligned}
$$

</details>

#### Exercise 1A.4. Distributivity of multiplication over addition of complex numbers

Page reference 10

$ \forall \alpha, \beta, \lambda \in \mathbb{C} $:
$$ \lambda (\alpha + \beta) = \lambda \alpha + \lambda \beta $$

<details>
<summary>Proof</summary>

Let $ \alpha = a_r + a_i \, i $, $ \beta = b_r + b_i \, i $, and $ \lambda = l_r + l_i \, i $.

$$
\begin{aligned}

\lambda (\alpha + \beta) &= (l_r + l_i \, i) ((a_r + b_r) + (a_i + b_i) \, i) \\

&= (l_r (a_r + b_r) - l_i (a_i + b_i)) + (l_r (a_i + b_i) + l_i (a_r + b_r)) \, i \\

&= (l_r a_r - l_i a_i + l_r b_r - l_i b_i) + (l_r a_i + l_i a_r + l_r b_i + l_i b_r) \, i \\

&= (l_r a_r - l_i a_i) + (l_r b_r - l_i b_i) + (l_r a_i + l_i a_r) \, i + (l_r b_i + l_i b_r) \, i \\

&= ((l_r a_r - l_i a_i) + (l_r a_i + l_i a_r) \, i) + ((l_r b_r - l_i b_i) + (l_r b_i + l_i b_r) \, i) \\

&= \lambda \alpha + \lambda \beta

\end{aligned}
$$

</details>

#### Exercise 1A.5. Additive inverse of complex numbers

Page reference 10

$$ \forall \alpha \in \mathbb{C} , \quad \exist \ \beta \in \mathbb{C} : \quad \alpha + \beta = 0 $$

<details>
<summary>Proof</summary>

Let $ \alpha = a_r + a_i \, i $. Seek $ \beta = b_r + b_i \, i $.

$$ (a_r + b_r) + (a_i + b_i) \, i = 0 + 0 \, i $$

This yields a system of real equations:
$$
\begin{aligned}
a_r + b_r &= 0 \\
a_i + b_i &= 0
\end{aligned}
$$

Solving for $ b_r $ and $ b_i $:
$$
\begin{aligned}
b_r &= -a_r \\
b_i &= -a_i
\end{aligned}
$$

Thus,
$$ \beta = -a_r - a_i \, i $$

</details>

#### Exercise 1A.6. Multiplicative inverse of complex numbers

Page reference 10

$$ \forall \alpha \in \mathbb{C} , \quad \alpha \neq 0 , \quad \exist \ \beta \in \mathbb{C} : \quad \alpha \, \beta = 1 $$

<details>
<summary>Proof</summary>

Let $ \alpha = a_r + a_i \, i , \ a_r \neq 0, \ a_i \neq 0 $. Let $ \beta = b_r + b_i \, i $.

$$ (a_r b_r - a_i b_i) + (a_r b_i + a_i b_r) \, i = 1 + 0 \, i $$

This yields a system of real equations:
$$
\begin{aligned}
a_r b_r - a_i b_i &= 1 \\
a_i b_r + a_r b_i &= 0
\end{aligned}
$$

Multiplying the first equation by $ a_r $, the second by $ a_i $, and adding them together:
$$ a_r^2 b_r - a_r a_i b_i + a_i a_r b_i + a_i^2 b_r = a_r $$

Resolving $ b_r $ and $ b_i $:
$$
b_r = \frac{a_r}{a_r^2 + a_i^2} \\
b_i = -\frac{a_i}{a_r^2 + a_i^2}
$$

Verifying:

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

</details>

#### Exercise 1A.7. Cube root of 1

Page reference 10

Let
$$ \alpha = \frac{-1 + \sqrt{3} \, i}{2} $$

Then:
$$ \alpha^3 = 1 $$

<details>
<summary>Proof</summary>

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

</details>

#### Exercise 1A.8. Square roots of $ i $

Page reference 10

Solve for $ \alpha \in \mathbb{C} $:
$$ \alpha^2 = i $$

<details>
<summary>Solution</summary>

Let $ \alpha = a_r + a_i \, i $.

$$
\begin{aligned}
(a_r + a_i \, i)^2 &= i \\
a_r^2 - a_i^2 + 2 a_r a_i \, i &= i \\
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

Thus,
$$ |a_r| = |a_i| = \frac{1}{\sqrt2} \\ $$

And finally,
$$ a_r = a_i = \frac{1}{\sqrt2} \quad \text{or} \quad a_r = a_i = - \frac{1}{\sqrt2} $$

The square roots of $ i $ are:
$$ \frac{1}{\sqrt2} + \frac{1}{\sqrt2} \, i \quad \ \text{or} \quad -\frac{1}{\sqrt2} - \frac{1}{\sqrt2} \, i $$

Verifying each of the solutions.

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

</details>

#### Exercise 1A.9

Page reference 10

Solve for $ x \in \R^4 $:
$$ (4, -3, 1, 7) + 2x = (5, 9, -6, 8) $$

<details>
<summary>Solution</summary>

Let $ x = (x_1, x_2, x_3, x_4) $.

$$
\begin{aligned}

(4, -3, 1, 7) + 2x &= (5, 9, -6, 8) \\

2x &= (1, 12, -7, 1) \\

x &= \left( \frac{1}{2}, 6, -\frac{7}{2}, \frac{1}{2} \right)

\end{aligned}
$$

</details>

#### Exercise 1A.10

Page reference 10

Explain why $ \not\exist \ \lambda \in \mathbb{C} $:
$$ \lambda (2 - 3 \, i, 5 + 4 \, i, -6 + 7 \, i) = (12 - 5 \, i, 7 + 22 \, i, -32 - 9 \, i) $$

<details>
<summary>Explanation</summary>

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

</details>

#### Exercise 1A.11. Associativity of addition of vectors

Page reference 11

$ \forall x, y, z \in F^n $:
$$ (x + y) + z = x + (y + z) $$

<details>
<summary>Proof</summary>

Let $ x = (x_1, x_2, \ldots, x_n) $, $ y = (y_1, y_2, \ldots, y_n) $, and $ z = (z_1, z_2, \ldots, z_n) $.

$$
\begin{aligned}

(x + y) + z &= ((x_1 + y_1, x_2 + y_2, \ldots, x_n + y_n) + (z_1, z_2, \ldots, z_n)) \\

&= ((x_1 + y_1) + z_1, (x_2 + y_2) + z_2, \ldots, (x_n + y_n) + z_n) \\

&= (x_1 + (y_1 + z_1), x_2 + (y_2 + z_2), \ldots, x_n + (y_n + z_n)) \\

&= (x_1, x_2, \ldots, x_n) + (y_1 + z_1, y_2 + z_2, \ldots, y_n + z_n) \\

&= x + (y + z)

\end{aligned}
$$

</details>

#### Exercise 1A.12. Associativity of scalar multiplication of vectors

Page reference 11

$ \forall x \in F^n $ and $ \forall a, b \in F $:
$$ (a b) x = a (b x) $$

<details>
<summary>Proof</summary>

Let $ x = (x_1, x_2, \ldots, x_n) $.

$$
\begin{aligned}

(a b) x &= ((a b) x_1, (a b) x_2, \ldots, (a b) x_n) \\

&= (a (b x_1), a (b x_2), \ldots, a (b x_n)) \\

&= a (b x_1, b x_2, \ldots, b x_n) \\

&= a (b x)

\end{aligned}
$$

</details>

#### Exercise 1A.13. Multiplicative identity of vectors

Page reference 11

$ \forall x \in F^n $:
$$ 1 x = x $$

<details>
<summary>Proof</summary>

Let $ x = (x_1, x_2, \ldots, x_n) $.

$$
\begin{aligned}

1 x &= (1 x_1, 1 x_2, \ldots, 1 x_n) \\

&= (x_1, x_2, \ldots, x_n) \\

&= x

\end{aligned}
$$

</details>

#### Exercise 1A.14. Distributivity of scalar multiplication over addition of vectors

Page reference 11

$ \forall \lambda \in F $ and $ \forall x, y \in F^n $:
$$ \lambda (x + y) = \lambda x + \lambda y $$

<details>
<summary>Proof</summary>

Let $ x = (x_1, x_2, \ldots, x_n) $ and $ y = (y_1, y_2, \ldots, y_n) $.

$$
\begin{aligned}

\lambda (x + y) &= \lambda (x_1 + y_1, x_2 + y_2, \ldots, x_n + y_n) \\

&= (\lambda (x_1 + y_1), \lambda (x_2 + y_2), \lambda (x_n + y_n)) \\

&= (\lambda x_1 + \lambda y_1, \lambda x_2 + \lambda y_2, \ldots, \lambda x_n + \lambda y_n) \\

&= (\lambda x_1, \lambda x_2, \ldots, \lambda x_n) + (\lambda y_1, \lambda y_2, \ldots, \lambda y_n) \\

&= \lambda x + \lambda y

\end{aligned}
$$

</details>

#### Exercise 1A.15. Distributivity of addition over scalar multiplication of vectors

Page reference 11

$ \forall a, b \in F $ and $ \forall x \in F^n $:
$$ (a + b) x = ax + bx $$

<details>
<summary>Proof</summary>

Let $ x = (x_1, x_2, \ldots, x_n) $.

$$
\begin{aligned}

(a + b) x &= ((a + b) x_1, (a + b) x_2, \ldots, (a + b) x_n) \\

&= (a x_1 + b x_1, a x_2 + b x_2, \ldots, a x_n + b x_n) \\

&= (a x_1, a x_2, \ldots, a x_n) + (b x_1, b x_2, \ldots, b x_n) \\

&= a (x_1, x_2, \ldots, x_n) + b (x_1, x_2, \ldots, x_n) \\

&= a x + b x

\end{aligned}
$$

</details>
