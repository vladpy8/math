# Chapter 1. Vector spaces

## Section 1C. Subspaces

### Embedded exercises

#### Embedded exercise 1. Example 1.37

Page reference 20

Let $ W $ and $ U $ be subspaces of $ F^3 $:
$$
U = \{ (x, 0, 0) \in F^3, \ x \in F \}
\\ W = \{ (0, y, 0) \in F^3, \ y \in F \}
$$

Verify:
$$ U + W = \{ (x, y, 0) \in F^3, \ x, y \in F \} $$

<details>
<summary>Proof</summary>

Let arbitrary vectors $ u \in U $ and $ w \in W $ be defined as:
$$
u = (x, 0, 0) \in U, \ x \in F
\\ w = (0, y, 0) \in W, \ y \in F
$$

Sum of vectors $ u + w $ can be expressed as:
$$ u + w = (x, 0, 0) + (0, y, 0) = (x, y, 0) $$

Thus,
$$ U + W \subseteq \{ (x, y, 0) \in F^3, \ x,y \in F \} $$

Conversely, arbitrary coordinate vector in $ (x, y, 0) \in F^3 $ can be expressed as:
$$ (x, y, 0) = (x, 0, 0) + (0, y, 0) = u + w $$

Thus,
$$ \{ (x, y, 0) \in F^3, \ x, y \in F \} \subseteq U + W $$

Therefore,
$$ U + W = \{ (x, y, 0) \in F^3, \ x, y \in F \} $$

</details>

#### Embedded exercise 2. Theorem 1.40. Sum of subspaces is a subspace

Page reference 21

Let $ V_1, V_2, \ldots, V_n $ be subspaces of $ V $.

$$ V_1 + V_2 + \ldots + V_n \ \text{is subspace of} \ V $$

<details>
<summary>Proof</summary>

##### 1. Additive identity

For $ 0 \in V_1, 0 \in V_2, \ldots, 0 \in V_n $:
$$ 0 = (0 + 0 + \ldots + 0) \in V_1 + V_2 + \ldots + V_n $$

##### 2. Closure under addition

Let
$$ v_1, u_1 \in V_1, \quad v_2, u_2 \in V_2, \quad \ldots, \quad v_n, u_n \in V_n $$

$$
(v_1 + v_2 + \ldots + v_n) \in (V_1 + V_2 + \ldots + V_n)
\\ (u_1 + u_2 + \ldots + u_n) \in (V_1 + V_2 + \ldots + V_n)
$$

Then,
$$
(v_1 + v_2 + \ldots + v_n) + (u_1 + u_2 + \ldots + u_n) =
(v_1 + u_1) + (v_2 + u_2) + \ldots + (v_n + u_n)
$$

Since $ V_1, V_2, \ldots, V_n $ are subspaces of $ V $:
$$ v_1 + u_1 \in V_1, \quad v_2 + u_2 \in V_2, \quad \ldots, \quad v_n + u_n \in V_n $$

And
$$ ((v_1 + u_1) + (v_2 + u_2) + \ldots + (v_n + u_n)) \in (V_1 + V_2 + \ldots + V_n) $$

##### 3. Closure under scalar multiplication

Let $ v_1 \in V_1, v_2 \in V_2, \ldots, v_n \in V_n $ and $ \lambda \in F $.

$$ \lambda (v_1 + v_2 + \ldots + v_n) = \lambda v_1 + \lambda v_2 + \ldots + \lambda v_n $$

Since $ V_1, V_2, \ldots, V_n $ are subspaces of $ V $:
$$ \lambda v_1 \in V_1, \quad \lambda v_2 \in V_2, \quad \ldots, \quad \lambda v_n \in V_n $$

Then,
$$ (\lambda v_1 + \lambda v_2 + \ldots + \lambda v_n) \in (V_1 + V_2 + \ldots + V_n) $$

</details>

#### Embedded exercise 3. Example 1.42

Page reference 22

Let $ U $ and $ W $ be subspaces of $ F^3 $:
$$
U = \{ (x, y, 0) \in F^3, \ x, y \in F \}
\\ W = \{ (0, 0, z) \in F^3, \ z \in F \}
$$

Then
$$ F^3 = U \oplus W $$

<details>
<summary>Proof</summary>

Let arbitrary vectors $ u \in U $ and $ w \in W $ be defined as:
$$
u = (x, y, 0) \in U, \ x, y \in F
\\ w = (0, 0, z) \in W, \ z \in F
$$

Then sum of vectors $ u + w $ can be expressed as:
$$ u + w = (x, y, 0) + (0, 0, z) = (x, y, z) $$

Thus,
$$ U + W \subseteq F^3 $$

Conversely, each coordinate vector in $ (x, y, z) \in F^3 $ can be *uniquely* expressed as:
$$ (x, y, z) = (x, y, 0) + (0, 0, z) = u + w $$

Uniqueness proof is obvious, if one assumes the opposite. Thus, it is not stated here.

Thus,
$$ F^3 \subseteq U + W $$

Which, together with the uniqueness of representation, means that
$$ F^3 = U \oplus W $$

</details>

#### Embedded exercise 4. Example 1.43

Page reference 22

Let
$$ n \in \N, \quad k \in [1, n] $$

Let
$$ \quad V_k = \{ (x_1, x_2, \ldots, x_n) \in F^n : \quad i \neq k \implies x_i = 0 \} $$

Then
$$ F^n = V_1 \oplus V_2 \oplus \dots \oplus V_n $$

<details>
<summary>Proof</summary>

Let arbitrary vectors $ v_1, v_2, \ldots, v_n $ be defined as:
$$
v_1 = (x_1, 0, \ldots, 0) \in V_1, \quad x_1 \in F \\
v_2 = (0, x_2, 0, \ldots, 0) \in V_2, \quad x_2 \in F
\\ \ldots \\
v_n = (0, 0, \ldots, 0, x_n) \in V_n, \quad x_n \in F
$$

Then sum of vectors $ v_1 + v_2 + \ldots + v_n $ can be expressed as:
$$ v_1 + v_2 + \ldots + v_n = (x_1, x_2, \ldots, x_n) $$

Thus,
$$ V_1 + V_2 + \ldots + V_n \subseteq F^n $$

Conversely, each coordinate vector in $ (x_1, x_2, \ldots, x_n) \in F^n $ can be *uniquely* expressed as:
$$
(x_1, x_2, \ldots, x_n) = (x_1, 0, \ldots, 0) + (0, x_2, \ldots, 0) + \ldots + (0, 0, \ldots, x_n) = v_1 + v_2 + \ldots + v_n
$$

Uniqueness proof is obvious, if one assumes the opposite. Thus, it is not stated here.

Therefore,
$$ F^n \subseteq V_1 + V_2 + \ldots + V_n $$

Which, together with the uniqueness of representation, means that
$$ F^n = V_1 \oplus V_2 \oplus \ldots \oplus V_n $$

</details>

### Exercises 1C

#### Exercise 1C.1

Page reference 24

##### Part A

