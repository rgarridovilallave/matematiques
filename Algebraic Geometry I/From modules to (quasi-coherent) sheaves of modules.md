We have a functor $Mod(A) \to Mod(Spec(A))$, $M \mapsto \tilde M$, given by$$\tilde M(U) = \{s: U \to \bigsqcup_{\mathfrak{p} \in U} M_\mathfrak{p} \mid s(\mathfrak{p}) \in M_\mathfrak{p},\ s = \frac{m}{a}\ \textrm{locally},\ m \in M, a \in A\}.$$
Note that $\tilde A = \mathcal{O}_{Spec(A)}$, $\tilde M(Spec(A)) = M$, $\tilde M(D(a)) \cong M_a$ and $(\tilde M)_\mathfrak{p} \cong M_\mathfrak{p}$.

In fact, the functor will land in quasi-coherent modules and will induce an equivalence of categories.

## Graded setting

Given $M$ graded $B$-module, define$$\tilde M(U) := \{ s: U \to \bigsqcup_{\mathfrak{p} \in U} M_{(\mathfrak{p})} \mid (i),(ii)\},$$
(i) $s(\mathfrak{p}) \in M_{(\mathfrak{p})}$,
(ii) locally $s = \frac{m}{b}$, $m \in M_d$,$b \in B_d$.

This produces a module in $Mod(Proj(B),\mathcal{O})$.

We also have that $(\tilde M)_\mathfrak{p} \cong M_{(\mathfrak{p})}$ for $\mathfrak{p} \in Proj(B)$. And also, for $a \in B_d$, $\tilde M|_{D_+(a)} \cong \tilde M_{(a)}$. Hence,$$\tilde M(D_+(a)) \cong \tilde M_{(a)} (Spec(B_{(a)})) \cong M_{(a)}.$$

(3) For all $M$ graded $B$-module, $\tilde M$ is a quasi-coherent module over $Proj(B)$.

(4) Assume $B$ Noetherian, and $M$ finite as a $B$-module. Then $\tilde M$ is in $Coh(Proj(B))$.

# Properties

## Exactness (affine setting)

The functor $\tilde M: Mod(A) \to Mod(\mathcal{O}_A)$ is exact.

*Proof.*

Consider a short exact sequence $0 \to M_1 \to M_2 \to M_3 \to 0$. The sequence that we obtain after applying $\tilde{(-)}$ is exact if, and only if, the following sequence is exact for all $\mathfrak{p}$:$$0 \to (\tilde M_1)_\mathfrak{p} \to (\tilde M_2)_\mathfrak{p} \to (\tilde M_3)_{\mathfrak{p}} \to 0.$$This sequence is isomorphic to$$0 \to (M_1)_\mathfrak{p} \to (M_2)_\mathfrak{p} \to (M_3)_\mathfrak{p} \to 0,$$which is exact because localisation is exact. **qed**

## Full (affine setting)

Let $M,N \in Mod(A)$, and let $g: \tilde M \to \tilde N$ be a morphism in $Mod(X,\mathcal{O}_X)$.

*We have to realise $g$ as a morphism of modules:*

**Step 1:** *Take global sections.*

We obtain $\varphi :M = \tilde M(X) \to \tilde N(X) = N$. We have to show that $(g - \tilde \varphi): \tilde M \to \tilde N$ is trivial on global sections.

**Step 2:** *It suffices to show triviality at the level of stalks.*

For every $\mathfrak{p} \in Spec(A)$, by the definition of $\varphi$ it holds that $\varphi_\mathfrak{p} = g_\mathfrak{p}$. **qed**

## Faithful (affine setting)

Start with $\varphi: M \to N$. Obtain $\tilde \varphi: \tilde M \to \tilde N$. Then $\varphi = \tilde \varphi(X):M = \tilde M(X) \to \tilde N(X) = N$, so $\tilde \varphi$ determines completely $\varphi$. This implies that $\tilde{(-)}$ is faithful. **qed**

## $A$-modules = Quasicoherent sheaves over $Spec(A)$ (affine setting)

**Proposition.** $\widetilde{(-)}$ provides an equivalence of categories $Mod(A) \stackrel{\cong}{\to} QCoh(Spec(A))$.

