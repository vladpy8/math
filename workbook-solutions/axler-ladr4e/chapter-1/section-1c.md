# Chapter 1. Vector spaces

## Section 1C. Subspaces

### Embedded exercises

#### Embedded exercise 1. Example 1.37

Page reference 20

Let
$$
U = \{ (x, 0, 0) \in F^3, \ x \in F \} \\
W = \{ (0, y, 0) \in F^3, \ y \in F \}
$$

Verify:
$$ U + W = \{ (x, y, 0) \in F^3, \ x, y \in F \} $$

<details>
<summary>Proof</summary>

Let
$$
u = (x, 0, 0) \in U, \ x \in F \\
w = (0, y, 0) \in W, \ y \in F
$$

Each sum of vectors $ u + w $ can be expressed as:
$$ u + w = (x, 0, 0) + (0, y, 0) = (x, y, 0) $$

Thus,
$$ U + W \subseteq \{ (x, y, 0) \in F^3, \ x,y \in F \} $$

Conversely, each coordinate vector in $ (x, y, 0) \in F^3 $ can be expressed as:
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
$$ 0 = 0 + 0 + \ldots + 0 \quad \in V_1 + V_2 + \ldots + V_n $$

##### 2. Closure under addition

Let
$$ v_1, u_1 \in V_1, \quad v_2, u_2 \in V_2, \quad \ldots, \quad v_n, u_n \in V_n $$

Then,
$$ (v_1 + v_2 + \ldots + v_n) + (u_1 + u_2 + \ldots + u_n) = (v_1 + u_1) + (v_2 + u_2) + \ldots + (v_n + u_n) $$

Since $ V_1, V_2, \ldots, V_n $ are subspaces of $ V $:
$$ v_1 + u_1 \in V_1, \quad v_2 + u_2 \in V_2, \quad \ldots, \quad v_n + u_n \in V_n $$

And
$$ (v_1 + u_1) + (v_2 + u_2) + \ldots + (v_n + u_n) \quad \in V_1 + V_2 + \ldots + V_n $$

##### 3. Closure under scalar multiplication

Let $ v_1 \in V_1, v_2 \in V_2, \ldots, v_n \in V_n $ and $ \lambda \in F $.

$$ \lambda (v_1 + v_2 + \ldots + v_n) = \lambda v_1 + \lambda v_2 + \ldots + \lambda v_n $$

Since $ V_1, V_2, \ldots, V_n $ are subspaces of $ V $:
$$ \lambda v_1 \in V_1, \quad \lambda v_2 \in V_2, \quad \ldots, \quad \lambda v_n \in V_n $$

Then,
$$ \lambda (v_1 + v_2 + \ldots + v_n) = \lambda v_1 + \lambda v_2 + \ldots + \lambda v_n \quad \in V_1 + V_2 + \ldots + V_n $$

</details>

#### Embedded exercise 3. Example 1.42

Page reference 22

Let
$$
U = \{ (x, y, 0) \in F^3, \ x, y \in F \} \\
W = \{ (0, 0, z) \in F^3, \ z \in F \}
$$

Then
$$ F^3 = U \oplus W $$

<details>
<summary>Proof</summary>

Let
$$
u = (x, y, 0) \in U, \ x, y \in F \\
w = (0, 0, z) \in W, \ z \in F
$$

Then each sum of vectors $ u + w $ can be expressed as:
$$ u + w = (x, y, 0) + (0, 0, z) = (x, y, z) $$

Thus,
$$ U + W \subseteq F^3 $$

Conversely, each coordinate vector in $ (x, y, z) \in F^3 $ can be *uniquely* expressed as:
$$ (x, y, z) = (x, y, 0) + (0, 0, z) = u + w $$

Thus,
$$ F^3 \subseteq U + W $$

Therefore,
$$ F^3 = U + W $$

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

Let
$$
v_1 = (x_1, 0, \ldots, 0) \in V_1, \quad x_1 \in F \\
v_2 = (0, x_2, 0, \ldots, 0) \in V_2, \quad x_2 \in F \\
\vdots \\
v_n = (0, 0, \ldots, 0, x_n) \in V_n, \quad x_n \in F
$$

