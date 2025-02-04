If $X$ is **factorial** (and satisfies #), then $CaCl(X) \cong Cl(X)$.

v. [[Cartier divisor class group]], [[Weil divisor class group]].
# Proofs

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