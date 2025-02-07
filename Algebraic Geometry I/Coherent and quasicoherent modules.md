Let $(X,\mathcal{O}_X)$ be a ringed space. A $\mathcal{O}_X$-module $\mathcal{F}$ is called:
- **Quasi-coherent** if locally $\mathcal{F}$ is a quotient of free sheaves, i.e. for every $x \in X$ there exists an open neighbourhood $U \ni x$ such that $\mathcal{O}_U^{\oplus I} \to \mathcal{O}_U^{\oplus J} \to \mathcal{F}|_U \to 0$ is exact. Here the sets $I$ and $J$ needn't be finite!
- **Coherent** if a) **finite type:** for every $x \in X$ there exists an open neighbourhood $U \ni x$ such that $\mathcal{O}^{\oplus n}_U \to \mathcal{F}|_U$ is surjective, and b) **every $\mathcal{O}^{\oplus n}_V \to \mathcal{F}|_V$ has locally finitely generated kernel:** for every open set $V \subseteq X$ and every $\varphi: \mathcal{O}_V^{\oplus n} \to \mathcal{F}|_V$, the kernel $ker(\varphi)$ is locally finitely generated, i.e. for every $x \in V$ there exists $x \in U \subseteq V$ open such that $\mathcal{O}^{\oplus m}_U \to ker(\varphi)|_U$ is surjecitve.

Note that coherent => quasi-coherent.

We define the full subcategories $Coh(X,\mathcal{O}_X) \subseteq QCoh(X,\mathcal{O}_X) \subseteq Mod(X,\mathcal{O}_X)$. Note that $Coh(X,\mathcal{O}_X)$ is an abelian category, while $QCoh(X)$ is abelian when $(X,\mathcal{O}_X)$ is a scheme. v. [[Categoria abeliana]]

# Propietats

## Coherent and quasicoherent sheaves over schemes

If the base locally ringed spaces is a **scheme** (v. [[Scheme]]), then the definitions of coherent and quasi-coherent $\mathcal{O}_X$-modules simplify. Fix $(X,\mathcal{O}_X)$ a scheme.

An $\mathcal{O}_X$-module $\mathcal{F}$ is **quasi-coherent** if, and only if, there exists an affine open covering $\{U_i\}_i$ of $X$, with $U_i \cong Spec(A_i)$, such that $\mathcal{F}|_{U_i} \cong \tilde{M_i}$ for some $A_i$-module $M_i$. (v. [[From modules to (quasi-coherent) sheaves of modules]])

An $\mathcal{O}_X$-module $\mathcal{F}$ is **coherent** if, and only if, there exists an open covering satisfying the previous properties, and moreover the $M_i$ can be taken to be finitely generated (as $A_i$-modules).

## Principis de prolongació (analítica)

### Esquemes afins

Let $X = Spec(A)$ be an affine scheme, and let $\mathcal{F}$ be a quasi-coherent sheaf on $X$.
1. If $s$ is a global section of $\mathcal{F}$ that vanishes on some $D(f)$, then there exists some $n > 0$ such that $f^n s = 0$.
2. For every section $t$ of $\mathcal{F}$ on $D(f)$ there exists some $n > 0$ such that $f^n t$ extends to a global section of $\mathcal{F}$.

v. [[Algebraic geometry (Hartshorne)]] Lemma II.5.3.

*Interpretació.*

Comencem amb el cas que l'esquema és integral (v. [[Scheme]]), és a dir, que $A$ és un domini d'integritat. Podem interpretar (1) com una espècie de **principi de prolongació analítica**, ja que és equivalent a: "si dues seccions globals coincideixen en un obert bàsic, aleshores són la mateixa". La condició (2) diu que tota secció local estén a una de global.

El cas general bàsicament afegeix la correcció que s'ha de tenir en compte quan no es parla de coses integrals: afegir potències. Reemplacem *"són la mateixa"* per *"són la mateixa llevat d'una potència de $f$"*, i *"s'anul·la"* per *"s'anul·la llevat d'una potència de $f$"*.

