Consider the poset of open coverings (with totally ordered index set) of $X$ given by$$\{U_i\}_{i\in I} \leq \{V_j\}_{j\in J} \iff \exists r: J \to I\quad V_j \subseteq U_{r(j)},$$where the $r: J \to I$ are morphisms of **ordered** sets.

**Achtung!** Aquí la $r$ forma part de l'estructura? Segons el que hi diu, no, però llavors el següent no té sentit.

Define the **coordiante-free Cech cohomology** as$$CH^p(X,\mathcal{F}) := colim_{\{U_i\}_i} CH^p(\{U_i\}_i, \mathcal{F}),$$where in the diagram the morphism associated to $\{U_i\}_i \leq \{V_j\}_j$ is$$\prod_{i_0 < \cdots < i_p} \mathcal{F}(U_{i_0, \dots, i_p}) \to \prod_{j_0 < \cdots < j_p} \mathcal{F}(V_{j_0, \dots, j_p}),\quad \alpha \mapsto (\alpha_{r(j_0), \dots, r(j_p)})_{j_0 < \cdots < j_p}.$$
*It's often the case* that $CH^p(X,\mathcal{F}) \cong H^p(X,\mathcal{F})$.

# Propietats

## Grau 1

En grau 1 tenim l'isomorfisme $CH^1(X,\mathcal{F}) \cong H^1(X,\mathcal{F})$.