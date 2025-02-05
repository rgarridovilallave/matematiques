Let $B$ be a graded ring. As a set,$$Proj(B) := \{\mathfrak{p} \subseteq B \mbox{ homogeneous P.I.},\ B_+ \not\subseteq \mathfrak{p}\}.$$
The second condition is equivalent to asking that, in $\mathbb{P}^1$ we dont' have $[0:0]$.

**Zariski topology.** Define closed sets of $Proj(B)$ to be$$V_+(\mathfrak{a}) := \{\mathfrak{p} \subseteq B\ \textrm{homogeneous}\ \mid \mathfrak{a} \subseteq \mathfrak{p}\},$$for homogeneous ideals $\mathfrak{a} \subseteq B$.

If $a \in B_d$, then $D_+(a) := Proj(B) \setminus V_+((a)) = \{\mathfrak{p} \subseteq B\ \textrm{homogeneous}\ \mid a \notin \mathfrak{p}\}$.

**Structure sheaf.** Two options:

*First option:* $Proj(B) = \bigcup_{a \in B_d,\ d > 0} D_+(a)$. Then use $D_+(a) \cong_{Top} Spec(B_{(a)})$ and glue.

*Second option:* Global definition! For $U \subseteq Proj(B)$ open, set$$\mathcal{O}_{Proj(B)}(U) := \{ s: U \to \bigsqcup_{\mathfrak{p} \in U} B_{(\mathfrak{p})} \mid (i),(ii) \},$$where:
(i) $s(\mathfrak{p}) \in B_{(\mathfrak{p})}$,
(ii) Locally $s = \frac{a}{b}$ with $a,b \in B_d$ (homogeneous elements of the same degree).

Let $\mathcal{O} = \mathcal{O}_{Proj(B)}$. Then:
1. For every $\mathfrak{p} \in Proj(B)$, $\mathcal{O}_\mathfrak{p} \cong B_{(\mathfrak{p})}$. (this implies that it is a locally ringed spaces)
2. For every $a \in B_d$, $d>0$, $(D_+(a),\mathcal{O}|_{D_+(a)}) \cong (Spec(B_{(a)}), \mathcal{O})$.

**Corollary.** $Proj(B)$ is a scheme.

# Propietats

- $V_+(\mathfrak{a}) \cup V_+(\mathfrak{b}) = V_+(\mathfrak{a} \cap \mathfrak{b})$.
- $\bigcap_i V_(\mathfrak{a}_i) = V_+(\sum_i \mathfrak{a}_i)$.
- $V_+(B_+) = \emptyset$ and $V_+((0)) = Proj(B)$.
- This defines a topology.
- $Proj(B) \subseteq Spec(B)$, and the Zariski topology on $Proj(B)$ is the induced one from $Spec(B)$ v. [[Zariski topology]].
- $\mathfrak{a},\mathfrak{b} \subseteq B$ homogeneous ideals. Then$$V_+(\mathfrak{a}) \subseteq V_+(\mathfrak{b}) \iff \mathfrak{b} \cap B_+ \subseteq \sqrt{\mathfrak{a}}.$$

*Proof.* For => in the last one, use that if $\mathfrak{a} \subseteq \mathfrak{p}$ and $\mathfrak{a}$ homogeneous, then $\mathfrak{a} \subseteq \mathfrak{p}^h \subseteq \mathfrak{p}$. **qed**

- $Proj(B) = \emptyset$ if, and only if, $B_+ \subseteq \mathfrak{N}_B$.

## Basic open sets

Let $a \in B_d$ with $d > 0$. Then there exists a homeo$$D_+(a) \cong Spec(B_{(a)}).$$
Atenció! $d=0$ no funciona. Per exemple prenem $B = k[X_0,X_1]$, $B_d = \langle X_0^{i_0} X_1^{i_1} \mid i_0 + i_1 = d \rangle$. Prenem $a = 1 \in k = B_0$. Aleshores $D_+(1) = Proj(B)$, mentre que $Spec(B_{(1)}) = Spec(k)$.

*Proof sketch.*

$D_+(a) \subseteq D(a) \cong Spec(B_a) \to Spec(B_{(a)})$ where $B_{(a)}$ denotes the [[Homogeneous localization]]. We get continuous map $\varphi: D_+(a) \to Spec(B_{(a)})$.

***Step 1:*** *$\varphi$ is surjective.*

***Step 2:*** *$\varphi$ is injective.*

***Step 3:*** *$\varphi$ is open.*

**qed**

## Morphism from Proj(B) to Spec(B_0)

There exists a morphism of schemes $$Proj(B) \to Spec(B_0),\quad \mathfrak{p} \mapsto \mathfrak{p} \cap B_0.$$
Locally we have$$D_+(a) \cong Spec(B_{(a)}) \to Spec(B_0),$$where the second one is induced by $B_0 \subseteq B_{(a)}$.

## Morphism of schemes induced by a morphism of graded rings

Let $\varphi: S_\bullet \to T_\bullet$ be a homomorphism of graded rings (preserving degrees). Let $U = \{\mathfrak{p} \in Proj(T) \mid \mathfrak{p} \nsupseteq \varphi(S_+)\}$. Then $\varphi$ induces a morphism $U \to Proj(S)$, i.e. a rational map $Proj(T) \to Proj(S)$. v. [[Rational map]]

# Exemples

## Projective space

v. [[Projective space]]