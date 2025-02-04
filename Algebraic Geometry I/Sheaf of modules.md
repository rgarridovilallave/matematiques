
Let $(X,\mathcal{O}_X)$ be a ringed space. A **sheaf of $\mathcal{O}_X$-modules** is a sheaf $\mathcal{F}$ on $X$ together with the structure of an $\mathcal{O}_X(U)$-module on $\mathcal{F}(U)$ for every $U$ open, such that for every open $V \subseteq U \subseteq X$, the restriction $\rho_{UV}: \mathcal{F}(U) \to \mathcal{F}(V)$ is a morphism of $\mathcal{O}_X(U)$-modules ($\mathcal{F}(V)$ is viewed as a $\mathcal{O}_X(U)$-module via $\mathcal{O}_X(U) \to \mathcal{O}_X(V)$).

Given $\mathcal{F} \in Mod(X,\mathcal{O}_X)$, we say it is...
- **Free:** $\mathcal{F} \cong \mathcal{O}_X^{\oplus I}$, $I$ index set. If $\# I < \infty$, we say that it's free of **rank** $\# I$.
- **Locally free:** $\mathcal{F}|_{U_i} \cong \mathcal{O}_X|_{U_i}^{\oplus I}$ for some open covering $\{U_i\}_i$ of $X$.
- **Invertible:** $\mathcal{F}$ is locally free of rank $1$.

We have a tensor product in $Mod(X,\mathcal{O}_X)$. More explicitly, $\mathcal{F} \otimes \mathcal{G}$ is defined as the sheafification of$$U \mapsto \mathcal{F}(U) \otimes_{\mathcal{O}_X(U)} \mathcal{G}(U).$$

# Propietats

## Forgetful functor

The forgetful functor $U: Mod(X,\mathcal{O}_X) \to Sh(X)$ is **faithful** but **not full**.

## Abelian category

$Mod(X,\mathcal{O}_X)$ is an abelian category. v. [[Categoria abeliana]]

## Sheafification

Es pot fer la sheafification d'un pre-sheaf de $\mathcal{O}_X$-modules, i s'obté un sheaf de $\mathcal{O}_X$-modules. v. [[Sheafification]]

## Restriction

Given $U \subseteq X$ open, the restricition functor $Mod(X,\mathcal{O}_X) \to Mod(U,\mathcal{O}_X|_U)$ is **exact**.

## Adjunction given by change of underlying sheaf

Let $X$ be a topological space with two sheaves of rinfs $\mathcal{O}_X$,. $\mathcal{O}_X'$, and a morphism of sheaves $f:\mathcal{O}_X \to \mathcal{O}_{X'}$. Then we have an adjunction (nonstandard notation)$$- \otimes_{\mathcal{O}_X} \mathcal{O}_X' \dashv \textrm{restriction\ scalars}.$$

## Adjunction given by a morphism of ringed spaces

With more abstract nonsense (using the (co?)unit of the adjunction $f^{-1} \dashv f_*$) we obtain another functor $$f^*: Mod(Y,\mathcal{O}_Y) \to Mod(X,\mathcal{O}_X).$$It is compatible with the forgetful functor and $f^{-1}$. This compatibility implies its **right exactness** (?).

Let $(f,f^\sharp): (X,\mathcal{O}_X) \to (Y, \mathcal{O}_Y)$ be a morphism of ringed spaces.

**Direct image functor $f_*: Mod(X,\mathcal{O}_X) \to Mod(Y,\mathcal{O}_Y)$.** Consider a $\mathcal{O}_X$-module $\mathcal{F}$. We can take its sheaf-theoretic direct image$$U \mapsto \mathcal{F}(f^{-1}U),\quad U \subseteq Y,$$which inherits a $f_*\mathcal{O}_X$-module structure. It's a module in $Mod(Y,f_* \mathcal{O}_X)$. The morphism $f^\sharp: \mathcal{O}_Y \to f_* \mathcal{O}_X$ allows us to pull back the $f_* \mathcal{O}_X$-module structure to a $\mathcal{O}_Y$-module. Thus we get an element in $Mod(Y,\mathcal{O}_Y)$.

Putting all of this together gives a functor $f_*: Mod(X,\mathcal{O}_X) \to Mod(Y,\mathcal{O}_Y)$, which is the composite$$Mod(X,\mathcal{O}_X) \to Mod(Y,f_*\mathcal{O}_X) \to Mod(Y,\mathcal{O}_Y).$$
It's compatible with the forgetful functor and the direct image functor (of sheaves), so we deduce that it's **left exact**.

**Inverse image functor $f^*: Mod(Y,\mathcal{O}_Y) \to Mod(X,\mathcal{O}_X)$.*** Consider a $\mathcal{O}_Y$-module $\mathcal{F}$. We can take its sheaf-theoretic inverse image $f^{-1} \mathcal{F}$ and obtain a $f^{-1} \mathcal{O}_Y$-module. The morphism $f^\sharp: \mathcal{O}_Y \to f_*\mathcal{O}_X$ is in natural bijection (because of the sheaf-theoretic adjunction $f^{-1} \dashv f_*$ v. [[Direct and inverse image functors for sheaves]]) with a morphism $f^{-1} \mathcal{O}_Y \to \mathcal{O}_X$. Now take the $\mathcal{O}_X$-module $f^{-1} \mathcal{F} \otimes_{f^{-1} \mathcal{O}_Y} \mathcal{O}_X$, which is a $\mathcal{O}_X$-module.

