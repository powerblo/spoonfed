#pset
# PSET III
## **TF**
Let $V$, $W$ be vector spaces. Let $T\in\mathcal{L}(V,W)$.
1. $T$ is an isomorphism if and only if it carries a basis of $V$ to a basis of $W$.
2. For any $U\leq V$, there exists a $T$ such that $\text{ker}(T)=U$.
3. For linear maps between vector spaces over $\mathbb{R}$
	1. $T(\lambda v)=\lambda T(v)$ is enough to imply linearity.
	2. $T(v+w)=T(v)+T(w)$ is enough to imply linearity.

Let $V$ be finite-dimensional. Let $U\leq V$.
4. Let $T\in\mathcal{L}(U,W)$. Then $T$ can be extended to a linear map on $V$; there exists $S\in\mathcal{L}(V,W)$, $\forall u\in U$, $T(u)=S(u)$.
5. Let $T\in\mathcal{L}(U,V)$. Then $T$ can be extended to an invertible operator on $V$; there exists $S\in\mathcal{L}(V)$, $\forall u\in U,T(u)=S(u)$.
  
Let $V$ be finite-dimensional. Let $T$ etc. $\in\mathcal{L}(V)$.
6. Let $T^2=0$. Then $\text{rk}(T)\leq\frac{1}{2}\dim V$.
7. $T_1T_2T_3$ is surjective if and only if $T_2$ is surjective.
8. $T_1T_2=I$ if and only if $T_2T_1=I$.

Let $U,V,W$ be vector spaces. Let $T\in\mathcal{L}(U,V),S\in\mathcal{L}(V,W)$.
1. Prove or disprove. If an inequality is true, when does equality hold?
	1. $\text{im}(ST)=\text{im}(S)$ if and only if $\text{im}(T)=V$
	2. $\text{rk}(ST)\leq\min(\text{rk}(S),\text{rk}(T))$
	3. $\text{ker}(ST)=\text{ker}(T)$ if and only if $\text{ker}(S)=\{0\}$
	4. $\text{null}(ST)\leq\text{null}(S)+\text{null}(T)$
3. If $ST$ is invertible, then $S$ and $T$ are invertible.

Let $T$ etc. $\in\mathcal{L}(V,\mathbb{F})$ for some vector space $V$ over $\mathbb{F}$.
1. Let $u\notin\text{ker}(T)$. $V=\ker{T}\oplus\{au:a\in\mathbb{F}\}$.
2. Let $T_1$ and $T_2$ have the same kernel; they are a constant multiple of each other.
<br />

## **SNEU**
Let $V,W$ be vector spaces. Let $T\in\mathcal{L}(V,W)$.

Let $\beta=\{v_i\}^n_{i=1}$ be a collection of vectors $v_i\in V$.
1.  $\beta$ spans $V$ : $\{Tv_i\}^n_{i=1}$ spans $\text{im }T$
2. $\beta$ is linearly independent in $V$ : $\{Tv_i\}^n_{i=1}$ is linearly independent in $W$

Let $T$ be an operator; $T_1,T_2,T_3\in\mathcal{L}(V)$.
1. $T_1T_2=T_2T_1$ for all $T_2$ : $T_1$ is a scalar multiple of the identity map
2. $T_1=T_2S$ for some $S\in\mathcal{L}(V)$ : $\text{im}(T_1)\subseteq\text{im}(T_2)$
3. $T_1=T_2S$ for some invertible $S\in\mathcal{L}(V)$ : $\text{im}(T_1)=\text{im}(T_2)$
4. $T_2T_1=I$ : $T_2=p[T_1]$ for some polynomial with $\mathbb{F}$ coefficients
5. $T_2$ is surjective : $T_1T_2T_3$ is surjective
6. $T_2$ is invertible, $T_2^{-1}=T_3T_1$ : $T_1T_2T_3=I$

<br />

**Dual Space**
When equipped with the operations of addition and scalar multiplication [[r-operations#^ec8a19|componentwise]], the set of linear maps $\mathcal{L}(V,W)$ becomes a vector space itself.
1. Prove that $V$ and $\mathcal{L}(\mathbb{F},V)$ is isomorphic.

Define an invariant subspace $U\leq V$ of a linear map $T\in\mathcal{L}(V,W)$ to be a subspace *preserved* by $T$; $T(U)\subseteq U$.
1. 