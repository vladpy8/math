# Chapter 1. Vector spaces. <br>Section 1C. Subspaces

## Exercises 1C

Page 24

### Exercise 1C.1

Page 24

#### Part a

Let $ U_a \subseteq F^3 $

$$ U_a = \{ (x_1, x_2, x_3) \in F^3 : \quad x_1 + 2x_2 + 3x_3 = 0 \}. $$

---

#### Part b

Let $ U_b \subseteq F^3 $

$$ U_b = \{ (x_1, x_2, x_3) \in F^3 : \quad x_1 + 2x_2 + 3x_3 = 4 \}. $$

---

#### Part c

Let $ U_c \subseteq F^3 $

$$ U_c = \{ (x_1, x_2, x_3) \in F^3 : \quad x_1 x_2 x_3 = 0 \}. $$

---

#### Part d

Let $ U_d \subseteq F^3 $

$$ U_d = \{ (x_1, x_2, x_3) \in F^3 : \quad x_1 = 5x_3 \}. $$

---

### Exercise 1C.2

Page 24

#### Part a

Let $ b \in F $

Let $ U_a \subseteq F^4 $

$$ U_a = \{ (x_1, x_2, x_3, x_4) \in F^4 : \quad x_3 = 5x_4 + b  \} $$

Then

$$ U_a \ \text{is a subspace of} \ F^4 \iff b = 0 $$

---

#### Part b

Let $ U_b \subseteq \R^{[0,1]} $

$$ U_b = \{ f \in \R^{[0,1]} : \quad f \ \text{is continuous on} \ [0,1] \} $$

Then $ U_b $ is a subspace of $ \R^{[0,1]} $

---

#### Part c

Let $ U_c \subseteq \R^{\R} $

$$ U_c = \{ f \in \R^{\R} : f \ \text{is differentiable on} \ \R \} $$

Then $ U_c $ is a subspace of $ \R^{\R} $

---

#### Part d

Let $ b \in \R $

Let $ U_d \subseteq \R^{(0,3)} $

