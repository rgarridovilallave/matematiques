Let $(I, \leq)$ be a poset (v.[[Partially ordered set]]) and $\mathcal{C}$ be a category. A **directed system of objects in $\mathcal{C}$ indexed by $I$** is a functor $I^{op} \to \mathcal{C}$.

A **direct limit** of a directed system $(A_i,\rho_i): I^{op} \to \mathcal{C}$ is a colimit of $(A_i,\rho_i)$.

# Properties

- They always exist in $Ab$, and equal$$colim (A_i,\rho_i) \cong \bigoplus_i A_i / N,$$where $$N = \langle a_i - \rho_{ij} (a_i) \mid a_i \in A_i,\ i \leq j\rangle.$$
- They always exist in $Set$, and equal$$colim(A_i,\rho_i) \cong \bigsqcup_i A_i/\sim,$$where$$A_i \ni a_i \sim a_j \in A_j \iff \exists k,\ \rho_{ik}(a_i) = \rho_{jk}(a_j).$$
- As sets, $colim^{Set}(A_i,\rho_i) \cong colim^{Ab}(A_i,\rho_i)$.
- The direct limit is exact in $Ab$.