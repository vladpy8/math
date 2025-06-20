# Solving logarithm and exponential equations

## Model equation

Let $ F $ be real-valued function of $ x \in \R, x > 0 $ and $ \alpha, \beta \in \R, \ \alpha \ne 0$

$$ F(\alpha, \beta, x) = \ln(x) + \alpha \, x - \beta $$

Solve for $ \alpha, \beta, x $

$$ F(\alpha, \beta, x) = 0 $$

### Solution existence and uniqueness

Set $ \alpha, \beta $ fixed

The function $ F $ is continuously differentiable in its domain

Derivative of $ F $ by $ x $ is

$$ D_x \, F(\alpha, \beta, x) = \frac{1}{x} + \alpha $$

Considering two ranges of $ \alpha $

#### Positive $ \alpha $

For $ \alpha > 0 $ and $ \forall x > 0, \ D_x \, F(\alpha, \beta, x) > 0 $, the function $ F $ is strictly monotonous by x

Let $ \lambda \in \R, \ \lambda > 0, \ \lambda < \min(\alpha, 1) $

$$ \lambda \, e^{-1 -|\beta|} < 1 $$

$$ \frac{\lambda \, e^{-1 -|\beta|}}{\alpha} < e^{1 + |\beta|} $$

Given two points

$$ F(\alpha, \beta, e^{1 + |\beta|}) = 1 + |\beta| + \alpha e^{1 + |\beta|} - \beta \ge 1 + \alpha e^{1 + |\beta|} > 0 $$

$$
\begin{aligned}

F \left(\alpha, \beta,  \frac{\lambda \, e^{-1 -|\beta|}}{\alpha} \right) &= \ln\left( \frac{\lambda \, e^{-1 -|\beta|}}{\alpha} \right) + \alpha \, \frac{\lambda \, e^{-1 -|\beta|}}{\alpha} - \beta \\

&= \ln(\lambda) - 1 - |\beta| - \ln(\alpha) + \lambda \, e^{-1 -|\beta|} - \beta \\

&< 0

\end{aligned}
$$

Considering continuity of the function $ F $, its strict monotonicity, as well as two points, in which function results in negative and positive values, one may conclude that there indeed exists a unique solution of the equation

$$ \forall \alpha > 0, \ \forall \lambda \in \R, \ \lambda > 0, \ \lambda < \min(\alpha, 1) \ \ \exist! \, x \in \R, \ x \in \left( \frac{\lambda \, e^{-1 -|\beta|}}{\alpha}, e^{1 + |\beta|} \right): F(\alpha, \beta, x) = 0 $$

#### Negative $ \alpha $

For $ \alpha < 0 $ and $ \forall x < \frac{1}{|\alpha|}, \ D_x \, F(\alpha, \beta, x) > 0 $, and $ \forall x > \frac{1}{|\alpha|}, \ D_x \, F(\alpha, \beta, x) < 0 $

Since $ x = \frac{1}{|\alpha|}, \ D_x \, F(\alpha, \beta, x) = 0 $, there is maximum of the function $ F(\alpha, \beta, x) $ in this point

$$ F\left(\alpha, \beta, \frac{1}{|\alpha|}\right) = \ln\left(\frac{1}{|\alpha|}\right) + \alpha \, \frac{1}{|\alpha|} - \beta = -\ln(|\alpha|) - 1 - \beta $$

#### Negative $ \alpha $, maximum below zero

If $ \frac{1}{|\alpha|} < e^{1 + \beta} $, there are no solutions of the equation $ F(\alpha, \beta, x) = 0 $, since maximum of the function is below $ 0 $

$$
\begin{aligned}

\ln\left( \frac{1}{|\alpha|} \right) = - \ln(|\alpha|) &< 1 + \beta \\

F\left(\alpha, \beta, \frac{1}{|\alpha|}\right) &< 0

\end{aligned}
$$

#### Negative $ \alpha $, maximum is zero

If $ \frac{1}{|\alpha|} = e^{1 + \beta} $, then $ x = \frac{1}{|\alpha|} $ becomes an unique solution, since this is the only maximum of the function $ F $

$$ F\left(\alpha, \beta, \frac{1}{|\alpha|}\right) = 0 $$

#### Negative $ \alpha $, maximum above zero

If $ \frac{1}{|\alpha|} > e^{1 + \beta} $, more thorough considerations are required

$$ F\left(\alpha, \beta, \frac{1}{|\alpha|}\right) > 0 $$

Let $ \lambda \in \R, \ \lambda > 0, \ \lambda < |\alpha| $

$$ \lambda \, e^{-1 -|\beta|} < |\alpha| \, e^{-1 -|\beta|} < |\alpha| \, e^{1 + \beta} < 1 $$

$$ 0 < \frac{\lambda \, e^{-1 -|\beta|}}{|\alpha|} < \frac{1}{|\alpha|} $$

Given the point

$$
\begin{aligned}

