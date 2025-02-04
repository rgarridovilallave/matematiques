Sigui $A$ un anell i $\mathfrak{a} \subseteq A$ un ideal. El seu **ideal radical**, denotat $rad(\mathfrak{a})$ ó $\sqrt{\mathfrak{a}}$, és l'ideal de $A$ generat pels $x \in A$ tals que $x^n \in \mathfrak{a}$ per alguna $n$.

# Propietats

## Fórmula de la intersecció d'ideals primers

$\sqrt{\mathfrak{a}} = \bigcap_{\mathfrak{a} \subseteq \mathfrak{p}} \mathfrak{p}$, on la intersecció es fa per tots els ideals primers $\mathfrak{p}$ que contenen $\mathfrak{a}$.

## Ideal radical d'un ideal homogeni

Sigui $A$ un anell graduat, i $\mathfrak{a} \subseteq A$ un ideal homogeni. Aleshores $\sqrt{\mathfrak{a}}$ també és homogeni.

*Proof.* Escollim $a = \sum_{d=d_0}^n a_d \in \sqrt{\mathfrak{a}}$. Aleshores $a^n \in \mathfrak{a}$ per alguna $n$, així que $a^n_{d_0} \in \mathfrak{a}$ i, per tant, $a_{d_0} \in \sqrt{\mathfrak{a}}$. Ara repetim l'argument per $a - a_{d_0}$. **qed**