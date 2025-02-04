Sigui $A$ un anell (commutatiu, unitari, $1 \neq 0$).

$X := Spec(A)$ with the [[Zariski topology]]. Let $\mathcal{O}_X$ be the sheaf on $X = Spec(A)$ defined by $$\mathcal{O}_X(U) := \{s: U \to \sqcup_{\mathfrak{p} \in U} A_\mathfrak{p}\ \textrm{s.t.}\ (1), (2)\},$$where $A_\mathfrak{p}$ denotes the $\mathfrak{p}$-localization of $A$, i.e. $(A \setminus \mathfrak{p})^{-1} A$, and
1. $s(\mathfrak{p}) \in A_\mathfrak{p}$ for every $\mathfrak{p} \in U$,
2. **Locally rational:** For every $\mathfrak{p} \in U$ there exists an open set $\mathfrak{p} \in V \subseteq U$ and $a, b \in A$ such that for every $\mathfrak{q} \in V$, $b \notin \mathfrak{q}$ and $s(\mathfrak{q}) = \frac{a}{b} \in A_\mathfrak{q}$.

The restriction maps are given by restriction.

v. "Theory of complex functions in several variables", Kiyoshi Oka (orígens, justificació de la notació)

# Propietats

## Stalk

Let $X = Spec(A)$. For every point $\mathfrak{p} \in X$, $\mathcal{O}_{X,\mathfrak{p}} \cong A_\mathfrak{p}$. **AIXÒ SIGNIFICA INVERTIR ==FORA== DE L'IDEAL !!!!**

v. [[Algebraic geometry (Hartshorne)]] Proposition II.2.2(a).

*Proof.*

Consider the morphism $\mathcal{O}_{X,\mathfrak{p}} \to A_\mathfrak{p}$ that sends a germ with associated section $s: U \to \sqcup_\mathfrak{q} A_\mathfrak{q}$ to $s(\mathfrak{p}) \in A_\mathfrak{p}$. We show that this is an isomorphism.

***Injectivity:*** Given two germs $(s_1)_\mathfrak{p}, (s_2)_\mathfrak{p} \in \mathcal{O}_{X,\mathfrak{p}}$ with the same image in $A_{\mathfrak{p}}$, one can find a small enough open neighbourhood $U$ of $\mathfrak{p}$ such that $s_i(\mathfrak{q}) = \frac{a_i}{b_i}$ for every $\mathfrak{q} \in U$. Then $h(a_1b_2 - a_2 b_1)  =0$ for some $h \in A \setminus \mathfrak{p}$, and hence $s_1 = s_2$ when restricted to $\mathcal{O}_X(D(h) \cap U)$. This implies the equality of the germs $(s_1)_\mathfrak{p} = (s_2)_\mathfrak{p}$.

***Surjectivity.*** Let $\frac{a}{f} \in A_\mathfrak{p}$, with $a \in A$, $f \in A \setminus \mathfrak{p}$. The section $s$ defined on $D(f)$ by $s(\mathfrak{q}) := \frac{a}{f}$ is well-defined and sent to $\frac{a}{f}$ by the morphism $\mathcal{O}_{X,\mathfrak{p}} \to A_\mathfrak{p}$. This shows the surjectivity. **qed**

## Seccions en les boles $D(a)$

Let $X = Spec(A)$. For every $a \in A$, $\mathcal{O}_X(D(a)) \cong A_a$. **AIXÒ SIGNIFICA INVERTIR L'ELEMENT !!!**

v. [[Algebraic geometry (Hartshorne)]] Proposition II.2.2(b).

*Nota.* Aquí $A_a$ denota la localització de $A$ **en** $a$, és a dir, s'inverteix $a$. No s'ha de confondre amb $A_{(a)}$ (ó $A_{\mathfrak{p}}$), que significa la localització **fora** de $(a)$ (ó $A_{\mathfrak{p}}$) i s'inverteix $A \setminus (a)$ (ó $A \setminus \mathfrak{p}$).

*Proof.*

Define $\psi: A_a \to \mathcal{O}_X(D(a))$ by $\frac{b}{a^n} \mapsto (\mathfrak{p} \mapsto \frac{b}{a^n} \in A_\mathfrak{p})$.

**Injectivitat:** Siguin $\frac{b_1}{a^{n_1}}, \frac{b_2}{a^{n_2}} \in A_a$ tals que la seva imatge en $A_\mathfrak{p}$ coincideix per cada ideal primer $\mathfrak{p} \in D(a)$. Cal veure que són el mateix element, és a dir, que existeix alguna potència $a^m \in (a)$ tal que $a^m(b_1 a^{n_2} - b_2 a^{n_1}) = 0$. Per això estudiem l'aniquilador $\mathfrak{a} := Ann(b_1 a^{n_2} - b_2 a^{n_1})$.

Si veiem que $V(\mathfrak{a}) \cap D(a) = \emptyset$ automàticament tindrem que $a^n \in \mathfrak{a}$ per alguna $n$ (v. [[Zariski topology]]).

