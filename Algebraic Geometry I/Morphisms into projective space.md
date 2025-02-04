## Correspondence

For a fixed scheme $X$, morphisms $X \to \mathbb{P}^n$ are in bijection with the data $(\mathcal{L}, s_0, \dots, s_n)$, where $\mathcal{L}$ is an invertible sheaf and $s_0, \dots, s_n$ are global sections of $\mathcal{L}$ with no common zeroes, up to isomorphism of these data.

v. [[The Rising Sea]] 16.4.1.

*Achtung!* "with no common zeros" significa que no hi ha cap zero que sigui comú en totes les seccions alhora! Pot passar que hi hagi dues seccions que s'anul·lin en un mateix punt. Això de fet és anàleg al fet que les coordenades projectives no s'anul·len totes alhora.

*Proof.*

**EXISTENCE.**

Defined by glueing on the open sets $X_i := \{x \in X \mid (s_i)_x \notin \mathfrak{m}_x \mathcal{L}_x\}$, which cover $X$ by the assumption on $s_0, \dots, s_n$. Define $f_i: X_i \to D_+(X_i) \subseteq \mathbb{P} ^n_A$ corresponding to $A[X_j/X_i]_j \to \Gamma(X_i, \mathcal{O}_{X_i})$ given by $X_j/X_i \mapsto s_j s_i^{-1}$.

**UNIQUENESS.**

Exercise. **qed**

## Improvement! Immersions

==Achtung! aquí hi ha alguna cosa que m'ensumo que no està bé... Però la idea és bona!==

In some cases, the construction can be improved to render $f$ an **immersion**.

**Setup/hypothesis.** Consider an invertible sheaf $\mathcal{L}$ and global sections $s_0, \dots, s_n$ of $\mathcal{L}$. Suppose that $X_{s_i} := \{x \in X \mid s_i(x) \neq 0\} \cong Spec(B_i)$ with each $B_i$ of finite type over $A$. Write$$A[X_{i1}, \dots, X_{in}] \to B,\quad X_{ij} \mapsto b_{ij}.$$
**Notation.** For $s$ a section of $\mathcal{L}$, write $s(x)$ for the class of $s_x$ in $\mathcal{L}_x/\mathfrak{m}_x \mathcal{L}_x$.

**Pas 1.** *Principi de prolongació analítica.* (v. [[Coherent and quasicoherent modules]])

There exists some $k>0$ such that $s_i^k b_{ij}$ extends to some $t_{ij} \in H^0(X,\mathcal{L}^{\otimes k})$. (en primer lloc la $k$ s'obté individualment, i llavors la prenem global perquè només n'hi ha un nombre finit)

**Pas 2.** *Definició del morfisme: "hi afegim més espai".*

Com que $s_0^k, \dots, s_n^k$ generen globalment $\mathcal{L}^{\otimes k}$, determinen un morfisme $(\mathcal{L}^{\otimes k}; s_0^k, \dots, s_n^k): X \to \mathbb{P}^n$, però que no necessàriament és una immersió. Però si hi afegim les seccions $\{t_{ij}\}_{ij}$, sí que serà una immersió.

Sigui $\tilde f: X \to \mathbb{P}^M_A$ el morfisme sobre $Spec(A)$ obtingut a partir de $(\mathcal{L}^{\otimes k}; s_i^k, t_{ij})$, on $M := r+1+\#\{t_{ij}\}_{ij}$ és molt gran. Aquest morfisme satisfà, per construcció, que $\tilde f^* \mathcal{O}(1) \cong \mathcal{L}^{\otimes k}$, $\tilde f^* X_i = s_i$ i $\tilde f^* X_{ij} = t_{ij}$.

**pregunta:** *Aquí no hauria de ser $\tilde f^* X_i = s_i^k$ ????*

**Pas 3.** *Comprovació que és una immersió.*

Estudi local. Considerem el recobriment de $\mathbb{P}^M_A$ pels oberts $D_+(X_i)$ i $D_+(X_{ij})$.

***Pas 3.1.*** *La imatge està continguda en $\bigcup_i D_+(X_i)$.*

Això és perquè $\tilde f^{-1}(\bigcup_i D_+(X_i)) = \bigcup_i X_{s_i} = X$.

***Pas 3.2.*** *Estudi de les restriccions de $\tilde f$ a $X_{s_i}$.*

La restricció $\tilde f|_{X_{s_i}}$ factoritza a través de $D_+(X_i) \subseteq \mathbb{P}^M_A$, i ve donada per$$A[X_j/X_i, X_{ij}/X_i] \to B_i,$$que és exhaustiu per hipòtesi.

Això prova que $\tilde f$ és una immersió. **qed**

## Local criterion for closed embeddings into projective space

Let $k$ be an algebraically closed field, let $X$ be a projective scheme over $Spec(k)$, and let $\mathcal{L}$ be an invertible sheaf on $X$. Given $s_0, \dots, s_n \in H^0(X, \mathcal{L})$ generators, one has an induced morphism $f: X \to \mathbb{P}^n_k$ (v. [[Morphisms into projective space]]) such that $f^* \mathcal{O}(1) \cong \mathcal{L}$ and $f^* X_i = s_i$.

**Question:** When is this a closed embedding?

**Partial answer:** A [[Ample sheaf]] "ample sheaf = immersion into projective space, for some power" hi ha una resposta parcial. Bàsicament, si $(\mathcal{L};s_0,\dots,s_n)$ satisfan aquesta propietat, aleshores cal que $\mathcal{L} = \mathcal{M}^{\otimes r}$ per algun feix invertible $\mathcal{M}$ i alguna $r$. Però volem un criteri més **geomètric**.

