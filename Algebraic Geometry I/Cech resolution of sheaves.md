El complex de Cech (v. [[Cohomologia de Cech]]), que està format per grups abelians, es pot estendre a un complex format per feixos. Sigui $\{U_i\}_i$ un recobriment per oberts de $X$, i $\mathcal{F}$ un feix en $X$. Es defineix$$\mathcal{C}^p(\{U_i\}_i, \mathcal{F}) := \prod_{i_0 < \dots < i_p} j_* (\mathcal{F}|_{U_{i_0} \cap \cdots \cap U_{i_p}}),$$where $j: \bigcap_{j=0}^p U_{i_j} \to X$ denotes the inclusion (depends on the subindices $i_0, \dots, i_p$).

L'aplicació diferencial $d: \mathcal{C}^p \to \mathcal{C}^{p+1}$ es defineix igual que en el cas abelià:$$d_p: \mathcal{C}^p \to \mathcal{C}^{p+1},\quad d_p(s_{i_0,\dots,i_p})_{i_0 < \cdots < i_p} := \left( \sum_{k=0}^{p+1} (-1)^k s_{i_0,\dots, \hat i_k, \dots, i_{p+1}}|_{U_{i_0} \cap \cdots \cap U_{i_{p+1}}} \right)_{i_0 < \cdots < i_{p+1}}$$
# Propietats

## Seccions globals

Les seccions globals de $\mathcal{C}^\bullet(\{U_i\}_i, \mathcal{F})$ recuperen el complex de Cech estàndard (v. [[Cohomologia de Cech]]).

## Exactitud

El complex $\mathcal{C}^\bullet(\{U_i\}_i, \mathcal{F})$ és exacte.

**Corol·lari.** $\mathcal{C}^\bullet(\{U_i\}_i,\mathcal{F})$ és una resolució de $\mathcal{F}$.

*Demostració.*

És suficient veure que $\mathcal{C}^\bullet(\{U_i\}_i,\mathcal{F})_x$ és exacte per tota $x \in X$ (v. [[Stalk]]).

***Idea.*** *Construïm una homotopia $\theta: id \Rightarrow 0$.*

***Pas 1.*** *Construcció.*

Donat $\alpha_x \in \mathcal{C}^k(\{U_i\}_i,\mathcal{F})_x$, definim $\theta(\alpha_x) \in \mathcal{C}^{k-1}$ de la següent manera. Prenem un entorn obert prou petit $x \in V$ que està contingut en algun $U_j$, i prenem un representant $\alpha = (\alpha_{i_0 < \dots < i_k})_{i_0< \dots< i_k}$ de $\alpha_x$. Definim $\theta(\alpha_x)$ com l'stalk de$$(\alpha_{j<i_0<\dots<i_{p-1}})_{i_0 < \dots < i_{p-1}}$$en $x$.

*Nota:* si per exemple ens apareix l'índex $2<2<3$, aleshores és zero. Si ens apareix $2<1<3$, és el negatiu de $1<2<3$. etc...

***Pas 2.*** *Cal veure que està ben definit (i.e. que no depèn del representant, ni tampoc de $j$ si $V \subseteq U_j, U_{j'}$).*

***Pas 3.*** *Cal veure que és l'homotopia desitjada.*

Cal veure que $(d\theta + \theta d)(\alpha) = \alpha$. **qed**