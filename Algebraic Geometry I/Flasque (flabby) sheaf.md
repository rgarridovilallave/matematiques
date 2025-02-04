A sheaf is called **flasque (flabby)** if the restriction map $\mathcal{F}(X) \to \mathcal{F}(U)$ is surjective for every $U$. Equivalently, $\rho_{UV}: \mathcal{F}(U) \to \mathcal{F}(V)$ is surjective for every $V \subseteq U$.

# Propietats

## A lifting problem

For $U \subseteq X$ open, consider$$\underline{\mathbb{Z}}_U(W) := \begin{cases} \underline{\mathbb{Z}}(W),& W \subseteq U,\\ 0,& \textrm{oth.}\end{cases}$$
Then $Hom_{Sh(X)}(\underline{\mathbb{Z}}_U, \mathcal{F}) \cong \mathcal{F}(U)$.

Therefore, if the following lifting problem has a solution for every $V \subseteq U$, then $\mathcal{F}$ is flasque.
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd} {\underline{\mathbb{Z}}_V} & {\underline{\mathbb{Z}}_U} \\ {\mathcal{F}} \arrow[hook, from=1-1, to=1-2] \arrow[from=1-1, to=2-1] \arrow[dashed, from=1-2, to=2-1] \end{tikzcd}
\end{document}
```

Crec que el recíproc també és cert.

## Injective => Flasque

Every injective sheaf is flasque.

*Proof.* La injectivitat de $\mathcal{F}$ fa verificar el lifting problem, ja que $\underline{\mathbb{Z}}_V \to \underline{\mathbb{Z}}_U$ és un monomorfisme. **qed**

## Quan el primer terme d'una ses és flasque

Si en la successió exacta curta$$0 \to \mathcal{F}_1 \to \mathcal{F}_2 \to \mathcal{F}_3 \to 0$$el terme $\mathcal{F}_1$ és flasque, aleshores hi ha una successió exacta curta$$0 \to \mathcal{F}_1(U) \to \mathcal{F}_2(U) \to \mathcal{F}_3(U) \to 0$$per cada obert $U \subseteq X$.

**Corol·lari.** Això és equivalent a dir que $H^1(X,\mathcal{F}_1) =0$ per $\mathcal{F}_1$ flasque.

*Proof.*

***Reducció.*** És suficient veure-ho per $U = X$, ja que la restricció d'una flasque és flasque.

Denote $\varphi: \mathcal{F}_2 \to \mathcal{F}_3$.

Let $s \in \mathcal{F}_3(X)$. We want to see that it comes from $\mathcal{F}_2(X)$.

***Idea.*** Bàsicament veiem que sempre podem engrandir el domini de definició d'un aixecament local de $s$. Això ho formalitzem amb una reducció a l'absurd.

***Step 1.*** *Setup per la reducció a l'absurd: conjunt d'aixecaments locals.*

Considerem el conjunt d'aixecaments locals de $s$, i.e. parelles $(U,t)$, on $U \subseteq X$ és un obert i $t \in \mathcal{F}_2(U)$ satisfà $\varphi(t) = s|_U$. Es pot ordenar mitjançant $(U, t) \leq (U', t')$ <=> $U \subseteq U'$ i $t'|_U = t$.

**Volem veure** que tot element maximal $(U,t)$ satisfà $U = X$.

**Reducció a l'absurd:** suposem que no, i.e. que hi ha algun element maximal $(U,t)$ amb $U \neq X$. Prenem $x \in X \setminus U$.

***Step 2.*** *Aixecament local de $s$ al voltant de $x$.*

Existeix un entorn $x \in U_x \subseteq X$, i una $t_x \in \mathcal{F}_2(U_x)$, tal que $\varphi_{U_x}(t_x) = s|_{U_x}$. Això és perquè $\varphi$ és un epimorfisme (per hipòtesi), així que és exhaustiva en l'stalk de $x$.

***Step 3.*** *Enganxem $t$ i $t_x'$ (secció relacionada amb $t_x$), de manera que haurem trobat un element més gran que $(U,t)$.*

Cal veure que enganxen, és a dir, que $t|_{U \cap U_x} = t_x|_{U \cap U_x}$. De fet això no serà així, però sí que definirem una $t_x'$ que ho satisfarà en lloc de $t_x$.

La diferència $t|_{U \cap U_X} - t_x|_{U \cap U_x}$ és un element de $\mathcal{F}_2(U \cap U_x)$ que s'envia a zero per $\varphi$. Per tant, és al nucli de $\varphi$, és a dir, "viu" a dins de $\mathcal{F}_1(U \cap U_x)$ (per ==exactitud==).

Com que $\mathcal{F}_1$ és ==flasque==, existeix $v \in \mathcal{F}_1(U_x)$ que restringeix a $t|_{U \cap U_x} - t_x|_{U \cap U_x}$. Definim $t_x' := t_x + v$ en $\mathcal{F}_2(U_x)$. Satisfà:
- $\varphi(t'_x) = \varphi(t_x) + \varphi(v) = s|_{U_x} + 0 = s|_{U_x}$, així que aixeca $s$ en $U_x$. Això és perquè $v \in \ker \varphi$ per ==exactitud==.
- $t|_{U \cap U_x} - t'_x|_{U \cap U_x} = t|_{U \cap U_x} - t_x|_{U \cap U_x} - (t|_{U \cap U_x} - t_x|_{U \cap U_x}) = 0$.

Bàsicament, estem aixecant la diferència del que volem que s'anul·li, i l'estem restant al que volem que s'anul·li, així que per força s'ha d'anul·lar. Tenim sort que en afegir aquest terme seguint estant a sobre de $s$, i això és per exactitud. **qed**

## Quan el primer i el segon terme d'una ses són flasque

Si en la successió exacta curta$$0 \to \mathcal{F}_1 \to \mathcal{F}_2 \to \mathcal{F}_3 \to 0$$els termes $\mathcal{F}_1$ i $\mathcal{F}_2$ són flasque, també ho és $\mathcal{F}_3$.

*Demostració.*

Com que $\mathcal{F}_1$ és flasque, tenim successions exactes$$0 \to \mathcal{F}_1(X) \to \mathcal{F}_2(X) \to \mathcal{F}_3(X) \to 0$$i$$0 \to \mathcal{F}_1(U) \to \mathcal{F}_2(U) \to \mathcal{F}_3(U) \to 0,$$i les restriccions $U \subseteq X$ donen un morfisme de successions exactes amb el primer i el segon terme exhaustius (perquè $\mathcal{F}_1$ i $\mathcal{F}_2$ són flasque). El [[Five lemma]] implica que $\mathcal{F}_3(X) \to \mathcal{F}_3(U)$ també és flasque. **qed**

## Flasque => $\Gamma(X,-)$-acíclic

Si $\mathcal{F}$ és flasque, aleshores $\mathcal{F}$ és $\Gamma(X,-)$-acíclic

*Demostració.*

Ja hem vist que $H^1(X,\mathcal{F}) = 0$ en "quan el primer terme d'una ses és flasque".

Considerem una successió exacta curta $$0 \to \mathcal{F} \to \mathcal{I} \to \mathcal{G} \to 0$$amb $\mathcal{I}$ injectiu i, per tant, també flasque. Com que els dos primer termes són flasque, també ho és el tercer. Tenim, per tant, que $H^1(X,\mathcal{F})$, $H^1(X,\mathcal{I})$ i $H^1(X, \mathcal{G})$ s'anul·len.

Inductivament, suposem que la cohomologia $n$-èsima d'un feix flasque s'anul·la. La successió exacta llarga associada a la ses anterior és$$0 = H^n(X,\mathcal{G}) \to H^{n+1}(X,\mathcal{F}) \to H^{n+1}(X,\mathcal{I}) = 0,$$on el primer s'anul·la per HI, i el tercer en ser $\mathcal{I}$ injectiu. Es dedueix que $H^{n+1}(X,\mathcal{F}) = 0$. **qed**

## Flasque => $f_*$-acíclic

Exercici :_(