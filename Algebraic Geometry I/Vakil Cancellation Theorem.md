v. [[The Rising Sea]] 10.1.19.

Consider a property $(P)$ of morphisms of schemes such that:
1. $(P)$ is preserved under composition.
2. $(P)$ is stable under base change.

Then, given two morphisms $X \stackrel{f}{\to} Y \stackrel{g}{\to} Z$ such that $g \circ f$ and $\Delta_g$ have $(P)$, also $f$ has $(P)$.

*Proof.*

Note that $f$ factors as $X \to X \times_Z Y \to Y$. We have to see that both morphisms satisfy (P).

1. The scheme $X$ is the pullback of $X \times_Z Y \to Y \times_Z Y \leftarrow Y$ by the [[Magic square]], where we have $(f, id_Y): X \times_Z Y \to Y \times_Z Y$ and $\Delta_g: Y \to Y \times_Z Y$. Since $\Delta_g$ satisfies (P), $X \to X \times_Z Y$ also satisfies (P).
2. The scheme $X \times_Z Y$ is the pullback of $Y \to Z \leftarrow X$. Since $X \to Z$ satisfies (P), $X \times_Z Y \to Y$ also satisfies (P).

**qed**

Cert en totes les categories???? Crec que sí! !!!!! :)))