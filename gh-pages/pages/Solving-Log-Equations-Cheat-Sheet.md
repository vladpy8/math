# Solving log equations cheat sheet

## Model equation

Let $ \alpha, \beta \in \R, \ \alpha \ne 0$

Let $ F_{\alpha, \beta} $ be real-valued function of $ x \in \R, x > 0 $

$$ F_{\alpha, \beta}(x) = \ln(x) + \alpha \, x - \beta $$

Solve for $ x \in \R $

$$ F_{\alpha, \beta}(x) = 0 $$

### Solution existence and uniqueness

The function $ F_{\alpha, \beta} $ is continuous and differentiable in its domain

Derivative of $ F_{\alpha, \beta} $ by $ x $ is

$$ D_x \, F_{\alpha, \beta}(x) = \frac{1}{x} + \alpha $$

Considering two ranges of $ \alpha $

#### Positive $ \alpha $

For $ \alpha > 0 $, and $ \forall x > 0, \ D_x \, F_{\alpha, \beta}(x) > 0 $, the function $ F_{\alpha, \beta}(x) $ is strictly monotonous

Let $ \lambda \in \R, \ \lambda > 0, \ \lambda < \alpha, |\beta| $

Given two points

$$ F_{\alpha, \beta}(e^{|\beta|}) = |\beta| + \alpha e^{|\beta|} - \beta \ge \alpha e^{|\beta|} > 0 $$

$$ F_{\alpha, \beta}\left( \frac{\lambda}{\alpha} \right) = \ln\left( \frac{\lambda}{\alpha} \right) + \alpha \, \frac{\lambda}{\alpha} - \beta = (\ln(\lambda) -\ln(\alpha)) + (\lambda - \beta) < 0 $$

???

$$ F_{\alpha, \beta}\left( \frac{\lambda \, e^{-|\beta|}}{\alpha} \right) = \ln\left( \frac{\lambda \, e^{-|\beta|}}{\alpha} \right) + \alpha \, \frac{\lambda \, e^{-|\beta|}}{\alpha} - \beta = \ln(\lambda) - \ln(\alpha) - |\beta| + \lambda \, e^{-|\beta|} - \beta $$

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

If $ \frac{1}{|\alpha|} > e^{1 + \beta} $, thorough considerations are required

$$ F_{\alpha, \beta}\left(\frac{1}{|\alpha|}\right) > 0 $$

Since $ F_{-1,0} $ is monotonous and decreasing for $ x > 1 $

$$ \forall x \in \R, \ x > 1, \ F_{-1,0}(x) < F_{-1,0}(1) $$

$$
\ln(x) - x < -1 \\
\ln(x) < x - 1 < x
$$

Let $ \gamma \in \R, \ \gamma > \ln(3 + |\beta| + |\ln(|\alpha|)|) $

$$ e^{\gamma} > 3 + |\beta| + |\ln(|\alpha|)| > - \beta - \ln(|\alpha|) $$

$$ e^{\gamma} > 3 > \ln(3) $$

$$ e^{\gamma} > \gamma > 1 $$

$$ \frac{e^{\gamma}}{|\alpha|} > \frac{1}{|\alpha|} $$

Let $ \lambda \in \R, \ \lambda > 0, \ \lambda < |\alpha| $

$$ \lambda \, e^{-1 -|\beta|} < |\alpha| \, e^{-1 -|\beta|} < |\alpha| \, e^{1 + \beta} < 1 $$

$$ 0 < \frac{\lambda \, e^{-1 -|\beta|}}{|\alpha|} < \frac{1}{|\alpha|} $$

Given two points
$$
\begin{aligned}

F_{\alpha, \beta}\left( \frac{3 \, e^{\gamma}}{|\alpha|} \right) &= \ln\left( \frac{3 \, e^{\gamma}}{|\alpha|} \right) + \alpha \, \frac{3 \, e^{\gamma}}{|\alpha|} - \beta \\

&= \ln(3) + \gamma - \ln(|\alpha|) - 3 \, e^{\gamma} - \beta \\

&> 0

\end{aligned}
$$

$$
\begin{aligned}

F_{\alpha, \beta}\left( \frac{\lambda \, e^{-1 -|\beta|}}{|\alpha|} \right) &= \ln\left( \frac{\lambda \, e^{-1 -|\beta|}}{|\alpha|} \right) + \alpha \, \frac{\lambda \, e^{-1 -|\beta|}}{|\alpha|} - \beta \\

&= \ln(\lambda) - 1 - |\beta| - \ln(|\alpha|) - \lambda \, e^{-1 -|\beta|} - \beta \\

&< 0

\end{aligned}
$$
