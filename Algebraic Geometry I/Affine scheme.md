An **affine scheme** is a locally ringed space $(X,\mathcal{O}_X)$ which is isomorphic to $Spec(A)$ for some ring $A$. (v. [[Structure sheaf]])

# Propietats

## Rings = Affine schemes

Let $A$ and $B$ be rings. There is a bijection$$Hom_{Ring}(A,B) \cong Hom_{Sch}((Spec(B), \mathcal{O}_{Spec(B)}),\ (Spec(A), \mathcal{O}_{Spec(A)})).$$
This gives an equivalence of categories$$(AffSch)^{op} \cong Ring.$$

*Proof.*

***Step 1.*** *Definition of the bijection.*

Given $(f,f^\sharp)$ morphism of schemes, take the morphism of rings $$f^\sharp_{(Spec(A))}: A = \mathcal{O}_{Spec(A)}(Spec(A)) \to f_*\mathcal{O}_{Spec(B)}(Spec(A)) = B.$$

In the opposite direction, suppose given $\varphi: A \to B$ morphism of rings. We want to define $(f,f^\sharp)$. On the one hand, $f(\mathfrak{p}) := \varphi^{-1}(\mathfrak{p})$. On the other hand, we define $f^\sharp$ on the open sets $D(a)$ (they form a basis). It's given by the localisation of $\varphi$ at $a$:$$\mathcal{O}_A(D(a)) = A_a \to B_{\varphi(a)} = (f_* \mathcal{O}_B)(D(a)).$$
***Step 1.1.*** *The morphism $f^\sharp_\mathfrak{p}$ is local for every $\mathfrak{p}$.*

This is because it comes from a localisation.

***Step 2.*** *These give an actual bijection.*

Finalment queda veure que aquestes assignacions són inverses l'una de l'altra. **qed**

## Preimage of a basic open set

Let $f: Spec(A) \to Spec(B)$ be induced by $\varphi: B \to A$. Then $$f^{-1}D(b) = D(\varphi b),\quad b \in B.$$
*Demostració.*

$D(b)$ és el conjunt d'ideals primers $\mathfrak{p} \subseteq B$ que no contenen $b$. Per tant, $f^{-1}D(b)$ són els ideals primers $\mathfrak{q} \subseteq A$ tals que $\varphi^{-1}\mathfrak{q}$ no conté $b$. Aquesta condició és equivalent a la condició que $\mathfrak{q} \subseteq A$ no contingui $\varphi b$, que és el mateix que demanar que $\mathfrak{q} \in D(\varphi b)$. **qed**

## Finite modules

Assume $\varphi: A \to B$ is a ring homomorphism, and $b_i \in B$ such that $(b_i)_i = B$. If $B_{b_i}$ is of finite type over $A$ (for all $i$), then also $B$ is of finite type over $A$.

Recordem que "$B$ is of finite type over $A$" significa que "B is a finite $A$-module".

**Interpretació geomètrica:** Let $f: Spec(B) \to Spec(A)$ be a morphism of affine schemes, and consider a finite open covering $\{D(b_i)\}_i$ of $B$. If each restriction $f|_{D(b_i)}$ makes $A \to B_{b_i}$ a finite $A$-module, then $f$ makes $A \to B$ a finite $A$-module.

En altres paraules, la condició que $f: Spec(B) \to Spec(A)$ fa $A \to B$ un $A$-mòdul finit es pot comprovar localment.

v. [[Standard tricks with schemes]]