*Demostració (1).*

Com que mòduls quasi-coherents sobre $Spec(A)$ <-> $A$-mòduls (v. [[From modules to (quasi-coherent) sheaves of modules]]) per mitjà del functor $\widetilde{(-)}$, obtenim un problema purament algebraic: *If $s \in M$ is zero in the localization $M_f$, then $f^n s = 0$.* Aquesta és precisament la definició de localització. **qed**

*Demostració (2).*

Com abans, obtenim un problema algebraic: *For every $t \in M_f$ there exists some $n > 0$ and some $\tilde t \in M$ such that $\tilde t = f^n t$ in $M_f$.*

Considerem $t \in M_f$. Per la definició de $M_f$, existeix alguna $n>0$ tal que $f^n t \in M \subseteq M_f$. Prenem $\tilde t := f^n t$. **qed**

*Comentari sobre la demostració d'en Hartshorne.*

La demostració donada a [[Algebraic geometry (Hartshorne)]] II.5.3 és molt més enravessada, ja que es prenen recobriments i tota la pesca. Però em dona la sensació que la demostració que he escrit aquí és suficient. És possible que la seva complicació es degui al fet que utilitza una definició diferent de mòdul quasi-coherent.

### Esquemes generals

Sigui $X$ un esquema i $\mathcal{F}$ un feix quasi-coherent en $X$. For $f \in \Gamma(X,\mathcal{O}_X)$, denote $X_f := \{x \mid f_x \notin \mathfrak{m}_x\}$. ==Suppose that $X$ is quasi-compact.==
1. If $s$ is a global section of $\mathcal{F}$ that vanishes on some $X_f$, then there exists some $n > 0$ such that $f^n s = 0$.
2. For every section $t$ of $\mathcal{F}$ on $X_f$ there exists some $n > 0$ such that $f^n t$ extends to a global section of $\mathcal{F}$.

Però encara més general...

### Coefficients (?) on an invertible line bundle

Sigui $X$ un esquema, $\mathcal{L}$ un feix invertible en $X$ (v. [[Sheaf of modules]]) i $\mathcal{F}$ un feix quasi-coherent en $X$. For $f \in \Gamma(X,\mathcal{L})$, denote $X_f := \{x \mid f_x \notin \mathfrak{m}_x \mathcal{L}_x \}$. ==Suppose that $X$ is quasi-compact.==
1. If $s$ is a global section of $\mathcal{F}$ that vanishes on some $X_f$, then $f^n s \in \Gamma(X,\mathcal{F} \otimes \mathcal{L}^{\otimes n})$ vanishes for some $n > 0$.
2. ==Suppose that $X$ has a finite covering by affine open sets $U_i$ such that $\mathcal{L}|_{U_i}$ is free for all $i$, and such that $U_i \cap U_j$ is quasi-compact for all $i,j$.== For every section $t$ of $\mathcal{F}$ on $X_f$ there exists some $n > 0$ such that $f^n t \in \Gamma(X_f, \mathcal{F} \otimes \mathcal{L}^{\otimes n})$ extends to a global section of $\mathcal{F} \otimes \mathcal{L}^{\otimes n}$.

v. [[Algebraic geometry (Hartshorne)]] II.5.14.

*Proof (1).*

**Step 1.** *Wise covering: open affine sets such that the restriction of $\mathcal{L}$ is free.*

Since $X$ is quasi-compact, we can find a finite covering by open affine subsets such that the restriction of $\mathcal{L}$ to each of these open sets is free. In each of these open sets we can express the restriction of $\mathcal{F}$ using the functor $\widetilde{(-)}$ (v. [[From modules to (quasi-coherent) sheaves of modules]]).

**Step 2.** *Work locally.*

It suffices to show the statement for every open set of the covering (because the open cover is finite, and the we'll take $n$ to be the maximum of the local $n$'s).

***Step 2.1.*** *Local setup.*

