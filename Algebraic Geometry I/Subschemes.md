If $(X, \mathcal{O}_X)$ is a scheme and $U\subseteq X$ open, then $(U, \mathcal{O}_X|_{U})$ is called an **open subscheme** of $X$. Observem que, si $i: U \to X$ és la inclusió, aleshores $\mathcal{O}_X|_{i(U)} = i^{-1} \mathcal{O}_X$. Comparar amb [[Reduced induced scheme]].

If $Spec(B) \subseteq Spec(A)$ is an open subscheme, then $Spec(B) = \bigcup_{i=1}^n Spec(A_{a_i})$.

It's not true that any open subscheme $U \subseteq X = Spec(A)$ of an affine scheme is again affine. Take for example $\mathbb{A}^n_k \setminus \{\textrm{origin}\}$ with $n \geq 2$ ($n = 1$ is not a counterexample because it's isomorphci to the hyperbola).

# Closed subschemes

## First definition

**Closed subscheme** of $(X, \mathcal{O}_X)$ is an equivalence class of morphisms of schemes$$(i,i^\sharp): (Z,\mathcal{O}_Z) \to (X,\mathcal{O}_X)$$such that:
1. $i$ is a homeomorphism with a closed subset of $X$,
2. $i^\sharp: \mathcal{O}_X \to i_* \mathcal{O}_Z$ is surjective (meaning that $\mathcal{O}_{X,i(z)} \to \mathcal{O}_{Z,z}$ is surjective for every $z$).

The equivalence relation is given by isomorphisms in the overcategory $Sch_{/(X,\mathcal{O}_X)}$.

The morphisms $(i,i^\sharp)$ are called **closed immersions**.

## Second definition

A **closed subscheme** of $(X,\mathcal{O}_X)$ is a closed subspace $i: Z \to X$ together with:
- A scheme $(Z,\mathcal{O}_Z)$ on $Z$
- A sheaf of ideals $\mathcal{V}_Z \subseteq \mathcal{O}_X$

such that:$$(\mathcal{O}_X/\mathcal{V}_Z)^+ \cong i_* \mathcal{O}_Z.$$

*Intuïció.* En geometria algebraica clàssica, les subvarietats tancades de $\mathbb{A}^2_k$ són $V(f)$, que estan en bijecció amb els ideals $(f) \subseteq k[X,Y,Z]$. A més, l'anell de coordenades és $k[X,Y,Z]/(f)$. Comparar això amb la segona definició de closed subscheme.

# Propietats

## Correspondència ideals de $A$ <-> subesquemes tancats de $Spec(A)$

Let $A$ be a ring. There's a natural bijection$$\{\mathfrak{a} \subseteq A\ \textrm{ideal}\} \cong \{Z \subseteq Spec(A)\ \textrm{closed\ subscheme}\}.$$
*Proof.*

->] For an ideal $\mathfrak{a} \subseteq A$, take $(Z,\mathcal{O}_Z) = (Spec(A/\mathfrak{a}), \mathcal{O}_{A/\mathfrak{a}})$, $\mathcal{V}_Z(D(a)) := \mathfrak{a}_a$. Per comprovar l'isomorfisme $(\mathcal{O}_X/\mathcal{V}_Z)^+ \cong i_* \mathcal{O}_Z$ es fa al nivell de stalks.

<-] A closed subscheme $(Z, \mathcal{O}_Z) \subseteq (Spec(A), \mathcal{O}_A)$ induces $A = \Gamma(X,\mathcal{O}_X) \to \Gamma(Z,\mathcal{O}_Z)$. Define $\mathfrak{a}$ to be the kernel of this map.

To show that de composite $\{\textrm{closed\ subschemes}\} \to \{\textrm{ideals}\} \to \{\textrm{closed\ subschemes}\}$ is the identity requires some more work. In other words, we have to show that the following closed subschemes of $(X,\mathcal{O}_X)$ are the same:$$(Spec(A/\mathfrak{a}_Z), \mathcal{O}_{A/\mathfrak{a}_Z}) \stackrel{?}{=} (Z,\mathcal{O}_Z).$$Here $\mathfrak{a}_Z \subseteq A$ denotes the kernel of $\Gamma(X,\mathcal{O}_Z) \to \Gamma(Z,\mathcal{O}_Z)$.

