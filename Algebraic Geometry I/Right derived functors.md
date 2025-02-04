Assume $F: \mathcal{A} \to \mathcal{B}$ is an additive, left exact functor, and suppsoe that $\mathcal{A}$ has enough injectives (v. [[Enough injectives]]). Define$$R^i F(A) := \frac{ker(FI_i \to FI_{i+1})}{im(FI_{i-1} \to FI_i)},$$where $A \to I_\bullet$ is an injective resolution of $A$.

Donada $0 \to A' \to A \to A'' \to 0$ successió exacta curta, hi ha morfismes $\delta^i: R^i F(A'') \to R^{i+1}F(A')$ que doten $R^iF$ d'estructura de $\delta$-functor. v. [[delta-Functor]], *Definció dels connecting homomorphisms*.

**Theorem (Grothendieck).** $(R^i F, \delta^i)$ is a **universal** $\delta$-functor with $R^0F = F$.

## Definició dels connecting homomorphisms

Sigui $0 \to A' \to A \to A'' \to 0$ una successió exacta curta.

***Pas 1.*** *Construïm resolucions injectives $A' \to I_\bullet$, $A \to J_\bullet$, $A'' \to K_\bullet$ tals que $0 \to I_i \to J_i \to K_i \to 0$ és una successió exacta curta per cada $i$.*

De fet, gràcies a la inducció només ens cal mostrar com es construeix una fila a partir de l'anterior.

Escollim $I_0$ i $K_0'$ arbitraris. Hi ha un monomorfisme de $I_0 \sqcup_{A'} A$ a algun $J_0'$ injectiu, ja que estem suposant que hi ha [[Enough injectives]]. Es defineix $J_0 := J_0' \oplus K_0'$, i es pren $K_0$ el cokernel de $I_0 \to J_0$. *Algo així...*

**Pregunta:** Llavors aquí podria prendre $K_0' := 0$ ???

Es procedeix inductivament.

***Observació.*** Com que cada fila $0 \to I_i \to J_i \to K_i \to 0$ és exacta, i els seus elements són injectius, es té que $J_i = I_i \oplus K_i$ (splits... v. [[Mòdul injectiu]]). En particular $FJ_i \to FK_i$ és exhaustiu.

Tenim:$$R^i FA'' = H^i(FK_\bullet) = \frac{ker(FK_i \to FK_{i+1})}{im(FK_{i-1} \to FK_i)}.$$
***Step 2.*** *Construcció del connecting homomorphism per mitjà d'un diagram chase.*

Given $[a] \in R^i FA''$, one produces an element $b \in FI_{i+1}$ that represents a cohomology class in $R^{i+1} FA'$ by performing a diagram chase in the following diagram:
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[ampersand replacement=\&] \&\&\& {FK_{i-1}} \\ 0 \& {FI_i} \& {FJ_i} \& {FK_i} \\ 0 \& {FI_{i+1}} \& {FJ_{i+1}} \& {FK_{i+1}} \\ \& {FI_{i+2}} \& {FJ_{i+2}} \arrow[from=1-4, to=2-4] \arrow[from=2-1, to=2-2] \arrow[from=2-2, to=2-3] \arrow[from=2-2, to=3-2] \arrow[from=2-3, to=2-4] \arrow[from=2-3, to=3-3] \arrow[from=2-4, to=3-4] \arrow[from=3-1, to=3-2] \arrow[from=3-2, to=3-3] \arrow[from=3-2, to=4-2] \arrow[from=3-3, to=3-4] \arrow[from=3-3, to=4-3] \arrow[from=4-2, to=4-3] \end{tikzcd}
\end{document}
```

# Propietats

## Acyclycity is enough

If $A \to I_\bullet$ is an $F$-acyclic resolution of $A$, then$$R^iF(A) \cong H^i(FI_0 \to FI_1 \to \cdots).$$
*Proof.*

***Cas fàcil.*** Assume $0 \to A \to I_0 \to I_1 \to 0$ is an $F$-acyclic resolution of $A$.

We have an exact sequence$$0 \to FA \to FI_0 \stackrel{\varphi}{\to} FI_1 \to R^1 FA \to R^1FI_0 = 0,$$where the last entry is exact because of acyclicity. Then$$R^1FA = coker(\varphi) = H^1(FI_0 \to FI_1),\quad FA = ker(\varphi) = H^0(FI_0 \to FI_1).$$
***Cas general.*** Trenquem la successió exacta llarga en successions exactes curtes?

**qed**

## Value at degree $0$

$R^0F(A) \cong F(A)$,

## Independence of choice

*Demo.* Donades dues resolucions injectives, podem construir un morfisme de resolucions $f: (A \to I_\bullet) \to (A \to J_\bullet)$ que estengui la identitat en $A$. Indueix un morfisme de successions $F(f): F(I_\bullet) \to F(J_\bullet)$, i també indueix $H^i(FI_\bullet) \to H^i(FJ_\bullet)$ per cada $i$. Aquests morfismes naturals són isomorfismes. **qed**

## Value at injectives (flasque)

In particular, if $A = I$ is injective, taking the injective resolution $0 \to A \to I \to 0$ yields $R^iF(A) =  0$ for $i > 0$.

An alternative proof can be obtained by using that every injective resolution of $A$ splits, because $A$ is injective. v. [[Mòdul injectiu]]. Una generalització d'això es pot trobar a [[Flasque (flabby) sheaf]].

## Universality

It suffices to check that the $R^iF$ are evasable (v. [[delta-Functor]]). Given $A$, choose $A \to I_0$ monomorphism with $I_0$ injective. Not that $R^i FI_0 = 0$ for $i > 0$. This implies evasability (v. [[Erasable functor]]).

# Exemples

## Functor Ext en la categoria de grups abelians

La categoria de grups abelians té enough injectives. Donat $G$ un grup abelià, $Hom_{Ab}(G,-): Ab \to Ab$ és un functor exacte per l'esquerra. Per tant, es poden definir els functors derivats $R^i Hom(G,-)$, que es denoten $Ext^i(G,-)$ (v. [[Functor ext]]).

## Categoria de feixos

La categoria de feixos (sobre un espai topològic $X$) té suficients injectius. *Demo.* Com que $Ab$ és una categoria abeliana, per cada $x$ es pot prendre $j: \mathcal{F}_x \to I_x$ monomorfisme amb $I_x$ injectiu. Aleshores $\mathcal{I} := \prod (j_x)_* I_x$, on $j_x: * \to X$ envia $* \mapsto x$. Aleshores per cada $\mathcal{G}$ es té que$$Hom_{Sh(X)}(\mathcal{G},\mathcal{I}) = \prod Hom(\mathcal{G_x}, I_x).$$etc etc etc. #casa **qed**

### Seccions globals

Com que les seccions globals $\Gamma(X,-): Sh(X) \to Ab$ són left exact, es **defineix** la **cohomologia del feix** $H^i(X;\mathcal{F}) := R^i \Gamma(X,-)(\mathcal{F})$. (v.[[Direct and inverse image functors for sheaves]])

## Imatge directa

Sigui $f: X \to Y$. Aleshores la imatge directa $f_*: Sh(X) \to Sh(Y)$ és left exact. Es defineix així $R^i f_*(\mathcal{F})$.