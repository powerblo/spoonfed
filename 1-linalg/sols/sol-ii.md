#pset
# PSET II
## **TF**
1. A basis can contain the zero vector.
2. An empty collection of vectors is linearly independent.
3. An empty collection of vectors cannot be a generating collection.
4. The span of an empty collection of vectors is empty.
5. In the vector space of polynomials with real coefficients up to degree $n$, $\mathcal{P}_n(\mathbb{R})$, any $n$ collection of polynomials with one polynomial for each degree $1\leq i\leq n$ spans $\mathcal{P}_n(\mathbb{R})$.
6. The union of three subspaces of a vector space is a subspace if and only if one of the subspaces contains the other two.

Let $V$ be a vector space. Let $U$ etc. denote subspaces of $V$.
7. For arbitrary $S_1,S_2\subset V$, $\text{span}(S_1\cup S_2)=\text{span}(S_1)+\text{span}(S_2)$.
8. Let $\beta$ and $\gamma$ be basis vectors of $U_1$ and $U_2$.
	1. $\beta\cup\gamma$ is a basis of $U_1\oplus U_2$.
	2. $\beta\cap\gamma$ is a basis of $U_1\cap U_2$.
9. Let $\beta$ be a linearly independent collection of vectors in $U$. 
    $\beta$ is linearly independent in $V$.
10. $V$ is infinite dimensional if and only if there is a sequence of vectors $v_1,v_2,\cdots\in V$ such that the collection $\{v_i\}^n_{i=1}$ is linearly independent for every positive integer $n$.
11. A [[d-vector-space#^49ab4e|nontrivial]] vector space $V$ over $\mathbb{R}$ can be written as the union of a finite collection of proper subspaces $\{U_i\}^n_{i=1}$, such that for each $i$, $U_i\varsubsetneq\bigcup_{j\neq i}U_j$.

Let $V$ be a finite dimensional vector space. Let $U$ etc. denote subspaces of $V$.
12. If $\dim U=\dim V$, then $U=V$.
13. Two vector spaces over the same field with the same cardinality have the same dimension.
14. The [[s-dimension-sum-subspace#S Dimension of Sum of Subspaces|equation for the dimension of sum of subspaces]] can be generalised to 3 subspaces; i.e. $\dim(U_1+U_2+U_3)=\dim U_1+\dim U_2+\dim U_3$$-dim(U_1\cap U_2)-\dim(U_2\cap U_3)-\dim(U_3\cap U_1)$$+\dim(U_1\cap U_2\cap U_3)$.
<br />

## **SNEU**
Let $V$ be a vector space. Let $U$ etc. denote subspaces of $V$.
1. $U_1+U^\prime=U_2+U^\prime$ : $U_1=U_2$
2. $V=U_1\oplus U^\prime=U_2\oplus U^\prime$ : $U_1=U_2$

Let $V$ be a vector space. Let $\beta=\{v_i\}^n_{i=1}$ be a collection of vectors $v_i\in V$.
3. $\beta$ is linearly independent : 
	1. For $w_j=\sum^j_{i=1}v_i$, $\{w_j\}^n_{j=1}$ is linearly independent
	2. For $\lambda\in\mathbb{F}$, $\lambda\neq0$, $\{\lambda v_i\}^n_{i=1}$ is linearly independent
	3. $\{v_i+w\}^n_{i=1}$ is linearly dependent if and only if $w\in\text{span}(v_1,\cdots,v_n)$
	4. Every finite subset of $\{v_i\}^n_{i=1}$ is linearly independent
4. $\beta$ is linearly dependent : 
	1. There exists distinct $w,w_1,\cdots,w_m$ such that $w\in\text{span}(w_1,\cdots,w_m)$
5. $\beta$ is a basis of $V$ :
	1. $\beta$ spans $V$ but any proper subset of $\beta$ does not
	2. $\beta$ is linearly independent in $V$ but any proper [[0-set-theory#D Superset|superset]] of $\beta$ is not
	3. $V=\bigoplus_{i=1}^n\text{span}(\{v_i\})$
	4. For an arbitrary $U\leq V$,  $U=\bigoplus_{i\in I}U\cap\text{span}(\{v_i\})$

Let $V$ be a vector space. Let $\{U_i\}_{i\in I}$ be a collection of distinct subspaces of $V$.
6. Independence of the collection; for each $i\in I$, $U_i\cap(\sum_{j\neq i}U_j)=\{0\}$ : Uniqueness of expression of zero; $0$ cannot be written as a sum of nonzero vectors from each $U_i$
<br />

## **Additional Problems**
1. Find an [[d-group#D Group|Abelian group]] $V$ and field $F$ such that there are two different definitions of a scalar product making $V$ a vector space over $F$.
2. A vector $v=(a_1,\cdots,a_n)\in\mathbb{R}^n$ is strongly positive if $\forall i,a_i>0$. Prove that a subspace $U$ of $\mathbb{R}^n$ contains a strongly positive vector, then $U$ has a basis consisting of strongly positive vectors.
3. Re-solve the following PSET problems, but this time assuming finite scalar fields.
	1. TF 12 : A [[d-vector-space#^49ab4e|nontrivial]] vector space $V$ over a finite $\mathbb{F}$ can be written as the union of a finite collection of proper subspaces $\{U_i\}^n_{i=1}$, such that for each $i$, $U_i\varsubsetneq\bigcup_{j\neq i}U_j$.
4. Common Complement : Let $V$ be over $\mathbb{R}$. Prove that if $U_i$ are subspaces with equal dimension, then there exists a subspace $U^\prime$ such that $V=U^\prime\oplus U_i$ for each $i$.