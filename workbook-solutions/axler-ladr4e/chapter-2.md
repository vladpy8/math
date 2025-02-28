# Chapter 2. Finite-dimensional vector spaces

### Linear combinations example

page 28

Prove that there is no solution

$$ (17, -4, 5) = a_1 (2, 1, -3) + a_2 (1, -2, 4) $$

---

One vector equation leads to three field of numbers equations

$$
\begin{aligned}

17 &= 2 a_1 + a_2 \\

-4 &= a_1 - 2 a_2 \\

5 &= -3 a_1 + 4 a_2

\end{aligned}
$$

Adding first equation multiplied by 2 and second equation

$$
34 + (-4) = (4 a_1 + 2 a_2) + (a_1 - 2 a_2) \implies a_1 = 6
$$

Adding second equation multiplied by 2 and third equation

$$
-8 + 5 = (2 a_1 - 4 a_2) + (-3 a_1 + 4 a_2) \implies a_1 = 3
$$

### Polynomials are vector subspace

page 30

Given the field $ F $, vector space $ F^F = \{ f : F \rightarrow F \} $ and the subset of all polynomial functions

$$
P = \{ \ p(x) \in F^F : \quad \exist \ n \in N, \quad \exist ! \ a_0, a_1, ..., a_n \in F, \quad \forall x \in F, \quad \ p(x) = \sum_{i = 0}^{n}{a_i x^i} \}
$$

Prove that this subset is a subspace of $ F^F $

---

Let

$$
p(x), l(x) \in P , \ \ \lambda \in F
$$

Additive identity holds

$$
\exist \ c_0 = 0 : \quad \forall x \in F, \quad 0(x) = c_0 = 0
$$

$$
0 \in P
$$

Addition is closed under $ P $

$$

(p + l)(x) = p(x) + l(x) = \sum_{i=0}^{n} a_i x^i + \sum_{j=0}^{m} b_j x^j = \sum_{k=0}^{\max(n,m)} (\tilde{a}_k + \tilde{b}_k) x^k \\

\tilde{a}_i = \begin{cases}
	a_i \ \text{ if } i \in I, i \le n \\
	0 \ \text{ else }
\end{cases} \\

\tilde{b}_j = \begin{cases}
	b_j \ \text{ if } j \in I, j \le m \\
	0 \ \text{ else }
\end{cases} \\

$$

$$
p + l \in P
$$

Scalar multiplication is closed under $ P $

$$
\lambda \, p_1(x) = \lambda \, \sum_{i=0}^{n} a_i x^i = \sum_{i=0}^{n} (\lambda \, a_i) x^i
$$

$$
\lambda \, p_1 \in P
$$


### Removing vector from list of linearly independent

page 33

$$
a_1 v_1 + a_2 v_2 + ... + a_m v_m = 0 \ \Leftrightarrow \ a_1 = 0, \ a_2 = 0, \ ..., \ a_m = 0 \\
a_1' v_1 + a_2' v_2 + ... + a_{m-1}' v_{m-1} = 0 \\
a_1' v_1 + a_2' v_2 + ... + a_{m-1}' v_{m-1} + 0 \ v_m  = 0
$$

Some $ a_k' \ne 0 $

And some $ a_k' \ne 0 $
