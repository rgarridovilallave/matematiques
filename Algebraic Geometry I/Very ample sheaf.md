Let $\pi: X \to Y$ be a proper morphism of schemes. We say that an invertible sheaf $\mathcal{L}$ on $X$ is **$\pi$-very ample** if $X = Proj_Y \mathcal{S}_\bullet$ with $\mathcal{L} \cong \mathcal{O}(1)$, where $\mathcal{S}_\bullet$ is a quasi-coherent shea of algebras on $Y$ satisfying
1. $\mathcal{S}_\bullet$ is "generated in degree 1"
2. $\mathcal{S}_1$ is finite type

v. [[The Rising Sea]] 17.2.2.

Alternativament, if there is a **closed** immersion $i: X \to \mathbb{P}^r_Y$ for some $r$, such that $i^* \mathcal{O}(1) \cong \mathcal{L}$.

v. [[Algebraic geometry (Hartshorne)]] II.5.16 +.

*Nota.* El Hartshorne no demana que la immersió sigui tancada, mentre que en Huybrechts sí. A mi em sembla més natural demanar que sigui tancada.

# Interpretació: feix molt ample <-> feix guerxo

Sigui $A$ un anell. L'espai projectiu $n$-dimensional sobre $A$ és $\mathbb{P}^n_A = Proj(A[X_0,\dots,X_n])$. Aquest té el feix guerxo $\mathcal{O}(1)$ i, en general, $\mathcal{O}(d)$ per cada $d \in \mathbb{Z}$.

*Nota.* Tot això es podria fer amb espai projectiu sobre un esquema $Y$, però no ha faré per no complicar les coses.

Un poden considerar esquemes *a dins de $\mathbb{P}^n_A$*, els anomenats **esquemes projectius (sobre $A$)**. Aquests són els esquemes $X$ equipats amb un morfisme $X \to Spec(A)$ projectiu, és a dir, tal que existeix una immersió tancada $i: X \to \mathbb{P}^n_A$ sobre $A$. Ara ens podem preguntar: com generalitzem el feix guerxo $\mathcal{O}(1)$ a l'esquema projectiu $X$ sobre $A$ ?

Una generalització de $\mathcal{O}(1)$ seria un feix $\mathcal{L}$ de $\mathcal{O}_X$-mòduls tal que, quan restringíssim $\mathcal{O}(1)$ a la "imatge de $X$", donés $\mathcal{L}$. Això és demanar que $i^* \mathcal{O}(1) \cong \mathcal{L}$.

Ara bé, en cap moment fixem la immersió $i$. És a dir, un esquema és projectiu sobre $A$ si existeix *alguna* immersió tancada $i: X \to \mathbb{P}^n_A$ a sobre de $A$, i un feix $\mathcal{L}$ és molt ample si existeix *alguna* immersió tancada $i: X \to \mathbb{P}^n_A$  tal que $i^* \mathcal{O}(1) \cong \mathcal{L}$. És a dir, que pensem $X$ en abstracte, sense fixar cap immersió (podria haver-n'hi més d'una!). En particular, també observem que, per tal que un esquema admeti un feix molt ample, cal que aquest sigui projectiu.

*Punt de vista geomètric.* El feix guerxo en l'espai projectiu es pot pensar com les *equacions lineals* definibles en el propi espai, de manera que els zeros d'una secció seva són les *varietats lineals*. De la mateixa forma, els zeros d'una secció d'un feix molt ample són les *restriccions de varietats lineals quan es pensa l'esquema a dins d'un espai projectiu*.

*Eslògan.* Per tant, en general tot allò cert per ($\mathbb{P}^r_A$, $\mathcal{O}(1)$) també serà cert per ($X$ esquema projectiu, $\mathcal{L}$ feix molt ample en $X$).

Això no és així de senzill, i sovint cal afegir-hi detalls tècnics com la Noetherianitat. Alguns exemples de teoremes que es demostren així:
- [[Serre's vanishing theorems]]

Hipòtesis/trucs que poden ser útils, i per què:
- **Noetherianitat:** com que $i: X \to \mathbb{P}^r_A$ és una immersió tancada, és també un morfisme finit. Si $X$ i $\mathbb{P}^r_A$ són Noetherians, aleshores per cada $\mathcal{F} \in Coh(X)$, també $i_*\mathcal{F} \in Coh(\mathbb{P}^r_A)$. v. [[Coherent and quasicoherent modules]]
- **Exactness of $i_*$:** ???? s'utilitza en [[Serre's vanishing theorems]] demo 2. Això en general no és cert.