If $0 \to \mathcal{F}_1 \stackrel{\varphi}{\to} \mathcal{F}_2 \stackrel{\psi}{\to} \mathcal{F}_3 \to 0$ is exact, then $0 \to \mathcal{F}_1(U) \to \mathcal{F}_2(U) \to \mathcal{F}_3(U)$ is exact for every $U$ (note that the zero on the right is missing!).

En altres paraules, $\Gamma(U,-)$ is **left exact**.

*Proof.* (part crítica)

Let $t \in \mathcal{F}_2(U)$ with $\psi_U(t) = 0$. Then $0 = \psi_U(t)_x = \psi_x(t_x)$, so $t_x \in \ker(\psi_x) = im(\varphi_x)$. We can write $t_x = \varphi_x(s^x)$ for some $s^x \in (\mathcal{F}_1)_x$. We have this for every $x$. Now glue the germs. **"qed"**

v. [[Stalk]] "Exactitud".