$$ U_a = \{ (x_1, x_2, x_3) \in F^3 : \quad x_1 + 2 x_2 + 3 x_3 = 0 \} $$

Decide if $ U_a \ \text{is subspace of} \ F^3 $.

<details>
<summary>Solution</summary>

$ U_a $ is a subspace of $ F^3 $

###### 1. Additive identity

$$ 0 + 2 \cdot 0 + 3 \cdot 0 = 0 $$

Then,
$$ 0 = (0, 0, 0) \in U_a $$

###### 2. Closure under addition

Let arbitrary vectors be defined as:
$$
u = (x_1, x_2, x_3) \in U_a
\\ v = (y_1, y_2, y_3) \in U_a
$$

Since both $ u $ and $ v $ are in $ U_a $:
$$
x_1 + 2 x_2 + 3 x_3 = 0 \\
y_1 + 2 y_2 + 3 y_3 = 0
$$

Adding both equations gives;
$$ (x_1 + y_1) + 2 (x_2 + y_2) + 3 (x_3 + y_3) = 0 $$

Thus,
$$ u + v = (x_1 + y_1, x_2 + y_2, x_3 + y_3) \in U_a $$

###### 3. Closure under scalar multiplication

Let arbitrary vector and scalar be defined as:
$$
u = (x_1, x_2, x_3) \in U_a
\\ \lambda \in F
$$

Since $ u \in U_a $:
$$ x_1 + 2 x_2 + 3 x_3 = 0 $$

Multiplying both sides by $ \lambda $:
$$ \lambda (x_1 + 2 x_2 + 3 x_3) = \lambda x_1 + 2 \lambda x_2 + 3 \lambda x_3 = 0 $$

Thus,
$$ \lambda u = (\lambda x_1, \lambda x_2, \lambda x_3) \in U_a $$

</details>

##### Part B

$$ U_b = \{ (x_1, x_2, x_3) \in F^3 : \quad x_1 + 2 x_2 + 3 x_3 = 4 \} $$

Decide if $ U_b \ \text{is subspace of} \ F^3 $.

<details>
<summary>Solution</summary>

$ U_b $ is not a subspace of $ F^3 $, since additive identity does not belong to $ U_b $.

$$ 0 + 2 \cdot 0 + 3 \cdot 0 \neq 4 $$

Therefore,
$$ 0 = (0, 0, 0) \notin U_b $$

</details>

##### Part C

$$ U_c = \{ (x_1, x_2, x_3) \in F^3 : \quad x_1 x_2 x_3 = 0 \} $$

Decide if $ U_c \ \text{is subspace of} \ F^3 $.

<details>
<summary>Solution</summary>

$ U_c $ is not a subspace of $ F^3 $, since closure under addition does not hold.

Let
$$
u = (1, 0, 0) \in U_c
\\ v = (0, 1, 0) \in U_c
\\ w = (0, 0, 1) \in U_c
$$

Then
$$
u + v + w = (1, 0, 0) + (0, 1, 0) + (0, 0, 1) = (1, 1, 1)
$$

$$ 1 \cdot 1 \cdot 1 \neq 0 $$

Thus,
$$ u + v + w = (1, 1, 1) \notin U_c $$

</details>

##### Part D

$$ U_d = \{ (x_1, x_2, x_3) \in F^3 : \quad x_1 = 5 x_3 \} $$

Decide if $ U_d \ \text{is subspace of} \ F^3 $.

<details>
<summary>Solution</summary>

$ U_d $ is a subspace of $ F^3 $.

###### 1. Additive identity

$$ 0 = 5 \cdot 0 $$

Then,
$$ 0 = (0, 0, 0) \in U_d $$

###### 2. Closure under addition

Let arbitrary vectors be defined as:
$$
u = (x_1, x_2, x_3) \in U_d
\\ v = (y_1, y_2, y_3) \in U_d
$$

Since both $ u $ and $ v $ are in $ U_d $:
$$
x_1 = 5 x_3 \\
y_1 = 5 y_3
$$

Adding both equations:
$$ (x_1 + y_1) = 5 (x_3 + y_3) $$

Thus,
$$ u + v = (x_1 + y_1, x_2 + y_2, x_3 + y_3) \in U_d $$

###### 3. Closure under scalar multiplication

Let arbitrary vector and scalar be defined as:
$$
u = (x_1, x_2, x_3) \in U_d
\\ \lambda \in F
$$

Since $ u \in U_d $:
$$ x_1 = 5 x_3 $$

Multiplying both sides by $ \lambda $:
$$ \lambda x_1 = 5 \lambda x_3 $$

Thus,
$$ \lambda u = (\lambda x_1, \lambda x_2, \lambda x_3) \in U_d $$

</details>

#### Exercise 1C.2

Page reference 24

Example 1.35.

##### Part A

Let for $ b \in F $:
$$ U_a = \{ (x_1, x_2, x_3, x_4) \in F^4 : \quad x_3 = 5 x_4 + b \} $$

Then
$$ U_a \ \text{is a subspace of} \ F^4 \iff b = 0 $$

<details>
<summary>Proof</summary>

Backward implication proof is almost copy-paste of exercise 1C.1 part D with minor changes.

(Put proper reference here)

Forward implication is:
$$ U_a \ \text{is a subspace of} \ F^4 \implies b = 0 $$

Which is easy to prove by contradiction. Assume $ U_a $ is indeed a subspace, while $ b \neq 0 $.

Let
$$ 0 = (0, 0, 0, 0) $$

Then,
$$ 0 = 5 \cdot 0 + b = b \neq 0 $$

By assumption $ U_a $ is a subspace, while $ 0 \notin U_a $. This is a contradiction, which proves the forward implication.

</details>

##### Part B

Let
$$ U_b = \{ f \in \mathbb{R}^{[0, 1]} :\quad f \ \text{is continuous} \} $$

Then
$$ U_b \ \text{is a subspace of} \ \mathbb{R}^{[0, 1]} $$

<details>
<summary>Proof</summary>

###### 1. Additive identity

The zero function is:
$$ 0(x) = 0 \quad \forall x \in [0, 1] $$

Then $ 0 \in U_b $ since constant function is continuous.

###### 2. Closure under addition

Let $ f, g \in U_b $.

Then $ f + g $ is:
$$ (f + g)(x) = f(x) + g(x) \quad \forall x \in [0, 1] $$

Since $ f $ and $ g $ are continuous functions, their sum is also continuous.

Thus,
$$ f + g \in U_b $$

###### 3. Closure under scalar multiplication

Let $ f \in U_b $ and $ \lambda \in \mathbb{R} $.

Then $ \lambda f $ is:
$$ (\lambda f)(x) = \lambda f(x) \quad \forall x \in [0, 1] $$

Since $ f $ is continuous, its scalar multiple is also continuous.

Thus,
$$ \lambda f \in U_b $$

</details>

##### Part C

Let
$$ U_c = \{ f \in \mathbb{R}^{\mathbb{R}} :\quad f \ \text{is differentiable} \} $$

Then
$$ U_c \ \text{is a subspace of} \ \mathbb{R}^{\mathbb{R}} $$

