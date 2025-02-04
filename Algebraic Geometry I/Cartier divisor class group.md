Let $X$ be any scheme. Define a presheaf on affine $U = Spec(A) \subseteq X$ given by $U \mapsto Q(A) := S^{-1}A$ where $S = \{a \in A \mid \textrm{non-zero\ divisor}\}$.

Define $\mathcal{K}_X$ to be the sheafification of this presheaf. In fact it's a sheaf of rings.

Consider $\mathcal{K}_X^\times \subseteq \mathcal{K}_X$ sheaf of abelian groups.

Note that $\mathcal{O}_X \subseteq \mathcal{K}_X$ and also $\mathcal{O}_X^\times \subseteq \mathcal{K}_X^\times$, and these inclusions are compatible with the other natural inclusions defining $(-)^\times$.

Consider the following sheaf quotient, which gives a short exact sequence of sheaves of abelian groups:$$0 \to \mathcal{O}_X^\times \to \mathcal{K}_X^\times \to [\mathcal{K}_X^\times/\mathcal{O}_X^\times]^+ \to 0.$$
From now on we supress $[-]^+$ from the notation.

Define a **Cartier divisor** $D$ to be a global section of $\mathcal{K}^\times_X /\mathcal{O}_X^\times$, i.e. an element in $H^0(X, \mathcal{K}_X^\times/\mathcal{O}_X^\times)$.

One can take a good enough open covering $\{U_i\}_i$ of $X$. We can represent $D$ by $\{f_i\}_i$, where $f_i \in \mathcal{K}_X^\times(U_i)$ such that $f_i/f_j \in \mathcal{O}_X^\times(U_i \cap U_j) \subseteq \mathcal{K}_X^\times(U_i \cap U_j)$.

**Remark.** This representation of Cartier divisor is not unique.

Any Cartier divisor in the image of $$H^0(X, \mathcal{K}_X^\times) \to H^0(X, \mathcal{K}_X^\times/\mathcal{O}_X^\times)$$is called a **principal** Cartier divisor. If $X$  is integral, then $$H^0(X,\mathcal{K}_X^\times) = K(X)^\times$$and hence this map is $f\mapsto (f)$ v. [[Principal Weil divisor]]

Now consider the long exact sequence associated to the short exact sequence of the quotient $\mathcal{K}_X^\times/\mathcal{O}_X^\times$.
- IF $X$ is proper, integral and $k$ is algebraically closed, then $H^0(X,\mathcal{O}_X^\times)$ = k$.
- If $X$ is integral, then $H^0(X,\mathcal{K}_X^\times) = K(X)^\times$.
- $H^1(X,\mathcal{O}_X^\times) = Pic(X)$ v. [[Picard group]]

Define the **Cartier divisor class group** as $$CaCl(X) := H^0(X,\mathcal{K}_X^\times/\mathcal{O}_X^\times)/\sim,$$wjere $D \sim D'$ (linearly equivalent) if $D - D'$ is a Cartier principal divisor.

**Warning: additive vs multiplicative notation.** If $D = \{f_i, U_i\}_i$ and $D' = \{f_i', U_i\}_i$, then $D-D' = \{f_i/f_i', U_i\}_i$.

# Propietats

## Integral => Coincideix amb el grup de Picard

v. [[Picard group]]

By the above long exact sequence we have an inclusion $CaCl(X) \subseteq Pic(X)$.

**Proposició.** If $X$ is integral, then the inclusion $CaCl(X) \subseteq Pic(X)$ is an isomrophism.

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

# Example

If $A$ is an integral domain, then the presheaf is the quotient field.

If $X$ is integral, then $Q(A) = K(X)$ and hence $\mathcal{K}_X$ is the constant sheaf $\underline{K(X)}$ and also $\mathcal{K}_X^\times = \underline{K(X)^\times}$.

## Projective spaces

Let $k$ be a field. The Cartier divisor class group of $\mathbb{P}^n_k$ is isomorphic to $\mathbb{Z}$. v. [[Projective space]]