Then each sum of vectors $ v_1 + v_2 + \ldots + v_n $ can be expressed as:
$$ v_1 + v_2 + \ldots + v_n = (x_1, x_2, \ldots, x_n) $$

Thus,
$$ V_1 + V_2 + \ldots + V_n \subseteq F^n $$

Conversely, each coordinate vector in $ (x_1, x_2, \ldots, x_n) \in F^n $ can be *uniquely* expressed as:
$$ (x_1, x_2, \ldots, x_n) = (x_1, 0, \ldots, 0) + (0, x_2, \ldots, 0) + \ldots + (0, 0, \ldots, x_n) = v_1 + v_2 + \ldots + v_n $$

Thus,
$$ F^n \subseteq V_1 + V_2 + \ldots + V_n $$

Therefore,
$$ F^n = V_1 + V_2 + \ldots + V_n $$

</details>

### Exercises 1C

#### Exercise 1C.1

Page reference 24

##### A

$$ U_a = \{ (x_1, x_2, x_3) \in F^3 : \quad x_1 + 2 x_2 + 3 x_3 = 0 \} $$

Decide if $ U_a \ \text{is subspace of} F^3 $.

<details>
<summary>Solution</summary>

U_a is a subspace of $ F^3 $

###### 1. Additive identity

Let
$$ u = (0, 0, 0) \in U_a $$

Then,
$$ 0 = 0 + 2 \cdot 0 + 3 \cdot 0 \quad \in U_a $$

###### 2. Closure under addition

Let
$$
u = (x_1, x_2, x_3) \in U_a \\
v = (y_1, y_2, y_3) \in U_a
$$

Since both $ u $ and $ v $ are in $ U_a $:
$$
x_1 + 2 x_2 + 3 x_3 = 0 \\
y_1 + 2 y_2 + 3 y_3 = 0
$$

Adding both equations:
$$ (x_1 + y_1) + 2 (x_2 + y_2) + 3 (x_3 + y_3) = 0 $$

Thus,

$$ u + v = (x_1 + y_1, x_2 + y_2, x_3 + y_3) \quad \in U_a $$

###### 3. Closure under scalar multiplication

Let
$$
u = (x_1, x_2, x_3) \in U_a \\
\lambda \in F
$$

Since $ u \in U_a $:
$$ x_1 + 2 x_2 + 3 x_3 = 0 $$

Multiplying both sides by $ \lambda $:
$$ \lambda (x_1 + 2 x_2 + 3 x_3) = \lambda x_1 + 2 \lambda x_2 + 3 \lambda x_3 = 0 $$

Thus,
$$ \lambda x_1 + 2 \lambda x_2 + 3 \lambda x_3 = 0 \quad \in U_a $$

</details>

##### B

$$ U_b = \{ (x_1, x_2, x_3) \in F^3 : \quad x_1 + 2 x_2 + 3 x_3 = 4 \} $$

Decide if $ U_b \ \text{is subspace of} F^3 $.

<details>
<summary>Solution</summary>

U_b is not a subspace of $ F^3 $, since additive identity does not belong to $ U_b $.

Let
$$ u = (0, 0, 0) \in U_b $$

Then,
$$ 0 + 2 \cdot 0 + 3 \cdot 0 \neq 4  $$

</details>

##### C

$$ U_c = \{ (x_1, x_2, x_3) \in F^3 : \quad x_1 x_2 x_3 = 0 \} $$

Decide if $ U_c \ \text{is subspace of} F^3 $.

<details>
<summary>Solution</summary>

U_c is not a subspace of $ F^3 $, since closure under addition does not hold.

Let
$$
u = (1, 0, 0) \in U_c \\
v = (0, 1, 0) \in U_c \\
w = (0, 0, 1) \in U_c
$$

Then
$$
u + v + w = (1, 0, 0) + (0, 1, 0) + (0, 0, 1) = (1, 1, 1)
$$

$$ 1 \cdot 1 \cdot 1 \neq 0 $$

