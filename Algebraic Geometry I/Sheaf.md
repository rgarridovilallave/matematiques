# Definitions

## Easy definition

Un **feix** $\mathcal{F}$ (amb valors en els cjts, grups abelians, anells, espais vectorials, ...) sobre un espai topològic $X$ és un prefeix $\mathcal{F}: \textrm{Ouv}(X)^{op} \to Ab$  tal que:
1. **Axioma de localitat:** Per cada $U \subseteq X$ obert i cada recobriment $\{U_i\}_{i \in I}$  de $U$, si $s,s' \in \mathcal{F}(U)$ satisfan que $s_{|U_i} = s'_{U_i}$ per cada $i$, aleshores $s = s'$.
2. **Axioma d'enganxament:** Per cada obert $U \subseteq X$ i cada recobriment $\{U_i\}_{i \in I}$ de $U$, si $\{s_i \in \mathcal{F}(U_i)\}_{i \in I}$ és una família de seccions que satisfà ${s_i}_{|U_i \cap U_j} = {s_j}_{|U_i \cap U_j}$, aleshores existeix una secció $s \in \mathcal{F}(U)$ tal que $s_{|U_i} = s_i$.

*Morfismes.* Un morfisme de feixos és senzillament un morfisme entre els prefeixos subjacents. Dóna lloc a la categoria $Sh_{\mathcal{C}}(X)$ de feixos en $X$. Per definició, $Sh_{\mathcal{C}}(X)$ és una categoria plena dins de $PSh_{\mathcal{C}}(X)$.

*Notació.*
- Els elements de $\mathcal{F}(U)$ s'anomenen **seccions (locals)** de $U$.
- Si $s$ és una secció de $V$ i $U\subseteq V$, $s_{|U}$ denota $(U \subseteq V)(s)$ i s'anomena la **restricció** de $s$ en $U$.
- $\mathcal{F}(X)$ s'anomena l'**espai de seccions globals**, i es denota $\Gamma(X, \mathcal{F})$.

*Remarques.*
- A vegades es demana que $\mathcal{F}(\emptyset)$ sigui l'objecte terminal de la categoria.
- L'axioma de localitat és conseqüència de l'axioma d'enganxament.

## Categorical definition

A **sheaf** over a topological space $X$ with values in a category $\mathcal{C}$ is a presheaf $\mathcal{F}: \textrm{Ouv}_X^{op} \to \mathcal{C}$ such that for every collection of open sets $\{U_i\}_i$, the map $$\mathcal{F}(U) \to \prod_i \mathcal{F}(U_i)$$ is the [[Equalizer]] of $$\prod_i \mathcal{F}(U_i) \stackrel{\psi_1,\psi_2}{\rightrightarrows} \prod_{i,j} \mathcal{F}(U_i \cap U_j)$$where $\psi_1((s_i)_i) := (s_i|_{U_i \cap U_j})_{i,j}$ and $\psi_2((s_i)_i) := (s_j|_{U_i \cap U_j})_{i,j}$, and $U := \bigcup_i U_i$.

*Observació.* Si la categoria d'arribada és abeliana, la condició de l'equalizer és equivalent a que el morfisme $\mathcal{F}(U) \to \prod_i \mathcal{F}(U_i)$ sigui el nucli de $\prod_i \mathcal{F}(U_i) \to \prod_{i,j} \mathcal{F}(U_i \cap U_j)$, $(s_i)_i \mapsto (s_i|_{U_i \cap U_j} - s_j|_{U_i \cap U_j})_{i,j}$

*Interpretació.*

Sigui $\mathcal{C} = Ab$ (o una categoria similar).

Un con de $\prod_i \mathcal{F}(U_i) \rightrightarrows \prod_{ij} \mathcal{F}(U_i \cap U_j)$ és un objecte $A$, que s'ha de pensar com un candidat a espai de seccions de $U$, juntament amb morfismes (restriccions) $\rho_i: A \to \mathcal{F}(U_i)$, tals que, per cada secció (element) $s \in A$, es té que $$\rho_i(s)|_{U_i \cap U_j} = \rho_j(s)|_{U_i \cap U_j}\quad \forall i,j.$$
La condició que $\mathcal{F}(U)$ sigui un límit (i no merament un con) permet deduir els axiomes d'**enganxament** i de **localitat**.