Fix an open set $U \cong Spec(A)$ of the covering. The restriction of $\mathcal{L}$ on $U$ is isomorphic (as an $A$-module, and under the correspondence $\widetilde{(-)}$) to $A$, and the restriction $f|_U$ corresponds to some section $g \in A \cong \mathcal{L}(U)$. The intersection of $X_f$ with $U$ corresponds to$$X_f \cap U = \{ x \in U \mid f_x \notin \mathfrak{m}_x \mathcal{L}_x \} \cong \{x \in U \mid g_x \notin \mathfrak{m}_x A_x\} = D(g) \subseteq Spec(A) \cong U.$$
The restriction $\mathcal{F}|_U$ corresponds to an $A$-module $M$. The global section $s$ of $\mathcal{F}$ corresponds to an element $s \in M$.

***Step 2.2.*** *Use the analogous result in the affine setting.*

We now use the result in the affine setting. Since $s$ vanishes on $X_f \cap U = D(g)$, there exists some $n > 0$ such that $g^n s = 0$. By the definition of $g$, this is the same as saying that the section $f^n s \in \Gamma(U, \mathcal{F} \otimes \mathcal{L}^{\otimes n})$ vanishes for some $n > 0$. **qed**

## Direct & inverse image of (quasi)coherent sheaves

*Outlook.* We study how (quasi)coherentness is preserved by the direct & inverse image functors.

In the **affine world**,

|                | Direct image $f_*$                                | Inverse image $f^*$ |
| -------------- | ------------------------------------------------- | ------------------- |
| Quasi-coherent | :)                                                | :)                  |
| Coherent       | v. "direct image of coherent needn't be coherent" | :)                  |

In the **general setting**,

|                | **Direct image $f_*$**                            | **Inverse image $f^*$**          |
| -------------- | ------------------------------------------------- | -------------------------------- |
| Quasi-coherent | :), if Noetherian domain                          | :)                               |
| Coherent       | v. "direct image of coherent needn't be coherent" | :), if locally Noetherian domain |

*Proof method:* ==REDUCE TO AFFINE==.

### Affine world

> [!quote] Direct image preserves quasi-coherent, inverse image preserves coherent & quasi-coherent

Let $\varphi: A \to B$, and consider the associated $f: X = Spec(B) \to Spec(A) = Y$. Then:
1. If $\mathcal{F} \in QCoh(X)$, then $f_* \mathcal{F} \in QCoh(Y)$.
2. If $\mathcal{G} \in QCoh(Y)$, then $f^* \mathcal{G} \in QCoh(X)$.
3. If $\mathcal{G} \in Coh(Y)$, then $f^* \mathcal{G} \in Coh(X)$.

v. [[From modules to (quasi-coherent) sheaves of modules]]

*Proof (1).* Això és perquè la imatge directa es correspon, sota l'equivalència de categories $\widetilde{(-)}$, amb la restricció d'escalars (v. [[From modules to (quasi-coherent) sheaves of modules]]). **qed**

*Proof (2).* Això segueix del fet que la imatge inversa es correspon amb l'estensió d'escalars (v. [[From modules to (quasi-coherent) sheaves of modules]]). **qed**

*Proof (3).* We traduce the statement with the equivalence $\widetilde{(-)}$. Suppose that $M$ is a finitely generated $A$-module. Then there exists an exact sequence of $A$-modules$$0 \to I \to A^{\oplus n} \to M \to 0.$$
Since $(-)\otimes_A B$ is right exact, it produces an exact sequence$$I \otimes_A B \to B^{\oplus m} \to M \otimes_A B \to 0.$$
We deduce that $M \otimes_A B$ is a finitely generated $B$-module. **qed**

### General setting!

>[!quote] Under some Noehterianity conditions on the domain: direct image preserves quasi-coherent, inverse image preserves coherent & quasi-coherent.

