$B$ graded ring, $S \subseteq B$ multiplicative subset consisnting of homogheneous ideals. Then we define$$S^{-1} B := \bigoplus_d (S^{-1}B)_d,\quad (S^{-1}B)_d := \left\{ \frac{a}{b} \mid a \in B_e,\ b \in S \cap B_{e'},\ e-e' = d \right\}.$$
Note that eventhough $B$ is non-negatively graded $S^{-1} B$ can have negative degrees.

# Exemples

## Multiplicative system coming from a prime ideal

Let $\mathfrak{p} \subseteq B$ be a prime ideal. Define $S := \{b \in B \setminus \mathfrak{p}\ \textrm{homogeneous}\}$. Then$$B_{(\mathfrak{p})} := (S^{-1}B)_0$$is the homogeneous localization of $B$ on $\mathfrak{p}$ (note that it's no longer a graded ring).

## Multiplicative system arising from a single element

Let $a \in B_d$ and define $S := \{a^n \mid n \geq 0\}$. Define$$B_{(a)} := (S^{-1}B)_0 = \left\{ \frac{b}{a^n}  \mid b \in B_{nd}\right\} \subseteq S^{-1}B =: B_a.$$
## Exercise 58

$\mathfrak{q} \in Spec(B_{(a)})$, $a \in B_d$ then $\sqrt{\mathfrak{q}B_a} \subseteq B_a$ prime ideal homogeneous.