Assume #. To any $f \in K(X)^\times$, we associate its **principal Weil divisor** as$$(f) := \sum_{Y \subseteq X} v_Y(f) \cdot Y,$$where $Y \subseteq X$ is taken over all prime divisors. (it's a [[Weil divisor]])

We write $(f) = (f)_0 - (f)_\infty$, where $(f)_0 := \sum_{v_Y(f)>0} v_Y(f) Y$ (called **zero divisor**) and $(f)_\infty := \sum_{v_Y(f) <0}(-v_Y(f)) Y$ (called **pole divisor**).

# Propietats

## Well-defined

We have to check that the sum is finite.

*Proof.*

For $f \in K(X) = Q(\mathcal{O}(U))$ for every $\emptyset \neq U \subseteq X$ open. Write $f = g/h$, for $g,h \in \mathcal{O}(U)$.

Pass to $U \cap X_h$, and we can assume $f \in \mathcal{O}(U)$.

The complement of $U$ is closed. Because of Noetherianity, there exist at most finitely many prime divisors contained in the complement $X \setminus U$.

Also for $Y \cap U \neq \emptyset$, all valuations $v_Y(f) \geq 0$. Hence, there exist at most finitely many prime divisors $Y \subseteq X$ such that $v_Y(f) < 0$.

Now we do the same for $f^{-1}$, and we deduce an analogous statement which translates to: there exist at most finitely many prime divisors $Y \subseteq X$ such that $v_Y(f) > 0$.

He're we've used that $v_Y$ is a group homomorphism, hence $v_Y(f^{-1}) = -v_Y(f)$.

## Group homomorphism

$(f \cdot g) = (f) + (g)$. Hence, $K(X)^\times \to Div(X)$, $f \mapsto (f)$ is a group homomorphism.

# Exemples

## Un exemple il·lustratiu en el pla afí

We work in $\mathbb{A}^2_\mathbb{C}$. Consider the *rational function*$$f(X,Y) = \frac{1}{X^2} + \frac{1}{Y} = \frac{X^2 + Y}{X^2Y} \in K(\mathbb{A}^2_\mathbb{C})^\times = \mathbb{C}(X,Y)^\times.$$
The unique prime divisors $Y$ such that $\nu_Y(f) \neq 0$ are those associated to the **prime** ideals $(X^2+Y)$, $(X)$ and $(Y)$ of $\mathbb{C}[X,Y]$, i.e. $Y = V(X^2+Y),\ V(X),\ V(Y)$.

Hence, the **principal divisor** $(f)$ associated to $f$ is$$(f) = 1 \cdot V(X^2 + Y) - 2\cdot V(X^2) - 1 \cdot V(Y).$$
The associated **zero divisor** is$$(f)_0 = 1 \cdot V(X^2 + Y),$$while the associated **pole divisor** is$$(f)_\infty = 2 \cdot V(X^2) + 1 \cdot V(Y).$$

## Affine plane

Take $X = \mathbb{A}^2_k = Spec(k[X_1,X_2])$. Then $f = X_1/X_2 \in K(X) = k(X_1,X_2)$. Define $Y := V(X_1) \subseteq X$.

The zero divisor is $(f)_0 = Y= V(X_1)$, and the pole divisor is $(f)_\infty = V(X_2)$.