**Remarks:**
1. The proposition shows that for every $\mathcal{F} \in QCoh(Spec(A))$, $\mathcal{F}(X)_a \cong \mathcal{F}(D(a))$.
2. If $\mathcal{F} \to \mathcal{G}$ is surjective in $QCoh(Spec(A))$ then $\mathcal{F}(X) \to \mathcal{G}(X)$ is also surjective.
3. Assume that for $M \in Mod(A)$ the associated sheaf $\tilde M \in QCoh(X)$ is actually coherent. Then $M$ is finite over $A$.
4. If $A$ is Noetherian and $M$ is a finite $A$-module, then $\tilde M \in Coh(Spec(A))$.

**PART I:** *We show that the functor lands in quasicoherent sheaves over $Spec(A)$.*

Pick a presentation for $M$, i.e. $\varphi: A^{\oplus J} \to M$ surjective. This is equivalent to an exact sequence$$A^{\oplus I} \to A^{\oplus J} \stackrel{\varphi}{\to} M \to 0.$$
Apply the $\widetilde{(-)}$ functor, which is exact, and obtain the exact sequence of $\mathcal{O}_X$-modules$$\mathcal{O}^{\oplus I}_X \to \mathcal{O}^{\oplus J}_X \to \tilde M \to 0.$$
This precisely means that (v. [[Coherent and quasicoherent modules]]) $\tilde M \in QCoh(A)$. **qed**

**PART II: ESSENTIAL SURJECTIVITY:**

***Step 1:*** *Easy case: suppose that there exists a sequence $\mathcal{O}_X^{\oplus I} \to \mathcal{O}_X^{\oplus J} \to \mathcal{F} \to 0$ (it exists locally because it is quasicoherent).*

Compte perquè l'argument és una mica estrany... Denotem $\mathcal{O}^{\oplus I}_X \to \mathcal{O}^{\oplus J}_X \stackrel{\alpha}{\to} \mathcal{F} \to 0$.

Taking global sections we obtain an associated sequence, although it needn't be exact:$$A^{\oplus I} \to A^{\oplus J} \stackrel{\alpha_0}{\to} \mathcal{F}(X) \to 0,\quad \alpha_0 := \Gamma(X,\alpha).$$
The morphism $\alpha_0$ factors through its image, $A^{\oplus_J} \stackrel{\alpha_0}{\to} im(\alpha_0) \subseteq \mathcal{F}(X)$, thus giving a surjective morphism $\alpha_0: A^{\oplus J} \to im(\alpha_0)$.

