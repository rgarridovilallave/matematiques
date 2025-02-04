## Topological properties

- $f$ is **open**/**closed** if $|X| \to |Y|$ is open/closed.
- $f$ is **dominant** if $f(|X|) \subseteq |Y|$ is dense. Note that, if $f$ is closed, this is equivalent to the surjectivity of $f$. Also, if $Y$ is integral with generic point $\eta$, then $f$ is dominant iff $\eta \in im(f)$.
- $f$ is **quasi-compact** if for every $V \subseteq Y$ open and quasi-compact, $f^{-1}(V)$ is quasi-compact.
- $f$ is **quasi-finite** if for all $y \in Y$, the fibre $f^{-1}(y)$ is finite.

## Semi-topological properties

- $f$ is an **open immersion** if there exists an open subsete $U \subseteq Y$ such that $(X,\mathcal{O}_X) \stackrel{f}{\to} (U,\mathcal{O}_Y|_U)$ is an isomorphism of schemes.
- $f$ is a **closed immersion** if there exists a closed subscheme $(Z,\mathcal{O}_Z) \subseteq (Y, \mathcal{O}_Y)$ such that $f$ factors through it and its factor is an isomorphism.
- $f$ is an **immersion** if there exists a closed subscheme $Z \subseteq Y$ and an open subscheme $U \subseteq Z$ such that $(X,\mathcal{O}_X) \stackrel{f}{\to} (U, \mathcal{O}_Z|_U)$ is an isomorphism of schemes. In other words, $f$ is the composition of a closed immersion after an open immersion.

## Scheme-theoretic properties

- $f$ is **locally of finite type** if there exists an open affine covering $\{Spec(A_i)\}_i$ of $Y$, and for each $i$ an affine open covering $\{Spec(B_{ij})\}_j$ of $f^{-1}(Spec(A_i))$, such that $A_i \to B_{ij}$ makes $B_{ij}$ a finite type $A_i$-==algebra==.
- $f$ is called **of finite type** if it's locally of finite type and the open coverings $\{Spec(B_{ij})\}_j$ are finite for every $i$.
- $f$ is **affine** if there exists an open affine covering $\{Spec(A_i)\}_i$ such that $f^{-1}(Spec(A_i))$ is affine.
- $f$ is **finite** if it's affine and, in addition, $f^{-1}(Spec(A_i)) = Spec(B_i)$ with $A_i \to B_i$ making $B_i$ a finite $A_i$-==module==.

## Altres

- A morphism of schemes $f: X \to Y$ is said to be **separated** if the diagonal morphism $\Delta: X \to X \times_Y X$ given by $(id_X,id_X)$  (v. [[Fibre product]]) is a **closed immersion** (v. [[Subschemes]]). An $S$-scheme $X$ is separated if the diagonal $\Delta_{X/S}$ is a closed immersion.
- A morphism $f$ is **proper** if it is separated, of finite type and universally closed. The latter means that for every $Y' \to Y$, the morphism $X \times_Y Y' \to Y'$ is closed.
- **Projective:** if there exists a closed embedding $X \to \mathbb{P}^m_Y$ over $Y$. v. [[The Rising Sea]] 17.3.

# Formes dèbil i forta

| Tipus de morfisme      | Forma dèbil                                                                                                                                                                                                                                                            | Forma forta                                                                                                                                                                              |
| ---------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Quasicompact           | There exists a covering $Y = \bigcup_i V_i$ by affine open subsets $V_i$ such that, for every $i$, the inverse image $f^{-1}V _i$ is quasi-compact.                                                                                                                    | For every quasi-compact open subset $V \subseteq Y$, the preimage $f^{-1} V$ is quasicompact.                                                                                            |
| Locally of finite type | There exists a covering $Y = \bigcup_i V_i$ by open affine subschemes $V_i \cong Spec(A_i)$, and for each $i$ a covering $Y = \bigcup_i U_{ij}$ by open affine subschemes $U_{ij} \cong Spec(B_{ij})$, making $A_i \to B_{ij}$ a finitely generated ==$A_i$-algebra==. | For every affine open subscheme $V$ of $Y$, and every affine open subscheme $U$ of $f^{-1}V$, the ==$\Gamma(V,\mathcal{O}_Y)$-algebra== $\Gamma(U,\mathcal{O}_X)$ is finitely generated. |
| Affine                 | There exists a covering $Y = \bigcup_i V_i$ by open affine subschemes such that $f^{-1} V_i$ is also affine.                                                                                                                                                           | The preimage of every open affine $V \subseteq Y$ is affine.                                                                                                                             |
| Finite                 | Affine & $f^{-1} Spec(A_i) = Spec(B_i)$ makes $A_i \to B_i$ a finite $A_i$-module.                                                                                                                                                                                     | For every affine open $V \subseteq Y$, with $V \cong Spec(A)$, we have that $f^{-1} Spec(A) = Spec(B)$ and makes $A \to B$ a finite $A$-module.                                          |

## Quasicompact

Cal veure que la forma dèbil implica la forta.

Sigui $V \subseteq Y$ obert. El recobrim per oberts bàsics (dins de $V_i$) $\{D_{V_{i_r}}(s_r)\}_{r=1}^n$. Aleshores $$f^{-1}V = \bigcup_{i=1}^n f^{-1} D_{V_{i_r}}(s_r).$$
Com que es tracta d'una unió finita, és suficient veure que $f^{-1}D_{V_i}(s)$ és quasi-compacte, per cada $V_i$ i cada $s \in \Gamma(V_i,\mathcal{O}_Y)$.

Com que l'antiimatge de $V_i$ és quasi-compacta (per hipòtesi), podem trobar un recobriment finit per cartes afins $\{U_{ij}\}_{j=1}^m$ de $f^{-1} V_i$. Si la restricció $U_{ij} \to V_i$ de $f$ té morfisme associat que envia $s \mapsto t_j$, aleshores$$f^{-1} D_{V_i}(s) = \bigcup_{j=1}^m D_{U_{ij}}(t_j),$$ja que l'antiimatge d'un obert bàsic es calcula així (v. [[Scheme]]).

Com que els $D_{U_{ij}}(t_j)$ són quasi-compactes (ja que són afins), i la unió és finita, es dedueix que $f^{-1} D_{V_i}(s)$ és quasi-compacte, tal i com es volia veure. **qed**

## Locally of finite type

v. [[Algebraic geometry I schemes (llibre)]] 

Take open affine $V = Spec(A) \subseteq Y$, and $U = Spec(B) \subseteq f^{-1} V$. We want to see that $A \to B$ makes $B$ a finitely generated $A$-algebra.

**Reduction.** *It suffices to study the case $Y = V = Spec(A)$.*

Consider the open affine cover $\{V_i\}_i$ of $Y$ provided by the "locally of finite type" assumption. Write $V_i\cong Spec(A_i)$. For every $i$, there exists an affine open cover $\{U_{ij}\}_j$ of $V_i$, with $U_{ij} \cong Spec(B_{ij})$, such that $A_i \to B_{ij}$ makes $B_{ij}$ a finite-type $A_i$-algebra.

**First step.** *Find an affine open covering of the preimage of basic open subsets of $V_i$ that satisfy the hypothesis of the "locally of finite type" property.*

Consider $s \in A_i$, and take the basic open sets $D_{V_i}(s) \subseteq V_i$. Each preimage $f^{-1}D_{V_i}(s)$ can be covered by basic open subsets of the $U_{ij}$. For instance, $f^{-1} D_{V_i}(s) \cap U_{ij}$ is an open set of $U_{ij}$, and now use that the basic open sets form a basis for the topology of $U_{ij} \cong Spec(B_{ij})$.

Each such basic open set $D_{U_{ij}}(t)$ has affine coordinate ring $B_{ij,t}$. Since $B_{ij}$ is a finite type $A_i$-algebra, there exists a surjective morphism $A_i[X_1, \dots, X_n] \to B_{ij}$. This can be extended to $A_i[X_1,\dots,X_n,T^{-1}] \to B_{ij,t}$. Hence, $D_{U_{ij}}(t)$ satisfies the desired hypothesis of the "locally of finite type" morphisms.

**Reduction.** *Finding a finer cover, reduce to the case that the $V_i$ are basic open sets. Write $V_i = D(s_i)$.*

**Reduction.** *Step 1 allows us to replace the affine open coverings $\{U_{ij}\}_j$ of $f^{-1} V_i$ by basic open coverings satisfying the same hypothesis. Further, these new coverings are compatible with preimages of basic open subsets of $V_i$.*

**Reduction.** *Refining the new affine open coverings $\{U_{ij}\}_j$ using the same procedure, we can assume that $U$ is covered by a subcover of it. We can now assume that $U = X$, and hence $X = Spec(B)$.*

**Step 2.** *Affine... and hence algebra!*

TODO :)

**qed**

## Affine

Difícil!!! v. [[The Rising Sea]] 7.3.3.

# Stable properties

Let $P$ be some property of morphisms of schemes. We say that it's **stable under base change** if for all fibre product diagrams, if the vertical right arrow has $P$ then the vertical left arrow also has $P$.

Realment hi ha moltes propietats que satisfan (BC), a continuació només en poso algunes (que són les que hem demostrat, i alguna altra). Tota propietat raonable satisfà (BC). No són raonables: aplicació oberta, aplicació tancada, dominant????.

|                        | (BC) | (COMP)      | (CANC)                     | (LOCS) | (LOCT) |
| ---------------------- | ---- | ----------- | -------------------------- | ------ | ------ |
| Open                   |      | X           |                            | X      | X      |
| Closed                 |      | X           |                            |        | X      |
| Universally closed     | X    | X           | if $g$ separated           |        | X      |
| Quasi-compact          | X    | X           | if $g$ **quasi**-separated |        | X      |
| Quasi-finite           | X    | X           | if $g$ **quasi**-separated |        | X      |
| Open immersion         | X    | X           | if $g$ unramified          |        | X      |
| Closed immersion       | X    | X           | if $g$ separated           |        | X      |
| Immersion              | X    | X           | X                          |        | X      |
| Locally of finite type | X    | X           | X                          | X      | X      |
| Of finite type         | X    | X           | if $g$ separated           |        | X      |
| Affine                 | X    | X           | X                          |        | X      |
| Finite                 | X    | X           | if $g$ **quasi**-separated |        | X      |
| Separated              | X    | X           | X                          |        | X      |
| Proper                 | X    | X           | if $g$ separated           |        | X      |
| Projective             | X    | if $g$ qcqs | if $g$ separated           |        |        |
| Monomorphism           | X    | X           | X                          |        | X      |

## Closed immersions (BC)

If $X \to Y$ is a closed immersion, and $Z \to Y$ is any morphism, then $X \times_Y Z \to Y$ is also a closed immersion.

**Achtung!** Estic utilitzant una notació estranya, ja que el producte fibrat l'escrivim com $X \times_Y Z$. És a dir, els esquemes $X$ i $Z$ són sobre $Y$.

*Proof.*

**Step 1.** *Reduction to $X$ and $Y$ affine.*

Let $X \to Y$ be a closed immersion, and cover $Y$ by $\{Spec(A_i)\}_i$. Then $X$ can be covered by $\{Spec(A_i/I_i)\}_i$ (això és per la correspondència ideals <-> subesquemes tancats en el cas afí, v. [[Subschemes]]). Hence it suffices to prove it for affine schemes $X$ and $Y$.

**Step 2.** *Reduction to $Z$ affine.*

Cover $Z$ by affine open charts $\{Z_i\}_i$. Then $X \times_Y Z$ is obtained by glueing $\{X \times_Y Z_i\}_i$ appropriately. If each $X \times_Y Z_i \to Y$ is a closed embedding, the glued $X \times_Y Z \to Y$ will also be a closed embedding.

**Step 3.** *"quotients are preserved by tensor products"*

Consider $Spec(A/I) \to Spec(A)$, and apply base change over $Spec(B) \to Spec(A)$. Then we obtain $Spec(A/I \otimes_A B)$. Since$$A/I \otimes_A B \cong B/IB,$$where $IB$ is "the ideal generated by $I$ and the $B$-action". Hence we obtain a closed immersion. **qed**

## Affine (BC)

If $f: X \to S$ is affine, then $\bar f:X \times_S S' \to S'$ is affine for all base extensions $g:S' \to S$.

*Proof.*

**Step 1.** *Candidat: senzillament prenem les preimatges d'un recobriment distingit proporcionat per l'afinitat.*

Sigui $\{V_i\}_i$ un recobriment per oberts afins de $S$ tal que $f^{-1}V_i$ és afí. Escollim, per cada $i$, un recobriment per oberts afins $\{V_{ij}'\}_j$ de $g^{-1} V_i \subseteq S'$. Cal veure que, per cada $i,j$, l'obert $\bar{f}^{-1} V_{ij}' \subseteq X \times_S S'$ és afí.

**Pas 2.** *Comprovació.*

Per una propietat del producte fibrat que es demostra a l'hora de veure l'existència (v. [[Fibre product]], "existència"), tenim que$$\bar f^{-1} V_{ij}' \cong X \times_S V_{ij}'.$$
Per construcció, com que $gV_{ij}' \subseteq gg^{-1} V_i \subseteq V_i$, tenim que$$X \times_S V_{ij}' \cong X \times_{V_i} V_{ij}' \cong f^{-1} V_i \times_{V_i} V_{ij}'.$$
Aquest és un producte fibrat on només hi apareixen afins així que és afí. Els dos darrers isomorfismes segueixen de la definició de producte fibrat. **qed**

## Finite (BC)

v. https://math.stackexchange.com/questions/1967029/finite-morphism-is-stable-under-base-change

If $f: X \to S$ is finite, then $\bar f:X \times_S S' \to S'$ is finite for all base extensions $g:S' \to S$.

*Demostració.*

**Pas 1.** *Resseguim la demostració que els morfismes afins són preservats per canvi de base.*

Només cal comprovar que el recobriment trobat a la demostració "affine is preserved by base change" satisfà la propietat addicional de finitud, sempre que comencem amb un recobriment amb la propietat de finitiud.

Posem $V_i \cong Spec(A_i)$, $f^{-1} V_i \cong Spec(B_i)$ tal que $A_i \to B_i$ dota $B_i$ d'una estructura de $A_i$-mòdul finit. Posem també $V_{ij}' \cong Spec(B'_{ij})$. Aleshores$$\bar{f}^{-1} V_{ij}' \cong f^{-1} V_i \times_{V_i} V_{ij}' \cong Spec(B_i \otimes_{A_i} B'_{ij}).$$
**Pas 2.** *Veiem que $B_i \otimes_{A_i} B_{ij}'$ és un $B_{ij}'$-mòdul finitament generat.*

Per cada $i$ hi ha morfismes exhaustius $A_i^{\oplus n_i} \to B_i$. Obtenim morfismes $$B_{ij}'^{\oplus n_i} \cong A_i^{\oplus n_i} \otimes_{A_i} B_{ij}' \to B_i \otimes_{A_i} B_{ij}',$$que són exhaustius perquè el ==producte tensorial $-\otimes_{A_i} B_{ij}'$ és exacte per la dreta==. **qed**

## Separated (BC)

## Separated (COMP)

Consider $X \stackrel{f}{\to} Y \stackrel{g}{\to} Z$.

Use the [[Magic square]] for $(f,f)$. Define $X \to X \times_Z X$ by $\Delta_{g \circ f}$, $\Delta_f: X \to X \times_y X$ and $f: X \to Y$. Since we have a pullback diagram, we deduce tha $\Delta_{g \circ f}$ is a closed immersion. **qed**

## Proper (COMP)

Finite type and (univ) closed are closed under composition. Since we've already seen that separated morphisms are closed under composition, we're done.

## Separated (CANC)

If $g \circ f$ is separated, then $f$ is separated.

*Proof.*

***Reduction:*** *It's enough to see that $\Delta_f(X) = \psi^{-1}(\Delta_{g \circ f}(X))$ (we always have the inclusion $\subseteq$).*

*Proof II.*

Use the [[Valuative Criterion]], i.e. that if we have two liftings, then they're the same. Each lifting for the problem with $f$ induces liftings for the problem with $g$ (postcomposing with $g$). We obtain that the initial morphisms are the same. **qed**

## Proper (CANC)

If $g \circ f$ is proper, $g$ is separated and $f$ is quasi-compact, then $f$ is proper.

*Proof.*

We already know that $f$ is separated.

***Step 1:*** *$f$ is of finite type.*

Since $f$ is quasi-compact, it's enough to show that $f$ is locally of finite type. Hence, we can assume everything to be affine. Easy computation (jajan't).

***Step 2:*** *$f$ is universally closed.*

Draw the pullback square for $f': Y' \times_Y X \to Y'$, where $Y' \to Y$, and append $g: Y \to Z$. The $f'$ factors through $Y' \times_Z X$. Draw also this diagram. Since $g \circ f$ is universally closed, we deduce that the second factor in $f': Y' \times_Y X \stackrel{\beta}{\to} Y' \times_Z X \to Y'$ is closed. Hence it suffices to show that $\beta$ is closed.

By the [[Magic square]], since $\Delta_g: Y \to Y \times_X Y$ is a closed immersion (because $g$ is separated), we deduce that $\beta$ is also a closed immersion. **qed**

## Universally closed (CANC)

Use [[Vakil Cancellation Theorem]].

# Traducció de les propietats per morfismes entre esquemes afins

| Propietat              | $f: Spec(A) \to Spec(B)$ esquemes afins (denotem també per $f$ el morfisme $f: B \to A$)                                                                                                                                                                                                                                                                                                  |
| ---------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Open                   |                                                                                                                                                                                                                                                                                                                                                                                           |
| Closed                 | Going-up property (v. [[Going-up theorem]])                                                                                                                                                                                                                                                                                                                                               |
| Universally closed     |                                                                                                                                                                                                                                                                                                                                                                                           |
| Dominant               |                                                                                                                                                                                                                                                                                                                                                                                           |
| Quasi-compact          | $\perp$                                                                                                                                                                                                                                                                                                                                                                                   |
| Quasi-finite           |                                                                                                                                                                                                                                                                                                                                                                                           |
| Open immersion         |                                                                                                                                                                                                                                                                                                                                                                                           |
| Closed immersion       | Es correspon amb $B \to B/I$, per algun ideal $I \subseteq B$ (v. [[Subschemes]]).                                                                                                                                                                                                                                                                                                        |
| Immersion              |                                                                                                                                                                                                                                                                                                                                                                                           |
| Locally of finite type | Recobriment $(b_i)_i = B$, i per cada $i$ recobriment $(a_{ij})_j = A_{fb_i}$, tal que $f: B_{b_i} \to (A_{fb_i})_{a_{ij}}$ dota $(A_{fb_i})_{a_{ij}}$ d'estructura de $B_{b_i}$-àlgebra finita. *En particular, si el recobriment de $B$ és trivial, demanem: recobriment $(a_j)_j$ de $A$ tal que $f: B \to A_{a_j}$ dota $A_{a_j}$ d'estructura de $B$-àlgebra finita (per cada $j$).* |
| Of finite type         | <=> Locally of finite type.                                                                                                                                                                                                                                                                                                                                                               |
| Affine                 | $\perp$                                                                                                                                                                                                                                                                                                                                                                                   |
| Finite                 | Existeix un recobriment $(b_i)_i = B$ tal que, per cada $i$, $f: B_{b_i} \to A_{fb_i}$ indueix una estructura de $B_{b_i}$-mòdul finit en $A_{fb_i}$, i.e. $A_{fb_i} = \sum_{j=1}^{n_i} B_{b_i} \cdot x_{ij}$. *En particular, si el recobriment de $B$ és trivial, demanem: que $f$ indueixi una estructura de $B$-mòdul finit en $A$, i.e. $A = \bigoplus_{j=1}^n B \cdot x_j$.*        |
| Separated              |                                                                                                                                                                                                                                                                                                                                                                                           |
| Proper                 |                                                                                                                                                                                                                                                                                                                                                                                           |

Per $k$ un cos, estudiem els morfismes $f: Spec(A) \to Spec(k)$.

| Propietat              |                                                                                                  |
| ---------------------- | ------------------------------------------------------------------------------------------------ |
| Open                   | $\perp$                                                                                          |
| Closed                 | $\perp$                                                                                          |
| Universally closed     |                                                                                                  |
| Dominant               |                                                                                                  |
| Quasi-compact          |                                                                                                  |
| Quasi-finite           |                                                                                                  |
| Open immersion         |                                                                                                  |
| Closed immersion       |                                                                                                  |
| Immersion              |                                                                                                  |
| Locally of finite type | $A = k[X_1,\dots,X_n]/I$ (i.e. $k$-àlgebra finitament generada)                                  |
| Of finite type         | <=> Locally of finite type                                                                       |
| Affine                 | $\perp$                                                                                          |
| Finite                 | $A = k \cdot X_1 \oplus \cdots \oplus k \cdot X_n$ (i.e. $k$-espai vectorial de dimensió finita) |
| Separated              |                                                                                                  |
| Proper                 |                                                                                                  |

# Suposem Noetherianitat...

## En el domini

Si $f: X \to Y$ és un morfisme amb $X$ Noetherià, automàticament...
- És quasi-compacte.

*Demostració de quasi-compacte.*

Tot obert d'un esquema Noetherià és quasi-compacte. v. [[Algebraic geometry I schemes (llibre)]] Lemma 1.25. **qed**

# Propietats

## Antiimatge de cartes afins per aplicacions afins

**Proposició.** $f: X \to Y$ is affine if, and only if, for every open affine $V \subseteq Y$, $f^{-1} V$ is affine.

(v. dèbil vs fort)

**Corol·lari 1.** If $X \to Spec(A)$ is affine, then $X$ is also affine.

**Corol·lari 2.** $f: X \to Y$ is finite if, and only if, for every affine open $V \subseteq Y$, with $V = Spec(A)$, we have that $f^{-1} Spec(A) = Spec(B)$ and makes $A \to B$ a finite $A$-module.

*Proof Corol·lari 2.*

=>]

It suffices to show that $B$ is finite over $A$. Cover $Y$ with affine charts $Spec(A_i)$ whose preimage is affine $Spec(B_i)$ and such that $B_i$ is finite over $A_i$.

*Proof proposition.*

**Reducció.** *We can reduce to the case that $Y = Spec(A)$.* Això és perquè podem recobrir el codomini per cartes afins.

If we set $B := \Gamma(X,\mathcal{O}_X)$, we have to show that $X = Spec(B)$.

Cover $Y$ with finitely many open affine subsets, $Spec(A) = \bigcup_i Spec(A_i)$, with $A_i =A_{a_i}$. Note that this implies that $(a_i) = A$.

By trick 6 in [[Standard tricks with schemes]], it's enough to show that $X_{a_i} := \{x \in X \mid (b_i)_x \in \mathcal{O}_{X,x}^\times\}$ is affine.

Let $b_i := f^\sharp(a_i)$. It's clear that $Spec(B_{b_i}) \subseteq X_{a_i}$. For the other inclusion, given $x \in X_{a_i}$ with image $y = f(x)$, .... ??? **qed**

## Caracterització de separated morphisms

$f: X \to Y$ is separated if, and only if, $\Delta(X) \subseteq X \times_Y X$ is a closed subset.

*Proof.*

=>] Easy.

<=]

We have to see:
1. The diagonal $\Delta: X \to \Delta(X)$ is a homeomorphism.
2. There map $\mathcal{O}_{X \times_Y X} \to \Delta_X \mathcal{O}_X$ is a surjection.

***First item:*** Use that the composite $X \stackrel{\Delta}{\to} \Delta(X) \subseteq X \times_Y X \to X$ is the identity.

***Second item:*** Local property! Assume $Y = Spec(A)$ and $U = Spec(B) \subseteq X$. Then $U \times_Y U = Spec(B \otimes_A B)$. It follows that the morphism is a surjection. **qed**

## Vakil Cancellation Theorem

v. [[Vakil Cancellation Theorem]]

Consider a property $(P)$ of morphisms of schemes such that:
1. $(P)$ is preserved under composition.
2. $(P)$ is stable under base change.

Then, given two morphisms $X \stackrel{f}{\to} Y \stackrel{g}{\to} Z$ such that $g \circ f$ and $\Delta_g$ have $(P)$, also $f$ has $(P)$.

## Nagata's compactification

v. [[Nagata's compactification]]

Let $f: X \to Y$ be separated and of finite type, with $X$ and $Y$ Noetherian. There exists a factorisation of $X$ as $X \stackrel{h}{\to} Z \stackrel{g}{\to} Y$, with $h$ an open immersion and $g$ proper.

## Valuative Criterion

v. [[Valuative Criterion]]

**Theorem.** Let $X$ be Noetherian, and $f: X \to Y$. Consider the diagrams of the form
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd} {Spec(k)} & X \\ {Spec(\mathcal{O}_\nu)} & Y \arrow[from=1-1, to=1-2] \arrow[hook', from=1-1, to=2-1] \arrow["f", from=1-2, to=2-2] \arrow[dashed, from=2-1, to=1-2] \arrow[from=2-1, to=2-2] \end{tikzcd}
\end{document}
```
where $k$ is a valuation field (v. [[Valuation of a field]]), and $\mathcal{O}_\nu$ is its valuation ring.

1. $f$ is **separated** if, and only if, for every solid diagram as above there exists at most one lift.
2. $f$ is **proper** if, and only if, for every solid diagram as above there exists exactly one lift.

Moreover, if $Y$ is also Noetherian, it suffices to check the diagrams with [[Discrete valuation ring]].

## Projective morphisms into affine schemes

Let $f: X \to Spec(A)$ be projective, with $A$ Noetherian, and $\mathcal{O}_X(1)$ is an $f$-very ample invertible sheaf. Let $\mathcal{F} \in Coh(X)$. There exists $n_0$ such that for every $n \geq n_0$, $\mathcal{F}(U) := \mathcal{F} \otimes \mathcal{O}_X(n)$ is finitely globally generated.

*Proof.*

***Reduction.*** *Reduce everything to projective spaces, i.e. $X = \mathbb{P}^m_A$, $\mathcal{F} \in Coh(\mathbb{P}^m_A)$. Then $\mathcal{F}|_{D_+(x_i)} = \tilde M_i$, $M_i =$ line bundle over $A[x_0/x_i, \dots, x_m/x_i]$, $M_i = H^0(D_+(x_i); \mathcal{F}) = \Gamma_*(\mathcal{F})_{(x_i)}$.*

## Theorem of Serre

**Proposition.** $k$ field, $A$ finite type $k$-algebra, $f: X \to Spec(A)$ projective, $\mathcal{F} \in Coh(X)$. Then $H^0(X;\mathcal{F})$ is a finite $A$-module.

More generally,

**Theorem (Serre).** If $X \to Spec(A)$ is projective, $A$ Noetherian, $\mathcal{O}_X(1)$ is very ample, and $\mathcal{F} \in Coh(X)$, then:
1. For every $j$, $H^j(X;\mathcal{F})$ is a finite $A$-module.
2. There exists some $n_0$ such that for every $n \geq n_0$, $j > 0$, $H^j(X;\mathcal{F}(n)) = 0$.

*Proof (proposition).*

***First step.*** Pick closed embedding $i: X \to \mathbb{P}^m_A$ over $Spec(A)$.

***Reduction*** *Since $H^0(X;\mathcal{F}) = H^+(\mathbb{P}^m_A, i_* \mathcal{F})$, WLOG we can assume $X = \mathbb{P}^m_A$. Now everything takes place in the projective space.*

We know that there exists a surjection $\mathcal{O}(-n)^{\oplus N} \to \mathcal{F}$. It induces a (non necessarily surjective)$$H^+(\mathbb{P}^m_A, \mathcal{O}(-n))^{\oplus N} \to H^0(\mathbb{P}^m_A;\mathcal{F}),$$which in turn induces $M := \Gamma_x(\mathcal{O}(-n)) \to \Gamma_x(\mathcal{F}).$

Define the image of this latter map to be $M'$.

Since $M \to M'$ surjection of graded modules, $\tilde M \to \tilde M'$ surjection. But $M \to \Gamma_x(\mathcal{F})$ factors through $M'$, so $\tilde M \to \tilde{\Gamma_x(\mathcal{F})} \cong \mathcal{F}$ factors through $\tilde M'$. Since $M = \mathcal{O}(-n)^{\oplus N} \to \mathcal{F}$ is surjective, $\tilde M' \to \mathcal{F}$ must also be surjective. Hence, $\tilde M' \cong \mathcal{F}$.

***Reduction.*** *$M$ finite graded $B$-module $\stackrel{?}{\implies}$ $H^0(\mathbb{P}^m;\tilde M)$ is a finite $A$-module.*

***Claim.*** *$H^0(\mathbb{P}^m_A;\tilde M)$ is finite over $A$.*

***Second step.*** *If $M$ is a finite module over $C$, and $C$ Noetherian, then $0 = N_0 \subseteq \cdots \subseteq N_n = N$ such that $N_i/N_{i-1} \simeq C/\mathfrak{p}_i$, with $\mathfrak{p}_i \subseteq C$ prime ideal. The same statement holds for graded $B$-modules, $B$ Noetherian.*

***Reduction.*** *We have to show that $H^0(\mathbb{P}^m_A, \tilde{(B/\mathfrak{p})}(n))$ is a finite $A$-module.*

***Reduction.*** *$B$ graded $A$-module, integral domain, finitely generated by $B_1$, $B_0$ finite type $k$-algebra.*

***Claim.*** *$H^0(Proj(B), \tilde{B(n)})$.*

***Step 3.*** *Pick finitely many nonzero generators $b_1, \dots, b_M \in B_1$ (as $B_0$-module).*

Then $$\mathcal{O}(n) = \tilde{B(n)} \stackrel{\cdot b_i}{\subseteq} \tilde{B(n+1)} \subseteq \cdots,$$so$$H^0(Proj(B), \tilde{B(n)}) \subseteq H^0(Proj(B), \tilde{B(n+1)}) \subseteq \cdots.$$
Since $A$ is Noetherian, it suffices to prove the claim for $n \geq 0$.

Define the graded ring $$B' := \bigoplus_{n \geq 0} H^0(Proj(B), \mathcal{O}(n)).$$
$B$ integral domain, so $B \subseteq Q(B)$. Let $\bar{B} \subseteq Q(B)$ be the integral closure of $B$. We want to show that $B' \subseteq \bar{B}$ is open.

... **qed**

*Sketch (theorem).*

***Step 1.*** [[Grothendieck's theorem]]

***Step 2 - Reduction.*** *$X = \mathbb{P}^m_A$.*

Pick a closed embedding $i: X \to \mathbb{P}^m_A$ over $Spec(A)$ such that $i^*\mathcal{O}(1) = \mathcal{O}_X(1)$. Observe that $i_*(\mathcal{F} \otimes \mathcal{O}_X(n)) \simeq i_*(\mathcal{F} \otimes i^*\mathcal{O}(n)) \simeq i_*(\mathcal{F}) \otimes \mathcal{O}(n)$.

Since $i_*$ is exact, $$H^j(X;\mathcal{F}(n)) \simeq H^j(\mathbb{P}^m; i_*(\mathcal{F}(n))) = H^j(\mathbb{P}^m;(i_*\mathcal{F})(n)).$$
***Step 3 - Reduction.*** *It suffices to show (1) and (2) for $H^j(\mathbb{P}^m_A; \mathcal{O}(n))$. i.e.*
1. *$H^j(...)$ fiinte $A$-module,*
2. *$H^j(...;\mathcal{O}(n)) = 0$ for $n >> 0$, $j > 0$.*

For every $\mathcal{F} \in Coh(\mathbb{P}^m_A)$ there exists$$0 \to \mathcal{F}' = \ker \varphi \to \mathcal{O}(-k)^{\oplus N} \stackrel{\varphi}{\to} \mathcal{F} \to 0$$short exact sequence, so$$H^j(\mathcal{O}(n-k))^{\oplus N} \to H^j(\mathcal{F}(n)) \to H^{j+1}(\mathcal{F}'(n)) \to \cdots.$$
This sequence vanishes at some point by [[Grothendieck's theorem]]. We deduce the reduction.

***Step 4.*** *Cech cohomology computation for $\mathbb{P}^m_A = \bigcup_{i=0}^m D_+(x_i)$.*

We have to show (black boxes! v. [[Algebraic geometry (Hartshorne)]] III.5):
1. $H^0(\mathbb{P}^m;\mathcal{O}(k)) \simeq (A[x_0,\dots,x_m])_0$ (this we already know it)
2. $H^j(\mathbb{P}^m;\mathcal{O}(k)) = 0$ for $0 < j < m$, for every $k$. This is something very special for projective sapces! KIn fact it almost characterizes them.
3. $H^n(\mathbb{P}^m_A;\mathcal{O}(-m-1)) \simeq A$. This is related to [[Serre duality]], which is the geometric version of [[Dualitat de Poincaré]].

**qed**

# Relació entre les propietats

![[WhatsApp Image 2024-12-05 at 16.25.43.jpeg]]

## Finite => Closed

*Proof.*

***First step.*** Suppose that $X = Spec(B) \stackrel{f}{\to} Y = Spec(A)$.

The associated morphism $\varphi:A \to B$ is finite (i.e. $B$ is a finite $A$-module). Factor it as $A \to A/ker \varphi \to B$. The second arrow is still finite, and $Spec(A/ker \varphi) = V(\ker \varphi) \subseteq Spec(A)$ closed subscheme. Hence we can reduce to showing that $Spec(B) \to V(ker(\varphi))$ is closed. This follows precisely from the [[Going-up theorem]].

***Second step.*** $f: X \to Y$ with $Y$ covered by $Spec(A_i)$, and $f^{-1} Spec(A_i) = Spec(B_i)$ with $B_i$ finite over $A_i$.

Topologia general: $Z \subseteq Y$ is closed iff $Y \setminus Z$ open iff $Spec(A_i) \setminus Z$ open for all $i$ iff $Z \cap Spec(A_i) \subseteq Spec(A_i)$ closed for all $i$.

Apply this to $Z = f(X)$, and then use the first step. **qed**

## Finite => Quasi-finite

*Proof.*

$f^{-1} Spec(A) = Spec(B)$.

The fibre is $f^{-1}(x) = \{\mathfrak{q} \subseteq B \mid \mathfrak{q}^c = \mathfrak{p}\}$, which is identified with $Spec(k(\mathfrak{p}) \otimes_A B)$.

Since $B$ is finite over $A$, $k(\mathfrak{p}) \otimes_A B$ is a finite-dimensional $k(\mathfrak{p})$-vector space. Since it's Artinian & Noetherian, Attiyah-MacDonald shows that its Spec is finite. **qed**

## Affine => Separated
## Finite => Proper

Finite => Affine => Separated.

Finite => Finite type.

Finite => Closed. & finite is stable under base change. From this conjunction we deduce universally closed. **qed**

## Projective => Proper

*Proof.*

***Reduction.*** *It suffices to show that $\mathbb{P}^m_\mathbb{Z} \to Spec(\mathbb{Z})$ is proper.* (using the properties of proper morphisms)

***Step 1.*** *Take a cover $\mathbb{P}^m_\mathbb{Z} = \bigcup_i D_+(x_i)$.*

***Step 2.*** *Induction, using that $\mathbb{P}^m_\mathbb{Z} \setminus D_+(x_1) = \mathbb{P}^{m-1}_\mathbb{Z}$*.

***WLOG.*** $\bar \eta \in \bigcap_i D_+(x_i)$.

## Finite <=> Quasi-finite & Proper

$f$ is finite if, and only if, $f$ is quasi-finite and proper.

## Closed immersion => Affine

Consider a closed embedding $f: X \to Y$. Take an affine open cover $\{U_i\}_i$ of $Y$, $U_i \cong Spec(A_i)$. Then $f^{-1} U_i \to U_i$ is still a closed embedding. It corresponds to an ideal $\mathfrak{a}_i \subseteq A_i$, i.e. $f^{-1} U_i \cong Spec(A_i/\mathfrak{a}_i)$ (v. [[Subschemes]] "correspondència"). **qed**

## Closed immersion => Proper

Closed immersion => Affine => Separated.

Closed immersion => Universally closed because closed immersions are closed and stable under base change.

Closed immersion => Finite type: take an affine open cover $\{Spec(A_i)\}_i$ of $Y$. Each preimage is isomorphic to $Spec(A_i/I_i)$. Each $A_i/I_i$ is clearly a finite-type $A_i$-algebra. **qed**

## Finite type => Quasicompact

Utilitzem la definició dèbil de quasicompacitat, és a dir, volem veure que existeix un recobriment per afins $\{V_i\}_i$ de $Y$ tal que $f^{-1} V_i$ és quasicompacte.

Com que $f$ és de tipus finit, existeix un recobriment per afins $\{V_i\}_i$ de $Y$ tal que $f^{-1} V_i$ es pot recobrir per un nombre finit d'afins $\{U_{ij}\}_{j=1}^{n_i}$ (que satisfan certes propietats addicionals). Prenem aquests recobriments. Aleshores$$f^{-1} V_i = \bigcup_{j=1}^{n_i} U_{ij}.$$
Com que els $U_{ij}$ són afins, són quasicompacte. Com que $f^{-1} V_i$ és la unió finita de quasicompactes, és quasicompacte. **qed**

## Finite type <=> Locally of finite type & Quasicompact

Finite type => Locally of finite type (per definició)

Finite type => Quasicompact (vist abans)

Queda veure la implicació <=.

Si tenim el reocbriment per afins $\{V_i\}_i$ de $Y$ tal que $f^{-1} V_i$ està recobert per afins $\{U_{ij}\}_j$ tal que blah blah blah, la quasicompactitat implica que es pot trobar un subrecobriment finit de $\{U_{ij}\}_j$. Això és precisament finite type. **qed**

## Monomorphism => Separated

Si $f$ és un monomorfisme aleshores $\Delta_f: X \to X \times_Y X$ és un isomorfisme (?). Això implica que, en particular, és un closed embedding. **qed**

# Exemples

COnsider the morphism of schemes $X = \mathbb{A}^1_k \setminus \{0\} \to Y = \mathbb{A}^2_k$ induced by$$k[X_1,X_2] \to k[X,X^{-1}],\quad X_1 \mapsto X,\ X_2 \mapsto 0$$is an immersion.

## Morphism between affine schemes

Every $f: Spec(A) \to Spec(B)$ is separated.

## Affine line

The affine line **is not proper!** Instead one uses the projective line.

## Quasifinite & Separated & Finite type & Surjective =/> Proper

Take the punctured affine line disjoint union affine line. Project to the affine line. It satisfies the conditions described above, but it's not proper because if we take the punctured line (as a closed subset of the disjoint union), its image is not closed.

## Taula amb exemples

| #   | Exemple                                                                                                | Open | Closed | Universally closed                                | Dominant | Quasicompact | Quasifinite | Open immersion | Closed immersion | Immersion | Locally of finite type | Of finite type | Affine | Finite | Separated | Proper |
| --- | ------------------------------------------------------------------------------------------------------ | ---- | ------ | ------------------------------------------------- | -------- | ------------ | ----------- | -------------- | ---------------- | --------- | ---------------------- | -------------- | ------ | ------ | --------- | ------ |
| 1   | $V(X^3-Y^2) \subseteq \mathbb{A}^2_\mathbb{C}$                                                         | No   | *Sí*   | *Sí*                                              | No       | Sí           | Sí          | No             | ==Sí==           | *Sí*      | Sí                     | Sí             | Sí     | *Sí*   | Sí (1)    | Sí     |
| 2   | $V(XY-1) \subseteq \mathbb{A}^2_\mathbb{C} \stackrel{\pi_1}{\to} \mathbb{A}^1_\mathbb{C}$              | Sí   | No     | No                                                | Sí       | Sí           | Sí          | Sí             | No               | *Sí*      | Sí                     | Sí             | Sí     | *No*   | Sí (1)    | No     |
| 3   | $\mathbb{P}^n_\mathbb{Z} \to Spec(\mathbb{Z})$                                                         |      |        | Sí (v. [[The red book of varieties and schemes]]) |          |              |             |                |                  |           |                        |                |        |        |           |        |
| 4   | $\mathbb{A}^1_\mathbb{C} \to Spec(\mathbb{C})$                                                         | Sí   | Sí     | No (2)                                            | Sí       | Sí           | No          | No             | No               | No        | Sí                     | Sí             | Sí     | *No*   | No (1)    | No (1) |
| 5   | line two origins $\to \mathbb{A}^1_\mathbb{C}$                                                         | Sí   | Sí     | *No*                                              | Sí       | Sí           | Sí          | No             | No               | No        | Sí                     | Sí             | No     | *No*   | Sí (1)    | No (1) |
| 6   | $\mathbb{A}^1_\mathbb{C} \sqcup (\mathbb{A}^1_\mathbb{C} \setminus \{0\}) \to \mathbb{A}^1_\mathbb{C}$ | Sí   | No (1) | *No*                                              | Sí       | Sí           | Sí          | No             | No               | No        | *Sí*                   | Sí             | Sí     | No     | *Sí*      | *No*   |
| 7   | $Spec(\mathbb{Q}) \to Spec(\mathbb{Z})$                                                                |      |        |                                                   |          |              |             |                |                  |           | No (1)                 | *No*           |        | *No*   |           | *No*   |

### Exemple 1

(1) Aquí utilitzem que $V(X^3-Y^2) \cong Spec(\mathbb{C}[X,Y]/(X^3-Y^2))$, i que $$\mathbb{C}[X,Y]/(X^3-Y^2) \otimes_{\mathbb{C}[X,Y]} \mathbb{C}[X,Y]/(X^3-Y^2) \cong \mathbb{C}[X,Y]/(X^3-Y^2).$$
De fet, segueix del fet que és una closed immersion.

### Exemple 2

(1) Aquí utilitzem que$$\mathbb{C}[X,Y]/(XY-1) \otimes_{\mathbb{C}[X]} \mathbb{C}[X,Y]/(XY-1) \cong \mathbb{C}[X,Y,Z]/(XY-1,XZ-1) \cong \mathbb{C}[X,Y]/(XY-1),$$on el darrer isomorfisme segueix de $Y = Y(XZ) = Z(XY) = Z$.

### Exemple 4

(1) Veure [[Valuative Criterion]]

(2) Take the fibred product $\mathbb{A}^2_\mathbb{C} = \mathbb{A}^1_\mathbb{C} \times_\mathbb{C} \mathbb{A}^1_\mathbb{C}$. The projection $\mathbb{A}^2_\mathbb{C} \to \mathbb{A}^1_\mathbb{C}$ is not closed because the image of the hyperbola $V(XY-1) \subseteq \mathbb{A}^1_\mathbb{C}$ is not closed in $\mathbb{A}^1_\mathbb{C}$.

### Exemple 5

(1) Veure [[Valuative Criterion]]

### Exemple 6

(1) La imatge del tancat $\mathbb{A}^1_\mathbb{C} \setminus \{0\} \subseteq \mathbb{A}^1_\mathbb{C} \sqcup (\mathbb{A}^1_\mathbb{C} \setminus \{0\})$ (dins de la segona component) no és tancada en $\mathbb{A}^1_\mathbb{C}$.

### Exemple 7

(1) Considerem un recobriment $(n_i)_i = \mathbb{Z}$ de $Spec(\mathbb{Z})$. Cal trobar, per cada $i$, un recobriment de $\mathbb{Q}[\frac{1}{n_i}] = \mathbb{Q}$. Per la naturalesa dels ideals de $\mathbb{Q}$, aquest recobriment ha de ser forçosament $(1) = \mathbb{Q}$. El morfisme $\mathbb{Z}[\frac{1}{n_i}] \to \mathbb{Q}$ dota $\mathbb{Q}$ d'una estructura de $\mathbb{Z}[\frac{1}{n_i}]$-àlgebra, però aquesta **no** és finitament generada. Això és perquè en $\mathbb{Z}[\frac{1}{n_i}]$ invertim un nombre finit de primers, mentre que en $\mathbb{Q}$ els invertim tots (infinits).