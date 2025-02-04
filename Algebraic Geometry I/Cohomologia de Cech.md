Sigui $X$ un espai topològic, $\{U_i\}_i$ un recobriment per oberts seu amb conjunt d'índexs ben ordenat. Es defineix$$C^k(\{U_i\}_i,\mathcal{F}) := \prod_{i_0 < \cdots < i_k} \mathcal{F}(U_{i_0} \cap \cdots \cap U_{i_k}),\quad k \geq 0.$$
Hi ha aplicacions diferencials$$d_p: C^p \to C^{p+1},\quad d_p(s_{i_0,\dots,i_p})_{i_0 < \cdots < i_p} := \left( \sum_{k=0}^{p+1} (-1)^k s_{i_0,\dots, \hat i_k, \dots, i_{p+1}}|_{U_{i_0} \cap \cdots \cap U_{i_{p+1}}} \right)_{i_0 < \cdots < i_{p+1}}.$$
La sheaf property implica que $d^2 = 0$.

Es defineix la **cohomologia de Cech** com la cohomologia d'aquest complex de cocadenes.

# Propietats

## Grau zero

La sheaf property implica que la diferencial en grau zero és zero, així que$$CH^0(\mathcal{F}) = \mathcal{F}(X).$$
## Grau 1

Un cicle de grau 1 és una tupla $(s_{ij})_{i<j}$ de seccions de $U_{ij}$ (per cada $i<j$) que satisfan que, per tota $i<j<k$,$$s_{jk}|_{U_{ijk}} - s_{ik}|_{U_{ijk}} + s_{ij}|_{U_{ijk}} = 0,$$és a dir, que$$s_{ij}|_{U_{ijk}} + s_{jk}|_{U_{ijk}} = s_{ik}|_{U_{ijk}}.$$Aquesta és precisament la **cocycle condition** que garanteix que les seccions locals $(s_{ij})_{i<j}$ es poden enganxar per donar una secció global del feix.

Com que no hi ha vores en grau 1 (ja que la diferencial en grau 0 és nul·la), $CH^1(\{U_i\}_i, \mathcal{F})$ són, precisament, les seccions en $\{U_{ij}\}_{ij}$ que enganxen bé.

La primera cohomologia de Cech coincideix amb la cohomologia de feixos usual:$$CH^1(\{U_i\}_i,\mathcal{F}) \cong H^1(X, \mathcal{F}),$$sense necessitat de demanar cap condició addicional.

## LES en cohomologia de Cech induïda per una SES (cas molt particular!)

Consider a short exact sequence of sheaves $0 \to \mathcal{F}_1 \to \mathcal{F}_2 \to \mathcal{F}_3 \to 0$, and let $\{U_i\}_i$ be an open covering of $X$ such that$$\mathcal{F}_2(U_{i_0} \cap \cdots \cap U_{i_p}) \to \mathcal{F}_3(U_{i_0} \cap \cdots \cap U_{i_p}),\quad i_0 < \cdots < i_p,$$is surjective. Then there's a long exact sequence$$0 \to CH^0(\{U_i\}_i, \mathcal{F}_1) \to CH^0(\{U_i\}_i, \mathcal{F}_2) \to CH^0(\{U_i\}_i, \mathcal{F}_3) \to CH^1(\{U_i\}_i, \mathcal{F}_1) \to CH^1(\{U_i\}_i, \mathcal{F}_2) \to CH^1(\{U_i\}_i, \mathcal{F}_3) \to \cdots.$$
*Proof.*

For every $j$, we have a short exact sequence of abelian groups$$0 \to C^j(\{U_i\}_i, \mathcal{F}_1) \to C^j(\{U_i\}_i, \mathcal{F}_2) \to C^j(\{U_i\}_i, \mathcal{F}_3) \to 0,$$on la part final (exhaustivitat) segueix de l'exhaustivitat dels morfismes $\mathcal{F}_2(U_{i_0} \cap \cdots \cap U _{i_p}) \to \mathcal{F}_3(U_{i_0} \cap \cdots \cap U_{i_3})$.

Les diferencials internes de cadascuna dels complexos de Cech indueixen morfismes de successions exactes llargues. Si transpose, obtenim una successió exacta llarga de complexos de cadenes. ==Aquesta dóna lloc a la successió exacta llarga en cohomologia desitjada (per àlgebra homològica).== **qed**

## Cohomologia de Cech de flasque/flabby sheaves

If $\mathcal{F}$ is flabby, then$$H^i(X,\mathcal{F}) = CH^i(\{U_i\}_i,\mathcal{F}) = 0,$$for every $i$ and every $\{U_i\}_i$ open cover.

*Observació.* Que els feixos flasque siguin $\Gamma(X,-)$-acíclics (és a dir, que tinguin cohomologia de feixos trivial) ja ho hem vist (v. [[Flasque (flabby) sheaf]]).

*Demostració.* No veig per què... Segurament ens hem d'adonar que la successió exacta llarga associada a la ses satisfà propietats de [[delta-Functor]].

## Morfisme de comparació

Sigui $\{U_i\}_i$ un recobriment per oberts de $X$, i $\mathcal{F}$ un feix en $X$. Existeix un morfisme de comparació$$CH^i(\{U_i\}_i,\mathcal{F}) \to H^i(X,\mathcal{F}),\quad i \geq 0.$$
*Demostració.*

El sheaf-theoretic Cech complex (v. [[Cech complex of sheaves]]) és una resolució de $\mathcal{F}$. També podem construir una resolució per injectius de $\mathcal{F}$ juntament amb un morfisme entre les dues resolucions. Aquest morfisme indueix el morfisme de comparació en cohomologia. (utilitzem que hi ha [[Enough injectives]])

***Cal veure:*** que no depèn de les eleccions. **qed**

## Quan la cohomologia de feixos en les interseccions és nul·la

Let $\mathcal{F}$ be a sheaf on $X$, $\{U_i\}_i$ an open cover of $X$, and assume that$$H^p(U_{i_0} \cap \cdots \cap U_{i_p}, \mathcal{F}|_{U_{i_0} \cap \cdots \cap U_{i_p}}) = 0,\quad p > 0,\ i_0 < \cdots < i_p.$$
Aleshores$$CH^p(\{U_i\}_i,\mathcal{F}) = H^p(X,\mathcal{F}).$$
**Achtung!** Potser el resultat només és cert per $p>0$, no ho sé...

*Proof.*

Take the resolution $0 \to \mathcal{F} \to \mathcal{C}^\bullet$ of $\mathcal{F}$ given by the sheaf-theoretic Cech complex (v. [[Cech complex of sheaves]]).

By assumption (**no ho veig!**), for $p>0$, $q \geq 0$ we have that$$H^p(\mathcal{C}^q(\{U_i\}_i,\mathcal{F})) = 0.$$
Hence, the resolution is a $\Gamma$-acyclic resolution of $\mathcal{F}$. This implies (v. [[Right derived functors]], "acyclicity is enouch") that$$H^p(X, \mathcal{C}^\bullet(\{U_i\}_i, \mathcal{F})) = H^p(\mathcal{C}^\bullet(\{U_i\}_i, \mathcal{F})) = CH^p(\{U_i\}_i,\mathcal{F}).$$**qed**

# Exemples

## Cohomologia de $S^1$

Prenem el recobriment $U_0 := \{y > -\frac{1}{2}\}$, $U_1 := \{y < \frac{1}{2}\}$. Aleshores $U_0 \cap U_1$ té dues components. S'arriba a la conclusió que$$CH^1(\{U_0,U_1\},\underline{\mathbb{Z}}) \cong \mathbb{Z}.$$