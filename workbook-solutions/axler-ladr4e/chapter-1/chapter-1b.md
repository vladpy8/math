# Chapter 1. Vector spaces.<br>Section 1B. Definitions of vector spaces

TODO:
1. Fix references
1. Add references

## Definitions

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

## Section exercises and questions

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

## Exercises 1B

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
