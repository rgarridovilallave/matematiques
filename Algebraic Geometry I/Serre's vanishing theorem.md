**Teorema (Serre).** Sigui $X$ un esquema projectiu sobre un anell Noetherià, $\mathcal{O}(1)$ un [[Very ample sheaf]] que és invertible (v. [[Sheaf of modules]].... cal demanar aquesta hipòtesi? no forma part de [[Very ample sheaf]]?), i $\mathcal{F}$ un feix coherent (v. [[Coherent and quasicoherent modules]]) de $\mathcal{O}_X$-mòduls. Existeix un enter $n_0$ tal que, per cada $n \geq n_0$, el feix $\mathcal{F}(n)$ es pot generar per un nombre **finit** de seccions globals.

v. [[Algebraic geometry (Hartshorne)]] II.5.17.

veure també [[Globally generated sheaf]]

# Demostració

**Pas 1:** *Reducció a $X = \mathbb{P}^r_A$.*

**Pas 2:** *Estudi local.*

Podem prendre el recobriment de $\mathbb{P}^r_A$ donat per $U_i := D_+(X_i)$. Com que $\mathcal{F}$ és coherent, $\mathcal{F}|_{U_i}$ és un $A[X_0/X_i, \dots, X_n/X_i]$-mòdul $\tilde M_i$ finitament generat per seccions que es corresponen amb $\{s_{ij}\}_j \subseteq M_i$.

**Pas 2:** *Prolongació de les seccions $s_{ij}$.*

Pel "principi de prolongació analítica" de [[Coherent and quasicoherent modules]], per cada $i$ existeix una $n_i > 0$ tal que $X_i^{n_{ij}} s_{ij} \in \Gamma(U_i, \mathcal{F} \otimes \mathcal{O}(1)^{\otimes n_{ij}})$ estén a una secció global de $\mathcal{F} \otimes \mathcal{O}(1)^{\otimes n_{ij}} \cong \mathcal{F}(n_{ij})$. Prenem $n := max_{ij} n_{ij}$. **qed**

*Achtung!* No veig on s'utilitza la hipòtesi de Noetherianitat.

# Corol·laris

Sigui $X$ un esquema projectiu sobre $A$ anell Noetherià, i sigui $\mathcal{F}$ un feix coherent en $X$. Aleshores $\mathcal{F}$ és un quocient de $\mathcal{O}_X(m)^{\oplus n}$ per algunes $m$, $n$. De fet, es té una successió exacta$$0 \to \mathcal{G} \to \mathcal{O}_X(m)^{\oplus n} \to \mathcal{F} \to 0,$$i $\mathcal{G}$ també és coherent.

v. [[Algebraic geometry (Hartshorne)]] Corollary II.5.18, 

*Demostració.*

Pel Teorema d'Esvaïment de Serre, hi ha una successió exacta $$\mathcal{O}_X^{\oplus n} \to \mathcal{F}(m) \to 0$$per algunes $m$, $n$.

Ara tensoritzem per $-\otimes_{\mathcal{O}_X} \mathcal{O}_X(-m)$, i com que és exacte per la dreta obtenim$$\mathcal{O}_X(-m)^{\oplus n} \to \mathcal{F} \to 0.$$
**qed**

*Achtung 1.* Al Hartshorne hi diu que, en la suma directa $\mathcal{O}(m)_X^{\oplus n}$, hi podríem tenir realment $\mathcal{O}(m_1)_X \oplus \cdots \oplus \mathcal{O}(m_n)_X$.

*Achtung 2.* En aquesta demostració no he vist que $\mathcal{G}$ sigui coherent...