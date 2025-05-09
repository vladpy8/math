# Chapter 1. Vector spaces.<br>Section 1B. Definitions of vector spaces

TODO:
1. Fix references
1. Add references

## Definitions

### Function vectors $ F^S $

Let $ F $ be a field of numbers

Let $ S $ be a set of arbitrary elements

$ F^S $ is set of functions

$$ F^S = \{ S \to F \} $$

$ \forall f, g \in F^S $, $ \ \forall x \in S $ and $ \forall \lambda \in F $

$$
\begin{aligned}

(f + g)(x) &= f(x) + g(x) \\

(\lambda f)(x) &= \lambda f(x)

\end{aligned}
$$

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

Let $ V $ be a vector space over field $ F $

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

Let $ V $ be a vector space over field $ F $

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

Let $ V $ be a vector space over field $ F $

Let $ v, w \in V $

$$ \exist ! \ x \in V : \quad v + 3 x = w $$

---

Let $ x, y \in V $

$$
v + 3 x = w \\
v + 3 y = w
$$

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

Let $ (V, +, \cdot) $ denote a *candidate* for a vector space $ V $ with operations of addition and scalar multiplication

Let $ A $ be the set of properties of vector spaces defined in 1.20 on page 12

Let $ A_m $ be a modified set of properties of vector spaces identical to $ A $ except additive inverse being replaced by

$$ \forall v in V \quad 0 v = 0 $$

Then $ \forall (V, +, \cdot) $

$$ (V, +, \cdot) \vDash A \iff (V, +, \cdot) \vDash A_m $$

---

The forward implication is proven in 1.30 on page 15

The backward implication is

$$ (V, +, \cdot) \vDash A_m \implies (V, +, \cdot) \vDash A $$

$ \forall v \in V $

$$
\begin{aligned}

0 &= 0 v = (1 + (-1)) v \\
&= v + (-1) v

\end{aligned}
$$

Thus

$$ \forall v \in V, \quad \exist \ w \in V, \quad w = (-1) v : \quad v + w = 0 $$

### Exercise 1B.6

Let $ \R_{\infty} = \R \cup \{\infty, -\infty\} $

Let addition on $ \R_{\infty} $ for $ \R \subseteq \R_{\infty} $ be defined as usual. Define addition on $ \R_{\infty} $ with infinity elements

$ \forall t \in \R $

$$
\begin{aligned}
t + \infty &= \infty + t = \infty + \infty = \infty \\
t + (-\infty) &= (-\infty) + t = (-\infty) + (-\infty) = -\infty \\
\infty + (-\infty) &= (-\infty) + \infty = 0
\end{aligned}
$$

Let scalar multiplication on $ \R_{\infty} $ for $ \R \subseteq \R_{\infty} $ be defined as usual. Define scalar multiplication on $ \R_{\infty} $ with infinity elements

$ \forall t \in \R $

$$
\begin{aligned}

t \cdot \infty &= \begin{cases}
	-\infty & \text{if} \ t < 0 \\
	0 & \text{if} \ t = 0 \\
	\infty & \text{if} \ t > 0
\end{cases}

\\
\\

t \cdot (-\infty) &= \begin{cases}
	\infty & \text{if} \ t < 0 \\
	0 & \text{if} \ t = 0 \\
	-\infty & \text{if} \ t > 0
\end{cases}

\end{aligned}
$$

Then $ \R_{\infty} $ is not a vector space

---

Associativity of addition doesn't hold

$ \forall t \in \R $

$$
\begin{aligned}

0 &= \infty + (-\infty) = (t + \infty) + (-\infty) \\
&= t + (\infty + (-\infty)) = t + 0 \\
&= t

\end{aligned}
$$

### Exercise 1B.7

Let $ S $ be an arbitrary nonempty set

Let $ V $ be a vector space over $ F $

Let $ V^S $ be a set of functions $ { S \to V } $

Define addition on $ V^S $

$$ \forall f, g \in V^S, \quad \forall x \in S, \quad (f + g)(x) = f(x) + g(x) $$


Define scalar multiplication on $ V^S $

$$ \forall \lambda \in F, \quad \forall f \in V^S, \quad \forall x \in S, \quad (\lambda f)(x) = \lambda f(x) $$

