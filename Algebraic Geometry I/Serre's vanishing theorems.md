**Teorema (Serre).** Sigui $X$ un esquema projectiu sobre un anell Noetherià $A$, $\mathcal{L}$ un $A$-very ample feix ==invertible (cal demanar aquesta hipòtesi? no forma part de [[Very ample sheaf]]?)==, i $\mathcal{F}$ un feix coherent de $\mathcal{O}_X$-mòduls. Existeix un enter $n_0$ tal que, per cada $n \geq n_0$, el feix $\mathcal{F}(n) := \mathcal{F} \otimes \mathcal{L}^{\otimes n}$ es pot generar per un nombre **finit** de seccions globals.

v. [[Algebraic geometry (Hartshorne)]] II.5.17.

v, [[Very ample sheaf]], [[Coherent and quasicoherent modules]], [[Globally generated sheaf]]

v. https://math.stackexchange.com/questions/231316/sheaves-created-by-global-sections-and-their-cohomology

Més en general, tenim el següent teorema:

**Theorem (Serre).** If $X \to Spec(A)$ is projective, $A$ Noetherian, $\mathcal{L}$ is very ample, and $\mathcal{F} \in Coh(X)$, then:
1. For every $j$, $H^j(X;\mathcal{F})$ is a finite $A$-module.
2. There exists some $n_0$ such that for every $n \geq n_0$, $j > 0$, $H^j(X;\mathcal{F}(n)) = 0$.

v. [[Algebraic geometry (Hartshorne)]] III.5.3.

# Demostració

## Primer teorema

*Proof.*

**Pas 1:** *Reducció a $X = \mathbb{P}^r_A$, $\mathcal{L} = \mathcal{O}_{\mathbb{P}^r_A}(1)$.*

***Pas 1.1.*** *Setup.*

Suppose that the statement is true for every $\mathbb{P}^r_A$. More concretely, if we fix a coherent sheaf $\mathcal{G}$ of $\mathcal{O}_{\mathbb{P}^r_A}$-modules, this means that there exists some $n_0 \geq 0$ such that $\mathcal{G} \otimes \mathcal{O}_{\mathbb{P}^r_A}(n)$ is globally generated for every $n \geq n_0$.

***Pas 1.2.*** *Use the projection formula!*

Since $\mathcal{L}$ is $A$-very ample, there exists an immersion $i: X \to \mathbb{P}^r_A$ for some $r$ such that $i^* \mathcal{O}_{\mathbb{P}^r_A}(1) \cong \mathcal{L}$. Using the projection formula (v. [[Projection formula (sheaves of modules)]]) we have a natural isomorphism$$i_*(\mathcal{F} \otimes_{\mathcal{O}_X} \mathcal{L}^{\otimes n}) \cong i_*\mathcal{F} \otimes_{\mathcal{O}_{\mathbb{P}^r_A}} \mathcal{O}_{\mathbb{P}^r_A}(n),$$and hence an isomorphism$$\mathcal{F} \otimes_{\mathcal{O}_X} \mathcal{L}^{\otimes n} \cong i^*(i_* \mathcal{F} \otimes_{\mathcal{O}_{\mathbb{P}^r_A}} \mathcal{O}_{\mathbb{P}^r_A}(n)).$$
Since the one on the right has global sections for $n \geq n_0$ for some $n_0 \geq 0$ (by hypothesis ...*see the technicality!*), we deduce what we wanted.

***Pas 1.3.*** *Technicality.*

In order to apply the hypothesis we're implicitly using that $i_* \mathcal{F}$ is a coherent sheaf of $\mathcal{O}_Y$-modules. This is in general not true, but it follows because $i$ is a finite morphism between ==Noetherian== schemes.

v. [[Coherent and quasicoherent modules]] "direct and inverse image of (quasi)coherent sheaves"

*Finiteness of $i$.* $i$ is a closed embedding, hence it's finite (v. [[Morphisms of schemes]]).

**Pas 2:** *Estudi local.*

Podem prendre el recobriment de $\mathbb{P}^r_A$ donat per $U_i := D_+(X_i)$. Com que $\mathcal{F}$ és coherent, $\mathcal{F}|_{U_i}$ és un $A[X_0/X_i, \dots, X_n/X_i]$-mòdul $\tilde M_i$ finitament generat per seccions que es corresponen amb $\{s_{ij}\}_j \subseteq M_i$.

**Pas 3:** *Prolongació de les seccions $s_{ij}$.*

Pel "principi de prolongació analítica" de [[Coherent and quasicoherent modules]], per cada $j$ existeix una $n_{ij} > 0$ tal que $X_i^{n_{ij}} s_{ij} \in \Gamma(U_i, \mathcal{F} \otimes \mathcal{O}(1)^{\otimes n_{ij}})$ estén a una secció global de $\mathcal{F} \otimes \mathcal{O}(1)^{\otimes n_{ij}} \cong \mathcal{F}(n_{ij})$. Prenem $n := max_{ij} n_{ij}$. **qed**

