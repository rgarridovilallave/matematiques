**Proposta de traducció:** feix guerxo.

Let $d \in \mathbb{Z}$ and $B$ a graded ring. Define the quasi-coherent module $\mathcal{O}(d) := \widetilde{B(d)}$ over $Proj(B)$ v. [[From modules to (quasi-coherent) sheaves of modules]].

Recall $M(d)_e := B_{e+d}$.

# Propietats

## Stalks

Sigui $\mathfrak{p} \in Proj(B)$, és a dir, un ideal primer homogeni tal que $B_+ \nsubseteq \mathfrak{p}$. Aleshores l'stalk de $\mathcal{O}(d)$ en $\mathfrak{p}$ és$$\mathcal{O}(d)_\mathfrak{p} = B(d)_\mathfrak{p} = \left\{ \frac{x}{y} \mid x \in B_{r+d},\ y \in B_{r} \setminus \mathfrak{p} \right\} \subseteq Q(B)_d.$$

# Exemples

## Recta projectiva

Intentem entendre les seccions de $\mathcal{O}_{\mathbb{P}^1_k}(n)$ en l'obert $U = D_+(Y)$, que pensem com $\mathbb{P}^1_k$ menys el punt de l'infinit $\infty=[1:0]$. Per una banda, les seccions del feix estructural són$$\Gamma(U, \mathcal{O}_{\mathbb{P}^1_k}) \cong k[X,Y]_{(Y)} = \left\langle \frac{X^r}{Y^r} \right\rangle_{r \geq 0}.$$
Per altra banda, les seccions del twisted module són$$\Gamma(U, \mathcal{O}_{\mathbb{P}^1_k}(n))\cong k[X,Y](n)_{(Y)}.$$
Si $n = 0$, recuperem el feix estructural. En general, obtenim el $k$-espai vectorial$$\left\langle \frac{X^iY^j}{Y^{i+j-n}} \mid i,j\geq 0,\ i+j \geq n \right\rangle,$$que és el $\Gamma(U,\mathcal{O}_{\mathbb{P}^1_k})$-mòdul$$\Gamma(\mathcal{O}_{\mathbb{P}^1_k}, U) \left\langle Y^{n} \right\rangle$$ja que $$\frac{X^iY^j}{Y^{i+j-n}} = \frac{X^i}{Y^i} \cdot \frac{Y^j}{Y^{j-n}} = \frac{X^i}{Y^i} \cdot Y^n.$$
## Projective spaces

Let $U_i := D_+(X_i) \subseteq \mathbb{P}^n_k$ for $k$ a field. Then$$\mathcal{O}_{\mathbb{P}^n_k}(1)(U_i) = k[X_0/X_i, \dots, X_n/X_i] \langle X_0, \dots, \hat X_i, \dots, X_n \rangle = k[X_0/X_i, \dots, X_n/X_i] \langle X_i \rangle.$$

És a dir, $\mathcal{O}_{\mathbb{P}^n_k}(1)$ és un feix invertible (v. [[Sheaf of modules]]).

Anàlogament, es demostra que$$\mathcal{O}_{\mathbb{P}^n_k(m)}(U_i) = k[X_0/X_i, \dots, X_n/X_i] \langle X_i^m \rangle,$$fins i tot crec que per $m$ negatiu!

Aleshores, per $r \geq 0$, les seccions globals de $\mathcal{O}_{\mathbb{P}^n_k}(r)$ són polinomis homogenis de grau $r$. Els esquemes tallats per una secció global de $\mathcal{O}_{\mathbb{P}^n_k}(r)$ es corresponen, per tant, amb les hipersuperfícies de grau $r$. Per $n = 2$, tenim que $r = 1$ són les rectes, $r = 2$, les còniques, $r = 3$, les cúbiques, $r = 4$, les quàdriques, etc.