- **Axioma d'enganxament (existència):** Sigui $s_i \in \mathcal{F}(U_i)$ tal que $s_i|_{U_i \cap U_j} = s_j|_{U_i \cap U_j}$ per cada $i,j$, és a dir, $(s_i)_i \in \prod_i \mathcal{F}(U_i)$ tal que $\psi_1((s_i)_i) = \psi_2((s_i)_i)$. Aleshores $(s_i)_i$ es pot posar dins de l'equalitzador, per definició. Com que demanem que l'equalitzador sigui $\mathcal{F}(U)$, deduïm que existeix $s \in \mathcal{F}(U)$ tal que $s|_{U_i} = s_i$.
- **Axioma de localitat (unicitat):** la unicitat ens diu que si dues seccions coincideixen en un recobriment, aleshores són la mateixa.

# Morfismes

## Associated presheaves and sheaves

Let $\varphi: \mathcal{F} \to \mathcal{G}$ be a morphism of abelian (podria ser una categoria abeliana qualsevol) presheaves. Define $\ker^{pr}(\varphi)$, $im^{pr}(\varphi)$, $coker^{pr}(\varphi)$ open-wise. The kernel is a sheaf, but this is no longer true for the image and the cokernel.

To get around this, define (v. [[Sheafification]]):
- $ker(\varphi) := ker^{pr}(\varphi)$,
- $im(\varphi) := (im^{pr}(\varphi))^+$,
- $coker(\varphi) := (coker^{pr}(\varphi))^+$.

These have the usual universal properties.

Kernel:
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[ampersand replacement=\&] \& {\mathcal{F}_0} \\ {\ker(\varphi)} \& {\mathcal{F}} \& {\mathcal{G}} \arrow[from=1-2, to=2-2] \arrow["{\varphi_0}", from=1-2, to=2-3] \arrow["{\exists!}", dashed, from=2-1, to=1-2] \arrow[from=2-1, to=2-2] \arrow["\varphi", from=2-2, to=2-3] \end{tikzcd}
\end{document}
```
Cokernel:
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[ampersand replacement=\&] {\mathcal{F}} \& {\mathcal{G}} \& {coker(\varphi)} \\ \& {\mathcal{G}_0} \arrow["\varphi", from=1-1, to=1-2] \arrow["{\varphi_0}"', from=1-1, to=2-2] \arrow[from=1-2, to=1-3] \arrow[from=1-2, to=2-2] \arrow["{\exists!}", dashed, from=1-3, to=2-2] \end{tikzcd}
\end{document}
```

The universal property of the image is deduced form the fact that $im(\varphi) = \ker(coker(\varphi))$.

## The kernel is a sheaf

We have to check the sheaf condition of $ker^{pr} \varphi$. Let $U = \bigcup_i U_i$, and $\{s_i \in (ker^{pr}\varphi)(U_i)\}_i$ such that $s_i|_{U_{ij}} = s_j|_{U_{ij}}$. The sheaf condition of $\mathcal{F}$ asserts the existence and uniqueness of some $s \in \mathcal{F}(U)$ such that $s|_{U_i} = s_i$. We have to see that $s \in (ker^{pr}\varphi)(U)$, i.e. that $\varphi(s) = 0$.

Note that $\varphi(s)|_{U_i} = \varphi(s|_{U_i}) = \varphi(0) = 0$ because $\varphi$ is a morphism of sheaves. The sheaf condition of $\mathcal{G}$ already implies that $\varphi(s) = 0$. **qed**

## Monomorphisms

TFAE:
1. $\varphi$ is a [[Monomorphism]] in $Sh(X)$.
2. $ker(\varphi) = 0$.
3. $\varphi_U$ is injective for every $U$ open.
4. $\varphi_x: \mathcal{F}_x \to \mathcal{G}_x$ is injective for every $x$.

*Proof (1) => (2).* Monomorphism means "$\varphi \varphi_0 = 0$ => $\varphi_0 = 0$". Apply this to $\varphi_0 =$ inclusion. **qed**

*Proof (2) <=> (3).* Follows from the fact that $ker = ker^{pr}$, and that $ker = 0$ <=> injective in the category of abelian groups. **qed**

*Proof (3) => (4).* Follows from the exactness of the direct limit (v. [[Direct limit]]). **qed**

