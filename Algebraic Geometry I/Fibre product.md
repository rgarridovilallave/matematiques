Let $X$ and $Y$ be two $S$-schemes. Their **fibre product** $X \times_S Y$ is the pullback $X \to S \leftarrow Y$ in the category of schemes, which is naturally an $S$-scheme.

# Aplicacions

## Fibre of a morphism

This allows to define the **fibre of a morphism of schemes at a point**. Let $f: X \to Y$ and $y \in Y$. Consider the morphism of schemes $Spec(k(y)) \to Y$, where $k(y)$ is the residue field of $Y$ at $y$. The fibre at $y$ is defined to be the fibre product $X \times_Y Spec(k(y))$. It's denoted $X_y$.

If the point $y$ is the (unique) generic point $\eta$ (in the case that the scheme is integral), then the fibre at $\eta$ is called the **generic fibre.**

## Deformations

Let $X_0$ be a scheme, and $f: X \to Y$ a morphism with $Y$ connected scheme and with $y_0 \in Y$ fixed such that the fibre $f^{-1}(y_0) = X_0$ (such an $f$ is called a family of deformations of $X_0$). The fibres $f^{-1}(y)$ are called deformations of $X_0$.

## Base extension

Let $X \to S$ be an $S$-scheme, and consider $S' \to S$. The $S'$-scheme obtained from $X$ by extending the base along $S' \to S$ is $X \times_S S'$.

## ??

Donat un $k$-scheme $X$ i un automorfisme $\sigma \in Aut(k)$, podem prendre el fibred product $X^\sigma := Spec(k) \times_{Spec(k)} X$, on el morfisme $Spec(k) \to Spec(k)$ és $\sigma$. Els esquemes $X$ i $X^\sigma$ són isomorfs, però en general no són isomorfs com a $k$-esquemes.

## Rational points

Let $K$ be a field, $\pi: X \to Spec(K)$ a $K$-scheme. Define$$X(K) := \{f: Spec(K) \to X \mid \pi \circ f = id_{Spec(K)}\} = Hom_{Sch/K}(Spec(K), X).$$
If $L/K$, then $X(L) := Hom_{Sch/K}(Spec(L),X)$.

## Galois actions

Let $k/k_0$ be a Galois extension with $G = Gal(k/k_0)$. By base change, define the functor$$Sch/k_0 \to Sch/k,\quad X_0 \mapsto X_0 \times_{k_0} k := X_0 \times_{Spec(k_0)} Spec(k).$$
There exists a group homomorphism$$G \to Iso_{Sch/k_0}(X)$$given by the universal property of the fibred product.

This induces:
- An action of $G$ on the **set** of closed points $X_{cl}$ of $X$.
- An action of $G$ on the **set** of $k$-rational points $X(k)$ of $X$.

The [[Teorema Fonamental de la Teoria de Galois]] implies that $X(k)^G = X_0(k_0)$.

## Graphs and diagonals

Let $f: X \to Y$ be a morphism in $Sch_{/S}$. The **graph** of $f$ is the morphism $\Gamma_f: X \to X \times_S Y$ given by $(id,f)$.

As a special case of a graph we have the diagonal, which is the graph of $id: X \to X$. More explicitly, it's the morphism $\Delta_{X/S}: X \to X \times_S X$ given by $(id,id)$.

# Propietats

## Existència

Fibre products exist in $Sch$.

**Remarca.** A posteriori, si analitzem la demostració veurem que hem demostrar les següents fórmules:
1. $Spec(A) \times_{Spec(C)} Spec(B) \cong Spec(A \otimes_C B)$. (**Step 1**)
2. Si $U \subseteq X$ és obert i $p_1: X \times_S Y \to X$ és la projecció a la primera component, aleshores $U \times_S Y \cong p^{-1}(U)$. (**Step 2**)
3. Recobrim $X$ per oberts $\{X_i\}_i$. Aleshores $X \times_S Y$ s'obté d'enganxar $X_i \times_S Y$ en les interseccions $X_{ij} \times_S Y$. (**Step 3**)
4. Si $X \times_S Y$ satisfà que la imatge de $X$ està continguda en $S_0$, aleshores $X \times_S Y \cong X \times_{S_0} Y_0$, on $Y_0$ és l'antiimatge de $S_0$.

*Demostració.*

**Step 1:** *En el món afí*

Sota la correspondència entre esquemes afins i anells, cal resoldre el pushout. Es pren $A \otimes_C B$, i d'aquesta forma $X \times_S Y \cong Spec(A \otimes_C B)$.