*Hipotheses.* The Noetherianity hypothesis is used -at least- in the reduction step (step 1, more concretely 1.3). (maybe it's also used in other places?)

## Demostració d'un cas particular del segon teorema!

El següent resultat és un cas particular del segon teorema, així com també ho són les seues conclusions. Es presenta la seva demostració ja que pot servir per a entendre la demostració del segon teorema. De fet, també servirà per la demostració del cas general.

**Proposició.** $k$ field, $A$ finite type $k$-algebra, $f: X \to Spec(A)$ projective, $\mathcal{F} \in Coh(X)$. Then $H^0(X;\mathcal{F})$ is a finite $A$-module.

*Observació.* En particular $A$ és Noetherià!

*Observació.* Moltes paraulotes però l'únic que estem dient és que les seccions globals estan finitament generades, ja que només estem tractant la cohomologia en grau zero (i no pas en graus positius, on sí que tindríem un resultat una mica més misteriós).

*Proof.* ==TODO!==

**Pas 1.** *Reduce to $X = \mathbb{P}^m_A$.*

Pick a closed embedding $i: X \to \mathbb{P}^m_A$ over $Spec(A)$. Since $$H^0(X,\mathcal{F}) = \mathcal{F}(X) = \mathcal{F}(i^{-1}(\mathbb{P}^m_A)) = i_*\mathcal{F}(\mathbb{P}^m_A) = H^0(\mathbb{P}^m_A, i_\ast \mathcal{F}),$$we can assume that $X = \mathbb{P}^m_A$.

**Pas 2.** *Setup in the projective case.*

We know that there exists a surjection $\mathcal{O}(-n)^{\oplus N} \to \mathcal{F}$. It induces a (not necessarily surjective)$$H^0(\mathbb{P}^m_A, \mathcal{O}(-n))^{\oplus N} \to H^0(\mathbb{P}^m_A;\mathcal{F}),$$which in turn induces $M := \Gamma_*(\mathcal{O}(-n)) \to \Gamma_*(\mathcal{F}).$ Denote with $M'$ the image of this map. Here $\Gamma_*(\mathcal{G}) := \bigoplus_{d \in \mathbb{Z}} \Gamma(\mathcal{G}(d))$ is the space of graded global sections.

**Pas 3.** *The image $M'$ is precisely $\mathcal{F}$.

We have a factorisation$$\Gamma_*(\mathcal{O}(-n))=M \to M' \to \Gamma_*(\mathcal{F})$$of $M \to \Gamma_*(\mathcal{F})$, which induces a factorisation$$\widetilde{\Gamma_*(\mathcal{O}(-n))} = \widetilde{M} \to \widetilde{M'} \to \widetilde{\Gamma_*(\mathcal{F})} \cong \mathcal{F}$$of $\widetilde{M} \to \widetilde{\Gamma_*(\mathcal{F})}$. The last isomorphism uses that $\mathcal{F}$ is quasi-coherent (it's a general fact of quasi-coherent sheaves of modules on Proj-schemes, v. [[Proj]] "global sections").

Since $M \to \Gamma_*(\mathcal{F})$ factors through $M'$, also $\tilde M \to \widetilde{\Gamma_*(\mathcal{F})} \cong \mathcal{F}$ factors through $\tilde M'$.

Since $M = \mathcal{O}(-n)^{\oplus N} \to \mathcal{F}$ is surjective, $\tilde M' \to \mathcal{F}$ must also be surjective. Hence, $\tilde M' \cong \mathcal{F}$.

**Reducció.** *$M$ finite graded $B$-module $\stackrel{?}{\implies}$ $H^0(\mathbb{P}^m;\tilde M)$ is a finite $A$-module.*

**Claim.** *$H^0(\mathbb{P}^m_A;\tilde M)$ is finite over $A$.*

**Pas 2.** *If $M$ is a finite module over $C$, and $C$ Noetherian, then $0 = N_0 \subseteq \cdots \subseteq N_n = N$ such that $N_i/N_{i-1} \simeq C/\mathfrak{p}_i$, with $\mathfrak{p}_i \subseteq C$ prime ideal. The same statement holds for graded $B$-modules, $B$ Noetherian.*

**Reducció.** *We have to show that $H^0(\mathbb{P}^m_A, \tilde{(B/\mathfrak{p})}(n))$ is a finite $A$-module.*

**Reducció.** *$B$ graded $A$-module, integral domain, finitely generated by $B_1$, $B_0$ finite type $k$-algebra.*

**Claim.** *$H^0(Proj(B), \tilde{B(n)})$.*

**Pas 3.** *Pick finitely many nonzero generators $b_1, \dots, b_M \in B_1$ (as $B_0$-module).*

Then $$\mathcal{O}(n) = \tilde{B(n)} \stackrel{\cdot b_i}{\subseteq} \tilde{B(n+1)} \subseteq \cdots,$$so$$H^0(Proj(B), \tilde{B(n)}) \subseteq H^0(Proj(B), \tilde{B(n+1)}) \subseteq \cdots.$$
Since $A$ is Noetherian, it suffices to prove the claim for $n \geq 0$.

Define the graded ring $$B' := \bigoplus_{n \geq 0} H^0(Proj(B), \mathcal{O}(n)).$$
$B$ integral domain, so $B \subseteq Q(B)$. Let $\bar{B} \subseteq Q(B)$ be the integral closure of $B$. We want to show that $B' \subseteq \bar{B}$ is open.

... **qed**

## Segon teorema

*Sketch.*

***Step 1.*** [[Grothendieck's Vanishing Theorem]]

***Step 2 - Reduction.*** *$X = \mathbb{P}^m_A$.*

Pick a closed embedding $i: X \to \mathbb{P}^m_A$ over $Spec(A)$ such that $i^*\mathcal{O}(1) \cong \mathcal{L}$. Observe that $i_*(\mathcal{F} \otimes \mathcal{L}^{\otimes n}) \cong i_*(\mathcal{F} \otimes i^*\mathcal{O}(n)) \cong i_*(\mathcal{F}) \otimes \mathcal{O}(n)$, where we're using [[Projection formula (sheaves of modules)]].

Since $i_*$ is exact, $$H^j(X;\mathcal{F}(n)) \cong H^j(\mathbb{P}^m; i_*(\mathcal{F}(n))) = H^j(\mathbb{P}^m;(i_*\mathcal{F})(n)).$$
***Step 3 - Reduction.*** *It suffices to show (1) and (2) for $H^j(\mathbb{P}^m_A; \mathcal{O}(n))$. i.e.*
1. *$H^j(\mathbb{P}^m_A)$ is a finte $A$-module,*
2. *$H^j(\mathbb{P}^m_A,\mathcal{O}(n)) = 0$ for $n >> 0$, $j > 0$.*

For every $\mathcal{F} \in Coh(\mathbb{P}^m_A)$ there exists$$0 \to \mathcal{F}' = \ker \varphi \to \mathcal{O}(-k)^{\oplus N} \stackrel{\varphi}{\to} \mathcal{F} \to 0$$short exact sequence, so$$H^j(\mathcal{O}(n-k))^{\oplus N} \to H^j(\mathcal{F}(n)) \to H^{j+1}(\mathcal{F}'(n)) \to \cdots.$$
This sequence vanishes at some point by [[Grothendieck's Vanishing Theorem]]. We deduce the reduction.

***Step 4.*** *Cech cohomology computation for $\mathbb{P}^m_A = \bigcup_{i=0}^m D_+(x_i)$.*

We have to show (black boxes! v. [[Algebraic geometry (Hartshorne)]] III.5):
3. $H^0(\mathbb{P}^m;\mathcal{O}(k)) \simeq (A[x_0,\dots,x_m])_0$ (this we already know it)
4. $H^j(\mathbb{P}^m;\mathcal{O}(k)) = 0$ for $0 < j < m$, for every $k$. This is something very special for projective sapces! KIn fact it almost characterizes them.
5. $H^m(\mathbb{P}^m_A;\mathcal{O}(-m-1)) \simeq A$. This is related to [[Serre duality]], which is the geometric version of [[Dualitat de Poincaré]].

**qed**

# Corol·laris

Sigui $X$ un esquema projectiu sobre $A$ anell Noetherià, i sigui $\mathcal{F}$ un feix coherent en $X$. Aleshores $\mathcal{F}$ és un quocient de $\mathcal{O}_X(m)^{\oplus n}$ per algunes $m$, $n$. De fet, es té una successió exacta$$0 \to \mathcal{G} \to \mathcal{O}_X(m)^{\oplus n} \to \mathcal{F} \to 0,$$amb $\mathcal{G}$ també coherent.

v. [[Algebraic geometry (Hartshorne)]] Corollary II.5.18, 

*Demostració.*

Pel Teorema d'Esvaïment de Serre, hi ha una successió exacta $$\mathcal{O}_X^{\oplus n} \to \mathcal{F}(m) \to 0$$per algunes $m$, $n$.

Ara tensoritzem per $-\otimes_{\mathcal{O}_X} \mathcal{O}_X(-m)$, i com que és exacte per la dreta obtenim que$$\mathcal{O}_X(-m)^{\oplus n} \to \mathcal{F} \to 0.$$
**qed**

*Achtung 1.* Al Hartshorne hi diu que, en la suma directa $\mathcal{O}(m)_X^{\oplus n}$, hi podríem tenir realment $\mathcal{O}(m_1)_X \oplus \cdots \oplus \mathcal{O}(m_n)_X$.

*Achtung 2.* En aquesta demostració no he vist que $\mathcal{G}$ sigui coherent...