*Proof (4) => (2).* És suficient fer un estudi dels germs: if $s \in ker (\varphi_U)$, then $0 = \varphi_U(s)_x = \varphi_x(s_x)$. But $\varphi_x$ is injective for every $x$, so $s_x = 0$ for every $x$. This implies that $s = 0$, ja que els stalks d'una secció la determinen. **qed**

*Proof (3) => (1).* Choose a composite $\mathcal{F}_0 \stackrel{\varphi_0}{\to} \mathcal{F} \stackrel{\varphi}{\to} \mathcal{G}$ that vanishes. Then, for every $U$, the composite $\mathcal{F}_0(U) \stackrel{(\varphi_0)_U}{\to} \mathcal{F}(U) \stackrel{\varphi_U}{\to} \mathcal{G}$ also vanishes, but since $\varphi_U$ is injective (and hence a monomorphism in $Ab$), it must be that $(\varphi_0)_U = 0$. Since this is true for every $U$, it follows that $\varphi_0 = 0$. **qed**

## Epimorphisms

Let $\varphi: \mathcal{F} \to \mathcal{G}$ be a morphism of sheaves. TFAE:
1. $\varphi$ is an epimorphism.
2. $coker(\varphi) = 0$.
4.$coker(\varphi_x) = 0$ for every $x$.

Moreover, the following implies 1 (& hence 2, 4):

3. $\varphi_U$ is surjective for every $U$.

Recall: epimorphism means "$\varphi_0 \varphi = 0$ => $\varphi_0 = 0$".

*Proof (1) => (4).*

```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[ampersand replacement=\&] {\mathcal{F}} \& {\mathcal{G}} \\ \& {coker^{pr}(\varphi)} \\ \& {coker(\varphi)} \arrow["\varphi", from=1-1, to=1-2] \arrow["0", from=1-1, to=2-2] \arrow["0"', from=1-1, to=3-2] \arrow[from=1-2, to=2-2] \arrow[from=2-2, to=3-2] \end{tikzcd}
\end{document}
```

Let $\psi$ be the composite $\mathcal{G} \to coker^{pr}(\varphi) \to coker(\varphi)$. Since $\psi \varphi = 0$ and $\varphi$ is an epimorphism, it follows that $\psi = 0$. This implies that $\psi_x: \mathcal{G}_x \to coker(\varphi)_x = coker(\varphi_x)$ is zero for every $x$. But this map is surjective for every $x$, hence $coker(\varphi_x) = 0$ for every $x$. **qed**

*Proof (4) => (2).*

Since $coker(\varphi)_x = coker(\varphi_x) = 0$ for every $x$, it follows that $coker(\varphi) = 0$. (v. [[Stalk]]) **qed**

*Proof (4) => (1).*

