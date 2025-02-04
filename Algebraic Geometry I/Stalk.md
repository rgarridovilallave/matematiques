Sigui $\mathcal{C}$ una categoria que admet límits directes. L'**stalk sobre $x \in X$** d'un feix $\mathcal{F}$ sobre $X$ amb valors en $\mathcal{C}$ és el límit directe (v. [[Direct limit]])
$$\mathcal{F}_x := \lim_{x \in U} \mathcal{F}(U).$$
*Moralment,* en l'stalk de $x$ dues seccions s'identifiquen si coincideixen en un entorn de $x$.

Since we have a map $\mathcal{F}(U) \to \mathcal{F}_x$ for every $x \in U$, there's a map $\mathcal{F}(U) \to \prod_{x \in U} \mathcal{F}_x$ (if the category admits products).

The **germ** of $s \in \mathcal{F}(U)$ at $x \in U$ is defined to be the image of $s$ under $\mathcal{F}(U) \to \mathcal{F}_x$. It's denoted $s_x$.

*Remark.*
- This constructions hold for presehaves, but some properties are lost.
- Taking stalks is a functor.

# Properties

## The stalks of a section determine it

The map $\mathcal{F}(U) \to \prod_{x \in U} \mathcal{F}_x$ is injective.

*Proof.* (in $Ab$)

If $s \in \mathcal{F}(U)$ satisfies $s_x = 0$ for every $x \in U$, then $s|_{V_x} = 0$ for some $x \in V_x \subseteq U$ for every $x$. Since $\mathcal{F}$ si a sheaf, this implies that $s =0 \in  \mathcal{F}(U)$. **qed**

## The stalks of a morphism determine it

A morphism $\varphi$ of abelian sheaves is zero if, and only if, $\varphi_x = 0$ for every $x$.

*Proof.*

$\Rightarrow$ ok. For $\Leftarrow$, given a section $s$ in $U$, $\varphi(s)_x = \varphi_x(s_x) = 0$. Hence, $\varphi$ vanishes in a neighbourhood of $x$. This is true for every $x$, so $\varphi = 0$. **qed**

**Corol·lari.** Applying this last result to $id: \mathcal{F} \to \mathcal{F}$ we obtain that $\mathcal{F} = 0$ <=> $\mathcal{F}_x = 0\ \forall\ x$.

## Stalk del nucli, la imatge i el conucli

v. [[Sheaf]]

Els stalks són: $ker(\varphi)_x = ker(\varphi_x)$, $im(\varphi)_x = im(\varphi_x)$, $coker(\varphi)_x = coker(\varphi_x)$.

## Exactitud

$\mathcal{F} \to \mathcal{G} \to \mathcal{H}$ is exact if, and only if, $\mathcal{F}_x \to \mathcal{G}_x \to \mathcal{H}_x$ is exact.

En altres paraules, $(-)_x$ is **exact**.

*Proof.*

=> ) easy (use that direct limits are exact).

<= ) $(\psi \varphi)_x = \psi_x \varphi_x = 0$ for every $x$, so $\psi \varphi = 0$. Moreover, $im(\varphi)_x = im(\varphi_x) = ker(\psi_x) = ker(\psi)_x$. **qed**

As a consequence: $0 \to \mathcal{F} \to \mathcal{G} \to \mathcal{H} \to 0$ is exact if, and only if, $0 \to \mathcal{F}_x \to \mathcal{G}_x \to \mathcal{H}_x \to 0$ is exact.

# Examples

## Stalk de les funcions holomorfes en $\mathbb{C}$

Si $\mathcal{O}_{\mathbb{C}}$ és el feix de funcions holomorfes $\mathbb{C} \to \mathbb{C}$, l'stalk $\mathcal{O}_{\mathbb{C},z}$ es pot identificar amb l'anell de sèries de potències que coinvergeixen en algun entorn de $z$.
## Stalk del feix constant

Since for $U$ small enough $\pi_0(U) = *$, we have that $\underline{G}_x \cong \mathbb{G}_x \cong G$.
