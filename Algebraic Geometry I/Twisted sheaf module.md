Let $d \in \mathbb{Z}$ and $B$ a graded ring. Define the quasi-coherent module $\mathcal{O}(d) := \widetilde{B(d)}$ over $Proj(B)$ v. [[From modules to (quasi-coherent) sheaves of modules]].

Recall $M(d)_e := B_{e+d}$.

# Propietats

## Stalks

Sigui $\mathfrak{p} \in Proj(B)$, és a dir, un ideal primer homogeni tal que $B_+ \nsubseteq \mathfrak{p}$. Aleshores l'stalk de $\mathcal{O}(d)$ en $\mathfrak{p}$ és$$\mathcal{O}(d)_\mathfrak{p} = B(d)_\mathfrak{p} = \left\{ \frac{x}{y} \mid x \in B_{r+d},\ y \in B_{r} \setminus \mathfrak{p} \right\} \subseteq Q(B)_d.$$

# Exemples

## Recta projectiva

Intentem entendre les seccions de $\mathcal{O}_{\mathbb{P}^1_k}(n)$ en l'obert $U = D_+((X-1)Y)$, que pensem com $\mathbb{P}^1_k$ menys el punt de l'infinit $\infty=[1:0]$. Per una banda, les seccions del feix estructural són$$\Gamma(\mathcal{O}_{\mathbb{P}^1_k}, U) \cong k[X,Y]_{((X-1)Y)} = \left\langle \frac{X^r Y^s}{(X-1)^{r+s}} \right\rangle_{\substack{r \geq 0 \\ s \in \mathbb{Z}}}.$$
Per altra banda, les seccions del twisted module són$$\Gamma(\mathcal{O}_{\mathbb{P}^1_k}(n), U) \cong k[X,Y](n)_{((X-1)Y)}.$$
Si $n = 0$, recuperem el feix estructural. En general, obtenim$$\left\langle \frac{X^r Y^s}{(X-1)^{r+s-n}} \right\rangle_{\substack{r \geq 0 \\ s \in \mathbb{Z}}},$$que és el $\Gamma(\mathcal{O}_{\mathbb{P}^1_k}, U)$-mòdul$$\Gamma(\mathcal{O}_{\mathbb{P}^1_k}, U) \left\langle (X-1)^{n} \right\rangle.$$
## Projective spaces

Let $U_i := D_+(X_i) \subseteq \mathbb{P}^n_k$ for $k$ a field. Then$$\mathcal{O}_{\mathbb{P}^n_k}(1)(U_i) = k[X_0/X_i, \dots, X_n/X_i] \langle X_0, \dots, \hat X_i, \dots, X_n \rangle = k[X_0/X_i, \dots, X_n/X_i] \langle X_i \rangle.$$

És a dir, $\mathcal{O}_{\mathbb{P}^n_k}(1)$ és un feix invertible (v. [[Sheaf of modules]]).

Anàlogament, es demostra que$$\mathcal{O}_{\mathbb{P}^n_k(m)}(U_i) = k[X_0/X_i, \dots, X_n/X_i] \langle X_i^m \rangle,$$fins i tot crec que per $m$ negatiu!

Aleshores, per $r \geq 0$, les seccions globals de $\mathcal{O}_{\mathbb{P}^n_k}(r)$ són polinomis homogenis de grau $r$. Els esquemes tallats per una secció global de $\mathcal{O}_{\mathbb{P}^n_k}(r)$ es corresponen, per tant, amb les hipersuperfícies de grau $r$. Per $n = 2$, tenim que $r = 1$ són les rectes, $r = 2$, les còniques, $r = 3$, les cúbiques, $r = 4$, les quàdriques, etc.

# Altres

## Morfismes d'esquemes projectius determinats per les seccions globals de $\mathcal{O}(1)$

Considerem $S_\bullet$ i $T_\bullet$ dos anells graduats **tals que** $T_0 = S_0 = A$ i que estan generats (com a àlgebra sobre el grau zero) pel grau 1, és a dir, $S_\bullet = A[S_1]$ i $T_\bullet = A [T_1]$.

No sé (???) si és cert que els morfismes $Proj(S_\bullet) \to Proj(T_\bullet)$ estan en bijecció amb els morfismes d'anells graduats $T_\bullet \to S_\bullet$, però el que sí que és cert és que tot morfisme d'anells graduats $T_\bullet \to S_\bullet$ indueix un morfisme en els esquemes projectius. Aquests darrers morfismes d'anells estan en bijecció amb morfismes de $A$-mòduls $T_1 \to S_1$.

Però $T_1 \cong \Gamma(Proj(T_\bullet),\ \mathcal{O}(1))$ i $S_1 \cong \Gamma(Proj(S_\bullet),\ \mathcal{O}(1))$, així que estan en bijecció amb els morfismes lineals entre les seccions globals de $\mathcal{O}_{Proj(T_\bullet)}(1)$ i les de $\mathcal{O}_{Proj(S_\bullet)}(1)$.

En particular, si $s_0, \dots, s_n \in S_1$ són un conjunt de generadors de $S_\bullet$ (és a dir, seccions globals que generen $\mathcal{O}_{Proj(S_\bullet)}(1)$), aleshores l'aplicació$$\langle X_0, \dots, X_n \rangle \to \langle s_0, \dots, s_n \rangle,\quad X_i \mapsto s_i$$de $A$-mòduls indueix un morfisme entre les seccions globals de $\mathcal{O}_{\mathbb{P}^n_A}(1)$ i les seccions globals de $\mathcal{O}_{Proj(S_\bullet)}(1)$, així que indueix un morfisme$$Proj(S_\bullet) \to \mathbb{P}^n_A.$$
Així és, per exemple, com es construeix el [[Segre embedding]].

v. [[Morphisms into projective space]] per un resultat general amb aquesta idea.