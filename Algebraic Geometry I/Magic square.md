v. Vakil, també v. https://mathoverflow.net/questions/80797/magic-square-of-fibered-products-vague-unclear

In the following situation:
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd} {X_1} \\ & Y & Z \\ {X_2} \arrow["{f_1}", from=1-1, to=2-2] \arrow["g"', from=2-2, to=2-3] \arrow["{f_2}"', from=3-1, to=2-2] \end{tikzcd}
\end{document}
```
the following is a fibre product (pullback... v. [[Fibre product]])
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd} {X_1 \times_Y X_2} & Y \\ {X_1 \times_Z X_2} & {Y \times_Z Y} \arrow[from=1-1, to=1-2] \arrow[from=1-1, to=2-1] \arrow["{\Delta_{Y/Z}}", from=1-2, to=2-2] \arrow[from=2-1, to=2-2] \end{tikzcd}
\end{document}
```

Demanem que $g \circ f_1 = g \circ f_2$ ????? Em penso que no...

Cert en totes les categories, crec!!!

*Interpretació.* El canvi de base de $\Delta_{Y/Z}: Y \to Y \times_Z Y$ sobre $f_1: X_1 \to Y$, $f_2: X_2 \to Y$, és $X_1 \times_Y X_2 \to X_1 \times_Z X_2$. És a dir, és substituir el primer factor de cada $Y$ per $X_1$, i el segon factor de cada $Y$ per $X_2$.

*Idea demostració.* Escriure explícitament què és un con pel fibre product. Llavors veure que $X_1 \times_Y X_2$ és un con universal. **qed**

# Corol·laris

## $g$ separated

If $g$ is separated, then $\Delta_{Y/Z}$ is a closed immersion, and since closed immersions are stable under basechange, $X_1 \times_Y X_2 \to X_1 \times_Z X_2$ is a closed immersion.