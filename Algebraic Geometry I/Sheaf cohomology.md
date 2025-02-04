$H^i$ denote the right derived functors of global sections, and $R^i f_*$ the right derived functors of direct image.
# Propietats

## $R^i f_*$ in terms of $H^i$

Let $f: X \to Y$ be continuous, and let $\mathcal{F}$ be a sheaf on $X$. Then$$R^i f_* \mathcal{F} = \Big[ U \subseteq Y \mapsto H^i(f^{-1}U,\mathcal{F}) \Big]^+.$$
*Proof.*

Take an injective resolution $\mathcal{I}_\bullet$ of $\mathcal{F}$. We can compute $R^i f_* \mathcal{F}$ as the (sheaf theoretic) cokernel of$$im(f_* \mathcal{I}_{i-1} \to f_* \mathcal{I}_i) \to ker(f_* \mathcal{I}_i \to f_* \mathcal{I}_{i+1}).$$
This cokernel is -by definition- the sheafification of the presheaf$$U \mapsto coker\Big( im(f_* \mathcal{I}_{i-1} \to f_* \mathcal{I}_i)(U) \to ker(f_* \mathcal{I}_i(U) \to f_* \mathcal{I}_{i+1}(U)) \Big).$$
**Delicate point:** the image is the sheaf-theoretic one, so we would also need to sheafify. This is why we're not moving $U$ inside of the image.

We now use the definition of $f_*$ and finally obtain that this equals $H^i(f^{-1}U,\mathcal{F})$. **qed**