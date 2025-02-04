Siguin $\mathcal{A}$ i $\mathcal{B}$ dues categories abelianes. Un **$\delta$-functor** és una successió de functors additius $\{T_n\}_{n \geq 0}$ (amb $F_{-1} = 0$) juntament amb morfismes $\delta_n: T_n(C) \to T_{n+1}(A)$ per cada successió exacta $0 \to A \to B \to C \to 0$ tal que:
1. Hi ha **successió exacta llarga** (associada a $0 \to A \to B \to C \to 0$).
2. Cada morfisme de successions exactes curtes indueix un morfisme de successions exactes llargues.

Un $\delta$-functor $T$ s'anomena **universal** si, per cada $\delta$-functor $S$ i cada morfisme $S_0 \to T_0$, existeix un únic morfisme de $\delta$-functors $S \to T$ que estén $S_0 \to T_0$.

*Observació.* En particular, l'estensió $\tilde f: S \to T$ implica que, per cada successió exacta curta $X_\bullet$, s'obté un morfisme induït $\tilde f_n: S_n(X_\bullet) \to T_n(X_\bullet)$.

**Problema:** Donat un functor additiu $F: \mathcal{A} \to \mathcal{B}$, existeix un $\delta$-functor $T$ amb $T_0 = F$?

Si aquest problema té solució amb $T$ universal, $T$ s'anomena **satèl·lit** de $F$.

*Application.* Usually one starts with a left exact functor $F: \mathcal{A} \to \mathcal{B}$, lets $H^0 := F$ and then obtains $H^i$ (when they exist) universal. These $H^i$ are also denoted $R^i F$. v. [[Right derived functors]]

# Propietats

## Determinat pel valor en grau $0$

Si $H^0$ existeix, determina un únic $\delta$-functor amb grau zero igual a $H^0$. (?)

## Erasable => universal

**Theorem (Grothendieck [Tohoku] '57).** If $(H^i,\delta^i)$ is a $\delta$-functor with $H^i$ **erasable** for every $i>0$, then $(H^i,\delta^i)$ is **universal**.

v. [[Erasable functor]]

# Referències

[[Weibel - Homological Algebra]]