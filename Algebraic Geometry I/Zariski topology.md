$A$ anell (commutatiu, $1 \neq 0$).

La **topologia de Zariski** en $Spec(A)$ ve donada pels conjunts tancats de la forma $V(\sigma) := \{\mathfrak{p} \mid \sigma \subseteq \mathfrak{p}\}$, per cada ideal $\sigma \subseteq A$.

Una base de la topologia ve donada pels conjunts oberts de la forma $$D(a) := \{\mathfrak{p} \mid a \notin \mathfrak{p}\},$$per $a \in A$.

# Propietats

## Intersecció de tancats

$$\bigcap_i V(\mathfrak{a}_i) = V\left(\sum_i \mathfrak{a}_i\right).$$

*Demostració.*

($\subseteq$) Sigui $\mathfrak{p} \in \bigcap_i V(\mathfrak{a}_i)$, és a dir, $\mathfrak{p}$ ideal primer que conté tots els $\mathfrak{a}_i$. Aleshores $\mathfrak{p}$ conté $\sum_i \mathfrak{a}_i$, així que $\mathfrak{p} \in V(\sum_i \mathfrak{a}_i)$.

($\supseteq$) Sigui $\mathfrak{p} \in V(\sum_i \mathfrak{a}_i)$, és a dir, $\mathfrak{p}$ ideal primer que conté $\sum_i \mathfrak{a}_i$. Com que $\mathfrak{a}_j \subseteq \sum_i \mathfrak{a}_i$ per cada $j$, es dedueix que $\mathfrak{a}_i \subseteq \mathfrak{p}$ per cada $i$ i, per tant, $\mathfrak{p} \in \bigcap_i V(\mathfrak{a}_i)$. **qed**

## Intersecció d'oberts bàsics

$D(f) \cap D(g) = D(fg)$.

*Demo.* $\mathfrak{p} \in D(f) \cap D(g)$ <=> $f, g \notin \mathfrak{p}$ <=>(en ser $\mathfrak{p}$ primer) $fg \notin \mathfrak{p}$ <=> $\mathfrak{p} \in D(fg)$. **qed**

## Tancat disjunt d'un obert bàsic

If $V(\mathfrak{a}) \cap D(f) = \emptyset$, there exists some $n$ such that $f^n \in \mathfrak{a}$.

*Demostració.*

S'ha de veure que $f \in \sqrt{\mathfrak{a}} = \bigcap_{\mathfrak{a} \subseteq \mathfrak{p}} \mathfrak{p}$ (v. [[Ideal radical]]). Sigui $\mathfrak{p}$ un ideal primer que conté $\mathfrak{a}$, és a dir, sigui $\mathfrak{p} \in V(\mathfrak{a})$. Per hipòtesi i primalitat, $\mathfrak{p} \notin D(f)$, és a dir, $f \in (f) \subseteq \mathfrak{p}$. Es dedueix que $f \in \bigcap_{\mathfrak{a} \subseteq \mathfrak{p}} \mathfrak{p} = \sqrt{\mathfrak{a}}$. **qed**

## Recobriments per oberts

Sigui $\{D(a_i)\}_i$ un recobriment per oberts de $Spec(A)$. Aleshores$$\emptyset = Spec(A) \setminus \bigcup_i D(a_i) = \{ \mathfrak{p} \mid \forall i\ a_i \in \mathfrak{p} \} = V((a_i)_i),$$és a dir, no hi ha cap ideal primer $\mathfrak{p} \subseteq A$ tal que $(a_i)_i \subseteq \mathfrak{p}$. En particular tampoc cap ideal maximal, així que deduïm que $(a_i)_i = A$. Per tant:$$\{D(a_i)\}_i \mbox{ recobreix } A \iff (a_i)_i = A.$$
De la mateixa forma, $\{D(a_i)\}_i$ recobreix $D(f)$ si, i només si, $f^n \in (a_i)_i$ per alguna $n$.

## De recobriments a àlgebra

Considerem un recobriment bàsic $\{D(h_i)\}_i$ de $D(f)$. Aleshores$$f \in \mathfrak{p} \iff \mathfrak{p} \notin D(f) \iff \forall i\ \mathfrak{p} \notin D(h_i) \iff \forall i\ h_i \in \mathfrak{p}.$$
En particular es dedueix que$$\sqrt{(f)} = \bigcap_{f \in \mathfrak{p}} \mathfrak{p} = \bigcap_{\forall i\ h_i \in \mathfrak{p}} \mathfrak{p} = \bigcap_i \sqrt{(h_i)} = \sqrt{\bigcap_i (h_i)}.$$
Existeixen $b_i \in A$ tals que $f^n = \sum_i b_i h_i$ per alguna $n$.

*Demostració.*

La condició de ser un recobriment es pot reformular amb tancats com $$V(f) = \bigcap_i V(h_i) \qquad ...= V\left(\sum_i (h_i)\right).$$
Com que $f \in \sqrt{V(f)}$, es dedueix que existeixen $n$ i $b_i \in A$ tals que $f^n = \sum_i b_i h_i$. **qed**

## El punt genèric

Ojo! Cal demanar que $A$ sigui un domini d'integritat, ja que altrament $(0) \notin Spec(A)$.

El punt genèric de $Spec(A)$ és l'ideal nul $(0)$. Propietats:
1. L'adherència de $\{(0)\}$ és tot $Spec(A)$.
2. $Spec(A)$ és Hausdorff si, i només si, $A$ és un cos.

*Demostració (1).*

Vegem que l'únic tancat bàsic que conté $(0)$ és el total. Els tancats bàsics són de la forma$$V(\mathfrak{a}) = \{ \mathfrak{p} \mid \mathfrak{a} \subseteq \mathfrak{p} \},$$així que per tal que $(0) \in V(\mathfrak{a})$ cal que $\mathfrak{a} \subseteq (0)$, és a dir, que $\mathfrak{a}= (0)$ i, per tant, $V(\mathfrak{a}) = Spec(A)$. **qed**

*Demostració (2).*

Si $Spec(A)$ és Hausdorff, $\{(0)\}$ és un tancat, així que $\{(0)\} = \overline{\{(0)\}} = Spec(A)$. Això implica que $A$ té un únic ideal maximal, que és l'ideal nul $(0)$. Per tant, $A$ és un cos. **qed**