Let $X$ be a scheme. Its **Picard group** is defined to be the set of invertible sheaves on $X$ modulo isomorphism, together with the operation given by the tensor product $\otimes$ of sheaves of modules (v. [[Sheaf of modules]]). It's an abelian group because of the symmetry of the tensor product.

The **neutral element** is $[\mathcal{O}_X]$, and the inverse is given by $-[\mathcal{F}] = [\mathcal{F}^\vee]$.

**Functoriality.** Given $f: X \to Y$ morphism of schemes, there's an induced morphism of groups $f^*: Pic(Y) \to Pic(X)$ given by the pullback $[\mathcal{L}] \mapsto [f^*\mathcal{L}]$. This amounts to saying that the Picard group is a functor $Sch^{op} \to Ab$.

# Propietats

## Picard group = First cohomology with invertible coefficients

Let $\mathcal{L}$ be an invertible sheaf on $X$, and take an open cover $\{U_i\}_i$ of $X$ and $\varphi_i: \mathcal{L}|_{U_i} \stackrel{\cong}{\to} \mathcal{O}|_{U_i}$ (the open cover can always be chosen such that the $\varphi_i$ exist). There are transitions functions$$\varphi_{ij}: \mathcal{O}|_{U_{ij}} \stackrel{\varphi_i^{-1}}{\longrightarrow} \mathcal{L}|_{U_{ij}} \stackrel{\varphi_j}{\longrightarrow} \mathcal{O}|_{U_{ij}}.$$
These $\varphi_{ij}$ are in bijection with $\varphi_{ij}(1) \in \Gamma(U_{ij}, \mathcal{O}_{U_{ij}}^\times)$. Moreover, they satisfy the cocycle conditions $\varphi_{ii} = 1$, $\varphi_{ij} \varphi_{ji} = 1$, $\varphi_{ij} \varphi_{jk} = \varphi_{ik}$. Hence, they define a cohomology class$$\{\varphi_{i}\}_{i} \in CH^1(\{U_{ij}\}_{ij}, \mathcal{O}_X^\times) \to CH^1(X,\mathcal{O}_X^\times) \cong H^1(X, \mathcal{O}_X^\times).$$
v. [[Coordinate-free Cech cohomology]] grau 1.

**Theorem.** The morphism $Pic(X) \to H^1(X,\mathcal{O}_X^\times)$ defined above is an isomorphism of groups.

v. [[Equivalence of the class groups in algebraic geometry]]

# Exemples

## Projective spaces

Let $k$ be a field. The Picard group of $\mathbb{P}^n_k$ is isomorphic to $\mathbb{Z}$, with generator $\mathcal{O}(1)$ v. [[Projective space]]

**Step 1.** *Injection $\mathbb{Z} \subseteq Pic(\mathbb{P}^n_k)$ given by $1 \mapsto \mathcal{O}(1)$.*

v. [[Twisted sheaf module]]

We have to check that $\mathcal{O}(d) \neq \mathcal{O}_{\mathbb{P}^n_k}$ for $d \geq 1$, i.e. that there's no torsion. This is because the stalks $\mathcal{O}(d)_\mathfrak{p}$ and $\mathcal{O}_{\mathbb{P}^n_k,\mathfrak{p}}$ are not isomorphic (for some $\mathfrak{p} \in Proj(k[X_0,\dots,X_n])$), for any $d \geq 1$.

For instance, take $\mathfrak{p} = (X_0)$. Then$$\mathcal{O}(d)_{(X_0)} = k\left\langle \frac{X_{i_1} \cdots X_{i_d}}{X_j} \mid i_1, \dots, i_d \in \{0, \dots, n\},\ j \in \{1,\dots,n\} \right\rangle,$$which has dimension $n(n+1)^d$ as a $k$-vector space, while$$\mathcal{O}_{\mathbb{P}^n_k,(X_0)} = k \left\langle \frac{X_i}{X_j} \mid i \in \{0,\dots, n\},\ j \in \{1,\dots,n\}\right\rangle,$$which has $k$-dimension $n(n+1)$.

**Step 2.** *It's actually surjective!*