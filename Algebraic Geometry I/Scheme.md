A **scheme** is a locally ringed space $(X,\mathcal{O}_X)$ that admits an open covering $\{U_i\}_i$ of $X$ such that $(U_i,\mathcal{O}_X|_{U_i})$ is an affine scheme. (v. [[Affine scheme]])

Els morfismes entre esquemes són els morfismes de locally ringed spaces.

Some extra properties:

***Topological properties:***
- **Connected:** The underlying topological space $X$ is connected.
- **Irreducible:** The underlying topological space is irreducible, i.e. it's not possible to find a decomposition $X = A \cup B$ with $A$, $B$ closed and nontrivial. Note that irreducibility is equivalent to $\overline{U} = X$ for every nonempty open $U$, and also to $U \cap V \neq \emptyset$ for $U, V \neq \emptyset$. Moroever, irreducibility implies connectedness.
- **Quasi-compact:** Every open covering of $X$ has a finite open subcovering.

***Scheme theoretic properties:***
- **Locally Noetherian:** $X$ can be covered by schemes $Spec(A_i)$ with $A_i$ Noetherian v. [[Noetherian ring]].
- **Noetherian:** Locally Noetherian + quasi-compact.
- **Reduced:** For every open $U\subseteq X$, $\Gamma(U,\mathcal{O}_X)$ is reduced (i.e. the only nilpotent element is $0$). This is equivalent to $\mathcal{O}_{X,x}$ reduced for every $x$.
- **Integral:** Every $\Gamma(U,\mathcal{O}_X)$ is an integral domain. Note that integral => reduced. Note that integral implies $\mathcal{O}_{X,x}$ integral, but the converse needn't hold.
- **Normal:** A scheme is normal if all of its stalks $\mathcal{O}_{X,x}$ are normal (normal ring = integrally closed in its field of fractions).

# Interpretació

## Reduced

Suposem que tenim un esquema reduït $(X,\mathcal{O}_X)$, i sigui $s \in \Gamma(U,\mathcal{O}_X)$ una secció en $U$ que s'anul·la en cada $x \in U$ (és a dir, que satisfà $s_x \in \mathfrak{m}_x$ per cada $x \in U$). Prenem cartes afins $U_i$, i denotem la restricció de $s$ en $U_i$ per $s_i$.

Com que $s_i$ s'anul·la en cada punt de $U_i$, $D(s_i) = \emptyset$ així que $s_i \in \mathfrak{N}_{A_i}$ (v. [[Structure sheaf]] "Nilradical"). Per tant, com que l'esquema és reduït, $s_i = 0$ per cada $i$. Això implica que $s = 0$.

En altres paraules, en els esquemes reduïts **una secció (local) s'anul·la en tots els punts si, i només si, és la secció zero**. El recíproc suposo que també és cert, però no ho sé.

# Propietats

## Separabilitat

**Propietat $T_0$:** Els esquemes són espais topològics $T_0$, és a dir, per cada parell de punts $x,y \in X$ existeix un obert $U$ que en conté exactament a un dels dos.

*Demostració.*

És suficient veure-ho per punts que es troben a dins de la mateixa carta afí, ja que altrament és trivial. És a dir, SPDG podem suposar que $X$ és un esquema afí, $X \cong Spec(A)$.

Si $\mathfrak{p}, \mathfrak{q} \in Spec(A)$ són tals que no existeix cap obert que en conté un però no l'altre, aleshores $\mathfrak{p} \in D(a) \iff \mathfrak{q} \in D(a)$, per cada $a \in A$. Desenvolupant aquesta equivalència es dedueix que $\mathfrak{p}= \mathfrak{q}$. **qed**

**Propietat $T_1$:** Els esquemes no satisfan, en general, la propietat de separació $T_1$ (recordem que això significa que per cada parell de punts $x, y \in X$ existeix un obert $U$ que conté $x$ però no $y$, i un altre obert $V$ que conté $y$ però no $x$).

Això es comprova veient que $(0)$ no és, en general, separable (per exemple en $Spec(\mathbb{Z})$).

## Rings = Affine schemes

v. [[Affine scheme]]

## Spec and global sections are adjoint

For any scheme $X$ and any ring $A$,$$Hom_{Sch}(X,Spec(A)) \cong Hom_{Ring}(A,\Gamma(X,\mathcal{O}_X)).$$
**Remark:** This is a generalization of the fact that AffSch^{op} = Rings. Es demostra prenent un recobriment per cartes afins.

## Glueing schemes