Exactness of $\widetilde{(-)}$ implies that $\widetilde{\alpha_0}: \widetilde{A^{\oplus J}} \to \widetilde{im(\alpha_0)}$ is an epimorphism. We obtain that $\alpha$ factors as $\mathcal{O}_X^{\oplus J} \stackrel{\widetilde{\alpha_0}}{\to} \widetilde{im(\alpha_0)} \subseteq \mathcal{F}$ (again it's a monomorphism because $\widetilde{(-)}$ is exact). But $\alpha$ was already an epimorphism, so $\widetilde{im(\alpha_0)} \subseteq \mathcal{F}$ is an epimorphism. This implies that $\mathcal{F} \cong \widetilde{im(\alpha_0)} =: \tilde M$.

***Step 2:*** *General case!*

Take affine open coverings $\{D(a_i)\}_i$ of $X = Spec(A)$. Then $\mathcal{F}|_{D(a_i)} \cong \tilde M_i$, with $M_i \in Mod(A_{a_i})$.

It's enough to show that $\tilde M(D(a)) \to \mathcal{F}(D(a))$ is an isomorphism. Then use the sheaf property to glue. **qed**

*Proof Remark (3).*

Coherentensss implies the xistence of a finite covering of $Spec(A)$, $\{D(a_i)\}_i$, plus surjections $\mathcal{O}_{D(a_i)}^{\oplus n} \to \tilde M|_{D(a_i)}$. By the previous remark we get a surjection on global sections (over $D(a_i)$), i.e. we get $A_{a_i}^{\oplus n_i} \to M_{a_i}$ surjective. This implies that $M$ itself is a finite $A$-module. **qed**

*Proof Remark (4).*

$M$ is finite, so there existst $A^{\oplus n} \to M$ surjective. This induces $\tilde A^{\oplus n} \to \tilde M$, so we deduce part (a) of coherentness.

For (v), take $V =D(a)$. Then $$\mathcal{O}_C^{\oplus n} \to \tilde M|_V$$ is surjective, but these are isomorphic to $\varphi:A_a^{\oplus n} \to M_a$ . Noetherianity implies that $ker(\varphi) \subseteq A_a^{\oplus n}$ is finitely generated as an $A_a$-module.

THIS imples the existence $A_a^{\oplus m} \to A_a^{\oplus n} \to M \to 0$ is exact, and hence $\mathcal{O}_V^{\oplus m} \to \mathcal{O}_V^{\oplus n} \to \tilde M \to 0$ is exact. This proves (b). **qed**

## Imatge directa = Restricció d'escalars

Calculem **explícitament** quina és la imatge directa de $\tilde M$ sota el morfisme $Spec(A) \to Spec(B)$ induït per $f: B \to A$. Recordem que aquesta imatge directa és $f_* \tilde M \in Mod(Spec(B), \mathcal{O}_B)$.

Sigui $M$ un $A$-mòdul donat per $\alpha: A \to M$. Aleshores $f_* \tilde M$ és el $\mathcal{O}_B$-mòdul següent:
- Donat $D(b) \subseteq Spec(B)$ obert bàsic, $(f_* \tilde M)(D(b)) = \tilde M(f^{-1}D(b)) = \tilde M (D(fb)) = M_{fb}$.
- L'estructura de $\mathcal{O}_B$-mòdul ve donada, per $D(b) \subseteq Spec(B)$ obert bàsic, com$$B_b \longrightarrow A_{fb} \stackrel{\alpha_{fb}}{\longrightarrow} M_{fb},$$ja que $\mathcal{O}_B(D(b)) = B_b$, $(f_*\mathcal{O}_A)(D(b)) = A_{fb}$ i $(f_* \tilde M)(D(b)) = M_{fb}$.

Per tant, observem que $f_* \tilde M = \widetilde{{}_B M}$, on ${}_BM$ és el $B$-mòdul donat per $B \stackrel{f}{\to} A \stackrel{\alpha}{\to} M$. És a dir, la imatge directa aplicada a un $\tilde M$ l'únic que fa és "restringir" l'estructura de $B$-mòdul de $M$ al llarg de $f$.

## El functor $\widetilde{(-)}$ respecta l'estructura monoidal

Let $M$ and $N$ be two $A$-modules. Then$$\widetilde{(M \otimes_A N)} \cong \tilde M \otimes_{\mathcal{O}_A} \tilde N.$$
(observem que això diu que el functor $Mod(A) \to Mod(\mathcal{O}_A)$ respecta l'estructura monoidal!)

Com que $\tilde M \otimes_{\mathcal{O}_A} \tilde N$ es defineix per mitjà de la feixificació de $\tilde M \otimes^{PSh}_{\mathcal{O}_A} \tilde N$ (v. [[Sheafification]], [[Sheaf of modules]]), és suficient veure que$$\widetilde{(M \otimes_A N)} \cong \tilde M \otimes^{PSh}_{\mathcal{O}_A} \tilde N,$$ja que implícitament també estaríem veient que $\tilde M \otimes_{\mathcal{O}_A}^{PSh} \tilde N$ és un feix, i la feixificació d'un feix és el propi feix.

En oberts bàsics $D(a) \subseteq Spec(A)$,$$\widetilde{(M \otimes_A N)}(D(a)) = (M \otimes_A N)_a = M_a \otimes_{A_a} N_a = \tilde{M}(D(a)) \otimes_{\mathcal{O}_A(D(a))} \tilde{N}(D(a)) = (\tilde M \otimes_{\mathcal{O}_A}^{PSh} \tilde N)(D(a)).$$
També es pot comprovar que les estructures de mòdul coincideixen. Es dedueix el resultat. **qed**

## Imatge inversa = Estensió d'escalars

M'ho crec xd

***Idea:*** Use the adjunction $f^* \dashv f_*$.

We get that $$Hom(f^* \mathcal{G}, \mathcal{F}) \cong Hom(\tilde{(M \otimes_A B)}, \mathcal{F}).$$
By the [[Yoneda lemma]] we obtain that $f^* \mathcal{G} \cong \tilde{(M \otimes_A B)}$.

# Exemples

## Exemple de la construcció en el pla afí

Considerem $M := k[X,Y]\langle A,B\rangle$ com a $k[X,Y]$-mòdul. Aleshores $\tilde M$ és un mòdul quasi-coherent en $\mathbb{A}^2_k$. A tall d'exemple, les seccions en $D(X) \subseteq \mathbb{A}^2_k$ estan generades per $A$ i $B$, on els coeficients venen donats per les seccions del feix estructural en $D(X)$, i.e. $k[X,X^{-1},Y]$. Per exemple, les següents són seccions en $\tilde M(D(X))$:$$A + X \cdot B,\quad X^{-1} \cdot A + X^2Y \cdot B,\quad \dots.$$