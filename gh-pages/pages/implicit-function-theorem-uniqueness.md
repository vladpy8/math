$$ \forall k \in [1, m]: F_k(\vec{x}, \vec{y}) = F_k(x_1, ..., x_n, y_1, ..., y_m) $$

$$ \forall k \in [1, m]:  F_k(\vec{x}, \phi_1(\vec{x}), ..., \phi_m(\vec{x})) = 0$$

Suppose

$$ \forall k \in [1, m]:  F_k(\vec{x}, \psi_1(\vec{x}), ..., \psi_m(\vec{x})) = 0$$

And at least for some $j$ and some $\vec{x^{(0)}}$

$$ \psi_j(\vec{x^{(0)}}) \neq \phi_j(\vec{x^{(0)}}) $$

Impossible. Proof:

$$ \forall k \in [1, m]:  \Delta y_k(\vec{x^{(0)}}) = \psi_k(\vec{x^{(0)}}) - \phi_k(\vec{x^{(0)}}) $$

For some $j$

$$ \Delta y_j(\vec{x^{(0)}}) \neq 0 $$

Then, delta of $F$ by Lagrange mean value theorem

$$ \forall k \in [1, m]: \Delta F_k (\vec{x^{(0)}}) = F_k(\vec{x^{(0)}}, \phi_1(\vec{x^{(0)}}), ..., \phi_m(\vec{x^{(0)}})) - F_k(\vec{x^{(0)}}, \psi_1(\vec{x^{(0)}}), ..., \psi_m(\vec{x^{(0)}})) = $$

$$ = \sum_{i=1}^{m} \frac{\partial{F_k}}{\partial{y_i}} (\vec{x^{(0)}}, \vec{y^{(c)}}) \Delta y_i (\vec{x^{(0)}}) = 0 $$

Given solutions by Cramer's Rule, in case of unique solution it must be zero, which contradicts initial statement
