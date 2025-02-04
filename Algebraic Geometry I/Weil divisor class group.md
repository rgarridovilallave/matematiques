The **(Weil) divisor class group** $Cl(X)$ is the abelian group $Div(X)/\{\textrm{principal\ divisors}\}$. It can also be defined as the quotient of $Div(X)$ by the linear equivalence $\sim$ given by $$\sum n_Y Y \sim \sum m_Y Y \iff \sum_Y (n_Y-m_Y)Y \mbox{ is a principal divisor.}$$
v. [[Principal Weil divisor]]

v. [[Algebraic geometry (Hartshorne)]] II.6. for more details.

# Propietats

## Surjectivity of the restriction map

Assume $X$ satisfies #, and $Z \subsetneq X$ closed. Then the restriction map $Cl(X) \to Cl(U)$ is **surjective**, where $U := X \setminus Z$ open in $X$.

It's well-defined because $K(X) = K(U)$.

Surjectivity is because: If $W \subseteq U$ prime divisor, then $\bar W \subseteq X$ prime divisor.

## Restriction when codimension >1

If $codim(Z \subseteq X) > 1$, then $Cl(X) \cong Cl(X \setminus Z)$.

## Exact sequence

If $Z = Y$ is a prime divisor, then there's an exact sequence$$\mathbb{Z} \to Cl(X) \to Cl(X \setminus Z) \to 0,$$where thre first arrow is given by $1 \mapsto Y$.

# Exemples

## Affine line

$X = \mathbb{A}^1_k$ with $k$ algebraically closed. Then $Cl(\mathbb{A}^1_k) = 0$.

*Proof.*

$Y \subseteq X$ prime divisor is a closed point $\{(X-\lambda)\}$, which is in correspondence with $k$.

The function field is $K(\mathbb{A}^1_k) = k(X)$. Define $f := X - \lambda \in K(\mathbb{A}^1_k)$. This is principal. **qed**

## Spec of principal ideal domains

Let $A$ be a Noetherian, integral (these two conditions are assumed in order for # to be satisfied), **principal ideal domain**. Then $Cl(Spec(A)) = 0$.

*Proof.*

**Step 1.** *Setup.*

Let $Y \subseteq Spec(A)$ be a prime divisor, which is in correspondence with a prime ideal $\mathfrak{p} \subseteq A$. Since $A$ is a ==principal ideal domain==, $\mathfrak{p} = (f)$ for some $f \in A$. This implies that $Y = V(f)$.

**WTS:** *$(f) = Y$.* v. [[Principal Weil divisor]]

**Step 2.**

Consider any $Z \subseteq Spec(A)$ prime divisor, which is associated to some $(g) \subseteq A$ prime ideal (again because of ==PID==). The valuation $\nu_Z: K(Spec(A))^\times = Q(A)^\times \to \mathbb{Z}$ has $\nu_Z(f) = 0$ if $f \notin (g)$.

If $f \in (g)$, then $f = gk$ for some $k \in A$. If $g \notin (f)$, then $k \in (f)$ by primality so $k = f\ell$, i.e. $f = fg\ell$ and this implies (because of ==integrality==) $g \in A^\times$, which is a contradiction because $(g)$ can't be the total ideal (as it represents a prime divisor v. [[Prime divisor]]). This implies that $(f) = (g)$ and hence $Y = Z$.

Therefore,$$(f) = \sum_{Z \subseteq Spec(A)} \nu_Z(f) \cdot Z = 1 \cdot V(f) = Y.$$
**qed**

## Projective line

$\mathbb{P}^1_k$ with $k$ algebraically closed. Then $Cl(\mathbb{P}^1_k) \cong \mathbb{Z}$.

*Proof.*

Prime divisors are just points, corresponding to $[a_0:a_1]$.

Let $Y, Y'$ be two prime divisors corresponding to $[a_0:a_1]$ and $[a_0':a_1']$ (in terms of prime ideals, $(a_1 X_0 - a_0 X_1)$ and $(a_1' X_0 - a_0' X_1)$).

Pbserve that $K(\mathbb{P}^1_k) = k(X_0/X_1)$. Define $f := \frac{a_0 X_1 - a_1 X_0}{a_0' X_1 - a_1' X_0} = \frac{a_0 - a_1 X_0/X_1}{a_0' - a_1' X_0/X_1}$. THe numerator vanishes exactly at $Y$, and the denominator, at $Y'$, i.e. $(f) = Y-Y'$.

As a consequence, any $D = \sum n_Y \cdot Y - \sum n_Y' Y$ with $n_Y, n_Y' > 0$ and $\sum n_Y  = \sum n_{Y'}$ is a principal divisor.

Hence we get a surjective map $Div(\mathbb{P}^1) \to \mathbb{Z}$ given by $\sum n_Y Y \mapsto \sum n_Y$. Its kernel contains all pricipal divisors, so $Cl(\mathbb{P}^1) \cong \mathbb{Z}$. **qed**

## Projective spaces

Let $k$ be a field. The Weil divisor class group of $\mathbb{P}^n_k$ is isomorphic to $\mathbb{Z}$, with generator the hyperplane $H := V_+(X_0) \subseteq \mathbb{P}^n_k$. v. [[Projective space]]