Let $(X_i, \mathcal{O}_{X_i})$, $i = 1,2$, schemes, together with an isomorphism of schemes$$(\varphi,\varphi^\sharp): (U_1,\ \mathcal{O}_{X_1}|_{U_1}) \stackrel{\cong}{\to} (U_2,\ \mathcal{O}_{X_2}|_{U_2}),$$for some open subsetes $U_i\subseteq X_i$.

Then we can glue them.

## Affine charts in locally Noetherian schemes

v. [[Algebraic geometry (Hartshorne)]] Proposition II.3.2.

**Proposition.** $X$ is locally Noetherian if, and only if, every open affine chart is of the form $Spec(A)$ with $A$ Noetherian.

**Corollary.** If $Spec(A)$ is a locally Noetherian scheme, then $A$ is Noetherian.

*Proof (proposition).*

=>]

Take an open affine chart $U$, which is isomorphic to some $Spec(B)$. Let $Spec(A_i)$ cover $X$ with $A_i$ Noetherian (by hypothesis).

***Step 1:*** *Reduction to a purely algebraic statement.*

The basic open sets $D(f)$, $f \in A_i$, are noetherian affine schemes because they're isomorphic to $(A_i)_f$, and $A_i$ is Noetherian. Cover $U$ by such basic open sets. Quasi-compactness of $U$ allows to take a finite subcover.

**Warning!** A more subtle argument is probably needed...

This yields the algebraic problem: **Let $B$ be a ring, and suppose that $f_1, \dots, f_r \in A$ are such that they generate the unit ideal, and the $B_{f_i}$ are Noetherian. Is $B$ also Noetherian?**

We can now proceed to prove this algebraic statement.

**Warning!** My notation differs with Hartshorne's.

***Step 2:*** *We show the following equality:*$$\mathfrak{a} = \bigcap_i \varphi_i^{-1}(\varphi_i(\mathfrak{a}) B_{f_i}),\quad \mathfrak{a} \subseteq B\ \textrm{ideal},$$*where $\varphi_i: B \to B_{f_i}$ denotes the localisation.*

***Step 3:*** *Show that $B$ is indeed Noetherian.*

Take a chain of ideals $\mathfrak{a}_1 \subseteq \mathfrak{a}_2 \subseteq \cdots$ in $B$. We obtain a chain of ideals in $B_{f_i}$$$\varphi_i(\mathfrak{a}_1) B_{f_i} \subseteq \varphi_i(\mathfrak{a}_2) B_{f_i} \subseteq \cdots$$for every $i$. Each of these stabilizes at some $n_i$, because the $B_{f_i}$ are Noetherian. Let $n := max_i (n_i)$. Then the chain obtained by intersecting, for every $i$, the preimages under $\varphi_i$ of these chains, stabilizes at $n$. But it coincides with the original chain $\mathfrak{a}_1 \subseteq \cdots$ in $B$, so we deduce Noetherianity of $B$. **qed**

## Integral <=> Irreducible & reduced

A scheme is **integral** if, and only if, it's **irreducible** and **reduced**.

*Proof.*

=>]

Integral implies reduced by definition. If $X$ weren't irreducible, then $\mathcal{O}_X(U_1 \cup U_2) = \mathcal{O}_X(U_1) \times \mathcal{O}_X(U_2)$ for some $U_1 \cap U_2 = \emptyset$ !!!

<=]

Let $s_1, s_2 \in \Gamma(U, \mathcal{O}_X)$, $U$ nonempty, such that $s_1 s_2 = 0$.

***Recall:*** If $\mathfrak{m}_x$ is the maximal ideal of $\mathcal{O}_{X,x}$, then $V_x := \{x \in U \mid s_x \in \mathfrak{m}_x\}$ is closed in $U$. (v. "Some open (and closed) sets").

***Step 1:*** *Some $s_i$ "vanishes" in the whole $U$. (WLOG, $s_1$)*

Define $V_i := \{x \in U \mid (s_i)_x \in \mathfrak{m}_x\}$, which are closed in $U$. The condition $s_1 s_2 = 0$ implies that $V_1 \cup V_2 = U$. WLOG, by the irreducibility of $U$ suppose that $V_1 = U$.

***Step 2:*** $s_1 = 0$.

Això és perquè $s_1$ s'anul·la en tots els punts de $U$, i l'esquema és reduït (v. "Intuïció"). A continuació es dóna una justificació més estensa.

It's checked that $s_1 = 0$ in every affine chart $Spec(A) \subseteq U$. The restriction of $s_1$ on such a chart is some $t \in A \cong \Gamma(Spec(A), \mathcal{O}_X)$. This $t$ satisfies (by definition) that $D(t) = \emptyset$, so $t$ belongs to the nilradical of $A$ (v. [[Nilradical]], [[Structure sheaf]] "Nilradical"). Since $X$ is reduced, $\mathfrak{N}_A = 0$, so $t = 0$. Glueing we deduce that $s_1 = 0$. **qed**

