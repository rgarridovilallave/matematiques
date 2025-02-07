**Theorem.** Let $X$ be Noetherian, and $f: X \to Y$. Consider the diagrams of the form
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd} {Spec(k)} & X \\ {Spec(\mathcal{O}_\nu)} & Y \arrow[from=1-1, to=1-2] \arrow[hook', from=1-1, to=2-1] \arrow["f", from=1-2, to=2-2] \arrow[dashed, from=2-1, to=1-2] \arrow[from=2-1, to=2-2] \end{tikzcd}
\end{document}
```
where $k$ is a valuation field (v. [[Valuation of a field]]), and $\mathcal{O}_\nu$ is its valuation ring.

1. $f$ is **separated** if, and only if, for every solid diagram as above there exists at most one lift.
2. $f$ is **proper** if, and only if, for every solid diagram as above there exists exactly one lift.

Moreover, if $Y$ is also Noetherian, it suffices to check the diagrams with [[Discrete valuation ring]].

v. [[Morphisms of schemes]]

*Nota:* Observem que l'existència de lifts és una condició **local**.

# Demostració

## Separated (first part of the theorem)

=>]

Consider two lifts $\varphi_1$ and $\varphi_2$. We need to show that they're the same.

***Step 1:*** *Set-theoretically.*

Let $\varphi := \varphi_1 \times \varphi_2: Spec(\mathcal{O}_\nu) \to X \times_Y X$. The restriction to $Spec(k) \subseteq Spec(\mathcal{O}_\nu)$ lands in the diagonal $\Delta_f(X)$.

The diagonal is closed because $f$ is separated. Hence, $\varphi(Spec(\mathcal{O}_\nu)) \subseteq \varphi(\bar{\mathfrak{m}}) \subseteq \Delta_f(X)$, so $\varphi_1(\mathfrak{m}) = \varphi_2(\mathfrak{m})$.

***Step 2:*** *Scheme-theoretically.*

Without loss of generality we can assume that $X$ and $Y$ are affine. Obtain that $\varphi$ factors through the diagonal (as schemes). **qed**

## Proper (second part of the theorem)

=>]

We have to construct the lift $\varphi$ (properness implies separatedness which in turn implies that, if it exists, it must be unique).

Let $X' := Spec(\mathcal{O}_\nu) \times_Y X$. We have $\varphi:Spec(k) \to X'$.

$\varphi(\eta) \in X'$, and its closure is a clsoed subset of $X'$.

Since $f$ is proper, $f'$ is also proper (traspose of $f$ on the fibred product that defines $X'$), so $f'(\overline{\varphi(\eta)}) \subseteq Spec(\mathcal{O}_\nu)$ is closed. But $Spec(\mathcal{O}_\nu) = \{\eta,\mathfrak{m}_\nu\}$. Hence $\mathfrak{m}_\nu \in f'(\overline{\varphi(\eta)})$. Hence there exiusts $x \in \overline{\varphi(\eta)}$ such that $f'(x) = \mathfrak{m}_\nu$.

... **qed**

# Exemples

## Line with two origins

Let $X$ be the affine line with double origin, and consider the projection $X \to \mathbb{A}^1_k$. We want to show that this morphism is not separated.

Take the discrete valuation ring $\mathcal{O}_\nu = k[t]_{(t)}$, and $k(t)$. Consider the lifting problem given by $k[x] \to k[t]_{(t)}$, $x \mapsto t$, and $k[x] \to k(t)$, $x \mapsto t$. There are two morphisms solving the lifting problem, depending through which copy of $\mathbb{A}^1_k \subseteq X$ it factors.

## Affine line

We show that $\mathbb{A}^1_k \to Spec(k)$ is not proper. Consider $k(t)$, $\mathcal{O}_\nu = k[t]_{(t)}$. Let $Spec k(t) \to \mathbb{A}^1_k$ be given by $k[X] \to k[t]$, $x \mapsto t^{-1}$, and $Spec(k[t]_{(t)}) \to Spec(k)$ be given by $k \subseteq k[t]_{(t)}$. There are no solutions of the lifting problem because $t^{-1} \notin k[t]_{(t)}$.