**Direct image functor:** Let $f: X \to Y$ be a continuous morphism. There's an induced functor$$f_*: Sh(X) \to Sh(Y)$$defined by $(f_* \mathcal{F})(U) := \mathcal{F}(f^{-1}(U))$. (also should specify the image of the restriction maps, and check that it's indeed a sheaf (and not only a presheaf)). The image of a morphism $\varphi: \mathcal{F} \to \mathcal{G}$ is $(f_*\varphi)_U := \varphi_{f^{-1}(U)}$.

**Inverse image functor:** Let $f: X \to Y$ be a continuous function. There's an induced (contravariant) functor $$f^{-1}:Sh(Y) \to Sh(X)$$defined by (given $\mathcal{G} \in Sh(Y)$):
- $f^{-1}\mathcal{G}$ is the sheafification of the presheaf $V \subseteq X \mapsto colim_{f(V) \subseteq U} \mathcal{G}(U)$.
- For $V_1 \subseteq V_2$, the restriction $\rho^{f^{-1} \mathcal{G}}_{V_1,V_2}$ is the natural map $colim_{f(V_2) \subseteq U} \mathcal{G}(U) \to colim_{f(V_1) \subseteq U} \mathcal{G}(U)$.
- To define $f^{-1} \varphi$ use the universal property of the sheafification functor.

# Properties

By definition,
- $(f_* \mathcal{F})_y \cong colim_{y \in U} \mathcal{F}(f^{-1}(U))$,
- $(f^{-1} \mathcal{G})_x \cong \mathcal{G}_{f(x)}$,
- There's a morphism $(f_*\mathcal{F})_{f(x)} \to \mathcal{F}_x$.

## Adjunction

$f^{-1}$ is left adjoint to $f_*$.

As a consequence,
- When the adjunction is applied to $\mathcal{F} = f^{-1} \mathcal{G}$, the identity $id_{f ^{-1} \mathcal G}$ gives the adjunction morphism $\mathcal{G} \to f_* f^{-1} \mathcal{G}$.
- Likewise, one obtains the adjunction morphism $f^{-1} f_* \mathcal{F} \to \mathcal{F}$.

## Exactness of $f^{-1}$

$f^{-1}: Sh(Y) \to Sh(X)$ is exact.

*Proof.*

$f^{-1} \mathcal{G}_1 \to f^{-1}\mathcal{G}_2 \to f^{-1} \mathcal{G}_3$ is exact if, and only if, $(f^{-1} \mathcal{G}_1)_x \to (f^{-1}\mathcal{G}_2)_x \to (f^{-1} \mathcal{G}_3)_x$ is exact for every $x$. It is indeed exact because $(f^{-1} \mathcal{G}_i)_{x} = (\mathcal{G}_i)_{f(x)}$ (by definition), and by hypothesis we have exactness of the stalks (v. [[Stalk]]). **qed**

## Left exactness of $f_*$

$f_*: Sh(X) \to Sh(Y)$ is **left** exact.

*Proof.*

The sequence$$0 \to \mathcal{F}_1(f^{-1}(U)) \to \mathcal{F}_2(f^{-1}(U)) \to \mathcal{F}_3(f^{-1}(U))$$is exact for every $U \subseteq Y$.

Hence, after taking the direct limit $colim_{y \in U}$ we still have an exact sequence, since the direct limit is exact (v. [[Direct limit]]). By definition, this is an exact sequence$$0 \to (f_* \mathcal{F}_1)_y \to (f_* \mathcal{F}_2)_y \to (f_* \mathcal{F}_3)_y.$$
**qed**

# Exemples

## $X \to *$

Consider $f: X \to *$. Then$$f_*:Sh(X) \to Sh(*) = Ab$$sends a sheaf $\mathcal{F}$ over $X$ to $\mathcal{F}(f^{-1}(*)) = \mathcal{F}(X)$. Therefore, $f_* = \Gamma(X,-)$. Aquí s'observa que $f_*$ no és right exact, ja que hi ha $\mathcal{F}_2 \to \mathcal{F}_3$ exhaustives amb $\mathcal{F}_2(X) \to \mathcal{F}_3(X)$ no exhaustiu.

The inverse image$$f^{-1}: Ab=Sh(*) \to Sh(X)$$sends an abelian group $A$ to the constant sheaf $\underline{A}$.

## $* \to X$

Consider $f: * \to X$. Then$$f_*: Ab = Sh(*) \to Sh(X)$$maps an abelian group $A$ to the sheaf$$f_*A: U \mapsto \begin{cases}A,& x \in U,\\ 0\end{cases}.$$
The inverse sheaf $$f ^{-1}: Sh(X) \to Sh(*) = Ab$$sends $\mathcal{F}$ to its stalk $\mathcal{F}_{f(*)}$ at $f(*)$.