The $ V^S $ is a vector space over $ F $

---

#### 1. Commutativity of addition

$ \forall f, g \in V^S $

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

$ \forall f, g, h \in V^S $

$$ (f + g) + h = f + (g + h) $$

---

$ \forall x \in S $

$$
\begin{aligned}
((f + g) + h)(x) &= (f + g)(x) + h(x) \\
&= (f(x) + g(x)) + h(x) \\
&= f(x) + (g(x) + h(x)) \\
&= f(x) + (g + h)(x) \\
&= (f + (g + h))(x)
\end{aligned}
$$

#### 3. Associativity of scalar multiplication

$ \forall f \in V^S $ and $ \forall a, b \in F $

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

Let $ 0 \in V^S $

$$ 0(x) = 0, \quad \forall x \in S $$

$ \forall f \in V^S $

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

#### 4. Additive inverse

$$ \forall f \in V^S, \quad \exist g \in V^S, \quad f + g = 0 $$

---

Let $ g \in V^S $

$$ g(x) = -f(x), \quad \forall x \in S $$

Then

$$
\begin{aligned}
(f + g)(x) &= f(x) + g(x) \\
&= f(x) + (-f(x)) \\
&= 0 \\
\end{aligned}
$$

Thus, $ f + g = 0 $

#### 5. Multiplicative identity

$ \forall f \in V^S $

$$ 1 f = f $$

---

$ \forall x \in S $

$$
\begin{aligned}
(1 f)(x) &= 1 \cdot f(x) \\
&= f(x)
\end{aligned}
$$

#### 6. Distributivity of scalar multiplication over addition

$ \forall f, g \in V^S $ and $ \forall a \in F $

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

#### 7. Distributivity of addition over scalar multiplication

$ \forall f \in V^S $ and $ \forall a, b \in F $

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

### Exercise 1B.8

Let $ V_C = V \times V $

Denote $ (u, v) \in V_C $ as $ u + i \, v $

Define addition on $ V_C $

$$ \forall u_1, v_1, u_2, v_2 \in V, \quad (u_1 + i \, v_1) + (u_2 + i \, v_2) = (u_1 + u_2) + i \, (v_1 + v_2) $$

Define complex scalar multiplication on $ V_C $

$$ \forall a, b \in \R, \quad \forall u, v \in V, \quad (a + b \, i)(u + i \, v) = (au - bv) + i \, (av + bu) $$

The $ V_C $ is a complex vector space

---

#### 1. Commutativity of addition

$ \forall u_1, v_1, u_2, v_2 \in V $

$$ (u_1 + i \, v_1) + (u_2 + i \, v_2) = (u_2 + i \, v_2) + (u_1 + i \, v_1) $$

---

$$
\begin{aligned}
(u_1 + i \, v_1) + (u_2 + i \, v_2) &= (u_1 + u_2) + i \, (v_1 + v_2) \\
&= (u_2 + u_1) + i \, (v_2 + v_1) \\
&= (u_2 + i \, v_2) + (u_1 + i \, v_1)
\end{aligned}
$$

#### 2. Associativity of addition

$ \forall u_1, v_1, u_2, v_2, u_3, v_3 \in V $

$$ ((u_1 + i \, v_1) + (u_2 + i \, v_2)) + (u_3 + i \, v_3) = (u_1 + i \, v_1) + ((u_2 + i \, v_2) + (u_3 + i \, v_3)) $$

---

$$
\begin{aligned}
((u_1 + i \, v_1) + (u_2 + i \, v_2)) + (u_3 + i \, v_3) &= ((u_1 + u_2) + i (v_1 + v_2)) + (u_3 + i \, v_3) \\
&= ((u_1 + u_2) + u_3) + i \, ((v_1 + v_2) + v_3) \\
&= (u_1 + (u_2 + u_3)) + i \, (v_1 + (v_2 + v_3)) \\
&= (u_1 + iv_1) + ((u_2 + u_3) + i \, (v_2 + v_3)) \\
&= (u_1 + iv_1) + ((u_2 + iv_2) + (u_3 + iv_3))
\end{aligned}
$$

#### 3. Associativity of scalar multiplication

$ \forall a, b, c, d \in \R, \forall u, v \in V $

