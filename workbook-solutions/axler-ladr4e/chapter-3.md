$ T $ is linear map

$$ (Tf)(x) = x^2 f(x) $$

Additivity

$$ (T(f_1 + f_2))(x) = T f_1 (x) + T f_2(x) $$

Proof:

Let \( f_1 \) and \( f_2 \) be functions. Then,

$$
(T(f_1 + f_2))(x) = x^2 (f_1(x) + f_2(x))
$$

Using the distributive property of multiplication over addition, we get

$$
x^2 (f_1(x) + f_2(x)) = x^2 f_1(x) + x^2 f_2(x)
$$

By definition of \( T \), this can be written as

$$
x^2 f_1(x) + x^2 f_2(x) = (Tf_1)(x) + (Tf_2)(x)
$$

Therefore,

$$
(T(f_1 + f_2))(x) = (Tf_1)(x) + (Tf_2)(x)
$$

This proves that \( T \) is linear.

Homogeneity

$$ (T(\lambda f))(x) = \lambda T f (x) $$

Proof:

Let $ \lambda $ be a scalar and $ f $ be a function. Then,

$$
(T(\lambda f))(x) = x^2 (\lambda f(x))
$$

Using the associative property of multiplication, we get

$$
x^2 (\lambda f(x)) = \lambda (x^2 f(x))
$$

By definition of \( T \), this can be written as

$$
\lambda (x^2 f(x)) = \lambda (Tf)(x)
$$

Therefore,

$$
(T(\lambda f))(x) = \lambda (Tf)(x)
$$

This proves the homogeneity of \( T \).