## Generic point in integral schemes

If $X$ is integral, there exists a unique $\eta \in X$ (called the **generic point** of $X$) such that $\overline{\{\eta\}} = X$. Such a point is $(0)$.

*Proof.*

Existence is trivial. We show uniqueness. Take two such generic points $\eta$ and $\eta'$.

There exists an open affine chart that contains $\eta$. Since the complementary of such an affine chart is closed, and the adherence of $\{\eta'\}$ is the whole $X$, it must be that $\eta'$ belongs to the same affine chart as $\eta$. We can restrict now to affine schemes (and use that they're integral). **qed**

**Remark.** Amb això es demostra també que el punt genèric pertany a totes les cartes afins de $X$.

## Some open (and closed) sets

Given a global section $a \in \Gamma(X,\mathcal{O}_X)$, the set $X_a \subseteq X$ is defined as the set of points $x \in X$ such that $a_x \notin \mathfrak{m}_x$. This can be interpreted as the set of points in $X$ where the section $a$ doesn't vanish. It's clearly an open set (not so easy to prove...). In fact, in affine schemes we have that $X_a = D(a)$.

Some properties:
- $\{X_a\}_a$ is **not** a basis for the topology on $X$ (in general). For example take $\mathbb{P}^1_k$, $k$ field.
- If $X$ is Noetherian, then $\Gamma(X_a,\mathcal{O}_X) \cong \Gamma(X,\mathcal{O}_X)_a$.

De la mateixa forma es pot definir $V_a := X \setminus X_a$, que és tancat.

## Preimage of a basic open set inside an affine chart

Let $f: X \to Spec(A)$, and cover $X$ by $\{U_i \cong Spec(A_i)\}_i$. Let $D(a) \subseteq Spec(A)$. Then$$f^{-1} D(a) = \bigcup_i D(\varphi_i a),$$where $\varphi_i: A \to B_i$ is the morphism of rings associated to the restriction $Spec(A_i) \to Spec(A)$ of $f$.

**Observació.** Aquí hi ha un abús de notació, ja que la unió de la dreta s'està pensant sota l'isomorfisme $U_i \cong Spec(A_i)$. Cal enganxar les peces adientment.

*Demostració.*

Tenim:$$f^{-1} D(a) = \bigcup_i f|_{U_i}^{-1} D(a) \cong \bigcup_i D(\varphi_i a).$$
v. [[Affine scheme]] "preimage of a basic open set". **qed**

# Classical geometry to scheme theory

**Classical:** $k$ algebraically closed field, $X \subseteq k^n$ affine algebraic set (i.e. there exists some $\mathfrak{a} \subseteq k[X_1,\dots,X_n]$ such that $X = V(\mathfrak{a})$).

$X$ comes with the sheaf of regular functions $\mathcal{O}_X$ given by$$\mathcal{O}_X(U) := \left\{h: U \to k \mid h = \frac{g_1}{g_2}\ \textrm{locally},\ g_i \in k[X_1,\dots,X_n]\right\}.$$
The pair $(X,\mathcal{O}_X)$ is a locally ringed space **that is not a scheme**. But we can get a scheme out of it. Let $I(X)$ be the ideal of polynomials in $k[X_1,\dots,X_n]$ that vanish on $X$. By the [[Nullstellensatz]], $I(X) = \sqrt{\mathfrak{a}}$. The **affine coordinate ring** of $X$ is$$A(X) := k[X_1,\dots,X_n]/I(X).$$
Finally we define the (affine) scheme $(Spec A(X), \mathcal{O}_{A(X)})$.

**Claim.** There exists a natural morphism of locally ringed spaces $$(f,f^\sharp): (X,\mathcal{O}_X) \to (Spec A(X), \mathcal{O}_{A(X)}).$$
Define $f: X \to Spec A(X)$ using $X \subseteq k^n \to MaxSpec k[X_1,\dots,X_n]$ which factors through $MaxSpec A(X) \subseteq MaxSpec k[X_1,\dots,X_n]$. In fact, since $k$ is algebraically closed, $X$ gets identified with $MaxSpecA(X)$.

Define $f^\sharp: \mathcal{O}_{A(X)} \to f_* \mathcal{O}_X$ by sending an element $(s_\mathfrak{p})_\mathfrak{p} \in \mathcal{O}_{A(X)}$ to ??? #TODO **Idea:** locally $\mathcal{O}_{A(X)}$ és $(a_\mathfrak{p})_\mathfrak{p}$ amb $a_\mathfrak{p} \in A(X)_\mathfrak{p}$, mentre que $f_* \mathcal{O}_X$ és localment també un quocient de polinomis.

Cal comprovar que és un **local morphism** of ringed spaces.

**Remark:** For the definition of $(Spec A(X), \mathcal{O}_{A(X)})$ we only used that $X$ is an affine algebraic set (i.e. $X = V(\mathfrak{a})$).
# Exemples

## Feix estructural

[[Structure sheaf]]

## Dual numbers

$k$ field, $A = k[X]/(X^2)$ ring of dual numbers. Note that $Spec(A) = \{(0)\}$. We have the schemes $(Spec(k), \mathcal{O}_k)$ and $(Spec(A), \mathcal{O}_A)$. We construct a morphism $(f,f^\sharp): Spec(k) \to Spec(A)$:
- $f$ is the "identity"
- $f^\sharp: \mathcal{O}_A \to f_* \mathcal{O}_k$ is the quotient by the ideal $(\bar X) \subseteq A$.

We have another morphism $(g,g^\sharp): (Spec(A), \mathcal{O}_A) \to (Spec(k), \mathcal{O}_k)$ given by:
- $g$ is the "identity"
- $g^\sharp: \mathcal{O}_k = k \to A = g_* \mathcal{O}_A$ is just the natural embedding.

Then $(g,g^\sharp) \circ (f,f^\sharp) = id$, but they're not isomorphisms. Hence, $(Spec(k), \mathcal{O}_k)$ *sits inside* $(Spec(A), \mathcal{O}_A)$.

The dual are an exemple of a nonreduced (and nonintegral) scheme.

The dual numbers have two points ($(0)$ and $(\epsilon)$) whose closure is $Spec(k[\epsilon])$. Compare with "Generic point in integral schemes".

## $\mathbb{Z}$-schemes

There exists a unique morphism of schemes $X \to Spec(\mathbb{Z})$, where $Spec(\mathbb{Z})$ denotes the scheme and not only the topological space. Hence every scheme is trivially (and uniquely) a $\mathbb{Z}$-scheme.

If the unique morphism $X \to Spec(\mathbb{Z})$ has image contained in $\mathfrak{p}$, then it factors thourgh the unique morphism $Spec(\mathbb{Z}/\mathfrak{p}) \to Spec(\mathbb{Z})$. In these cases we say that $X$ is a $\mathbb{F}_p$- or $\mathbb{Q}$-scheme.

## k-algebras

Let $k$ be a field, and $A$ a $k$-algebra. Then the inclusion $k \subseteq A$ induces a morphism of schemes $Spec(A) \to Spec(k)$, so we view $Spec(A)$ as a $k$-scheme.

## Line with two origins

Consider two copies of the affine line $\mathbb{A}^1_k$, and take the identification $id: \mathbb{A}^1_k \setminus \{0\} \to \mathbb{A}^1_k \setminus \{0\}$. By glueing these two copies one obtains the line with two origins.

## Projective line obtained from glueing

Consider two copies of the affine line $\mathbb{A}^1_k$, and take the open subsets $U_1 = U_2 := Spec (k[X]_X) \subseteq \mathbb{A}^1_k$. Consider the scheme morphism given by $\varphi: X \mapsto X^{-1}$. The scheme obtained after glueing, which we denote by $X$, is the projective line $\mathbb{P}^1_k$.

To visualize this consider $k$ algebraically closed, and study the closed points of $X$. The closed points from the first copy of $\mathbb{A}^1_k$ represent $[1:t]$, while the ones from the second copy, $[t:1]$. We identify, for $t \neq 0$, $[1:t]$ with $[\frac{1}{t}:1]$. This gives the closed points of the projective line.

S'observa que les úniques seccions globals de $\mathbb{P}^1_k$ són constants, i.e. $\Gamma(\mathbb{P}^1_k, \mathcal{O}_{\mathbb{P}^1_k}) = k$. Sigui $s$ una secció global. Ve donada per un parell de polinomis (un per cada carta afí), $f, g \in k[X] = \Gamma(\mathbb{A}^1_k, \mathcal{O}_{\mathbb{A}^1_k})$, tal que $f(X) = g(X^{-1})$ en $Spec(k[X]_X) \subseteq \mathbb{A}^1_k$. L'única possibilitat és que $f=g$ siguin constants (i idèntics).

En particular aquesta observació impedeix que $\mathbb{P}^1_k$ sigui un esquema afí.

## Two axis

The scheme $Spec(k[X,Y]/(XY))$ represents the two lines crossing at the origin. It's connected but not irreducible.

It's a reduced, but not integral, scheme.