**Step 2:** *Suposem que $X \times_S Y$ existeix, i comprovem que $p_1^{-1}(U) \cong U \times_S Y$ per tot obert $U \subseteq X$, on $p_1: X \times_S Y \to X$.*

Sigui $(Z,f,g)$ un con de $U \to S \leftarrow Y$. La composició $Z \stackrel{f}{\to} U \subseteq X$ fa que, per la propietat universal de $X \times_S Y$, existeixi un únic $h: Z \to X \times_S Y$ que ho faci commutar tot. En particular, $p_1 \circ h$ cau a fins de $U \subseteq X$, així que $h$ cau a dins de $p_1^{-1}(U)$. Aquesta $h$ fa verificar a $p_1^{-1}(U)$ la propietat universal.

**Step 3:** *Enganxament en la primera variable.* Suposem que $X$ es pot recobrir per oberts $\{X_i\}_i$, de manera que cada $X_i \times_S Y$ existeix.

***Step 3.1.*** *Candidat a producte fibrat.*

Observem que, pel pas 2, els oberts $U_{ij} := p^{-1}_1(X_{ij}) \subseteq X_i \times_S Y$ són el producte fibrat $X_{ij} \times_S Y$. De la propietat universal obtenim isomorfismes d'esquemes $\varphi_{ij} = \varphi_{ji}$. Això dóna informació d'enganxament $(U_{ij}, \varphi_{ij})_{ij}$ (cal comprovar que se satisfà la identitat triangular). Enganxem els esquemes $U_{ij}$ segons aquesta informació d'enganxament, i aquest és el nostre candidat a producte fibrat.

***Step 3.2.*** *Comprovació que es tracta d'un producte fibrat.*

Això es fa enganxant els morfismes donats per les propietats universals locals (i.e. les de $X_{ij} \times_S Y$), de forma que obtenim una propietat universal global.

**Observació:** El pas 3 aplicat dues vegades demostra l'existència dels productes fibrats $X \times_S Y$ amb $S$ afí i $X,Y$ arbitraris. El recobriment $\{X_i\}_i$ de $X$ que escollim és un recobriment per cartes afins.

**Step 4.** *Cas general ($X$, $Y$, $S$ arbitraris).*

Considerem un recobriment per cartes afins $\{S_i\}_i$ de $S$, i siguin $\{X_i\}_i$ i $\{Y_i\}_i$ les antiimatges de $\{S_i\}_i$ per $X \to S$ i $Y \to S$. Aleshores $X_i \times_{S_i} Y_i$ existeixen (pels passos anteriors).

L'==observació clau== és que $X_i \times_{S_i} Y_i \cong X_i \times_S Y$, ja que un con per $X_i \to S_i \leftarrow Y_i$ és el mateix que un con per $X_i \to S \leftarrow Y$. Això és perquè el morfisme del con que va cap a $X_i$ és a sobre de $S_i$, i la commutativitat implica que el morfisme del con que va cap a $Y$ també ha de ser a sobre de $S_i$ (i per tant ha de caure a dins de $Y_i$).

Amb aquesta observació es dedueix que $X_i \times_S Y$ existeix. Ara utilitzem un dels passos anteriors per veure que $X \times_S Y$ també existeix. **qed**

# Exemples

## Recta projectiva

Considerem els $k$-esquemes $\mathbb{A}^1_k$ (dues vegades). Aleshores l'espai topològic subjacent de $\mathbb{A}^1_k \times_k \mathbb{A}^1_k$ **no coincideix** amb el producte fibrat dels espais topològics subjacents.

## Discrete valuation ring

Let $A$ be a discretre valuation ring (v. [[Discrete valuation ring]]) (in fact suppose that $A = \mathbb{Z}_{(p)}$), and let $Y = Spec(A)$. It has two points: the generic point $\eta$ and the closed point $t$.

Then $X_\eta$ is a scheme over $Spec(\mathbb{Q})$, and $X_t$ is a scheme over $Spec(\mathbb{F}_p)$. This allows two worlds to talk (different characteristics).

If however $Y = k[[x]]$, then $X_\eta$ is a $Spec(k((x)))$-scheme and $X_t$ is a $Spec(k)$-scheme.

## Fibre product between affine schemes

$Spec(A) \otimes_{Spec(C)} Spec(B) \cong Spec(A \otimes_C B)$. Això es demostra amb l'adjunció entre anells i esquemes (v. [[Scheme]], "Spec and global sections are adjoint")