Consider
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[ampersand replacement=\&] {\mathcal{F}} \& {\mathcal{G}} \\ \& {\mathcal{G}_0} \arrow["\varphi", from=1-1, to=1-2] \arrow["0", from=1-1, to=2-2] \arrow["\psi", from=1-2, to=2-2] \end{tikzcd}
\end{document}
```
Then the composite $\psi_x \varphi_x$ is zero for every $x$. Since $\varphi_x$ is an epimorphism (surjection) of abelian groups, $\psi_x = 0$ for every $x$. This implies that $\psi = 0$. **qed**

*Proof (2) => (1).*

$coker(\varphi) = 0$ is equivalent to $coker(\varphi_x) =  0$ for every $x$. Conclude as above. **qed**

*Proof (3) => (4).*

Since the direct limit is exact (v. [[Direct limit]]), $\varphi_x: colim_{x \in U} \mathcal{F}(U) \to colim_{x \in U} \mathcal{G}(U)$ is surjective for every $x$. **qed**

## Isomorphisms

Let $\varphi: \mathcal{F} \to \mathcal{G}$ be a morphism of sheaves. Then $\varphi$ is an isomorphism if, and only if, $\varphi_x$ is an isomorphism for every $x$.

*Proof.*

=> ) $\varphi \varphi^{-1} = id$ and $\varphi^{-1}\varphi = id$. Hence the same is true when applying $(-)_x$.

<= )  El kernel es cero. Veiem que és exhaustiu.

Consider $t \in \mathcal{G}(U)$. Since $\varphi_x$ is surjective, $t_x$ has a preimage $s^x$. There exists a neighbourhood $x \in V_x \subseteq U$ such that $\tilde{s ^x} \in \mathcal{F}(V_x)$ represents $s^x$. In this neighbourhood $V_x$ (which can be made smaller), $\varphi_{V_x}(\tilde{s_x})= t|_{V_x}$ (by definition of germ). These $\tilde{s^x}$ can be glued together (with the sheaf property) to a preimage $s \in \mathcal{F}(U)$ of $t$. **qed**

	Huybrechts "My notation is messed up"

# Exemples

## Funcions contínues en $\mathbb{R}$

$\mathcal{C}_X$ és un feix sobre $X$. Per cada obert $U$, es defineix $\mathcal{C}_X(U) := Hom_{Top}(U,\mathbb{R})$. Amb la suma de $\mathbb{R}$ es pot pensar com un feix de grups abelians, però de fet si hi afegim el producte esdevé un feix d'anells.

## Zeros de polinomis... i feix estructural!

Sigui $V = V(f_1,\dots,f_r)$ amb $f_i \in k[X_1,\dots,X_n]$ polinomis. Es defineix el feix $\mathcal{O}$ que val, en cada obert de Zariski $U \subseteq V$ (v. [[Zariski topology]]), l'anell de funcions regulars que prenen valors en $k$.

Recordem que una funció regular és aquella que localment és un quocient de polinomis.

Més en general, tenim el [[Structure sheaf]]. Aquest és l'exemple més important.

## Constant presheaf & constant sheaf

$X$ top space, $G$ abelian group. $\mathbb{G}$ is the constant **pre**sheaf $\mathbb{G}(U) = G$ for every $U \subseteq X$. 

$X$ top space, $G$ abelian group. $\underline{\mathbb{G}}(U) := G^{\pi_0(U)}$ with $G$ the discrete topology, is a sheaf. It's the sheafification (v. [[Sheafification]]) of the constant sheaf $\mathbb{G}$.

## Sheaf of differentiable functions

$X$ differentiable manifold, $\mathcal{C}_X^\textrm{diff}$ sheaf of differentiable manifolds. Analogous for complex manifolds.
## Exemple de morfisme de feixos

$X$ differentiable manifold. The inclusions $\mathcal{C}_X^\textrm{diff}(U) \subseteq \mathcal{C}_X(U)$ for every $U \subseteq X$ open define a morphism of sheaves.

## Precomposition with $\exp$

$X$ topological space, $\mathcal{F}$ sheaf on $X$ of continuous functions to $S^1$. There's a morphism of sheaves $\mathcal{C}_X \to \mathcal{F}$ given by precomposition with $\exp$.

## $coker^{pr}$ and $im^{pr}$ are not sheaves (in general)

Let $X = \{x_1,x_2\}$ with the discrete topology, and $G$ an abelian group. Fix $\mathcal{F} = \mathcal{G}$ the constant sheaf. Let:$$\varphi: \mathcal{F} \to \mathcal{G},\quad \varphi_U = \begin{cases} id_{G \times G},& U = X,\\ 0,& \textrm{oth.}\end{cases}$$
Then $$coker^{pr}(\varphi)(U) = \begin{cases} 0,& U = X,\\ G,& \textrm{oth.}\end{cases},$$which does not satisfy the sheaf condition. The very same example shows that $im^{pr}$ is not a sheaf (in general).

## Another counterexample (more sophisticated)

Let $X = \mathbb{C}^* = \mathbb{C} \setminus \{0\}$, $\mathcal{F} = \mathcal{O}_X =$ sheaf of holomorphic functions, $\mathcal{G} = \mathcal{O}_X^* =$ sheaf of holomorphic functions without zeroes. Consider the morphism $\exp: \mathcal{O}_X \to \mathcal{O}^*_X$.

Observe that $\exp: \mathcal{O}_X(X) \to \mathcal{O}_X^*(X)$ is not surjective (beacuse $\log(z)$ is not holomorphic in $\mathbb{C}^*$). This implies that $coker^{pr}(\varphi)(X) \neq 0$.

However, consider a covering $X = U_1 \cup U_2$ with $U_1, U_2$ simply connected. Then $\exp$ is surjective on $U_i$, $i = 1,2$. This implies that $coker^{pr}(\varphi)(U_i) = 0$.
