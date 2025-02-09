We have the following equivalences:
- The Picard group coincides with $H^1(X,\mathcal{O}_X^\times)$.
- If $X$ is **factorial** (and satisfies #), then $CaCl(X) \cong Cl(X)$.
- If $X$ is **integral**, then $CaCl(X) \cong Pic(X)$.

v. [[Cartier divisor class group]], [[Weil divisor class group]].

## Picard group = First cohomology with coefficients in $\mathcal{O}_X^\times$

v. [[Picard group]]

Let $\mathcal{L}$ be an invertible sheaf on $X$, and take an open cover $\{U_i\}_i$ of $X$ and $\varphi_i: \mathcal{L}|_{U_i} \stackrel{\cong}{\to} \mathcal{O}|_{U_i}$ (the open cover can always be chosen such that the $\varphi_i$ exist). There are transitions functions$$\varphi_{ij}: \mathcal{O}|_{U_{ij}} \stackrel{\varphi_i^{-1}}{\longrightarrow} \mathcal{L}|_{U_{ij}} \stackrel{\varphi_j}{\longrightarrow} \mathcal{O}|_{U_{ij}}.$$
These $\varphi_{ij}$ are in bijection with $\varphi_{ij}(1) \in \Gamma(U_{ij}, \mathcal{O}_{U_{ij}}^\times)$. Moreover, they satisfy the cocycle conditions $\varphi_{ii} = 1$, $\varphi_{ij} \varphi_{ji} = 1$, $\varphi_{ij} \varphi_{jk} = \varphi_{ik}$. Hence, they define a cohomology class$$\{\varphi_{i}\}_{i} \in CH^1(\{U_{ij}\}_{ij}, \mathcal{O}_X^\times) \to CH^1(X,\mathcal{O}_X^\times) \cong H^1(X, \mathcal{O}_X^\times).$$
v. [[Coordinate-free Cech cohomology]] grau 1.

**Theorem.** The morphism $Pic(X) \to H^1(X,\mathcal{O}_X^\times)$ defined above is an isomorphism of groups.

*Proof.*

**Step 1.** *Well defined.*

***Setup*.** Consider two open coverings $X = \bigcup_{i\in I} U_i = \bigcup_{j \in J} V_j$, and isomorphisms $\varphi_i: \mathcal{L}|_{U_i} \to \mathcal{O}_{U_i}$, $\psi_j: \mathcal{L}|_{V_j} \to \mathcal{O}_{V_j}$, which provide $\{\varphi_{ij}\}_{ij}, \{\psi_{ij}\}_{ij} \in H^1(X, \mathcal{O}^\times)$.

***Reduction*.** *We can assume that $I = J$ and $U_i = V_i$.*

This is because the explicit isomorphisms $CH^1(X, \mathcal{O}^\times) \cong H^1(X, \mathcal{O}^\times)$ allow to refine open coverings. Now refine $\{U_i\}_{i \in I}$ and $\{V_j\}_{j \in J}$ into a common open covering.

*Comentari.* Precisament el fet que estiguem utilitzant la versió coordinate-free de la cohomologia de Cech és el que ens permet escollir el recobriment que ens plagui i refinar.

***Have to show:*** *the (multiplicative) difference $\psi_{ij}^{-1} \varphi_{ij}$ is a boundary.*

*This is because the composite $\psi_{ij}^{-1}\varphi_{ij}$ must be multiplication by constant.*

To show this, develope $$\psi_{ij}^{-1} \varphi_{ij} = \psi_j \psi_i^{-1} \varphi_i \varphi_j^{-1} = \cdots = \eta_i \eta_j id,$$where $\eta_\ell \in H^0(U_\ell, \mathcal{O}^\times)$ is some scalar that corresponds to $\psi_\ell^{-1} \varphi_\ell: \mathcal{L}|_{U_k} \to \mathcal{L}|_{U_k}$ (this isomorphism is multiplication by $\eta_k$), or to its inverse.

This implies that $\psi_{ij}^{-1} \varphi_{ij}$ is a boundary.

**Step 2.** *Morphism of groups.*

Compute explicitly what the image of $\mathcal{L} \otimes \mathcal{M}$ is.

**Step 3.** *Bijection.*

This is because of the glueing formalism. **qed**
## Cartier class group = Weil class group

If $X$ is **factorial** (and satisfies #)!!!

**Lemma 0. (Commutative algebra)**
1. $A$ integrally closed domain => $A = \bigcap_{ht(\mathfrak{p}) = 1}A_\mathfrak{p}$.
2. $A$ factorial => $A$ integrally closed domain.

**Lemma 1 (Injectivity).** If $X$ is **normal**, then $H^0(X,\mathcal{K}^\times_X/\mathcal{O}^\times_X) \to Div(X)$ is **injective**.

*Proof.*

**Step 1.** *Formulate the problem with Cech cohomology.*

Take an open cover $\{U_i\}_i$ of $X$ with each $U_i$ affine ($U_i \cong Spec(A_i)$).

Take any $\{f_i \in \mathcal{K}_X(U_i)\}_i \in H^0(\mathcal{K}_X^\times/\mathcal{O}_X^\times)$, and suppose that it's sent to $D = \sum_Y n_Y \cdot Y = 0$ by the morphism that we're studying. Aquí estem utilitzant representants $f_i$, i cal que $f_i/f_j \in \mathcal{O}_X^\times(U_{ij})$ per tal que enganxin bé.

**Step 2.** *Commutative algebra trick!*

In particular $f_i \in (A_i)_\mathfrak{p}^\times$ for every prime ideal $\mathfrak{p} \subseteq A_i$ of height 1. Normality of $X$ implies that $A_i$ is integrally closed and hence$$f_i \in \bigcap_{ht(\mathfrak{p})=1} (A_i)^\times_\mathfrak{p} = A_i^\times = \mathcal{O}(U_i)^\times,$$so $\{f_i\}_i = 0$ in $H^0(\mathcal{K}_X^\times/\mathcal{O}_X^\times)$. **qed**

**Lemma 2 (Working locally towards surjectivity).** If $A$ is a factorial, integral domain, then $Cl(A) = Cl(Spec(A)) = 0$.

*Proof.*

*Work algebraically: prime divisors of $Spec(A)$ are in correspondence with height 1 prime ideals of $A$.*

Factoriality of $A$ implies that every prime ideal of $A$ of height 1 is principal. Hence, the corresponding varieties (which are all prime divisors of $A$) are principal divisors. **qed**

**Lemma 3 (Surjectivity).** If $X$ is **factorial**, then $H^0(X,\mathcal{K}_X^\times/\mathcal{O}_X^\times) \to Div(X)$ is **surjective**.

*Proof.*

Let $D = \sum_Y n_Y \cdot Y \in Div(X)$ be a Weil divisor.

**Step 1.** *Define the preimages locally.*

Fix $x \in X$. Factoriality of $X$ implies factoriality of $A := \mathcal{O}_{X,x}$. Consider the open subscheme $U := Spec(A) \subseteq X$ around $x$ ==(per què ho puc fer això? per què l'Spec de l'stalk dóna un open subscheme???)==

Restrict the Weil divisor: $D_x := \sum_Y n_Y \cdot (Y \cap U)$, where we sum all the terms whose intersection is nonempty.

Lemma 2 => there exists some $f_x \in Q(A) = K(X)$ such that $D_x = (f_x)$.

**Step 2.** *From local to global.*

Take an open covering $\{U_i\}_i$ of $X$ where the open sets are of the previous form, and hence we have well-defined $f_i$ such that $D|_{U_i} = (f_i)$. We have to check that these $f_i$ glue and hence give rise to a well-defined element in $H^0(X, \mathcal{K}_X^\times/\mathcal{O}_X^\times)$. This means that we have to check that$$f_i/f_j \in \mathcal{O}_X^\times(U_i \cap U_j),\quad \forall i,j.$$
Let $Y \subseteq X$ be a prime divisor. Then$$(f_i)|_{U_{ij}} - (f_j)|_{U_{ij}} = D|_{U_{ij}} - D|_{U_{ij}} = 0,$$so $\nu_Y(f_i/f_j) = 0$ and hence $f_i/f_j \in \mathcal{O}_{X,\eta_Y}^\times$. Since this is true for every prime divisor, it follows what we wanted to show because of factoriality (see Lemma 0): $U_{ij} = Spec(A_{ij})$, and hence$$f_i/f_j \in \bigcap_{ht(\mathfrak{p}) = 1} (A_{ij})_\mathfrak{p} = A_{ij}.$$
**qed**

**Lemma 4.** *The isomorphism above commutes with the quotients.*

$CaCl(X)$ is obtained from $H^0(X,\mathcal{K}_X^\times/\mathcal{O}_X^\times)$ by quotienting out the principal Cartier divisors, while $Cl(X)$ is obtained from $Div(X)$ by quotienting out Weil principal divisors. We have to check that, under the isomorphism above, these two classes of divisors are in bijection.

If $D$ is a principal Cartier divisor $\{f_i = f|_{U_i}\}_i$, then its image is the principal Weil divisor $(f) = (f)_0 - (f)_\infty$. **qed**

## Picard group = Cartier divisor class group

The short exact sequence $$0 \to \mathcal{O}_X^\times \to \mathcal{K}_X^\times \to \mathcal{O}_X^\times/\mathcal{K}_X^\times \to 0$$gives an inclusion $CaCl(X) \subseteq Pic(X)$. (v. [[Cartier divisor class group]] for the exact sequence)

**Proposició.** If $X$ is ==integral==, then the inclusion $CaCl(X) \subseteq Pic(X)$ is an isomrophism.

*Proof.*

For $X$ integral (then all open sets are connected, v. [[Scheme]]), $\mathcal{K}_X^\times$ is a constant sheaf, hence flabby (v. [[Flasque (flabby) sheaf]]), hence acyclic, hence $H^1(X,\mathcal{K}_X^\times) = 0$. **qed**

**Expicit computation! (and surjectivity more geometrically I guess).** We need a computation of the connecting homomorphism.

Given $s \in H^0(\mathcal{H})$, what's $\delta(s) \in CH^1(\mathcal{F})$ ?

Take an open covering $\{U_i\}_i$ of $X$, and $s_i \in H^0(U_i, \mathcal{G})$ with $\varphi(s_i) = s|_{u_i}$ such that $s_i|_{U_{ij}} - s_j|_{U_{ij}} \in H^0(U_{ij},\mathcal{F}) \subseteq H^0(U_{ij},\mathcal{G})$. Then $\delta(s)$ is represented by the cocycle codnition$$\{s_i|_{U_{ij}} - s_j|_{U_{ij}} \in H^0(U_{ij},\mathcal{F})\}_{ij}.$$
Apply this general discussion to our situation. Represent $F \in H^0(X,\mathcal{K}_X^\times/\mathcal{O}_X^\times)$ by $f_i \in \mathcal{K}_X^\times(U_i) = K(X)\setminus \{0\}$. THen $\delta(D) \in CH^1(X,\mathcal{O}_X^\times) = H^1(X,\mathcal{O}_X) \cong Pic(X)$ is given by the cocylce $\{f_i/f_j \in \mathcal{O}^\times(U_{ij})\}$.

Then $D \mapsto \delta(D) \mapsto \mathcal{O}(D) \in Pic(X)$. We can realize $\mathcal{O}(D)$ as a subsheaf of $\mathcal{K}_X^\times$ as follows: $\mathcal{O}(D)|_{U_i} = \mathcal{O}|_{U_i} \cdot f_i^{-1} \subseteq \mathcal{K}_X|_{U_i}$. Independence of choice on the intersections $U_{ij}$ follows becasue $f_i/f_j \in\mathcal{O}^\times(U_{ij})$.

With this definition, $\mathcal{O}(D) = \mathcal{O}|_{U_i} \cdot f_i^{-1}$. Now apply $\varphi_i$, which is multiplication by $f_i$. This gives an invertible sheaf in $Pic(X)$.

THis is nothing but $\delta(D) \in CH^1(X,\mathcal{O}_X^\times)$ unde rthe usual identification with $Pic(X)$.

blah blah blah.