Sigui $\mathfrak{p} \in D(a)$, és a dir, $\mathfrak{p}$ ideal primer que no conté $a$. Per hipòtesi (ja que les fraccions coincideixen en $A_\mathfrak{p}$) existeix $h \notin \mathfrak{p}$ tal que $h(b_1 a^{n_2} - b_2 a^{n_1}) = 0$, és a dir, $h \in \mathfrak{a}$. Això prova que $\mathfrak{a} \not\subseteq \mathfrak{p}$, és a dir, $\mathfrak{p} \notin V(\mathfrak{a})$.

**Exhaustivitat:** Sigui $s \in \mathcal{O}_X(D(a))$.

***Primer pas:*** *Recobrim $D(a)$ per oberts bàsics $\{D(h_i)\}_i$ de manera que $s = \frac{a_i}{h_i}$ en $D(h_i)$.*

En primer lloc, existeix un recobriment $\{D(g_i)\}_i$ de $D(a)$ de manera que $s = \frac{a_i}{g_i^{n_i}}$ en $D(g_i)$. Com que $D(g_i) = D(g_i^{n_i})$, podem posar $h_i := g_i^{n_i}$ i obtenir el recobriment desitjat.

***Segon pas:*** *El recobriment $\{D(h_i)\}_i$ es pot fer finit: $\{D(h_1),\dots,D(h_k)\}$.*

Utilitzem quasi-compacitat.

***Tercer pas:*** *Compatibilitat del recobriment amb les interseccions: existeix $n$ tal que $(h_i h_j)^n (a_i h_j - a_j h_i) = 0$ per tota $i,j$.*

Per cada $i,j$, la intersecció $D(h_i) \cap D(h_j)$ és $D(h_i h_j)$. Com que, per cada $\mathfrak{p} \in D(h_ih_j)$ es té que $\frac{a_i}{h_i} = s(\mathfrak{p}) = \frac{a_j}{h_j}$, per la injectivitat de $\psi$ (prenent $a = h_ih_j$) deduïm que $\frac{a_i}{h_i}$ i $\frac{a_j}{h_j}$ coincideixen en $A_{h_ih_j}$. En altres paraules, $(h_ih_j)^n(a_ih_j - a_j h_i) = 0$ per alguna $n=n(i,j)$. Com que el recobriment és finit, es pot escollir $n := max_{i,j} n(i,j)$.

***Quart pas:*** *Manipulació algebraica per veure que els valors locals provenen d'un de global.*

Per cada $i$ posem $a_i' := a_ih_i^n$, $h_i' := h_i^{n+1}$. Aleshores:
- $\frac{a_i'}{h_i'} = \frac{a_i}{h_i}$ en $A_{h_i}$, i
- $(h_ih_j)^n(a_ih_j-a_jh_i)$ es tradueix en $a'_ih'_j = a'_jh'_i$.

Oblidem la notació $'$.

Com que $\{D(h_i)\}_{i=1,\dots,k}$ és un recobriment de $D(a)$ per oberts bàsics, existeixen $m$ i $b_i \in A$ tals que $a^m = \sum_i b_i h_i$ (v. [[Zariski topology]]).

Sigui $\alpha := \sum_i b_i a_i$. Aleshores per cada $j$ es té que$$h_j \alpha = \sum_i b_i a_i h_j = \sum_i b_i h_i a_j = a^n a_j,$$és a dir, $\frac{\alpha}{a^n} = \frac{a_j}{h_j}$ en $D(h_j)$. Això implica que $\psi(\frac{\alpha}{a^n}) = s$. **qed**

## Quasi-compactness

The scheme $Spec(A)$ is quasi-compact.

*Proof.*

Assume $Spec(A) = \bigcup_i U_i$, and WLOG $U_i = D(a_i)$. This is equivalent to $V((a_i)_i) = \bigcap_i V(a_i) = \emptyset$. Hence, the ideal $(a_i)_i$ is the total ideal, so $1 = \sum_j b_j a_{i_j}$ for a finite sum. We can hence cover $Spec(A) = \bigcup_j D(a_{i_j})$. **qed**

## Nilradical

Sigui $s \in \Gamma(Spec(A), \mathcal{O}_A) \cong A$ una secció global. Pertany al nilradical (v. [[Nilradical]]) de $A$, $\mathfrak{N}_A$, si, i només si, pertany a tots els primers $\mathfrak{p} \in Spec(A)$, que és equivalent a $D(s) = \emptyset$.

En altres paraules, les seccions nilpotents (i.e. de $\mathfrak{N}_A$) són precisament aquelles que s'*anul·len* en tot punt $\mathfrak{p} \in Spec(A)$. Entenem que $s$ s'anul·la en $\mathfrak{p}$ si la classe de $s_\mathfrak{p}$ en $A_\mathfrak{p}/\mathfrak{p} A_\mathfrak{p}$ és zero.

# Exemples

## Feix estructural de $\mathbb{Z}$

- **Open sets:** all open sets are of the form $Spec(\mathbb{Z}[1/n])$, for $n \in \mathbb{Z} \setminus \{0\}$. Note that $D((n)) = Spec(\mathbb{Z}[1/n])$.
- **Structure sheaf** is explicitly given by $\mathcal{O}_X: Ouv_X^{op} \to Ab$, $Spec(\mathbb{Z}[1/n]) \mapsto \mathbb{Z}[1/n]$.
 