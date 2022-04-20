#pset
# PSET II
## **TF**
1. A basis can contain the zero vector.
2. An empty collection of vectors is linearly independent.
3. An empty collection of vectors cannot be a generating collection.
4. The span of an empty collection of vectors is empty.
5. In the vector space of polynomials with real coefficients up to degree $n$, $\mathcal{P}_n(\mathbb{R})$, any $n$ collection of polynomials with one polynomial for each degree $1\leq i\leq n$ spans $\mathcal{P}_n(\mathbb{R})$.
6. For arbitrary $S_1,S_2\subset V$, $\text{span}(S_1\cup S_2)=\text{span}(S_1)+\text{span}(S_2)$.
7. Let $\beta$ be a basis of $V$. Then $\beta$ spans $V$ but any proper subset of $\beta$ does not.
8. Let $\beta$ be a basis of $V$. Then $\beta$ is linearly independent in $V$ but any proper [[0-set-theory#D Superset|superset]] of $\beta$ is not. 
9. Let $\beta$ and $\gamma$ be basis vectors of $U$ and $W$, both subspaces of $V$. $\beta\cup\gamma$ is a basis of $U\oplus W$.
10. Let $\beta$ and $\gamma$ be basis vectors of $U$ and $W$, both subspaces of $V$. $\beta\cap\gamma$ is a basis of $U\cap W$.
11. Let $U$ be a subspace of $V$, and $S$ be a linearly independent collection of vectors in $U$. Then $S$ is linearly independent in $V$.
12. A [[d-vector-space#^49ab4e|nontrivial]] vector space $V$ over $\mathbb{R}$ can be written as the union of a finite collection of proper subspaces $\{U_i\}^n_{i=1}$, such that for each $i$, $U_i\varsubsetneq\bigcup_{j\neq i}U_j$.
13. The [[s-dimension-sum-subspace#S Dimension of Sum of Subspaces|equation for the dimension of sum of subspaces]] can be generalised to 3 subspaces; i.e. $\dim(U_1+U_2+U_3)=\dim U_1+\dim U_2+\dim U_3$$-dim(U_1\cap U_2)-\dim(U_2\cap U_3)-\dim(U_3\cap U_1)$$+\dim(U_1\cap U_2\cap U_3)$.
14. The union of three subspaces of $V$ is a subspace if and only if one of the subspaces contains the other two.
15. $\{v_i\}^n_{i=1}$ is a basis of $V$ if and only if $V=\bigoplus_{i=1}^n\text{span}(\{v_i\})$.
16. Let $\{v_i\}_{i\in I}$ be a basis of $V$ and $U$ a subspace of $V$. Then $U=\bigoplus_{i\in I}U\cap\text{span}(\{v_i\})$.
<br />

## **SNEU**
1. $V$ is infinite dimensional : There is a sequence of vectors $v_1,v_2,\cdots\in V$ such that the collection $\{v_i\}^n_{i=1}$ is linearly independent for every positive integer $n$

Let $U_1,U_2,W$ be subspaces of $V$.
1. $U_1+W=U_2+W$ : $U_1=U_2$
2. $V=U_1\oplus W=U_2\oplus W$ : $U_1=U_2$

Let $\{v_i\}^n_{i=1}$ be a collection of vectors $v_i\in V$.
1. $\{v_i\}^n_{i=1}$ is linearly independent : 
	1. For $w_j=\sum^j_{i=1}v_i$, $\{w_j\}^n_{j=1}$ is linearly independent
	2. For $\lambda\in\mathbb{F}$, $\lambda\neq0$, $\{\lambda v_i\}^n_{i=1}$ is linearly independent
	3. $\{v_i+w\}^n_{i=1}$ is linearly dependent if and only if $w\in\text{span}(v_1,\cdots,v_n)$
	4. Every finite subset of $\{v_i\}^n_{i=1}$ is linearly independent
5. $\{v_i\}^n_{i=1}$ is linearly dependent : There exists distinct $w,w_1,\cdots,w_m$ such that $w\in\text{span}(w_1,\cdots,w_m)$

Let $\{v_i\}^n_{i=1}$ and $\{w_j\}^n_{j=1}$ be collections of vectors $v_i,w_j\in V$.
1. $\{v_i\}^n_{i=1}$ and $\{w_j\}^n_{j=1}$ are linearly independent : There exists unique coefficients $\{a_{ij}\}_{1\leq i,j\leq n}$ such that $w_j=\sum^n_{i=1}a_{ij}v_i$

Let $\{U_i\}_{i\in I}$ be a collection of distinct subspaces of $V$.
1. Independence of the collection; for each $i\in I$, $U_i\cap(\sum_{j\neq i}U_j)=\{0\}$ : Uniqueness of expression of zero; $0$ cannot be written as a sum of nonzero vectors from each $U_i$
<br />

## **Additional Problems**
1. Find an [[d-group#D Group|Abelian group]] $V$ and field $F$ such that there are two different definitions of a scalar product making $V$ a vector space over $F$.
2. A vector $v=(a_1,\cdots,a_n)\in\mathbb{R}^n$ is strongly positive if $\forall i,a_i>0$. Prove that a subspace $U$ of $\mathbb{R}^n$ contains a strongly positive vector, then $U$ has a basis consisting of strongly positive vectors.