Let $f: X \to Y$ be a morphism of schemes.
1. **Inverse image preserves QCoh:** If $\mathcal{G} \in QCoh(Y)$, then $f^* \mathcal{G} \in QCoh(X)$.
2. **Inverse image preserves Coh (if locally Noetherian domain):** If $\mathcal{F}  \in Coh(Y)$ and $X$ locally Noetherian, then $f^* \mathcal{G} \in Coh(X)$.
3. **Direct image preserves QCoh (if Noetherian domain):** If $\mathcal{F} \in QCoh(X)$ and $X$ Noetherian, then $f_*\mathcal{F} \in QCoh(Y)$.

v. [[Scheme]]

**Warning!** For $\mathcal{F}$ a coherent sheaf on $X$, its direct image $f_* \mathcal{F}$ is only coherent (in general) if $f$ is proper (deep result!). v. exemple "Direct image of coherent needn't be coherent"

*Proof (1).*

***Idea:*** Reduce to affine: "quasi-coherent" is a local property. **qed**

*Proof (2).*

***Idea:*** Reduce to affine. Deduce that $f_{ij}^*(\mathcal{G}|_{Spec(A_i)})$ is coherent (because the inverse image of a coherent sheaf of modules on an affine open is still coherent), and then use local Noetherianity. **qed**

*Proof (3).*

***Idea:*** WLOG $Y = Spec(A)$ and $X = \bigcup_{i=1}^k Spec(B_i)$ (finite cover because of Noetherianity).

Cover the intersection $U_{ij}$ by finitely many open affines.

The sheaf property (v. [[Sheaf]]) gives$$0 \to \mathcal{F} \stackrel{restr.}{\longrightarrow} \bigoplus \mathcal{F}|_{U_i} \to \bigoplus \mathcal{F}|_{U_{ij}}$$exact (hi ha un abús de notació, falta la imatge directa!).

Apply the left exact functor $f_*$. The two terms on the right are quasi-coherent. We deduce that $f_* \mathcal{F}$ is quasi-coherent. **qed**

### Finite morphism between Noetherian schemes

If $f: X \to Y$ is a finite morphism between Noetherian schemes, then $f_*(Coh) = Coh$.

v. [[Morphisms of schemes]]

v. [[Hartshorne]] II Ex. 5.5.

*Proof.*

Consider $U = Spec(A)$ open in $Y$ such that $f^{-1}(U) = Spec(B)$ making $B$ a finite $A$-module.

Since $\mathcal{F}$ is coherent, $\mathcal{F}|_{f^{-1}(U)} = \widetilde{M}$ for some finitely generated $B$-module $M$. Hence, $f_* \mathcal{F}|_U = \widetilde{{}_AM}$, which is finitely generated as an $A$-module. **qed**

A on estic utilitzant la **noetherianitat** ????????

## Global sections of quasicoherent sheaves on projective schemes

v. [[Proj]] "global sections"

## Quasi-coherent sheaves live inside flabby & quasicoherent sheaves

Let $X$ be a ==Noetherian== scheme, and $\mathcal{F} \in QCoh(X)$. There exists an injective $\mathcal{F} \to \mathcal{I}$, with $\mathcal{I}$ quasi-coherent and flabby.

*Proof.*

**Step 1.** *Locally.*

Consider a finite covering $\{Spec(A_i)\}_{i=1,\dots,n}$ with each $A_i$ Noetherian. Let $\widetilde{M_i} := \mathcal{F}|_{Spec(A_i)}$. Since there are enough injectives, there exists a monomorphism $M_i \to I_i$ with $I_i$ injective $A_i$-module. These define $\widetilde{I_i}$ injective sheaves on $Spec(A_i)$, which are quasi-coherent and **flabby**.

**Step 2.** *Globally: take direct sums of the pushed forward sheaves.*

Consider the global sheaf $\bigoplus_{i=1,\dots,n} (\iota_i)_*(\widetilde{I_i})$, where $\iota_i: Spec(A_i) \subseteq X$ is the inclusion.