**Step 1:** *$Z \subseteq V(\mathfrak{a}_Z)$ ($\subseteq Spec(A)$) as sets.*

Suppose this is not true. Take an element $\mathfrak{p}$ in the complement $Z \setminus V(\mathfrak{a}_Z)$. The condition that it doesn't belong to $V(\mathfrak{a}_Z)$ is equivalent to the existence of some $a \in \mathfrak{a}_Z$ such that $\mathfrak{p} \in D(a)$.

The image of $a_\mathfrak{p} \in A_\mathfrak{p}$ in $\mathcal{O}_{Z,\mathfrak{p}}$ is zero beacuse $a \in \mathfrak{a}_Z = ker$. But since $a_\mathfrak{p}$ is a unit, $0$ should be a unit in $\mathcal{O}_{Z,\mathfrak{p}}$. Contradiction!

Now consider $(j,j^\sharp): (Spec(A/\mathfrak{a}_Z), \mathcal{O}_{A/\mathfrak{a}_Z}) \to (Spec(A), \mathcal{O}_A)$, and denote $(i, i^\sharp): (Z,\mathcal{O}_Z) \to (X, \mathcal{O}_X)$.

**Step 2:** *There exists a $g: j_{\ast} \mathcal{O}_{A/\mathfrak{a}_{Z}} \to i_{\ast} \mathcal{O}_{Z}$ that becomes a morphism from $j^\sharp$ to $i^\sharp$ in the undercategory. Note moreover that $g$ is still surjective.*

Surjectivity of $j^\sharp$ implies that it's an epimorphism and hence has a left inverse. We use it to construct $g$.

**Reduction:** Now we can replace $(i,i^\sharp):(Z,\mathcal{O}_Z) \subseteq (X,\mathcal{O}_X) = (Spec(A), \mathcal{O}_A)$ by $(j,j^\sharp):(Z,\mathcal{O}_Z) \subseteq (Spec(A/\mathfrak{a}_Z), \mathcal{O}_{A/\mathfrak{a}_Z})$.

**WLOG:** Without loss of generality we can assume that $A = \Gamma(X,\mathcal{O}_X) \subseteq \Gamma(Z,\mathcal{O}_Z)$. (==no veig per què... no tenim un kernel no-trivial $\mathfrak{a}_Z$?==)

**Step 3:** *$Z$ = $X$ as sets.*

Since $Z \subseteq X$ closed, $Z = V(a_1,a_2,\cdots)$ for certain $a_i \in A$. Pick some $a = a_i$, and hence $Z \subseteq V(a)$.

Since $Z$ is a closed subset of a quasi-compact space, it's also quasi-compact. We can hence cover $Z = \bigcup_{i=1}^n Spec(B_i)$. Let $b_i$ be the image of $a$ under $A \to \Gamma(Z,\mathcal{O}_Z) \to \mathcal{O}_Z(Spec(B_i)) = B_i$.

By definition, $Spec(B_i) \subseteq V(a)$ and hence every $\mathcal{p} \subseteq B_i$ primer contains $b_i$. This implies that $b_i$ is nilpotent, i.e. $b_i^{n_i} = 0$ for some power. We can choose a power $n$ such that the image of $a^n$ under $A \to B_i$ always vanishes.

The image of $a^n$ under $A \to \Gamma(Z,\mathcal{O}_Z)$ hence vanishes (by the sheaf condition). Since this map is injective, $a^n = 0$. This implies that $V(a) = X$, and hence $Z = X$ (because V(nilpotent) = Spec(A) ). This shows the equality as sets.

**Step 4:** *$Z =X$ as schemes.*

It remains to be shown that the structure sheaves are the same. We know that $i^\sharp$ is injective, it remains to be shown that it's surjective.

**Step 4.1:** *$D(s) = \{z \in Z \mid \varphi(s)_z \in \mathcal{O}^\times_{Z,z}\}$ where $\varphi: A \to \Gamma(Z,\mathcal{O}_Z)$.*

**qed**