**Adjuncition:** we have an adjunction $f^* \dashv f_*$.

## Exactness of the tensor product

The tensor product $-\otimes_{\mathcal{O}_X} \mathcal{F}$ is **left exact**. However, if $\mathcal{F}$ is locally free, then it becomes **exact**!

*Proof (exactness if $\mathcal{F}$ locally free).*

Let $\mathcal{G}' \to \mathcal{G} \to \mathcal{G}''$ be a short exact sequence of $\mathcal{O}_X$-modules. The sequence $\mathcal{G}' \otimes_{\mathcal{O}_X} \mathcal{F} \to \mathcal{G} \otimes{\mathcal{O}_X} \mathcal{F} \to \mathcal{G}'' \otimes_{\mathcal{O}_X} \mathcal{F}$ is exact if, and only if, it's exact after applying the stalks.

For every $x$, it becomes:$$\mathcal{G}'_x \otimes_{\mathcal{O}_{X,x}} \mathcal{F}_x \to \mathcal{G}_x \otimes{\mathcal{O}_{X,x}} \mathcal{F}_x \to \mathcal{G}''_x \otimes_{\mathcal{O}_{X,x}} \mathcal{F}_x.$$
Moreover, $\mathcal{F}_x$ is free, so $-\otimes_{\mathcal{O}_{X,x}} \mathcal{F}_x$ is exact. Since the original sequence (with the stalks) is exact, we deduce exactness. **qed**

## Using sheaves of modules to cut out

v. [[The Rising Sea]] Exercise 13.1.I.

Let $(X,\mathcal{O}_X)$ be a scheme, and $\mathcal{F}$ a locally free $\mathcal{O}_X$-module. For every global section $s \in \Gamma(X,\mathcal{F})$, define $V(s) \subseteq X$ as the smallest closed set that contains $\{x \in X \mid s_x \in \mathfrak{m}_x \}$.

# Exemples

## Smooth manifolds

Let $X$ be a smooth manifold. We can view the sheaf of smooth functions, $\mathcal{C}^\infty$, as a *subsheaf* of the sheaf of continuous functions $\mathcal{C}$.

## Vector fields on a smooth manifold

Let $M$ be a smooth manifold, and consider it as a locally ringed space $(M,\mathcal{C}^\infty)$. The smooth vector fields $\mathfrak{X}$ on $M$ define a sheaf on $M$. Moreover, for every $U \subseteq M$ open, $\mathfrak{X}$ is a $\mathcal{C}^\infty$-module, where the structure map is given by $\mathcal{C}^\infty(U) \otimes \mathfrak{X}(U) \to \mathfrak{X}(U)$, $(f,X) \mapsto f \cdot X$. This is clearly compatible with the restriction maps, so $\mathfrak{X}$ is a module over $(M,\mathcal{C}^\infty)$.

$\mathfrak{X}$ is **locally free** (because for every $p \in M$ there exists a small enough chart $(U,\varphi)$ around $p$ such that $\mathfrak{X}(U) = \mathcal{C}^\infty(U) \langle \partial/\partial x_i, \dots, \partial/\partial x_n\rangle$) It has rank $n = dim(M)$.

In general it's **not** free. Take for instance $M = S^2$, and an obstruction to freeness comes from the hairy ball theorem. In fact, **freeness** is equivalent to **parallelizability** of $M$.

## Complex manifolds

We have $\mathcal{O}_X \subseteq \mathcal{C}^\infty$, where $\mathcal{O}_X$ is the sheaf of holomorphic functions.

## Hom

Siguin $\mathcal{F}$ i $\mathcal{G}$ dos $\mathcal{O}_X$-mòduls. Aleshores el feix $Hom_{\mathcal{O}_X}(\mathcal{F},\mathcal{G})$ hereta una estructura natural de $\mathcal{O}_X$-mòdul.

Si $\mathcal{F}$ és localment lliure de rang $m$, i $\mathcal{G}$ és localment lliure de rang $n$, aleshores $Hom_{\mathcal{O}_X}(\mathcal{F},\mathcal{G})$ és localment lliure de rang $mn$. (v. Exercici 13.1.B [[The Rising Sea]])

*Demostració.*

Prenem un recobriment de $X$ tal que $\mathcal{F}$ i $\mathcal{G}$ són lliures en cadascun dels oberts que el componen (això ho podem fer refinant recobriments previs). En cada $U$ del recobriment tenim:$$Hom_{\mathcal{O}_X}(\mathcal{F},\mathcal{G})(U) \cong Hom_{\mathcal{O}_X|_U}((\mathcal{O}_X|_U)^{\oplus m}, (\mathcal{O}_Y|_U)^{\oplus n}) \cong (\mathcal{O}_X|_U)^{\oplus mn}.$$
**qed**