F \left(\alpha, \beta,  \frac{\lambda \, e^{-1 -|\beta|}}{|\alpha|} \right) &= \ln\left( \frac{\lambda \, e^{-1 -|\beta|}}{|\alpha|} \right) + \alpha \, \frac{\lambda \, e^{-1 -|\beta|}}{|\alpha|} - \beta \\

&= \ln(\lambda) - 1 - |\beta| - \ln(|\alpha|) - \lambda \, e^{-1 -|\beta|} - \beta \\

&< 0

\end{aligned}
$$

Since $ F(-1,0, x) $ is monotonous and decreasing for $ x > 1 $

$$ \forall x \in \R, \ x > 1, \ F(-1, 0, x) < F(-1, 0, 1) $$

$$
\ln(x) - x < -1 \\
\ln(x) < x - 1 < x \\
1 < x < e^x
$$

Let $ \gamma \in \R, \ \gamma > \ln(3 + |\beta| + |\ln(-\alpha)|) $

$$
e^{\gamma} > 3 + |\beta| + |\ln(-\alpha)| > - \beta - \ln(|\alpha|) \\
e^{\gamma} > 3 > \ln(3) \\
e^{\gamma} > \gamma > 1
$$

$$ \frac{e^{\gamma}}{|\alpha|} > \frac{1}{|\alpha|} $$

Given the point

$$
\begin{aligned}

F\left(\alpha, \beta,  \frac{3 \, e^{\gamma}}{|\alpha|} \right) &= \ln\left( \frac{3 \, e^{\gamma}}{|\alpha|} \right) + \alpha \, \frac{3 \, e^{\gamma}}{|\alpha|} - \beta \\

&= \ln(3) + \gamma - \ln(|\alpha|) - 3 \, e^{\gamma} - \beta \\

&< 0

\end{aligned}
$$

The function $ F $ is continuous, strictly monotonous in each interval between the points $ \frac{\lambda \, e^{-1 -|\beta|}}{|\alpha|}, \frac{1}{|\alpha|}, \frac{3 \, e^{\gamma}}{|\alpha|} $, as well as it results in negative, positive and negative sequence of values. Therefore it is possible to conclude that there are two solutions, one per each corresponding interval

$$ \forall \alpha < 0, \ \forall \lambda \in \R, \ \lambda > 0, \ \lambda < |\alpha|, \ \ \exist! \, x \in \R, \ x \in \left( \frac{\lambda \, e^{-1 -|\beta|}}{|\alpha|}, \frac{1}{|\alpha|} \right): F(\alpha, \beta, x) = 0 $$

$$ \forall \alpha < 0, \ \forall \gamma \in \R, \ \gamma > \ln(3 + |\beta| + |\ln(-\alpha)|), \ \ \exist! \, x \in \R, \ x \in \left( \frac{1}{|\alpha|}, \frac{3 \, e^{\gamma}}{|\alpha|} \right): F(\alpha, \beta, x) = 0 $$


#### Summary

There exists an unique solution if $ \alpha > 0 $ or $ \alpha < 0, \frac{1}{|\alpha|} = e^{1 + \beta} $. And there are two solutions of the equation if $ \alpha < 0, \frac{1}{|\alpha|} > e^{1 + \beta} $

### Solution function

Since the function $ F $ is continuously differentiable and monotonous under certain conditions, there do exist solutions of the equation $ F(\alpha, \beta, x) = 0 $, it might be further investigated that the equation determines implicit function $ x_{sol} $ as function of $ \alpha, \beta $

$$ \exists \, x_{sol} \in \{ \R^2 \rightarrow \R \}: \ F(\alpha, \beta, x_{sol}(\alpha, \beta)) = 0 $$

#### Positive $ \alpha $

The trivial solution is

$$ F(1, -1, 1) = 0 $$

Since for $ \alpha > 0 $ and $ \forall x > 0, \ D_x \, F(\alpha, \beta, x) > 0 $, and there does exist one solution, all criteria for the implicit function theorem are met

$$ x_{sol}(1, -1) = 1 $$

More over, function $ x_{sol} $ is continuously differentiable

$$
\begin{aligned}

D_{\alpha} \, x_{sol}(\alpha, \beta) &= - \frac{D_{\alpha} \, F(\alpha, \beta, x)}{D_{x} \, F(\alpha, \beta, x)} \\

&= - \frac{x}{\frac{1}{x} + \alpha} \\

&= - \frac{x^2}{1 + \alpha \, x}

\end{aligned}
$$

$$
\begin{aligned}

D_{\beta} \, x_{sol}(\alpha, \beta) &= - \frac{D_{\beta} \, F(\alpha, \beta, x)}{D_{x} \, F(\alpha, \beta, x)} \\

&= - \frac{(-1)}{\frac{1}{x} + \alpha} \\

&= \frac{x}{1 + \alpha \, x}

\end{aligned}
$$

TODO

$$ \frac{\partial}{\partial x} $$
