A **prime divisor** of $X$ is a closed integral subscheme $Y \subseteq X$ of codimension 1.

The **function field** of $Y$ is defined to be $K(Y) := \mathcal{O}_{Y,\eta_Y}$, where we're using assumption # (hence assuming integrality).

Since #, there exists a unique $\eta_Y \in Y$ generic point (its closure is $Y$).
- Function field: $K(Y):= \mathcal{O}_{Y,\eta_Y}$.
- $\mathcal{O}_{X,\eta_Y}$ is a discrete valuation ring.

v. [[Discrete valuation ring]]

Using assumption #, $\mathcal{O}_{X,\eta_Y} \subseteq K(X)$ is a DVR, which has maximal ideal $\mathfrak{m}_{\eta_Y} = (t)$. Think of $t$ as a coordinate which is transversal to $Y$. This gives a valuation$$v_Y:K(X)^\times \to \mathbb{Z},\quad t \mapsto 1.$$
Then $v_Y(\epsilon t^n) = n$ for $\epsilon \in \mathcal{O}^\times_{X,\eta_Y}$.

An element $f \in K(X)^\times$ has a **zero** along $Y \subseteq X$ prime divisor (v. [[Prime divisor]]) if $v_Y(f) >0$.

An element $f \in K(X)^\times$ has a **pole** along $Y \subseteq X$ prime divisor if $v_Y(f) <0$. We call $v_Y(f)$ its **order**.

# Exemples

## Circle in the affine plane

The ideal $(X^2 + Y^2 -1) \subseteq \mathbb{C}[X,Y]$ corresponds to the prime divisor $C$ of $\mathbb{A}^2_\mathbb{C}$ given by the unit circle.

Note that the generic point $\eta_C \in C$ can be described equivalently as:
- The ideal $(X^2 + Y^2 - 1)$ in $\mathbb{C}[X,Y]$.
- The ideal $(0)$ in $\mathbb{C}[X,Y]/(X^2 + Y^2-1)$.

The **function field** of $C$ is$$K(C) = \mathcal{O}_{C,\eta_C} = \mathcal{O}_{\mathbb{C}[X,Y]/(X^2+Y^2-1),\ (0)} = Q\left(\frac{\mathbb{C}[X,Y]}{(X^2+Y^2-1)}\right),$$which are the "generic functions that one can define on $C$". They can have poles because we're taking a generic point; if for instance we fixed a specific point, we would be allowed to have poles only *outside of* that point.

The **discrete valuation ring** is
$$\mathcal{O}_{\mathbb{A}^2_\mathbb{C},\eta_C} = \mathcal{O}_{\mathbb{A}^2_\mathbb{C},\ (X^2+Y^2-1)} = \left\{ \frac{f(X,Y)}{g(X,Y)} \ \Bigg\vert\ X^2 + Y^2 - 1 \nmid g(X,Y) \right\} \subseteq \mathbb{C}(X,Y) = K(\mathbb{A}^2_\mathbb{C}),$$
with maximal ideal $\mathfrak{m}_{\eta_C} = (X^2 + Y^2 - 1)\cdot \mathcal{O}_{\mathbb{A}^2_\mathbb{C}, \eta_C}$.

The **valuation** is hence given by$$\nu_C\left( (X^2 + Y^2 - 1)^r \cdot \frac{f(X,Y)}{g(X,Y)} \right) = r,\quad (X^2 + Y^2 - 1) \nmid f(X,Y),\ g(X,Y).$$
Note that above $r \geq 0$ because the valuation is taken in the discrete valuation ring $\mathcal{O}_{\mathbb{A}^2_\mathbb{C},\eta_C}$ (except from the zero element) instead of the function field of the whole space, $K(\mathbb{A}^2_\mathbb{C}) = \mathbb{C}(X,Y)$.

On the function field of the whole space, $K(\mathbb{A}^2_\mathbb{C}) = \mathbb{C}(X,Y)$, it's given by (except from the zero element, where it's undefined)$$\nu_C\left((X^2 + Y^2 - 1)^r \cdot \frac{f(X,Y)}{g(X,Y)}\right) = r, \quad (X^2 + Y^2 - 1) \nmid f(X,Y),\ g(X,Y).$$
Now the valuation takes values in $\mathbb{Z}$. It becomes clear that it gives the order of the pole / multiplicty of the zero at $C$.

The **quotient field** of $\mathcal{O}_{\mathbb{A}^2_\mathbb{C},\eta_C}$ is$$\mathcal{O}_{\mathbb{A}^2_\mathbb{C}, \eta_C}/\mathfrak{m}_{\eta_C} = \left\{ \frac{f(X,Y)}{g(X,Y)} \ \Bigg\vert\ (X^2 + Y^2 - 1) \nmid g(X,Y) \right\}/(X^2 + Y^2 - 1) = Q\left( \frac{\mathbb{C}[X,Y]}{(X^2 + Y^2 - 1)} \right) = K(C).$$