<details>
<summary>Proof</summary>

Repeat the proof from part B, but with differentiability instead of continuity. And with a wider domain.

</details>

##### Part D

Let $ b \in \mathbb{R} $.

Let
$$ U_d = \{ f \in \mathbb{R}^{[0, 3]} :\quad f \ \text{is differentiable}, \quad \ f'(2) = b \} $$

Then
$$ U_d \ \text{is a subspace of} \ \mathbb{R}^{[0, 3]} \iff b = 0 $$

<details>
<summary>Proof</summary>

###### Backward implication

Backward implication is:
$$ b = 0 \implies U_d \ \text{is a subspace of} \ \mathbb{R}^{[0, 3]} $$

<details>
<summary>Backward implication proof</summary>

Let $ b = 0 $.

###### 1. Additive identity

The zero function is:
$$ 0(x) = 0 \quad \forall x \in [0, 3] $$

Then $ 0 \in U_d $ since constant function is differentiable and its derivative is zero.

###### 2. Closure under addition

Let $ f, g \in U_d $.

Then $ f + g $ is:
$$ (f + g)(x) = f(x) + g(x) \quad \forall x \in [0, 3] $$

And $ f + g $ is differentiable since both $ f $ and $ g $ are differentiable.

Considering the derivative at $ x = 2 $:
$$ (f + g)'(2) = f'(2) + g'(2) = 0 + 0 = 0 $$

Therefore,
$$ f + g \in U_d $$

###### 3. Closure under scalar multiplication

Let $ f \in U_d $ and $ \lambda \in \mathbb{R} $.

Then $ \lambda f $ is:
$$ (\lambda f)(x) = \lambda f(x) \quad \forall x \in [0, 3] $$

And $ \lambda f $ is differentiable since $ f $ is differentiable.

Considering the derivative at $ x = 2 $:
$$ (\lambda f)'(2) = \lambda f'(2) = \lambda \cdot 0 = 0 $$

Therefore,
$$ \lambda f \in U_d $$

</details>

###### Forward implication

Forward implication is:
$$ U_d \ \text{is a subspace of} \ \mathbb{R}^{[0, 3]} \implies b = 0 $$

<details>
<summary>Forward implication proof</summary>

It is easy to prove by contradiction. Assume $ U_d $ is indeed a subspace, while $ b \neq 0 $.

The zero function is:
$$ 0(x) = 0 \quad \forall x \in [0, 3] $$

Then,
$$ 0'(2) = 0 \neq b $$

By assumption $ U_d $ is a subspace, while $ 0 \notin U_d $. This is a contradiction, which proves the forward implication.

</details>

</details>

##### Part E

Let
$$ U_e = \{ (x_k)_{k=1}^\infty \in \mathbb{C}^\infty : \quad \lim_{k \to \infty} x_k = 0 \} $$

Then
$$ U_e \ \text{is a subspace of} \ \mathbb{C}^\infty $$

<details>
<summary>Proof</summary>

###### 1. Additive identity

The zero sequence is defined as:
$$ 0 = (0, 0, 0, \ldots) $$

Then,
$$ \lim_{k \to \infty} 0 = 0 $$

Therefore,
$$ 0 \in U_e $$

###### 2. Closure under addition

Let arbitrary sequences be defined as:
$$
u = (x_k)_{k=1}^\infty \in U_e
\\ v = (y_k)_{k=1}^\infty \in U_e
$$

Since both $ u $ and $ v $ are in $ U_e $:
$$
\lim_{k \to \infty} x_k = 0
\\ \lim_{k \to \infty} y_k = 0
$$

By the properties of limits:
$$
\lim_{k \to \infty} (x_k + y_k) = \lim_{k \to \infty} x_k + \lim_{k \to \infty} y_k = 0 + 0 = 0
$$

Thus,
$$ u + v = (x_k + y_k)_{k=1}^\infty \in U_e $$

###### 3. Closure under scalar multiplication

Let arbitrary sequence and scalar be defined as:
$$
u = (x_k)_{k=1}^\infty \in U_e
\\ \lambda \in \mathbb{C}
$$

Since $ u \in U_e $:
$$ \lim_{k \to \infty} x_k = 0 $$

By the properties of limits:
$$
\lim_{k \to \infty} (\lambda x_k) = \lambda \cdot \lim_{k \to \infty} x_k = \lambda \cdot 0 = 0
$$

Thus,
$$ \lambda u = (\lambda x_k)_{k=1}^\infty \in U_e $$
</details>

#### Exercise 1C.3

Page reference 24

Let
$$
U = \{
	f \in \mathbb{R}^{(-4, 4)} : \quad
	f \ \text{is differentiable}, \quad
	f'(-1) = 3 \, f(2)
\}
$$

Then
$$ U \ \text{is a subspace of} \ \mathbb{R}^{(-4, 4)} $$

<details>
<summary>Proof</summary>

##### 1. Additive identity

The zero function is:
$$ 0(x) = 0 \quad \forall x \in (-4, 4) $$

The constant function is differentiable.

Considering the defining equation:
$$
\begin{aligned}
0'(-1) &= 0 (-1) = 0
\\ &= 3 \cdot 0(2) = 3 \cdot 0
\end{aligned}
$$

Then $ 0 \in U $.

##### 2. Closure under addition

Let $ f, g \in U $.

Then sum of functions $ f + g $ is:
$$ (f + g)(x) = f(x) + g(x) \quad \forall x \in (-4, 4) $$

And $ f + g $ is differentiable since both $ f $ and $ g $ are differentiable.

Both $ f $ and $ g $ are in $ U $:
$$
\begin{aligned}
f'(-1) &= 3 \, f(2)
\\ g'(-1) &= 3 \, g(2)
\end{aligned}
$$

Considering the defining equation:
$$
\begin{aligned}
(f + g)'(-1) &= f'(-1) + g'(-1)
\\ &= 3 \, f(2) + 3 \, g(2)
\\ &= 3 \, (f(2) + g(2))
\\ &= 3 \, (f + g)(2)
\end{aligned}
$$

Therefore,
$$ f + g \in U $$

##### 3. Closure under scalar multiplication

Let $ f \in U $ and $ \lambda \in \mathbb{R} $.

Then $ \lambda f $ is:
$$ (\lambda f)(x) = \lambda f(x) \quad \forall x \in (-4, 4) $$

And $ \lambda f $ is differentiable since $ f $ is differentiable.

Given that both $ f \in U $:
$$ f'(-1) = 3 \, f(2) $$

Considering the defining equation:
$$
\begin{aligned}
(\lambda f)'(-1) &= \lambda \, f'(-1)
\\ &= \lambda \, (3 \, f(2))
\\ &= 3 \, (\lambda \, f(2))
\\ &= 3 \, (\lambda f)(2)
\end{aligned}
$$

Therefore,
$$ \lambda f \in U $$

</details>

#### Exercise 1C.4

Page reference 24

For $ b \in \mathbb{R} $, let
$$
U = \{
	f \in \mathbb{R}^{[0, 1]} : \quad
	f \ \text{is continuous}, \quad
	\int_0^1 f(x) \, dx = b
\}
$$

Then
$$ U \ \text{is a subspace of} \ \mathbb{R}^{[0, 1]} \iff b = 0 $$

<details>
<summary>Proof</summary>

##### Backward implication

$$ b = 0 \implies U \ \text{is a subspace of} \ \mathbb{R}^{[0, 1]} $$

<details>
<summary>Backward implication proof</summary>

###### 1. Additive identity

The zero function is:
$$ 0(x) = 0 \quad \forall x \in [0, 1] $$

Then:
$$ \int_0^1 0(x) \, dx = 0 $$

Therefore, $ 0 \in U $.

###### 2. Closure under addition

Let $ f, g \in U $. Then $ f $ and $ g $ are continuous and:
$$
\int_0^1 f(x) \, dx = 0
\\ \int_0^1 g(x) \, dx = 0
$$

Since $ f $ and $ g $ are continuous, $ f + g $ is also continuous.

Using the properties of addition of integrals:
$$
\begin{aligned}
\int_0^1 (f + g)(x) \, dx &= \int_0^1 (f(x) + g(x)) \, dx
\\ &= \int_0^1 f(x) \, dx + \int_0^1 g(x) \, dx
\\ &= 0 + 0 = 0
\end{aligned}
$$

Therefore,
$$ f + g \in U $$

###### 3. Closure under scalar multiplication

Let $ f \in U $ and $ \lambda \in \mathbb{R} $.

Then $ f $ is continuous and:
$$ \int_0^1 f(x) \, dx = 0 $$

Since $ f $ is continuous, $ \lambda f $ is also continuous.

Using the properties of scalar multiplication of integrals:
$$
\begin{aligned}
\int_0^1 (\lambda f)(x) \, dx &= \int_0^1 \lambda f(x) \, dx
\\ &= \lambda \int_0^1 f(x) \, dx
\\ &= \lambda \cdot 0 = 0
\end{aligned}
$$

Therefore,
$$ \lambda f \in U $$

</details>

##### Forward implication

$$ U \ \text{is a subspace of} \ \mathbb{R}^{[0, 1]} \implies b = 0 $$

<details>
<summary>Forward implication proof</summary>

Assume $ U $ is a subspace of $ \mathbb{R}^{[0, 1]} $. Then $ U $ must contain the additive identity.

The zero function, being additive identity, is:
$$ 0(x) = 0 \quad \forall x \in [0, 1] $$

Since $ 0 \in U $, we have:
$$ \int_0^1 0(x) \, dx = \int_0^1 0 \, dx = 0 = b $$

Therefore, $ b = 0 $.

</details>

</details>

#### Exercise 1C.5. $ \mathbb{R}^2 $ as a subspace of $ \mathbb{C}^2 $

Page reference 24

Determine whether:
$$ \mathbb{R}^2 \ \text{is a subspace of the complex vector space} \ \mathbb{C}^2 $$

<details>
<summary>Solution</summary>

$$ \mathbb{R}^2 \ \text{is not a subspace of} \ \mathbb{C}^2 $$

It is easy to see once we consider the scalar multiplication closure property. The field in the context of this property is $ \mathbb{C} $.

Let $ u = (1, 0) \in \mathbb{R}^2 $, and $ \lambda = i \in \mathbb{C} $.

Then:
$$ \lambda u = i (1, 0) = (i, 0) \notin \mathbb{R}^2 $$

However, $ \mathbb{R}^2 $ would have become a subspace of $ \mathbb{C}^2 $ if we had used the field $ \mathbb{R} $ instead of $ \mathbb{C} $ for scalars. This is trivial to prove and won't be done here.

</details>

#### Exercise 1C.6

Page reference 24

##### Part A

Decide if $ U_R $ is a subspace of $ \mathbb{R}^3 $:
$$ U_R = \{ (a, b, c) \in \mathbb{R}^3 : \quad a^3 = b^3 \} $$

<details>
<summary>Solution</summary>

$ U_R $ is a subspace of $ \mathbb{R}^3 $.

###### 1. Additive identity

The zero vector is:
$$ 0 = (0, 0, 0) $$

Clearly $ 0^3 = 0^3 $, so $ 0 \in U_R $.

###### 2. Closure under addition

Let arbitrary vectors be defined as:
$$
u = (a_1, b_1, c_1) \in U_R
\\ v = (a_2, b_2, c_2) \in U_R
$$

Sum of the vectors is $ (u + v) \in \mathbb{R}^3 $:
$$ u + v = (a_1 + a_2, b_1 + b_2, c_1 + c_2) $$

Since both $ u $ and $ v $ are in $ U_R $:
$$
a_1^3 = b_1^3 \\
a_2^3 = b_2^3
$$

Considering that:
$$ \forall x, y \in \mathbb{R}, \quad x^3 = y^3 \iff x = y $$

<details>
<summary>Real values equality of cubes proof</summary>

Backward implication is trivial.

Forward implication is easily proven by contradiction. Assume $ x^3 = y^3 $ and $ x \neq y $. For definition, let $ x < y $, since the case $ x > y $ is symmetric.

By proving that $ x^3 < y^3 $, we get a contradiction.

###### Case 1. $ 0 < x < y $

$$
\begin{aligned}
x &< y
\\ x \cdot x &< y \cdot x
\\ x^2 &< y \cdot x
\end{aligned}
$$

$$
\begin{aligned}
x &< y
\\ x \cdot y &< y \cdot y
\\ x \cdot y &< y^2
\end{aligned}
$$

Thus
$$ x^2 < y \cdot x < y^2 $$

Next
$$
\begin{aligned}
x^2 &< y^2
\\ x^2 \cdot x &< y^2 \cdot x
\\ x^3 &< y^2 \cdot x
\end{aligned}
$$

$$
\begin{aligned}
x &< y
\\ x \cdot y^2 &< y \cdot y^2
\\ x \cdot y^2 &< y^3
\end{aligned}
$$

Therefore,
$$
x^3 < y^2 \cdot x < y^3
\\ x^3 < y^3
$$

###### Case 2. $ x = 0, 0 < y $

$$ x^3 = 0 $$

$$
\begin{aligned}
0 &< y
\\ 0 \cdot y &< y \cdot y
\\ 0 &< y^2
\\ 0 \cdot y &< y^2 \cdot y
\\ 0 &< y^3
\end{aligned}
$$

###### Case 3. $ x < 0, y = 0 $

$$
\begin{aligned}
x &< 0
\\ x \cdot (-x) &< 0 \cdot (-x)
\\ -x^2 &< 0
\\ -x^2 \cdot (-x) &< 0 \cdot (-x)
\\ x^3 &< 0
\end{aligned}
$$

###### Case 4. $ x < 0 < y $

Since $ x < 0 $ and $ y > 0 $, by applying the cases 2 and 3:
$$ -x^3 < 0 < y^3 $$

###### Case 5. $ x < y < 0 $

$$ 0 < -y < -x $$

Applying case 1:
$$ 0 < (-y)^3 < (-x)^3 $$

And,
$$ 0 < -y^3 < -x^3 $$

Therefore,
$$ x^3 < y^3 < 0 $$

</details>

We can state that:
$$
a_1 = b_1 \\
a_2 = b_2
$$

Adding both equations gives:
$$ a_1 + a_2 = b_1 + b_2 $$

Then, considering the defining equation of $ U_R $:
$$ (a_1 + a_2)^3 = (b_1 + b_2)^3 $$

Therefore,
$$ u + v \in U_R $$

###### 3. Closure under scalar multiplication

Let $ u = (a, b, c) \in U_R $ and $ \lambda \in \mathbb{R} $.

The scalar multiple of $ \lambda $ and $ u $ is $ \lambda u \in \mathbb{R}^3 $:
$$ \lambda u = (\lambda a, \lambda b, \lambda c) $$

Since $ u \in U_R $:
$$ a^3 = b^3 $$

Multiplying both sides by $ \lambda^3 $:
$$ (\lambda a)^3 = \lambda^3 a^3 = \lambda^3 b^3 = (\lambda b)^3 $$

Therefore,
$$ \lambda u \in U_R $$

</details>

##### Part B

Decide if $ U_C $ is a subspace of $ \mathbb{C}^3 $:
$$ U_C = \{ (a, b, c) \in \mathbb{C}^3 : \quad a^3 = b^3 \} $$

<details>
<summary>Solution</summary>

$ U_C $ is not a subspace of $ \mathbb{C}^3 $. The closure under addition property does not hold, which can be proven by counterexample.

Let arbitrary vectors be defined as:
$$
u = (r + i \, \sqrt{3} r, r - i \, \sqrt{3} r, 0) \in U_C
\\ v = (-r + i \, \sqrt{3} r, -r - i \, \sqrt{3} r, 0) \in U_C
\\ r \in \mathbb{R}, \ r > 0
$$

The formula for the cube of a complex number:
$$
\forall x = (x_r + i \, x_i) \in \mathbb{C}, \quad
x_r, x_i \in \mathbb{R}, \quad
x^3 = (x_r + i \, x_i)^3 = x_r^3 + i \, 3 x_r^2 x_i - 3 x_r x_i^2 - i \, x_i^3
$$

<details>
<summary>Complex cube formula proof</summary>

$$
\begin{aligned}

x^2 &= (x_r + i \, x_i)^2 = x_r^2 - x_i^2 + 2 i \, x_r x_i

\\ x^3 &= (x_r + i \, x_i)^3 = (x_r^2 - x_i^2 + 2 i \, x_r x_i) (x_r + i \, x_i)
\\ &= x_r^3 - x_i^2 x_r + 2 i \, x_r^2 x_i + i \, (x_r^2 x_i - x_i^3) - 2 x_r x_i^2
\\ &= x_r^3 + i \, 3 x_r^2 x_i - 3 x_r x_i^2 - i \, x_i^3

\end{aligned}
$$

</details>

Using the formula for the cube of a complex number for vector components of $ u $ and $ v $:

$$

\begin{aligned}

(r + i \, \sqrt{3} r)^3
&= r^3 + i \, 3 r^2 \sqrt{3} r - 3 r (\sqrt{3} r)^2 - i \, (\sqrt{3} r)^3
= -8 r^3

\\ (r - i \, \sqrt{3} r)^3
&= r^3 - i \, 3 r^2 \sqrt{3} r - 3 r (\sqrt{3} r)^2 - i \, (\sqrt{3} r)^3
= -8 r^3

\\ (-r + i \, \sqrt{3} r)^3
&= -r^3 + i \, 3 (-r)^2 \sqrt{3} r - 3 (-r) (\sqrt{3} r)^2 - i \, (\sqrt{3} r)^3
= 8 r^3

\\ (-r - i \, \sqrt{3} r)^3
&= -r^3 - i \, 3 (-r)^2 \sqrt{3} r - 3 (-r) (\sqrt{3} r)^2 - i \, (\sqrt{3} r)^3
= 8 r^3

\\ \end{aligned}
$$

Then,
$$
\begin{aligned}

((r + i \, \sqrt{3} r) + (-r + i \, \sqrt{3} r))^3
&= (i \, 2 \sqrt{3} r)^3 = - i \, 24 \sqrt{3} r^3

\\ ((r - i \, \sqrt{3} r) + (-r - i \, \sqrt{3} r))^3
&= (-i \, 2 \sqrt{3} r)^3 = i \, 24 \sqrt{3} r^3

\\ \end{aligned}
$$

Therefore, $ (u + v) \notin U_C $.

</details>

#### Exercise 1C.7

Page reference 24

Prove or give a counterexample that $ \forall U \subseteq \mathbb{R}^2, U \neq \emptyset $:
$$
\forall u, v \in U, \quad u + v \in U, \quad \ -u \in U \implies U \ \text{is a subspace of} \ \mathbb{R}^2
$$

<details>
<summary>Proof</summary>

This is not true. Consider the grid of integer points in $ \mathbb{R}^2 $:
$$ U = \{ (x, y) \in \mathbb{R}^2 : x, y \in \mathbb{Z} \} $$

This set contains the additive identity $ (0, 0) $, and is closed under addition.

However, it is not closed under scalar multiplication by any real number that is not an integer:
$$
\forall \lambda \in \mathbb{R} \setminus \mathbb{Z}, \quad \lambda (1, 0) = (\lambda, 0) \notin U
$$

</details>

#### Exercise 1C.8

Page reference 24

Give example of $ U \subseteq \mathbb{R}^2, U \neq \emptyset $:
$$
\forall \lambda \in \mathbb{R}, \forall u \in U, \lambda u \in U
, \quad \ U \ \text{is not a subspace of} \ \mathbb{R}^2
$$

<details>
<summary>Solution</summary>

Let the set be defined as the one consisting of the first and third quadrants of the Cartesian plane:
$$ U = \{ (x, y) \in \mathbb{R}^2 : x \cdot y \ge 0 \} $$

This set contains the additive identity $ (0, 0) $, and is closed under scalar multiplication:
$$
\forall \lambda \in \mathbb{R}
, \quad \forall (x, y) \in U, (x \cdot y) \ge 0
, \quad (\lambda x \cdot \lambda y) = \lambda^2 (x y) \ge 0
, \quad \lambda (x, y) \in U
$$

However, it is not closed under addition. Consider the sum of the following coordinate vectors:
$$
\forall r > 0, \quad u = (r, 0) \in U, \quad v = (0, -r) \in U
, \quad u + v = (r, -r)
, \quad r \cdot (-r) = -r^2 < 0
, \quad u + v \notin U
$$

</details>

#### Exercise 1C.9

Page reference 24

Let
$$
P = \{
	f \in \mathbb{R}^{\mathbb{R}}
	: \quad \left(
		\exists \ p \in \mathbb{R}, p > 0
		: \quad \forall x \in \mathbb{R}, \quad f(x) = f(x + p)
		\right)
	\}
$$

Decide if $ P $ is a subspace of $ \mathbb{R}^{\mathbb{R}} $.

<details>
<summary>Solution</summary>

$ P $ is not a subspace of $ \mathbb{R}^{\mathbb{R}} $. The closure under addition property does not hold, which can be proven by counterexample.

Let $ f, g \in \mathbb{R}^{\mathbb{R}} $ be defined as:
$$ f(x) = \sin(x), \quad g(x) = \sin(x \cdot \sqrt{2}) $$

The sum of these functions is $ f + g $:
$$ f(x) + g(x) = \sin(x) + \sin(x \cdot \sqrt{2}) $$

For $ f + g $ to be in $ P $, it *must* have a period $ p > 0 $ such that:
$$ p = n \cdot 2\pi = m \cdot \frac{2\pi}{\sqrt{2}}, \quad m, n \in \mathbb{Z} $$

Direct proof of the statement above goes far beyond the scope of this exercise.

The statement implies:
$$ \frac{m}{n} = \sqrt{2}, \quad m, n \in \mathbb{Z} $$

Which is not possible, since $ \sqrt{2} $ is irrational.

Therefore, $ f + g \notin P $.

</details>

#### Exercise 1C.10. Intersection of subspaces

Page reference 24

$$ V_1, V_2 \ \text{are subspaces of} \ V \implies V_1 \cap V_2 \ \text{is a subspace of} \ V $$

<details>
<summary>Proof</summary>

##### 1. Additive identity

The zero vector is in both $ V_1 $ and $ V_2 $, since they are subspaces of $ V $.

Then,
$$ 0 \in V_1 \cap V_2 $$

##### 2. Closure under addition

Let $ u, v \in V_1 \cap V_2 $.

Then
$$
u, v \in V_1, \ u, v \in V_2
\\ u + v \in V_1, \ u + v \in V_2
$$

Therefore,
$$ u + v \in V_1 \cap V_2 $$

##### 3. Closure under scalar multiplication

Let $ u \in V_1 \cap V_2 $ and $ \lambda \in F $.

Then
$$
u \in V_1, \ u \in V_2
\\ \lambda u \in V_1, \ \lambda u \in V_2
$$

Therefore,
$$ \lambda u \in V_1 \cap V_2 $$

</details>

#### Exercise 1C.11. Intersection of subspaces, arbitrary amount

Page reference 25

$$
\forall i \in I, \quad U_i \ \text{is a subspace of} \ V
\implies \bigcap_{i \in I} U_i \ \text{is a subspace of} \ V
$$

<details>
<summary>Proof</summary>

##### 1. Additive identity

$$ \forall i \in I, \quad 0 \in U_i $$

Therefore,
$$ 0 \in \bigcap_{i \in I} U_i $$

##### 2. Closure under addition

Let $ u, v \in \bigcap_{i \in I} U_i $.

Then
$$ \forall i \in I, \quad u, v \in U_i, \quad u + v \in U_i $$

Therefore,
$$ u + v \in \bigcap_{i \in I} U_i $$

##### 3. Closure under scalar multiplication

Let $ u \in \bigcap_{i \in I} U_i $ and $ \lambda \in F $.

Then
$$ \forall i \in I, \quad u \in U_i, \quad \lambda u \in U_i $$

Therefore,
$$ \lambda u \in \bigcap_{i \in I} U_i $$

</details>

#### Exercise 1C.12. Union of subspaces

Page reference 25

Let $ U_1, U_2 $ be subspaces of $ V $.

$$
U_1 \cup U_2 \ \text{is a subspace of} \ V
\iff (U_1 \subseteq U_2 \ \text{or} \ U_2 \subseteq U_1)
$$

<details>
<summary>Proof</summary>

##### Backward implication

Backward implication is trivial to prove, since $ U_1 \cup U_2 $ in case of $ U_1 \subseteq U_2 \ \text{or} \ U_2 \subseteq U_1 $ is the biggest of the two sets, which is either $ U_2 $ or $ U_1 $. And both of them are subspaces of $ V $.

##### Forward implication

Forward implication is easy to prove by contradiction. However, it requires a setup.

Let $ \bar{U_1} = U_1 \setminus U_2 $ and $ \bar{U_2} = U_2 \setminus U_1 $.

If at least one of these sets is empty, then the second statement of the forward implication immediately follows. Since,
$$
\bar{U_1} = \emptyset \implies U_1 \subseteq U_2
\\ \bar{U_2} = \emptyset \implies U_2 \subseteq U_1
$$

When both $ \bar{U_1} $ and $ \bar{U_2} $ are non-empty, the second expression of the forward implication cannot be true. This essentially forms the contradiction statement of the forward implication:
$$
U_1 \cup U_2 \ \text{is a subspace of} \ V,
\quad \text{and yet,} \quad
\bar{U_1} \neq \emptyset \ \text{and} \ \bar{U_2} \neq \emptyset
$$

Let arbitrary $ \bar{u_1} \in \bar{U_1} $ and $ \bar{u_2} \in \bar{U_2} $.

According to the closure under addition property of $ U_1 \cup U_2 $:
$$ \bar{u_1} + \bar{u_2} \in U_1 \cup U_2 $$

Then, either $ \bar{u_1} + \bar{u_2} \in U_1 $ or $ \bar{u_1} + \bar{u_2} \in U_2 $.

$$
\begin{aligned}
\bar{u_1} + \bar{u_2} \in U_1 \implies -\bar{u_1} + (\bar{u_1} + \bar{u_2}) \in U_1
\\ &\implies (-\bar{u_1} + \bar{u_1}) + \bar{u_2} \in U_1
\\ &\implies \bar{u_2} \in U_1
\end{aligned}
$$

Which contradicts the definition of $ \bar{U_2} $.

The same way goes for $ \bar{u_1} + \bar{u_2} \in U_2 $.

Given the impossibility of the contradiction, we can conclude that the forward implication holds.

</details>

#### [TODO] Exercise 1C.13

Page reference 25

Let $ U_1, U_2, U_3 $ be subspaces of $ V $.

$$
U_1 \cup U_2 \cup U_3 \ \text{is a subspace of} \ V
\iff (U_j \subseteq U_i \ \text{and} \ U_k \subseteq U_i
, \quad i, j, k \in \{1, 2, 3\}, i \neq j \neq k)
$$

<details>
<summary>Proof</summary>

</details>

#### Exercise 1C.14

Page reference 25

Let
$$ U = \{ (x, -x, 2x) \in F^3 : x \in F \} $$
$$ W = \{ (y, y, 2y) \in F^3 : y \in F \} $$

Describe $ U + W $ symbolically and verbally.

<details>
<summary>Solution</summary>

First of all both $ U $ and $ W $ are subspaces of $ F^3 $, since they satisfy all the necessary criteria.

<details>
<summary>Proof of subspace criteria</summary>

##### Additive identity

The zero vector is:
$$ 0 = (0, 0, 0) $$

Then:
$$ (0, -0, 2 \cdot 0) = (0, 0, 0) \in U $$
$$ (0, 0, 2 \cdot 0) = (0, 0, 0) \in W $$

##### Closure under addition

Let,
$$
u_1 = (x_1, -x_1, 2 \cdot x_1) \in U \\
u_2 = (x_2, -x_2, 2 \cdot x_2) \in U \\
w_1 = (y_1, y_1, 2 \cdot y_1) \in W \\
w_2 = (y_2, y_2, 2 \cdot y_2) \in W
$$

$$
\begin{aligned}
u_1 + u_2 &= (x_1, -x_1, 2 \cdot x_1) + (x_2, -x_2, 2 \cdot x_2)
\\ &= (x_1 + x_2, -(x_1 + x_2), 2 \cdot (x_1 + x_2))
\end{aligned}
$$

$$
\begin{aligned}
w_1 + w_2 &= (y_1, y_1, 2 \cdot y_1) + (y_2, y_2, 2 \cdot y_2)
\\ &= (y_1 + y_2, y_1 + y_2, 2 \cdot (y_1 + y_2))
\end{aligned}
$$

Therefore
$$
u_1 + u_2 \in U \\
w_1 + w_2 \in W
$$

##### Closure under scalar multiplication

Let
$$
\lambda \in F,
\\ u = (x, -x, 2 \cdot x) \in U
\\ w = (y, y, 2 \cdot y) \in W
$$

$$
\begin{aligned}
\lambda u &= \lambda(x, -x, 2 \cdot x)
\\ &= (\lambda x, -\lambda x, 2 \cdot \lambda x)
\\ \end{aligned}
$$

$$
\begin{aligned}
\lambda w &= \lambda(y, y, 2 \cdot y)
\\ &= (\lambda y, \lambda y, 2 \cdot \lambda y)
\\ \end{aligned}
$$

Therefore,
$$
\lambda u \in U
\\ \lambda w \in W
$$

</details>

The sum of the two subspaces $ U + W $ is a subspace of $ F^3 $:
$$ U + W = \{ (x + y, -x + y, 2(x + y)) : x, y \in F \} $$

Verbally, each subspace $ U $ and $ W $ can be described as a line in $ F^3 $ that passes through origin. The sum of the two subspaces is a plane in $ F^3 $ that passes through origin, and contains both lines.

</details>

#### Exercise 1C.15. Sum of a subspace with itself

Page reference 25

If $ U $ is a subspace of $ V $, determine $ U + U $.

<details>
<summary>Solution</summary>

$$ U + U = U $$

<details>
<summary>Proof</summary>

$$ \forall u \in U, \quad u = u + 0 \in U + U \implies U \subseteq U + U $$

$$
\forall u_1, u_2 \in U, \quad u_1 + u_2 \in U + U
\implies u_1 + u_2 \in U
\implies U + U \subseteq U
$$

</details>

</details>

#### Exercise 1C.16. Commutativity of addition of subspaces of vector spaces

Page reference 25

Determine whether:
$$ \forall U, W \ \text{subspaces of} \ V, \quad U + W = W + U $$

<details>
<summary>Solution</summary>

Let arbitrary $ u \in U $ and $ w \in W $.

$$
u + w \in U + W
, \quad u + w = w + u \in W + U
, \quad U + W \subseteq W + U
$$

$$
w + u \in W + U
, \quad w + u = u + w \in U + W
, \quad W + U \subseteq U + W
$$

Therefore,
$$ U + W = W + U $$

</details>

#### Exercise 1C.17. Associativity of addition of subspaces of vector spaces

Page reference 25

Determine whether:
$$ \forall V_1, V_2, V_3 \ \text{subspaces of} \ V, \quad (V_1 + V_2) + V_3 = V_1 + (V_2 + V_3) $$

<details>
<summary>Solution</summary>

Let arbitrary $ v_1 \in V_1 $, $ v_2 \in V_2 $, and $ v_3 \in V_3 $.

$$
(v_1 + v_2) + v_3 \in (V_1 + V_2) + V_3
, \quad (v_1 + v_2) + v_3 = v_1 + (v_2 + v_3) \in V_1 + (V_2 + V_3)
$$
$$ \quad (V_1 + V_2) + V_3 \subseteq V_1 + (V_2 + V_3) $$

$$
v_1 + (v_2 + v_3) \in V_1 + (V_2 + V_3)
, \quad v_1 + (v_2 + v_3) = (v_1 + v_2) + v_3 \in (V_1 + V_2) + V_3
$$

$$ \quad V_1 + (V_2 + V_3) \subseteq (V_1 + V_2) + V_3 $$

Therefore,
$$ (V_1 + V_2) + V_3 = V_1 + (V_2 + V_3) $$

</details>

#### Exercise 1C.18. Identity and inverses of addition of subspaces of vector spaces

Page reference 25

##### Part 1. Additive identity

There does exists an additive identity of addition of subspaces of $ V $.

<details>
<summary>Proof</summary>

Let additive identity be defined as:
$$ \{ 0 \} $$

Then,
$$ \forall U \ \text{subspace of} \ V, \quad U + \{ 0 \} = \{ u + 0 = u : u \in U \} = U $$

</details>

##### Part 2. Existence of additive inverses

Additive inverse does not exist in general for addition of subspaces of $ V $.

<details>
<summary>Proof</summary>

Let arbitrary $ U \ \text{be subspace of} \ V $. We seek $ W \ \text{subspace of} \ V $ such that:
$$ U + W = \{ 0 \} $$

Additive inverse must be general enough, so the cases when $ V = \{ 0 \} $ or $ U = \{ 0 \} $ are not considered.

$$ \forall u \in U, \quad u + 0 \in U + W, \quad u + 0 = u \in U + W, \quad U \subseteq U + W $$

Therefore,
$$ \forall W \subseteq V, \quad U + W \supseteq U \supsetneq \{ 0 \} $$

Generally, it is impossible to find a subspace $ W $ such that the inclusion property would not hold. Not to mention the existence of such $ W $ that would satisfy the additive inverse property.

</details>

Yet for particular case, when $ U = \{ 0 \} $, the additive inverse does exist:
$$ \{ 0 \} + \{ 0 \} = \{ 0 \} $$

#### Exercise 1C.19

Page reference 25

Prove or give a counterexample:

$$ ( V_1, V_2, U \ \text{are subspaces of} \ V : \quad V_1 + U = V_2 + U ) \implies V_1 = V_2 $$

<details>
<summary>Solution</summary>

The statement is not true.

Let
$$
V_1 = \{ (x, 0) \in F^2 : x \in F \} \\
V_2 = F^2 = \{ (x, y) \in F^2 : x, y \in F \}
\\ U = V_2
$$

According to [Exercise 1C.15](#exercise-1c15-sum-of-a-subspace-with-itself):
$$ V_2 + U = V_2 + V_2 = V_2 = F^2 $$

While,
$$
V_1 + U = V_1 + V_2 = \{ (x_1 + x_2, y) \in F^2 : x_1, x_2, y \in F \}
$$

Since, $ x_1 $ and $ x_2 $ are arbitrary:
$$
\forall x_1, x_2 \in F, \quad \exists \ x : \quad x = x_1 + x_2
\\ \forall x \in F, \quad \exists \ x_1, x_2 \in F : \quad x = x_1 + x_2
$$

Then
$$
\begin{aligned}
V_1 + U &= \{ (x_1 + x_2, y) \in F^2 : x_1, x_2, y \in F \}
\\ &= \{ (x, y) \in F^2 : x, y \in F \}
\\ &= F^2 = V_2
\end{aligned}
$$

Thus
$$ V_1 + U = V_2 + U = F^2 $$

While clearly $$ V_1 \neq V_2 $$

</details>

#### Exercise 1C.20

Page reference 25

Let
$$ U = \{ (x, x, y, y) \in F^4 : x, y \in F \} $$

Find
$$ W \ \text{subspace of} \ F^4 : \quad F^4 = U \oplus W $$

<details>
<summary>Solution</summary>

There are possibly many solutions. Yet one simple choice is:
$$ W = \{ (0, z, 0, t) \in F^4 : z, t \in F \} $$

$$
U + W = \{ (x, x + z, y, y + t) \in F^4 : x, y, z, t \in F \}
\\ U + W \subseteq F^4
$$

$$
\forall (a, b, c, d) \in F^4
, \quad \exists \ x, y, z, t \in F
: \quad x = a, \ y = c, \ z = b - a, \ t = d - c
$$

$$
\forall (a, b, c, d) \in F^4
, \quad \exists \ (x, x + z, y, y + t) \in U + W
: \quad (a, b, c, d) = (x, x + z, y, y + t)
\\ F^4 \subseteq U + W
$$

Therefore,
$$ F^4 = U + W $$

$$
u = (x, x, y, y) \in U, \quad w = (0, z, 0, t) \in W
, \quad u + w = (x, x + z, y, y + t) = (0, 0, 0, 0)
\implies x = 0, \ y = 0, \ z = 0, \ t = 0
$$

$$ U \cap W = \{ (0, 0, 0, 0) \} $$

Thus, using the theorem 1.46 for the condition of direct sum:
$$ F^4 = U \oplus W $$

</details>

#### Exercise 1C.21

Page reference 25

Let
$$ U = \{ (x, y, x + y, x - y, 2x) \in F^5 : \quad x, y \in F \} $$

Find
$$ W \ \text{subspace of} \ F^5 : \quad F^5 = U \oplus W $$

<details>
<summary>Solution</summary>

One possible choice is:
$$ W = \{ (0, 0, z, t, s) \in F^5 : z, t, s \in F \} $$

$$
U + W = \{ (x, y, x + y + z, x - y + t, 2x + s) \in F^5 : x, y, z, t, s \in F \}
\\ U + W \subseteq F^5
$$

$$
\forall (a, b, c, d, e) \in F^5
, \quad \exists \ x, y, z, t, s \in F
: \quad x = a, \ y = b, \ z = c - (a + b), \ t = d - (a - b), \ s = e - 2a
$$

$$
\forall (a, b, c, d, e) \in F^5
, \quad \exists \ (x, y, x + y + z, x - y + t, 2x + s) \in U + W
: \quad (a, b, c, d, e) = (x, y, x + y + z, x - y + t, 2x + s)
\\ F^5 \subseteq U + W
$$

Therefore,
$$ F^5 = U + W $$

$$
u = (x, y, x + y, x - y, 2x) \in U, \quad w = (0, 0, z, t, s) \in W
, \\ \quad u + w = (x, y, x + y + z, x - y + t, 2x + s) = (0, 0, 0, 0, 0)
\\ \implies x = 0, \ y = 0, \ z = 0, \ t = 0, \ s = 0
$$

$$ U \cap W = \{ (0, 0, 0, 0, 0) \} $$

Thus, using the theorem 1.46 for the condition of direct sum:
$$ F^5 = U \oplus W $$

</details>

#### Exercise 1C.22

Page reference 25

Let
$$ U = \{ (x, y, x + y, x - y, 2x) \in F^5 : \quad x, y \in F \} $$

Find
$$
W_1, W_2, W_3 \ \text{subspaces of} \ F^5
: \quad W_k \neq \{ 0 \}, \forall k \in \{ 1, 2, 3 \}
, \quad F^5 = U \oplus W_1 \oplus W_2 \oplus W_3
$$

<details>
<summary>Solution</summary>

It is easy to leverage [exercise 1C.21](#exercise-1c21) solution:
$$ W = \{ (0, 0, z, t, s) \in F^5 : z, t, s \in F \} $$

To do so one requires to split the subspace $ W $ into three subspaces:
$$
W_1 = \{ (0, 0, z, 0, 0) \in F^5 : z \in F \} \\
W_2 = \{ (0, 0, 0, t, 0) \in F^5 : t \in F \} \\
W_3 = \{ (0, 0, 0, 0, s) \in F^5 : s \in F \}
$$

One can use the results from [example 1.43](#embedded-exercise-4-example-143) to prove the division:
$$ W = W_1 \oplus W_2 \oplus W_3 $$

Therefore,
$$ F^5 = U \oplus ( W_1 \oplus W_2 \oplus W_3 ) $$

Using the associativity of sum of subspaces from [exercise 1C.17](#exercise-1c17-associativity-of-addition-of-subspaces-of-vector-spaces):
$$ F^5 = U + W_1 + W_2 + W_3 $$

Finally, using the theorem 1.45 and the uniqueness of zero vector in direct sum:
$$
\forall u \in U, \forall w \in W, \quad u + w = 0 \implies u = 0, \ w = 0
\\ \forall w_1 \in W_1, \forall w_2 \in W_2, \forall w_3 \in W_3
, \quad w_1 + w_2 + w_3 = 0 \implies w_1 = 0, \ w_2 = 0, \ w_3 = 0
\\ \therefore \forall u \in U, \forall w_1 \in W_1, \forall w_2 \in W_2, \forall w_3 \in W_3
, \quad u + w = u + (w_1 + w_2 + w_3) = 0 \implies u = 0, \ w_1 = 0, \ w_2 = 0, \ w_3 = 0
$$

Therefore,
$$ F^5 = U \oplus W_1 \oplus W_2 \oplus W_3 $$

</details>

#### Exercise 1C.23. Uniqueness of direct sum complements

Page reference 26

Prove or give a counterexample:

$$
\forall \ V_1, V_2, U \ \text{subspaces of} \ V
: \quad V = V_1 \oplus U, \ V = V_2 \oplus U \implies V_1 = V_2
$$

<details>
<summary>Solution</summary>

</details>

#### Exercise 1C.24. Decomposition of $ \mathbb{R}^{\mathbb{R}} $ into even and odd functions

Page reference 26

Let
$$ V_e = \{ f \in \mathbb{R}^{\mathbb{R}} : \quad \forall x \in \mathbb{R}, \quad f(-x) = f(x) \} $$
$$ V_o = \{ f \in \mathbb{R}^{\mathbb{R}} : \quad \forall x \in \mathbb{R}, \quad f(-x) = -f(x) \} $$

Then,
$$ \mathbb{R}^{\mathbb{R}} = V_e \oplus V_o $$

<details>
<summary>Proof</summary>

</details>