Thus,
$$ u + v + w = (1, 1, 1) \notin U_c $$

</details>

##### D

$$ U_d = \{ (x_1, x_2, x_3) \in F^3 : \quad x_1 = 5 x_3 \} $$

Decide if $ U_d \ \text{is subspace of} F^3 $.

<details>
<summary>Solution</summary>

U_d is a subspace of $ F^3 $.

###### 1. Additive identity

Let
$$ u = (0, 0, 0) \in U_d $$

Then,
$$ 0 = 5 \cdot 0 \quad \in U_d $$

###### 2. Closure under addition

Let
$$
u = (x_1, x_2, x_3) \in U_d \\
v = (y_1, y_2, y_3) \in U_d
$$

Since both $ u $ and $ v $ are in $ U_d $:
$$
x_1 = 5 x_3 \\
y_1 = 5 y_3
$$

Adding both equations:
$$ (x_1 + y_1) = 5 (x_3 + y_3) $$

Thus,
$$ u + v = (x_1 + y_1, x_2 + y_2, x_3 + y_3) \quad \in U_d $$

###### 3. Closure under scalar multiplication

Let
$$
u = (x_1, x_2, x_3) \in U_d \\
\lambda \in F
$$

Since $ u \in U_d $:
$$ x_1 = 5 x_3 $$

Multiplying both sides by $ \lambda $:
$$ \lambda x_1 = 5 \lambda x_3 $$

Thus,
$$ \lambda x_1 = 5 \lambda x_3 \quad \in U_d $$

</details>

#### Exercise 1C.2

Page reference 24

Example 1.35.

<details>
<summary>Proof</summary>

##### A

Let for $ b \in F $:
$$ U_a = \{ (x_1, x_2, x_3, x_4) \in F^4 : \quad x_3 = 5 x_4 + b \} $$

Then
$$ U_a \ \text{is a subspace of} F^4 \iff b = 0 $$

<details>
<summary>Proof</summary>

</details>

##### B
Let $ C[0,1] = \{ f \in \mathbb{R}^{[0,1]} :\quad f \ \text{is continuous} \} $.
$ C[0,1] \ \text{is a subspace of } \mathbb{R}^{[0,1]} $.
<details>
<summary>Proof</summary>

</details>

##### C. Example 1.35(c)
Let $ \mathcal{D}(\mathbb{R}) = \{ f \in \mathbb{R}^{\mathbb{R}} :\quad f \ \text{is differentiable} \} $.
$ \mathcal{D}(\mathbb{R}) \ \text{is a subspace of } \mathbb{R}^{\mathbb{R}} $.
<details>
<summary>Proof</summary>

</details>

