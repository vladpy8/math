# Solving log equations cheat sheet

## Model equation

Let $ \alpha, \beta \in \R, \ \alpha, \beta \ne 0$

Let $ F_{\alpha, \beta} $ be real-valued function for $ x \in \R, x > 0 $

$$ F_{\alpha, \beta}(x) = \ln(x) + \alpha \, x - \beta $$

Solve for $ x $

$$ F_{\alpha, \beta}(x) = 0 $$

### Solution existence and uniqueness

The function $ F_{\alpha, \beta} $ is continuous and differentiable in its domain

Derivative of $ F_{\alpha, \beta} $ by $ x $ is

$$ D_x \, F_{\alpha, \beta}(x) = \frac{1}{x} + \alpha $$

Considering two ranges of $ \alpha $

#### Positive $ \alpha $

For $ \alpha \ge 0 $, and $ \forall x > 0, \ D_x \, F_{\alpha, \beta}(x) > 0 $, the function $ F_{\alpha, \beta}(x) $ is strictly monotonous

Let $ \lambda \in \R, \ \lambda > 0, \ \lambda < \alpha, |\beta| $

Given two points

$$ F_{\alpha, \beta}(e^{|\beta|}) = |\beta| + \alpha e^{|\beta|} - \beta \ge \alpha e^{|\beta|} > 0 $$

$$ F_{\alpha, \beta}\left( \frac{\lambda}{\alpha} \right) = \ln\left( \frac{\lambda}{\alpha} \right) + \alpha \, \frac{\lambda}{\alpha} - \beta = (\ln(\lambda) -\ln(\alpha)) + (\lambda - \beta) < 0 $$

Considering continuity of the function $ F_{\alpha, \beta} $, its strict monotony, as well as two points, in which function results in negative and positive values, one may conclude that there indeed exists a unique solution to the equation, which is located between $ \frac{\lambda}{\alpha} $ and $ e^{\beta} $

#### Negative $ \alpha $

For $ \alpha < 0 $ and $ \forall x < \frac{1}{|\alpha|}, \ D_x \, F_{\alpha, \beta}(x) > 0 $, and $ \forall x > \frac{1}{|\alpha|}, \ D_x \, F_{\alpha, \beta}(x) < 0 $

Since $ x = \frac{1}{|\alpha|}, \ D_x \, F_{\alpha, \beta}(x) = 0 $, there is maximum of the function $ F_{\alpha, \beta}(x) $ in this point

$$ F_{\alpha, \beta}\left(\frac{1}{|\alpha|}\right) = \ln\left(\frac{1}{|\alpha|}\right) + \alpha \, \frac{1}{|\alpha|} - \beta = -\ln(|\alpha|) - 1 - \beta $$

If $ \frac{1}{|\alpha|} < e^{1 + \beta} $, there are no solutions to the equation $ F_{\alpha, \beta}(x) = 0 $, since maximum of the function is below $ 0 $

$$
\begin{aligned}

\ln\left( \frac{1}{|\alpha|} \right) = - \ln(|\alpha|) &< 1 + \beta \\

F_{\alpha, \beta}\left(\frac{1}{|\alpha|}\right) &< 0

\end{aligned}
$$

If $ \frac{1}{|\alpha|} = e^{1 + \beta} $, then $ x = \frac{1}{|\alpha|} $ becomes an unique solution, since this is the only maximum of the function $ F_{\alpha, \beta}(x) $

$$ F_{\alpha, \beta}\left(\frac{1}{|\alpha|}\right) = 0 $$

If $ \frac{1}{|\alpha|} > e^{1 + \beta} $

$$ F_{\alpha, \beta}\left(\frac{1}{|\alpha|}\right) > 0 $$

Let $ \gamma \in \R, \ \gamma > |\alpha|, \beta$

Let $ \lambda \in \R, \ \lambda > 0, \ \lambda < |\alpha|, \beta $

Given two points

$$
\begin{aligned}

F_{\alpha, \beta}\left(\frac{\lambda \, e^{|\beta|}}{|\alpha|}\right) &= \ln\left(\frac{\lambda \, e^{|\beta|}}{|\alpha|}\right) + \alpha \, \frac{\lambda \, e^{|\beta|}}{|\alpha|} - \beta \\
&= \ln(\lambda) + |\beta| - \ln(|\alpha|) - \lambda \, e^{|\beta|} - \beta

\end{aligned}
$$
