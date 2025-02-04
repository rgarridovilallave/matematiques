Let $k$ be a field. A **valuation** of $k$ is a map $\nu: k^\times \to \Gamma$, where $\Gamma$ is a totally ordered abelian group, such that
1. $\nu(xy) = \nu(x) + \nu(y)$,
2. $\nu(x+y) \geq min\{\nu(x),\nu(y)\}$.

Then the **valuation ring** (v. [[Discrete valuation ring]]) is$$\mathcal{O}_\nu := \{x \in k \mid \nu(x) \geq 0\}.$$
**Fact.** $Spec(k) \subseteq Spec(\mathcal{O}_\nu)$ is open. Note that $Spec(k) = \{\eta\}$, $Spec(\mathcal{O}_\nu) = \{\eta, \mathfrak{m}_\nu\}$, with $\eta$ open and $\mathfrak{m}_\nu$ closed.