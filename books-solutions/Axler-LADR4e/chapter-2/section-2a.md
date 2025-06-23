# Chapter 2. Finite-Dimensional Vector Spaces

## Section A. Span and Linear Independence

### Relevant definitions

#### Definition 1. Linear combination

Page reference: 28

A **linear combination** of a list $ v_1, \dots, v_m $ of vectors in $ V $ is a vector of the form:
$$ a_1 v_1 + \dots + a_m v_m $$
where $ a_1, \dots, a_m \in F $.

#### Definition 2. Span

Page reference: 29

The set of all linear combinations of a list of vectors $ v_1, \dots, v_m $ in $ V $ is called the **span** of $ v_1, \dots, v_m $, denoted by $ \text{span}(v_1, \dots, v_m) $.

$$ \text{span}(v_1, \dots, v_m) = \{ a_1 v_1 + \dots + a_m v_m : a_1, \dots, a_m \in F \} $$

The span of the empty list $ () $ is defined to be $ \{0\} $.

#### Definition 3. Spanning list

Page reference: 29

A list of vectors $ v_1, \dots, v_m $ **spans** $ V $ if:
$$ \text{span}(v_1, \dots, v_m) = V $$

#### Definition 4. Finite-dimensional vector space

Page reference: 30

A vector space is called **finite-dimensional** if some list of vectors in it spans the space.

#### Definition 5. Infinite-dimensional vector space

Page reference: 31

A vector space is called **infinite-dimensional** if it is not finite-dimensional.

#### Definition 6. Polynomial

Page reference: 30

A function $ p : F \to F $ is called a **polynomial** with coefficients in $ F $ if there exist $ a_0, \dots, a_m \in F $ such that:
$$ p(z) = a_0 + a_1 z + a_2 z^2 + \dots + a_m z^m, \quad \forall z \in F $$

$ \mathcal{P}(F) $ is the set of all polynomials with coefficients in $ F $.

#### Definition 7. Degree of a polynomial

Page reference: 31

A polynomial $ p \in \mathcal{P}(F) $ is said to have **degree** $ m $ if there exist scalars $ a_0, a_1, \dots, a_m \in F $ with $ a_m \neq 0 $ such that:
$$ p(z) = a_0 + a_1 z + \dots + a_m z^m, \quad \forall z \in F $$

The polynomial that is identically $ 0 $ is said to have degree $ -\infty $. The degree of a polynomial $ p $ is denoted by $ \text{deg } p $.

For a nonnegative integer $ m $, $ \mathcal{P}_m(F) $ denotes the set of all polynomials with coefficients in $ F $ and degree at most $ m $.

#### Definition 8. Linearly independent

Page reference: 32

A list $ v_1, \dots, v_m $ of vectors in $ V $ is called **linearly independent** if the only choice of $ a_1, \dots, a_m \in F $ that makes:
$$ a_1 v_1 + \dots + a_m v_m = 0 $$
is $ a_1 = \dots = a_m = 0 $.

The empty list $ () $ is also declared to be linearly independent.

#### Definition 9. Linearly dependent

Page reference: 33

A list of vectors in $ V $ is called **linearly dependent** if it is not linearly independent.

A list $ v_1, \dots, v_m $ of vectors in $ V $ is linearly dependent if there exist $ a_1, \dots, a_m \in F $, not all $ 0 $, such that:
$$ a_1 v_1 + \dots + a_m v_m = 0 $$

### Embedded exercises

#### Embedded exercise 1. System of equations with no solution

Page reference: 28

Let $ a_1, a_2 \in F $.

Verify that the following system of equations has no solution:
$$
\begin{aligned}
17 &= 2a_1 + a_2 \\
-4 &= a_1 - 2a_2 \\
5 &= -3a_1 + 4a_2
\end{aligned}
$$

<details>
<summary>Solution</summary>

</details>

#### Embedded exercise 2. P(F) is a vector space

Page reference: 30

Let $ \mathcal{P}(F) $ be the set of all polynomials with coefficients in $ F $.

With the usual operations of addition and scalar multiplication, $ \mathcal{P}(F) $ is a vector space over $ F $.

<details>
<summary>Solution</summary>

</details>

#### Embedded exercise 3. Sublist of a linearly independent list

Page reference: 33

If some vectors are removed from a linearly independent list, the remaining list is also linearly independent.

<details>
<summary>Solution</summary>

</details>

#### Embedded exercise 4. Linear dependence of a list in F^3

Page reference: 33