- $\widetilde I_i$ quasi-coherent => $(\iota_i)_*(\widetilde{I_i})$ quasi-coherent, because it's a direct image (and we're assuming $Spec(A_i)$ Noetherian) => $\bigoplus_i (\iota_i)_*(\widetilde{I_i})$ quasi-coherent.
- $\widetilde{I_i}$ flabby => $(\iota_i)_*(\widetilde{I_i})$ flabby => $\bigoplus_i (\iota_i)_*(\widetilde{I_i})$ flabby.
- Injectivity of $\mathcal{F} \to \bigoplus_i (\iota_i)_* (\widetilde{I_i})$: clear (it can be checked at the stalks, for example).

**qed**

## (Cech) cohomology of quasi-coherent sheaves

Let $X$ be a separated scheme, and $\{U_i\}_i$ an affine open cover. The induced map$$CH^i(\{U_i\}_i,\mathcal{F}) \to H^i(X,\mathcal{F})$$is bijective for $\mathcal{F}$ quasi-coherent.

v. [[Cohomologia de Cech]], v. [[Algebraic geometry (Hartshorne)]] III.4.5.

*Proof.*

$X$ separated => $U_{i_1,\dots, i_j}$ affine.

This implies (and also the fact that $\mathcal{F}$ is quasi-coherented) that $H^*(U_{i_1,\dots,i_j},\mathcal{F}) = 0$ for all $i>0$.

We deduce the bijection from a property of Cech cohomology. **qed**

## Kernel, cokernel and image (abelian categories?)

Let $X$ be a scheme, and let $f: \mathcal{F} \to \mathcal{G}$ be a morphism of $\mathcal{O}_X$-modules.
1. If $\mathcal{F}$ and $\mathcal{G}$ are **quasi-coherent**, them $ker(f)$, $coker(f)$ and $im(f)$ are also **quasi-coherent**.
2. If $\mathcal{F}$ and $\mathcal{G}$ are **coherent** and $X$ is **Noetherian**, then $ker(f)$, $coker(f)$ and $im(f)$ are also **coherent**.

v. [[Algebraic geometry (Hartshorne)]] II.5.7.

## Ideals in quasi-coherent sheaves

Let $Y$ be a scheme. The following are in bijection:
- $\mathcal{V}  \subseteq \mathcal{O}_Y$ sheaf of ideals $\mathcal{V} \in QCoh(Y)$.
- $X \subseteq Y$ closed subscheme.

*Proof.*

<-] Given a closed subscheme $i: X \subseteq Y$, we assign to it the kernel of $i^\sharp: \mathcal{O}_Y \to i_* \mathcal{O}_X$. **Well-defined:**
- One can see that $i_* \mathcal{O}_X$ produces a quasi-coherent sheaf (for this one has to use the fact that $i$ is a closed immersion).
- We deduce that the kernel is also quasi-coherent.

->] Given $\mathcal{V}$, define$$X := supp(\mathcal{O}_Y/\mathcal{V}),\quad \mathcal{O}_X := restriction?.$$
# Exemples

## Direct image of coherent needn't be coherent

Consider the unique $\mathbb{A}^1_k \to Spec(k)$, which is induced by the inclusion $k \to k[X]$. Consider the structure sheaf on $\mathbb{A}^1_k$ as a sheaf of modules. It's the associated sheaf of modules to the trivial $k[X]$-module $k[X]$ (v. [[From modules to (quasi-coherent) sheaves of modules]]). Its direct image (v. [[From modules to (quasi-coherent) sheaves of modules]] for the computation of the direct image of a contraction) is the sheaf of modules associated to $k[X]$ with $k$-module structure $k \to k[X]$.

It's clear that the first sheaf of modules is coherent (because $k[X]$ is a finitely generated $k[X]$-module, v. Coherent and quasicoherent sheaves over schemes), but the second one is **not** coherent (because $k[X]$ is no longer finitely generated as a $k$-module).

## A sheaf that is not quasi-coherent

In $\mathbb{A}^2_k$, the skyscraper sheaf is not quasi-coherent.