Let $V$ denote the $k$-vector space $k \langle s_0, \dots, s_n \rangle \subseteq H^0(X, \mathcal{L})$, which is called a **linear system**.

$f$ is a **closed immersion** if, and only if, the following hold:
1. $V$ **separates points**: for every $x, y \in X$ distinct and closed, there exists some $s \in V$ such that $s(x) = 0$ but $s(y) \neq 0$.
2. $V$ **separates tangent directions**: for every $x \in X$ closed, the composite$$k \langle s_x \mid s(x) = 0,\ s \in V \rangle \subseteq \mathfrak{m}_x \cdot \mathcal{L}_x \to \mathfrak{m}_x/\mathfrak{m}_x^2 \cdot\mathcal{L}_x$$is surjective.

**Achtung!** Crec que s'utilitzen "closed immersion" i "closed embedding" indistintament.

*Intuition of the property "seprarates tangent directions".* The Zariski tangent space (v. [[Zariski tangent space]]) of $X$ at $x$ is$$T_{X,x} := Hom_{k(x)}(\mathfrak{m}_x/\mathfrak{m}_x^2, k(x)).$$Think of the image of $s \in \langle s \in V \mid s(x) = 0 \rangle$ as a form $ds$ at $x$.

*Proof =>.*

**WLOG.** Assume $X \subseteq \mathbb{P}^n_k$ closed subscheme, so $f$ is the inclusion.

Take $x, y \in X$ distinct, closed points, which can be written as$$x = [a_0: \cdots : a_n],\ y = [b_0: \cdots: b_n].$$
**Pas 1.** *Construcció de la secció que separa $x$ i $y$.*

Com que $x \neq y$, els vectors $(a_0, \dots, a_n), (b_0, \dots, b_n) \in k^{n+1}$ són linealment independents, així que existeix una forma lineal no-nul·la $\ell$ tal que $\ell(a_0, \dots, a_n) = 0$ però $\ell(b_0, \dots, b_n) \neq 0$. Aquesta forma es pot escriure com $\ell(x_0, \dots, x_n) = \sum_i \ell_i x_i$.

Escollim la secció $s := \sum_i \ell_i s_i \in V$, que és $f^* \sum_i \ell_i X_i$. Aleshores$$s(x) = \ell(a_0, \cdots, a_n) = 0,\ s(y) = \ell(b_0, \cdots, b_n) \neq 0.$$
Això conclou la demostració de (i).

**WLOG.** Ara demostrem (ii), i per a això considerem $x \in X$ tancat que, sense pèrdua de generalitat, podem suposar que té coordenades $[1:0:\cdots:0]$ i, per tant, és a l'obert $D_+(X_0) \subseteq \mathbb{P}^n_k$.

**Pas 2.** *Prenem stalks.*

Com que $X \to \mathbb{P}^n_k$ és una closed immersion, el morfisme en stalks$$(k[X_i/X_0]_i)_{(X_i/X_0)_i} \to \mathcal{O}_{X,x}$$és exhaustiu, que fa que el següent també sigui exhaustiu:$$k\langle X_i/X_0\rangle_i \to \mathfrak{m}_x/\mathfrak{m}_x^2.$$
Recordem que estem identificant $\mathcal{L} \cong f^* \mathcal{O}(1)$, així que concloem amb (ii) (?????) **qed**

*Proof <=.* More complicated! **qed**

# Corol·laris

## If the sections don't globally generate $\mathcal{L}$

If $s_0, \dots, s_n$ don't globally generate $\mathcal{L}$, then we still get a unique morphism $\bigcup_i X_i \to \mathbb{P}^n_A$, where $X_i := \{x \in X \mid (s_i)_x \notin \mathfrak{m}_x \mathcal{L}_x\}$. This is a [[Rational map]].

**Remark.** We could ask for good properties of $f$. It's a closed immersion if, and only if, the restriction $f^{-1}D_+(X_i) \to D_+(X_i)$ is a closed immersion for every $i$. Since $D_+ (X_i)$ is affine, this is equivalent to $f^{-1} D_+(X_i)$ being affine and $A[X_j/X_i]_j \to H^0(f^{-1} D_+(X_i), \mathcal{O})$ being surjective. (???)

## Global point of view

We've related morphisms into $\mathbb{P}^n_A$ with sections of invertible bundles. Now, given $f: X \to T$ an arbitrary morphism of schemes, morphisms $X \to \mathbb{P}^n_T$ over $T$ correspond to cones over $T \to Spec(\mathbb{Z}) \leftarrow \mathbb{P}^n_{\mathbb{Z}}$. Asking that they're over $T$, these correspond to morphisms $X \to \mathbb{P}^n_{\mathbb{Z}}$ making the diagram commute. So they are determined by invertible bundles together with appropriate sections, although they needn't be in a 1-to-1 correspondence (because we have to ask for commutativity).

# Exemples

## Linear projection in projective space

The sections $X_0, \dots, X_n \in \Gamma(\mathbb{P}^{n+1}_k, \mathcal{L})$ (note that $X_{n+1}$ is missing!) don't globally generate $\mathcal{L}$. Hence, they induce a rational map$$f:\bigcup_{i=0}^n D_+(X_i) = \mathbb{P}^{n+1}_k \setminus \{ [0:\cdots:0:1] \} \to \mathbb{P}^n_k$$called **linear projection from $[0:\cdots:0:1]$**.

If $k = \bar k$, looking at the closed points we have$$f([x_0:\cdots:x_{n+1}]) = [x_0: \cdots: x_n].$$This explains why the map is not defined on $[0:\cdots:0:1]$, since $[0:\cdots:0]$ is not an element of the projective space.