$$ U_d = \{ f \in \R^{(0,3)} : f \ \text{is differentiable on} \ (0,3) \ \text{and} \ f'(2) = b \} $$

Then

$$ U_d \, \text{is a subspace of} \, \R^{(0,3)} \iff b = 0 $$

---

#### Part e

Let $ U_e \subseteq \mathbb{C}^{\infty} $

$$ U_e = \{ (x_n)_{n=1}^\infty \in \mathbb{C}^{\infty} : \quad \lim_{n \to \infty} x_n = 0 \}. $$

Then $ U_e $ is a subspace of $ \mathbb{C}^{\infty} $

---

### Exercise 1C.3. Differentiable functions as a Subspace

Let $ U \subseteq \R^{(-4,4)} $.
$$ U = \{ f \in \R^{(-4,4)} : f \text{ is differentiable and } f'(-1)=3f(2) \} $$
Prove that $U$ is a subspace of $\R^{(-4,4)}$.

---

### Exercise 1C.4. Continuous Functions with a Fixed Integral Value

Let $ b \in \R $.
Let $ U_b \subseteq \R^{[0,1]} $.
$$ U_b = \{ f \in \R^{[0,1]} : f \text{ is continuous and } \int_0^1 f(x) dx = b \} $$
Prove that $U_b$ is a subspace of $\R^{[0,1]} \iff b=0$.

---

### Exercise 1C.5. $ \R^2 $ as a Subspace of $ \mathbb{C}^2 $

Let $ U = \R^2 $.
Is $U$ a subspace of the complex vector space $\mathbb{C}^2$?

---

### Exercise 1C.6. Subsets Defined by $a^3=b^3$

#### Part a

Let $ U_a \subseteq \R^3 $.
$$ U_a = \{ (a,b,c) \in \R^3 : a^3=b^3 \} $$
Is $U_a$ a subspace of $\R^3$?

---

#### Part b

Let $ U_b \subseteq \mathbb{C}^3 $.
$$ U_b = \{ (a,b,c) \in \mathbb{C}^3 : a^3=b^3 \} $$
Is $U_b$ a subspace of $\mathbb{C}^3$?

---

### Exercise 1C.7. Conditions for a Subset of $ \R^2 $ to be a Subspace

Let $ U \subseteq \R^2, U \ne \emptyset $.
Given:
1. $ \forall u, v \in U \implies u+v \in U $
2. $ \forall u \in U \implies -u \in U $
Prove or disprove: $U$ is a subspace of $\R^2$.

---

### Exercise 1C.8. Closure under Scalar Multiplication but Not a Subspace

Find $ U \subseteq \R^2, U \ne \emptyset $ such that:
1. $ \forall \lambda \in \R, \forall u \in U \implies \lambda u \in U $
2. $U$ is not a subspace of $\R^2$.

---

### Exercise 1C.9. Set of Periodic Functions

Let $ V = \R^\R $.
A function $f \in V$ is periodic if $ \exists p \in \R, p > 0 $ such that $ \forall x \in \R, f(x) = f(x+p) $.
Let $ U = \{ f \in V : f \text{ is periodic} \} $.
Is $U$ a subspace of $V$? Explain.

---

### Exercise 1C.10. Intersection of Two Subspaces

Let $V_1, V_2$ be subspaces of $V$.
Prove that $V_1 \cap V_2$ is a subspace of $V$.

---

### Exercise 1C.11. Intersection of a Collection of Subspaces

Let $ \{U_i\}_{i \in I} $ be a collection of subspaces of $V$.
Prove that $ \bigcap_{i \in I} U_i $ is a subspace of $V$.

---

### Exercise 1C.12. Union of Two Subspaces

Let $U_1, U_2$ be subspaces of $V$.
Prove that $ (U_1 \cup U_2 \text{ is a subspace of } V) \iff (U_1 \subseteq U_2 \text{ or } U_2 \subseteq U_1) $.

---

### Exercise 1C.13. Union of Three Subspaces

Let $U_1, U_2, U_3$ be subspaces of $V$.
Prove that $ (U_1 \cup U_2 \cup U_3 \text{ is a subspace of } V) \iff (\exists i \in \{1,2,3\} \text{ such that } U_j \subseteq U_i \text{ for all } j \ne i \text{ where } j \in \{1,2,3\}) $.

*This exercise is surprisingly harder than Exercise 12, possibly because this exercise is not true if we replace F with a field containing only two elements.*

---

### Exercise 1C.14. Sum of Two Specific Subspaces in $F^3$

Let $ U \subseteq F^3 $.
$$ U = \{(x, -x, 2x) \in F^3 : x \in F\} $$
Let $ W \subseteq F^3 $.
$$ W = \{(x, x, 2x) \in F^3 : x \in F\} $$
Describe $U+W$ using symbols, and also give a description of $U+W$ that uses no symbols.

---

### Exercise 1C.15. Sum of a Subspace with Itself

Let $U$ be a subspace of $V$.
$U+U = ?$

---

### Exercise 1C.16. Commutativity of Subspace Addition

Let $U, W$ be subspaces of $V$.
Is $U+W = W+U$?

---

### Exercise 1C.17. Associativity of Subspace Addition

Let $V_1, V_2, V_3$ be subspaces of $V$.
Is $(V_1+V_2)+V_3 = V_1+(V_2+V_3)$?

---

### Exercise 1C.18. Additive Identity and Inverses for Subspace Addition

#### Part 1
Does $\exists Z_S$, a subspace of $V$, such that $\forall U \text{ (subspace of } V), U + Z_S = U$?

---

#### Part 2
For which subspace $U$ of $V$ does $\exists U'$, a subspace of $V$, such that $U+U' = Z_S$ (if $Z_S$ exists from Part 1)?

---

### Exercise 1C.19. Cancellation Property for Subspace Addition

Let $V_1, V_2, U$ be subspaces of $V$.
Given $V_1+U = V_2+U$.
Prove or disprove: $V_1=V_2$.

---

### Exercise 1C.20. Direct Sum Complement in $F^4$

Let $ U \subseteq F^4 $.
$$ U = \{(x,x,y,y) \in F^4 : x,y \in F\} $$
Find a subspace $W \subseteq F^4$ such that $F^4 = U \oplus W$.

---

### Exercise 1C.21. Direct Sum Complement in $F^5$

Let $ U \subseteq F^5 $.
$$ U = \{(x,y,x+y,x-y,2x) \in F^5 : x,y \in F\} $$
Find a subspace $W \subseteq F^5$ such that $F^5 = U \oplus W$.

---

### Exercise 1C.22. Multiple Direct Sum Complements in $F^5$

Let $ U \subseteq F^5 $.
$$ U = \{(x,y,x+y,x-y,2x) \in F^5 : x,y \in F\} $$
Find three subspaces $W_1, W_2, W_3 \subseteq F^5$ such that $W_1 \ne \{0\}, W_2 \ne \{0\}, W_3 \ne \{0\}$ and $F^5 = U \oplus W_1 \oplus W_2 \oplus W_3$.

---

### Exercise 1C.23. Uniqueness of Direct Sum Complement

Let $V_1, V_2, U$ be subspaces of $V$.
Given $V = V_1 \oplus U$ and $V = V_2 \oplus U$.
Prove or disprove: $V_1=V_2$.

*Hint: When trying to discover whether a conjecture in linear algebra is true or false, it is often useful to start by experimenting in $F^2$.* (page 26)

---

### Exercise 1C.24. Even and Odd Functions

Let $f: \R \to \R$.
$f$ is even if $ \forall x \in \R, f(-x)=f(x) $.
$f$ is odd if $ \forall x \in \R, f(-x)=-f(x) $.
Let $ V_e \subseteq \R^\R $.
$$ V_e = \{ f \in \R^\R : f \text{ is even} \} $$
Let $ V_o \subseteq \R^\R $.
$$ V_o = \{ f \in \R^\R : f \text{ is odd} \} $$
Prove that $ \R^\R = V_e \oplus V_o $.

---