See [Exercise 6](#exercise-6).

#### Embedded exercise 5. Verification of a linear combination

Page reference: 34

Let $ a, b \in \mathbb{R} $.

Verify that $ a=3, b=2 $ is a solution to the equation:
$$ (15, 16, 17) = a(1, 2, 3) + b(6, 5, 4) $$

<details>
<summary>Solution</summary>

</details>

### Exercises A

#### Exercise 1

Page reference: 37

Find a list of four distinct vectors in $ F^3 $ whose span equals:
$$ \{ (x, y, z) \in F^3 : x+y+z=0 \} $$

<details>
<summary>Solution</summary>

</details>

#### Exercise 2

Page reference: 37

Let $ v_1, v_2, v_3, v_4 $ be a list of vectors that spans $ V $.

Prove or give a counterexample: the list $ v_1 - v_2, v_2 - v_3, v_3 - v_4, v_4 $ also spans $ V $.

<details>
<summary>Solution</summary>

</details>

#### Exercise 3

Page reference: 37

Let $ v_1, \dots, v_m $ be a list of vectors in $ V $. For $ k \in \{1, \dots, m\} $, let:
$$ w_k = v_1 + \dots + v_k $$

Show that:
$$ \text{span}(v_1, \dots, v_m) = \text{span}(w_1, \dots, w_m) $$

<details>
<summary>Solution</summary>

</details>

#### Exercise 4

Page reference: 37

##### A

Let $ v \in V $.
$$ \{v\} \text{ is linearly independent} \iff v \neq 0 $$

<details>
<summary>Solution</summary>

</details>

##### B

Let $ v_1, v_2 $ be a list of two vectors in $ V $.
$$ \{v_1, v_2\} \text{ is linearly independent} \iff \text{neither vector is a scalar multiple of the other} $$

<details>
<summary>Solution</summary>

</details>

#### Exercise 5

Page reference: 37

Find a number $ t $ such that the list $ (3, 1, 4), (2, -3, 5), (5, 9, t) $ is not linearly independent in $ \mathbb{R}^3 $.

<details>
<summary>Solution</summary>

</details>

#### Exercise 6

Page reference: 37

Let $ c \in F $.
$$ \text{The list } ((2, 3, 1), (1, -1, 2), (7, 3, c)) \text{ is linearly dependent in } F^3 \iff c=8 $$

<details>
<summary>Solution</summary>

</details>

#### Exercise 7

Page reference: 37

##### A

Let $ \mathbb{C} $ be a vector space over $ \mathbb{R} $. The list $ 1+i, 1-i $ is linearly independent.

<details>
<summary>Solution</summary>

</details>

##### B

Let $ \mathbb{C} $ be a vector space over $ \mathbb{C} $. The list $ 1+i, 1-i $ is linearly dependent.

<details>
<summary>Solution</summary>

</details>

#### Exercise 8

Page reference: 37

Let $ v_1, v_2, v_3, v_4 $ be a linearly independent list of vectors in $ V $. The list $ v_1 - v_2, v_2 - v_3, v_3 - v_4, v_4 $ is also linearly independent.

<details>
<summary>Solution</summary>

</details>

#### Exercise 9

Page reference: 37

Let $ v_1, v_2, \dots, v_m $ be a linearly independent list of vectors in $ V $.

Prove or give a counterexample: the list $ 5v_1 - 4v_2, v_2, v_3, \dots, v_m $ is linearly independent.

<details>
<summary>Solution</summary>

</details>

#### Exercise 10

Page reference: 38

Let $ v_1, v_2, \dots, v_m $ be a linearly independent list of vectors in $ V $ and $ \lambda \in F $ with $ \lambda \neq 0 $.

Prove or give a counterexample: the list $ \lambda v_1, \lambda v_2, \dots, \lambda v_m $ is linearly independent.

<details>
<summary>Solution</summary>

</details>

#### Exercise 11

Page reference: 38

Let $ v_1, \dots, v_m $ and $ w_1, \dots, w_m $ be linearly independent lists of vectors in $ V $.

Prove or give a counterexample: the list $ v_1 + w_1, \dots, v_m + w_m $ is linearly independent.

<details>
<summary>Solution</summary>

</details>

#### Exercise 12

Page reference: 38

Let $ v_1, \dots, v_m $ be a linearly independent list of vectors in $ V $ and let $ w \in V $.
$$ \{v_1+w, \dots, v_m+w\} \text{ is linearly dependent} \implies w \in \text{span}(v_1, \dots, v_m) $$

<details>
<summary>Solution</summary>

</details>

#### Exercise 13

Page reference: 38

Let $ v_1, \dots, v_m $ be a linearly independent list of vectors in $ V $ and let $ w \in V $.
$$ \{v_1, \dots, v_m, w\} \text{ is linearly independent} \iff w \notin \text{span}(v_1, \dots, v_m) $$

<details>
<summary>Solution</summary>

</details>

#### Exercise 14

Page reference: 38

Let $ v_1, \dots, v_m $ be a list of vectors in $ V $. Let $ w_k = \sum_{i=1}^{k} v_i $ for $ k \in \{1, \dots, m\} $.
$$ \{v_1, \dots, v_m\} \text{ is linearly independent} \iff \{w_1, \dots, w_m\} \text{ is linearly independent} $$

<details>
<summary>Solution</summary>

</details>

#### Exercise 15

Page reference: 38

There does not exist a list of six polynomials that is linearly independent in $ \mathcal{P}_4(F) $.

<details>
<summary>Solution</summary>

</details>

#### Exercise 16

Page reference: 38

No list of four polynomials spans $ \mathcal{P}_4(F) $.

<details>
<summary>Solution</summary>

</details>

#### Exercise 17

Page reference: 38

$$ V \text{ is infinite-dimensional} \iff \exists \text{ a sequence } v_1, v_2, \dots \text{ in } V \text{ such that } \{v_1, \dots, v_m\} \text{ is linearly independent for every positive integer } m $$

<details>
<summary>Solution</summary>

</details>

#### Exercise 18

Page reference: 38

$ F^\infty $ is infinite-dimensional.

<details>
<summary>Solution</summary>

</details>

#### Exercise 19

Page reference: 38

The real vector space of all continuous real-valued functions on the interval $ [0, 1] $ is infinite-dimensional.

<details>
<summary>Solution</summary>

</details>

#### Exercise 20

Page reference: 38

Let $ p_0, p_1, \dots, p_m $ be polynomials in $ \mathcal{P}_m(F) $ such that $ p_k(2) = 0 $ for each $ k \in \{0, \dots, m\} $.

The list $ p_0, p_1, \dots, p_m $ is not linearly independent in $ \mathcal{P}_m(F) $.

<details>
<summary>Solution</summary>

</details>
