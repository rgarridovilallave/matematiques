Let $X$ be a scheme. An invertible sheaf $\mathcal{L}$ on $X$ is **ample** if, for every coherent sheaf $\mathcal{F}$ on $X$, there exists some $n_0$ such that $\mathcal{F} \otimes \mathcal{L}^{\otimes n}$ is globally generated for $n \geq n_0$.

v. [[Coherent and quasicoherent modules]], v. [[Ample sheaf]], v. [[Globally generated sheaf]]

The fact that $\mathcal{F} \otimes \mathcal{L}^{\otimes n}$ is globally generated can be restated to saying that the evaluation morphism $ev: H^0(\mathcal{F} \otimes \mathcal{L}^{\otimes n}) \otimes \mathcal{O}_{X,x} \to (\mathcal{F} \otimes \mathcal{L}^{\otimes n})_x$ is surjective for every $x \in X$.

# Trucs

Un truc utilitzat per demostrar coses sobre ample sheaves és el següent: $\mathcal{G}_1 \oplus \cdots \oplus \mathcal{G}_k$ és globally generated si, i només si, $\mathcal{G}_i$ és globally generated per cada $i$.

(potser cal demanar Noetherianitat de l'esquema base??? amb quanta generalitat ho puc utilitzar???)

# Propietats

## Stability

Let $X$ be a ==Noetherian scheme==, and let $\mathcal{L}$ be an invertible sheaf on $X$. The following are equivalent:
1. $\mathcal{L}$ is ample.
2. $\mathcal{L}^{\otimes n}$ is ample for every $n$.
3. There exists an $n$ such that $\mathcal{L}^{\otimes n}$ is ample.

**Achtung!** No entenc on s'utilitza la hipòtesi de Noetherianitat. Potser a l'hora de trencar suma directa???

*Demostració.*

It only remains to be shown that (3) => (1).

**Setup.**

Let $\mathcal{F}$ be a coherent sheaf on $X$. There exists some $m_0 > 0$ such that for every $m \geq m_0$ the sheaf $\mathcal{F} \otimes \mathcal{L}^{\otimes mn}$ is globally generated.

**Pas 1:** *Fem aparèixer els termes $\mathcal{F} \otimes \mathcal{L}^{\otimes mn+i}$ en una suma directa que és globally generated.*

Considerem $$\mathcal{F}' := \bigoplus_{i=0}^{n-1} \mathcal{F} \otimes \mathcal{L}^{\otimes i}.$$
Aleshores per $m \geq m_0$ tenim que $\mathcal{F}' \otimes \mathcal{L}^{\otimes mn}$ és globally generated, on aquí $m_0$ és el mateix que abans. **AIXÒ ÉS EL QUE NO ENTENC**

Si ara desenvolupem, per $m \geq m_0$ tenim$$\mathcal{F}' \otimes \mathcal{L}^{\otimes mn} = \bigoplus_{i=0}^{n-1} \mathcal{F} \otimes \mathcal{L}^{\otimes (mn+i)}.$$
**Pas 2:** *Ens fixem en cadascun dels sumands.*

Com que la suma és globally generated per $m \geq m_0$, deduïm que cadascun dels sumands $\mathcal{F} \otimes \mathcal{L}^{\otimes(mn+i)}$ és globally generated, per $m \geq m_0$ i $i = 0, \dots, n-1$, és a dir, que $\mathcal{F} \otimes \mathcal{L}^{\otimes r}$ és globally generated per $r \geq m_0n$. Això prova el que volíem. **qed**

## $\mathcal{L}^{\otimes n}$ globally generated

En general, si $\mathcal{L}$ és **ample**, no és cert que $\mathcal{L}^{\otimes n}$ sigui **globally generated** per alguna $n$. Sí que ho és, per exemple, si $\mathcal{O}_X$ és coherent sobre si mateix. A continuació donem un criteri on sí que es poden trobar seccions globals generadores.

**Proposition.** Assume $X \to Spec(A)$ of finite type, with $A$ Noetherian. For every ample sheaf $\mathcal{L}$ there exists some $n$ such that $\mathcal{L}^{\otimes n}$ is globally generated. Moreover, these global sections $\{s_i\}_i$ satisfy that $X_{s_i}$ is affine and of finite type over $A$.

**Pregunta:** Potser la hipòtesi que $X \to Spec(A)$ sigui de tipus finit només cal per deduir que $X_{s_i}$ sigui de tipus finit sobre $A$? I per tant $\mathcal{L}^{\otimes n}$ és globalment generat en casos més generals?

*Proof.*

Sigui $n > 0$ qualsevol. Més endavant l'utilitzarem com un enter tal que $\mathcal{V} \otimes \mathcal{L}^{\otimes n}$ sigui globalment generat (existeix perquè $\mathcal{L}$ és ample).

**Pas 1.** *Estudi local: seccions $s$ de $\mathcal{L}^{\otimes n}$ tals que $X_s$ és un entorn de $x$ afí i de tipus finit sobre $A$.*

Sigui $x \in X$, i escollim un entorn afí $x \in U \subseteq X$ amb $U \cong Spec(B)$ i $\mathcal{L}|_U \cong \mathcal{O}_U$.

***Pas 1.1.*** *Escollim el subesquema tancat $Z := X \setminus U$.*

Considerem el subesquema tancat $Z := X \setminus U$ (hi fiquem l'estructura d'esquema [[Reduced induced scheme]]), que dona lloc a la successió exacta de feixos coherents en $X$ següent:$$0 \to \mathcal{V} \to \mathcal{O}_X \to i_*\mathcal{O}_Z \to 0.$$
***Pas 1.2.*** *Podem obtenir seccions de $\mathcal{L}^{\otimes n}$ que provenen de les equacions que defineixen $Z$.*

Si tensoritzem la successió exacta anterior per $-\otimes\mathcal{L}^{\otimes n}$, com que $\mathcal{L}$ és locally free (i també $\mathcal{L}^{\otimes n}$) obtenim la successió exacta següent (v. [[Sheaf of modules]] "exactness of tensor product"):$$0 \to \mathcal{V} \otimes \mathcal{L}^{\otimes n} \to \mathcal{L}^{\otimes n} \to \mathcal{L}|_Z^{\otimes n} \to 0.$$
Per tant, tota secció global $s \in H^0(X, \mathcal{V} \otimes \mathcal{L}^{\otimes n})$ n'indueix una de $\mathcal{L}^{\otimes n}$ que "prové de les equacions que defineixen $Z$". Explícitament, això significarà que $s \in H^0(X,\mathcal{V} \otimes \mathcal{L}^{\otimes n}) \subseteq H^0(X, \mathcal{L}^{\otimes n})$.

***Pas 1.3.*** *Les seccions de $\mathcal{L}^{\otimes n}$ que provenen de les equacions que defineixen $Z$ s'anul·len en $Z$.*

Més explícitament, vegem que $Z \subseteq X \setminus X_s = U$ per cada secció que prové de les equacions que defineixen $Z$. Sigui $z \in Z$. Volem veure que $z \notin X_s$, és a dir, que $s_z \in \mathfrak{m}_z \cdot (\mathcal{V} \otimes \mathcal{L}^{\otimes n})_z$.

Si apliquem el functor exacte $(-)_z$ a la successió exacta anterior, obtenim$$0 \to (\mathcal{V} \otimes \mathcal{L}^{\otimes n})_z \to \mathcal{L}^{\otimes n}_z \to \mathcal{L}^{\otimes n}_z \to 0,$$així que $s_z \in (\mathcal{V} \otimes \mathcal{L}^{\otimes n}) = 0$. Això implica el que volíem veure.

***Pas 1.4.*** *$X_s$ és afí (i de tipus finit sobre $A$) per les seccions de $\mathcal{L}^{\otimes n}$ que provenen de les equacions que defineixen $Z$.*

Sigui $s$ una secció de $\mathcal{L}^{\otimes n}$ que prové de les equacions que defineixen $Z$. La podem restringir a $U$, $s|_U \in H^0(U, \mathcal{L}|_U^{\otimes n}) \cong H^0(U, \mathcal{O}_U)$. Denotem per $b \in H^0(U, \mathcal{O}_U)$ la seva imatge sota aquest isomorfisme. Aleshores $X_s \cong Spec(B_b)$, que és afí i de tipus finit sobre $A$ (perquè $B$ és de tipus finit sobre $A$).

**Pas 2.** *Obtenció de seccions globals.*

Amb la construcció del **Pas 1**, podem trobar un recobriment de $X$ de la forma $\{X_{s_i}\}_i$, on $s_i$ és una secció global de $\mathcal{L}^{\otimes n_i}$ i, a més, $X_{s_i} \cong Spec(B_i)$ amb $B_i$ de tipus finit sobre $A$.

Com que $X$ és ==quasi-compacte== (**per què????**), es pot prendre un subrecobriment finit i, per tant, prendre $n := max (n_i)$. (aquí també utilitzem que $X_s = X_{s^k}$). Es conclou que $\mathcal{L}^{\otimes n}$ és globalment generat, per alguna $n$. **qed**

## Ample sheaf = Immersion into projective space, for some power

Assume $X \to Spec(A)$ is of ==finite type==, with ==$A$ Noetherian==. An invertible sheaf $\mathcal{L}$ on $X$ is **ample** if, and only if, there exists some $n > 0$ and an immersion $i: X \to \mathbb{P}^n_A$ over $Spec(A)$ such that $i^* \mathcal{O}(1) \cong \mathcal{L}^{\otimes n}$.

v. [[Ample sheaf]]

*Proof.*

<=]