##### D. Example 1.35(d)
For $ b \in \mathbb{R} $, let $ U_b = \{ f \in \mathbb{R}^{(0,3)} :\quad f \ \text{is differentiable and } f'(2) = b \} $.
$ U_b \ \text{is a subspace of } \mathbb{R}^{(0,3)} \iff b = 0 $.
<details>
<summary>Proof</summary>

</details>

##### E. Example 1.35(e)
Let $ c_0 = \{ (x_k)_{k=1}^\infty \in \mathbb{C}^\infty :\quad \lim_{k \to \infty} x_k = 0 \} $.
$ c_0 \ \text{is a subspace of } \mathbb{C}^\infty $.
<details>
<summary>Proof</summary>

</details>

</details>

#### Exercise 1C.3. Subspace of differentiable functions

Page reference 24

Let $$

U = \{ f \in \mathbb{R}^{(-4,4)} : \quad f \ \text{is differentiable}, \quad f'(-1) = 3f(2) \} $$

$ U \ \text{is a subspace of } \mathbb{R}^{(-4,4)} $.

<details>
<summary>Proof</summary>

</details>

#### Exercise 1C.4. Subspace of continuous functions

Page reference 24

For $ b \in \mathbb{R} $, let $ U_b = \{ f \in \mathbb{R}^{[0,1]} :\quad f \ \text{is continuous and } \int_0^1 f(x) \, dx = b \} $.
$ U_b \ \text{is a subspace of } \mathbb{R}^{[0,1]} \iff b = 0 $.

<details>
<summary>Proof</summary>

</details>

#### Exercise 1C.5. $ \mathbb{R}^2 $ as a subspace of $ \mathbb{C}^2 $

Page reference 24

$ \mathbb{R}^2 \ \text{is a subspace of the complex vector space } \mathbb{C}^2? $

<details>
<summary>Solution</summary>

</details>

#### Exercise 1C.6. Subspace criterion involving $ a^3 = b^3 $

Page reference 24

Determine if $ U $ is a subspace for each $ U $ defined below.
<details>
<summary>Solution</summary>

##### A. $ U_R = \{ (a,b,c) \in \mathbb{R}^3 :\quad a^3 = b^3 \} $
Is $ U_R $ a subspace of $ \mathbb{R}^3 $?
<details>
<summary>Solution</summary>

</details>

##### B. $ U_C = \{ (a,b,c) \in \mathbb{C}^3 :\quad a^3 = b^3 \} $
Is $ U_C $ a subspace of $ \mathbb{C}^3 $?
<details>
<summary>Solution</summary>

</details>

</details>

#### Exercise 1C.7. Closure properties and subspace criteria in $ \mathbb{R}^2 $

Page reference 24

Prove or give a counterexample:
If $ U \subseteq \mathbb{R}^2, \ U \neq \emptyset $, and $ (\forall u,v \in U, \ u+v \in U) \land (\forall u \in U, \ -u \in U) $, then $ U \text{ is a subspace of } \mathbb{R}^2 $.

<details>
<summary>Proof</summary>

</details>

#### Exercise 1C.8. A set closed under scalar multiplication but not a subspace

Page reference 24

Provide $ U \subseteq \mathbb{R}^2 $ such that $ U \neq \emptyset $, $ (\forall \lambda \in \mathbb{R}, \forall u \in U, \lambda u \in U) $, and $ U $ is not a subspace of $ \mathbb{R}^2 $.

<details>
<summary>Solution</summary>

</details>

#### Exercise 1C.9. Set of periodic functions as a subspace

Page reference 24

Let $ P = \{ f \in \mathbb{R}^{\mathbb{R}} :\quad (\exists p \in \mathbb{R}, p>0 \text{ such that } \forall x \in \mathbb{R}, f(x) = f(x+p)) \} $.
Is $ P $ a subspace of $ \mathbb{R}^{\mathbb{R}} $? Explain.

<details>
<summary>Explanation</summary>

</details>

#### Exercise 1C.10. Intersection of two subspaces

Page reference 24

If $ V_1, V_2 \text{ are subspaces of } V $, then $ V_1 \cap V_2 \text{ is a subspace of } V $.

<details>
<summary>Proof</summary>

</details>

#### Exercise 1C.11. Intersection of an arbitrary collection of subspaces

Page reference 25

If $ \{ U_i \}_{i \in I} \text{ is a collection of subspaces of } V $, then $ \bigcap_{i \in I} U_i \text{ is a subspace of } V $.

<details>
<summary>Proof</summary>

</details>

#### Exercise 1C.12. Union of two subspaces

Page reference 25

Let $ U_1, U_2 $ be subspaces of $ V $.
$ U_1 \cup U_2 \ \text{is a subspace of } V \iff (U_1 \subseteq U_2 \text{ or } U_2 \subseteq U_1) $.

<details>
<summary>Proof</summary>

</details>

#### Exercise 1C.13. Union of three subspaces

Page reference 25

Let $ U_1, U_2, U_3 $ be subspaces of $ V $.
$ U_1 \cup U_2 \cup U_3 \ \text{is a subspace of } V \iff ((U_2 \subseteq U_1 \land U_3 \subseteq U_1) \lor (U_1 \subseteq U_2 \land U_3 \subseteq U_2) \lor (U_1 \subseteq U_3 \land U_2 \subseteq U_3)) $.

This exercise is surprisingly harder than Exercise 12, possibly because this exercise is not true if we replace F with a field containing only two elements.

<details>
<summary>Proof</summary>

</details>

#### Exercise 1C.14. Sum of specific subspaces in $ F^3 $

Page reference 25

Let $ U = \{ (x, -x, 2x) :\quad x \in F \} \subseteq F^3 $ and $ W = \{ (y, y, 2y) :\quad y \in F \} \subseteq F^3 $.
Describe $ U+W $ symbolically and verbally.

<details>
<summary>Solution</summary>

</details>

#### Exercise 1C.15. Sum of a subspace with itself

Page reference 25

If $ U \ \text{is a subspace of } V $, find $ U+U $.

<details>
<summary>Solution</summary>

</details>

#### Exercise 1C.16. Commutativity of subspace addition

Page reference 25

Is $ U+W = W+U $ for all subspaces $ U, W $ of $ V $?

<details>
<summary>Solution</summary>

</details>

#### Exercise 1C.17. Associativity of subspace addition

Page reference 25

Is $ (U_1+U_2)+U_3 = U_1+(U_2+U_3) $ for all subspaces $ U_1, U_2, U_3 $ of $ V $?

<details>
<summary>Solution</summary>

</details>

#### Exercise 1C.18. Identity and inverses for subspace addition

Page reference 25

For the operation of addition on the set of subspaces of $ V $:
<details>
<summary>Solution</summary>

##### 1. Existence of additive identity
Does an additive identity exist?
<details>
<summary>Solution</summary>

</details>

##### 2. Existence of additive inverses
Which subspaces possess additive inverses?
<details>
<summary>Solution</summary>

</details>

</details>

#### Exercise 1C.19. Cancellation in subspace addition

Page reference 25

Prove or give a counterexample:
If $ V_1, V_2, U $ are subspaces of $ V $ such that $ V_1 + U = V_2 + U $, then $ V_1 = V_2 $.

<details>
<summary>Proof</summary>

</details>

#### Exercise 1C.20. Direct sum complement in $ F^4 $

Page reference 25

For $ U = \{ (x,x,y,y) \in F^4 :\quad x,y \in F \} $, find a subspace $ W $ of $ F^4 $ such that $ F^4 = U \oplus W $.

<details>
<summary>Solution</summary>

</details>

#### Exercise 1C.21. Direct sum complement in $ F^5 $

Page reference 25

For $ U = \{ (x,y,x+y,x-y,2x) \in F^5 :\quad x,y \in F \} $, find a subspace $ W $ of $ F^5 $ such that $ F^5 = U \oplus W $.

<details>
<summary>Solution</summary>

</details>

#### Exercise 1C.22. Multiple direct sum complements in $ F^5 $

Page reference 25

For $ U = \{ (x,y,x+y,x-y,2x) \in F^5 :\quad x,y \in F \} $, find subspaces $ W_1, W_2, W_3 $ of $ F^5 $ such that $ W_k \neq \{0\} $ for $ k=1,2,3 $, and $ F^5 = U \oplus W_1 \oplus W_2 \oplus W_3 $.

<details>
<summary>Solution</summary>

</details>

#### Exercise 1C.23. Uniqueness of direct sum complements

Page reference 26

Prove or give a counterexample:
If $ V_1, V_2, U $ are subspaces of $ V $ such that $ V = V_1 \oplus U $ and $ V = V_2 \oplus U $, then $ V_1 = V_2 $.

Hint: When trying to discover whether a conjecture in linear algebra is true or false, it is often useful to start by experimenting in $ F^2 $.

<details>
<summary>Proof</summary>

</details>

#### Exercise 1C.24. Decomposition of $ \mathbb{R}^{\mathbb{R}} $ into even and odd functions

Page reference 26

Let $ V_e = \{ f \in \mathbb{R}^{\mathbb{R}} :\quad \forall x \in \mathbb{R}, \ f(-x) = f(x) \} $.
Let $ V_o = \{ f \in \mathbb{R}^{\mathbb{R}} :\quad \forall x \in \mathbb{R}, \ f(-x) = -f(x) \} $.
$ \mathbb{R}^{\mathbb{R}} = V_e \oplus V_o $.

<details>
<summary>Proof</summary>

</details>
