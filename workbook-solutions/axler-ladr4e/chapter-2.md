### Polynomials are vector subspace

page 30

Given the field $ F $ and the set of all polynomial functions


$ P = \{ \ p(x) \in F^F : \exists \ n \in N, \ \exists \ a_0, a_1, ..., a_n \in F \text{ such that } \ p(x) \equiv a_0 + a_1 x + a_2 x^2 + ... + a_n x^n \ \text{ for } \forall x \in F \ \} $

Prove that this set is a subspace of vector space

$ F^F = \{ f : F \rightarrow F \} $

---

$ p_1(x), p_2(x) \in P , \ \ \lambda \in F $

$ 0 = 0(x) \in P $

$ p_1(x) + p_2(x) = (a_0 + a_1 x + a_2 x^2 + ... + a_n x^n) + (b_0 + b_1 x + b_2 x^2 + ... + b_m x^m) $

$ = (a_0 + b_0) + (a_1 + b_1)x + (a_2 + b_2)x^2 + ... + (a_{\max(n,m)} + b_{\max(n,m)})x^{\max(n,m)} $

$ (p_1(x) + p_2(x)) \in P $

$ \lambda p_1(x) = \lambda (a_0 + a_1 x + a_2 x^2 + ... + a_n x^n) = (\lambda a_0) + (\lambda a_1)x + (\lambda a_2)x^2 + ... + (\lambda a_n)x^n $

$ \lambda p_1(x) \in P $

Therefore, we have shown that the set $P$ is closed under addition and scalar multiplication, and it contains the zero polynomial. Hence, $P$ is a subspace of the vector space $F^F$.


### Removing vector from list of linearly independent

page 33

$ a_1 v_1 + a_2 v_2 + ... + a_m v_m = 0 \ \Leftrightarrow \ a_1 = 0, \ a_2 = 0, \ ..., \ a_m = 0 $

Imagine

$ a_1' v_1 + a_2' v_2 + ... + a_{m-1}' v_{m-1} = 0 $

Some $ a_k' \ne 0 $

Then

$ a_1' v_1 + a_2' v_2 + ... + a_{m-1}' v_{m-1} + 0 \ v_m  = 0 $

And some $ a_k' \ne 0 $