## Nongeometric example...

Prenem $\sigma: \mathbb{Q}(\sqrt{2}) \to \mathbb{Q}(\sqrt{2})$ que envia $\sqrt{2} \mapsto -\sqrt{2}$. Aleshores $X^\sigma$, on $X = Spec(\mathbb{R})$, és ????

## Exemple

Consider $k = \mathbb{C}$, $X \subseteq \mathbb{P}^1_\mathbb{C}$ given by $\mathbb{P}^1_\mathbb{C} \setminus \{0 := [0:1],\ 1:= [1:1],\ \infty := [1:0],\ [\pi:1]\}$. A nontrivial fact is that $\pi$ and $e^\pi$ are algebraically independent (proven in 1996). ... this would work with any pair of algebraically independent numbers.

Consider $$\sigma: \bar{\mathbb{Q}}(\pi,e^\pi) \stackrel{\cong}{\to} \bar{\mathbb{Q}}(\pi,e^{\pi}),\quad \pi \mapsto e^{\pi},\ e^\pi \mapsto \pi.$$
Then $(\mathbb{P}^1_\mathbb{C})^\sigma = \mathbb{P}^1_\mathbb{C}$, and $X^\sigma = \mathbb{P}^1_\mathbb{C} \setminus \{0,1,\infty,[e^\pi:1]\}$. Suppose that $X^\sigma \cong X$ over $Spec(\mathbb{C})$. This isomorphism could be extended to some isomorphism $\mathbb{P}^1_\mathbb{C} \to \mathbb{P}^1_\mathbb{C}$ that permuted $\{0,1,\infty,\pi\} \leftrightarrow \{0,1,\infty,e^\pi\}$. But $Aut(\mathbb{P}^1_\mathbb{C}) = PGL(\mathbb{C}) = GL(2;\mathbb{C})/\mathbb{C}^\times$ (also over $Spec(\mathbb{C})$). This apparently is a contradiction.

## Rational points of the affine space

Let $X = \mathbb{A}^n_K$. Then $\mathbb{A}^n_K(K) \leftrightarrow K^n$.

<-] ?

->] Consider a $K$-rational point $x \in A^n_K(K)$, i.e. $x: Spec(K) \to \mathbb{A}^n_K$ morphism of $K$-schemes. It corresponds to a prime ideal $\mathfrak{p} \in K[X_1,\dots,X_n]$. The map $K[X_1,\dots,X_n] \to k$ factors through the residue field $k(\mathfrak{p})$, so $K$ sits inside $k(\mathfrak{p})$ and hence they're equal.


Més en general, $X = V(\mathfrak{a}) \subseteq \mathbb{A}^n_K$, aleshores $X(K)$ està en bijecció amb $\{(\lambda_1,\dots,\lambda_n) \in K^n \mid F(\lambda_1,\dots,\lambda_n) = 0,\ \forall F \in \mathfrak{a}\}$.sdfghjk

## Field extension $\bar{\mathbb{F}}_p / \mathbb{F}_p$

The Galois group of $\bar{\mathbb{F}}_p/\mathbb{F}_p$ is generated by the Frobenius and isomorphic to $\hat{\mathbb{Z}}$. Consider $X_0 \subseteq \mathbb{A}^n_{\mathbb{F}_p}$ affine scheme given by $F_1,\dots, F_k$. We want to know $X_0(\mathbb{F}_p)$, which are the solution of $F_1 = \cdots = F_n = 0$ in $\mathbb{F}_p^{\oplus n}$. This coincides, by what we've seen, with $X(\bar{\mathbb{F}}_p)^G$.

## Diagonal of the affine line

The diagonal of $\mathbb{A}^1_k$ over $S = Spec(k)$ is$$\Delta_{X/k}: \mathbb{A}^1_k \to \mathbb{A}^1_k \times_k \mathbb{A}^1_k = \mathbb{A}^2_k$$induced by $\varphi: k[X,Y] \to k[X]$, $X,Y \mapsto X$. Note that $ker \varphi = (X-Y)$, so $\Delta_{X/k}$ factors through $V(X-Y) \subseteq \mathbb{A}^2_k$.

## $Spec(K) \times_k Spec(K)$ for field extensions $K/k$

v. [[The Rising Sea]] 9.2.4.

If $K/k$ is a field extension and $G := Gal(K/k)$, then $K \otimes_k K \cong k^{\# G}$. Hence$$Spec(K) \times_k Spec(K) \cong \bigsqcup_{\# Gal(K/k)} Spec(K).$$