**Setup.** Consider an immersion $i: X \to \mathbb{P}^n_A$ over $Spec(A)$ such that $\mathcal{L}^{\otimes n} = i^* \mathcal{O}(1)$. Considerem un feix coherent $\mathcal{F}$ en $X$ qualsevol.

**Pas 1.** *Treballem en l'adherència de $i(X)$, on podem aplicar el Serre's vanishing theorem.*

Consider the closure $X \to \bar X \subseteq \mathbb{P}^n_A$. The sheaf $\mathcal{F}$ can be extended to a sheaf $\bar{\mathcal{F}} \in Coh(\bar{X})$. El [[Serre's vanishing theorems]] implica que $\overline{\mathcal{F}} \otimes \mathcal{O}(m)$ és globally generated per $m \geq m_0$ i alguna $m_0 > 0$.

**Pas 2.** *Tornem a $X$.*

Si ara ens restringim a $X$, obtenim que $\mathcal{F} \otimes \mathcal{L}^{\otimes mn}$ és globally generated per $m \geq m_0$. Com que $X$ és ==Noetherià==, això implica que $\mathcal{L}$ és ample (per la propietat d'**estabilitat** de ampleness).

=>]

**Pas 1.** *Escollim seccions globals amb la hipòtesi addicional (H).*

Per un resultat demostrat anteiorrment (v. "$\mathcal{L}^{\otimes n}$ globally generated"), existeixen seccions globals $s_1, \dots, s_r$ de $\mathcal{L}^{\otimes n}$ que la generen, i tals que $X_{s_i}$ és afí i de tipus finit sobre $A$.

**Pas 2.** *Com que tenim la hipòtesi addicional (H), apliquem la construcció millorada de morfismes cap a espais projectius.*

Amb aquestes hipòtesis addicionals en $X_{s_i}$, podem aplicar la construcció millorada de [[Morphisms into projective space]], de manera que obtenim una immersió $X \to \mathbb{P}^M_A$ sobre $Spec(A)$ tal que $i^* \mathcal{O}(1) \cong \mathcal{L}^{\otimes M}$ (revisar aquesta potència $\otimes M$). **qed**

## Ample = Some power is very ample

Això es dedueix de "Ample = Immersion into projective space":

Suppose that $X \to Spec(A)$ is **proper**. By the cancellation property every immersion is a closed immersion (v. [[Morphisms of schemes]]), so an invertible sheaf $\mathcal{L}$ is **ample** if, and only if, $\mathcal{L}^{\otimes n}$ is **very ample** for some $n>0$.

# Exemples

## Affine schemes

Every invertible sheaf on an affine scheme is ample.

*Demostració.*

Sigui $X = Spec(A)$, $\mathcal{L} = \widetilde{M}$ feix invertible en $X$, $\mathcal{F} = \widetilde{N}$ feix coherent en $X$. Aleshores existeix $m \in M$ tal que $\tilde M = A\langle m \rangle$, i existeixen $n_1, \dots, n_r \in N$ tals que $N = A \langle n_1, \dots, n_r \rangle$.

Aleshores $\mathcal{F} \otimes \mathcal{L}^{\otimes k}$ es correspon amb$$A \langle n_1 \otimes m^{\otimes k},\ \dots,\ n_r \otimes m^{\otimes k} \rangle,$$que està globalment generat per $\{n_i \otimes m^{\otimes k}\}_i$ per cada $k$. **qed**