$$ ((a + b \, i)(c + d \, i))(u + i \, v) = (a + b \, i)((c + d \, i)(u + i \, v)) $$

---

$$
\begin{aligned}
((a + b \, i)(c + d \, i))(u + i \, v) &= ((ac - bd) + (ad + bc) \, i)(u + i \, v) \\
&= ((ac - bd)u - (ad + bc)v) + i \, ((ac - bd)v + (ad + bc)u) \\
&= (acu - adv - bdu - bcv) + i \, (acv + adu - bdv + bcu) \\
&= (a(cu - dv) - b(du + cv)) + i \, (a(cv + du) + b(cu - dv)) \\
&= (a + b \, i)((cu - dv) + i \, (cv + du)) \\
&= (a + b \, i)((c + d \, i)(u + i \, v))
\end{aligned}
$$

#### 4. Additive identity

Let $ 0 \in V_C $

$$ 0 = (0, 0) = 0 + i \, 0 $$

$ \forall u, v \in V_C $

$$ u + i \, v + 0 = u + i \, v $$

---

$$
\begin{aligned}
(u + i \, v) + 0 &= (u + i \, v) + (0 + i \, 0) \\
&= (u + 0) + i \, (v + 0) \\
&= u + i \, v
\end{aligned}
$$

#### 5. Additive inverse

$$ \forall u, v \in V, \quad \exist \, w, p \in V, \quad u + i \, v + w + i \, p = 0 $$

---

Let

$$
w = -u \\
p = -v
$$

Then

$$
\begin{aligned}
(u + i \, v) + ((-u) + i \, (-v)) &= (u - u) + i \, (v - v) \\
&= 0 + i \, 0 \\
&= 0
\end{aligned}
$$

#### 6. Multiplicative identity

$ \forall u, v \in V_C $

$$ (1 + 0 \, i) (u + i \, v) = u + i \, v $$

---

$$
\begin{aligned}
(1 + 0 \, i)(u + i \, v) &= (1 \cdot u - 0 \cdot v) + i \, (1 \cdot v + 0 \cdot u) \\
&= u + i \, v
\end{aligned}
$$

#### 7. Distributivity of scalar multiplication over addition

$ \forall u_1, v_1, u_2, v_2 \in V_C $ and $ a, b \in \R $

$$ (a + b \, i) ((u_1 + i \, v_1) + (u_2 + i \, v_2)) = (a + b \, i)(u_1 + i \, v_1) + (a + b \, i)(u_2 + i \, v_2) $$

---

$$
\begin{aligned}
((a + b \, i) ((u_1 + i \, v_1) + (u_2 + i \, v_2))) &= (a + b \, i)((u_1 + u_2) + i \, (v_1 + v_2)) \\
&= (a(u_1 + u_2) - b(v_1 + v_2)) + i \, (a(v_1 + v_2) + b(u_1 + u_2)) \\
&= (a u_1 + a u_2 - b v_1 - b v_2) + i \, (a v_1 + a v_2 + b u_1 + b u_2) \\
&= ((a u_1 - b v_1) + i \, (a v_1 + b u_1)) + ((a u_2 - b v_2) + i \, (a v_2 + b u_2)) \\
&= (a + b \, i)(u_1 + i \, v_1) + (a + b \, i)(u_2 + i \, v_2)
\end{aligned}
$$

#### 8. Distributivity of addition over scalar multiplication

$ \forall u, v \in V_C $ and $ a, b, c, d \in \R $

$$ ((a + b \, i) + (c + d \, i))(u + i \, v) = (a + b \, i)(u + i \, v) + (c + d \, i)(u + i \, v) $$

---

$$
\begin{aligned}
((a + b \, i) + (c + d \, i))(u + i \, v) &= ((a + c) + (b + d) \, i)(u + i \, v) \\
&= ((a + c) u - (b + d) v) + i \, ((a + c) v + (b + d) u) \\
&= (a u - b v + c u - d v) + i \, (a v + b u + c v + d u) \\
&= ((a u - b v) + i \, (a v + b u)) + ((c u - d v) + i \, (c v + d u)) \\
&= (a + b \, i)(u + i \, v) + (c + d \, i)(u + i \, v)
\end{aligned}
$$
