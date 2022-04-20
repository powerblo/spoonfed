# I : Vector Spaces
## PSET I
### **TF**
1. In any vector space, for all $v\in V$, $av=bv$ implies $a=b$.
**False** : $v$ can be the zero vector.
   **Pf.** Cex. : for some $a\neq b$, if $v=0_V$, $av=bv=0_V$.
   
2. In any vector space, for all $a\in\mathbb{F}$, $av=aw$ implies $v=w$.
**False** : $a$ can be the zero scalar.
   **Pf.** Cex. : for some $v\neq w$, if $a=0$, $av=aw=0_V$.
   
3. For vector spaces over $\mathbb{C}$, it suffices to 
4. The set of all finite sequences equipped with component-wise addition and scalar multiplication is a vector space.
**True** : closure test on $\mathbb{R}^\infty$.
   **Pf.** The set of all sequences $\mathbb{R}^\infty$ is a VS. The subset of finite sequences is closed under addition and scalar products. Due to the subspace test, the subset is a VS.
   
5. A vector space must contain at least one element.
**True** : the null set is not a VS.
   **Pf.** The null set does not satisfy the [[d-vector-space#^31a50e|existence of identity]] axiom.
   
6. A vector space must containt at least two elements.
**False** : the set $\{0_V\}$ is a vector space.
   **Pf.** With the relations $0_V+0_V=0_V$ and $a0_V=0_V$, the vector space axioms are all satisfied.

Let $(V,+,\cdot)$ over $\mathbb{F}$ be a vector space. These problems are about alternative operations.

1. Let $\mathbb{F}=\mathbb{C}$. Define a new scalar multiplication $\cdot|_{\mathbb{R}}$, a restriction of the scalar multiplication on the scalar field $\mathbb{R}$. Then $(V,+,\cdot_\mathbb{R})$ is a vector space.
**True**
   **Pf.** For any axiom involving a single scalar, if $a\in\mathbb{R}$, then $a\in\mathbb{C}$, and thus it holds. For the scalar product associativity axiom, because $\mathbb{R}$ is a subfield of $\mathbb{C}$ closed under multiplication, for any $a,b\in\mathbb{R}$, $ab\in\mathbb{R}$, and thus $a(bv)=(ab)v$ is well defined in the new operation.
   
2. Define a new addition $+^\prime$, such that $a+^\prime b=c\cdot a+c\cdot b$ for some scalar $c$. Then $(V,+^\prime,\cdot)$ is a vector space.
**True**
   **Pf.** 
<br />

### **SNEU**
1. For every $v,w\in V$, there exists $a\in V$ such that $v+a=w$ : for every $v,w\in V$, there exists $a\in V$ such that $w+a=v$ 

These problems are about the [[d-vector-space|vector space axioms]], with an extra step; explain if the two "axioms" A and B can "replace" each other. This means that any vector space that satisfies A', the axioms including A, must also satisfy B', the axioms including B; and vice versa.
Note that this means equivalent statements would indeed be "replacable axioms".
1. Additive inverse axiom : $0v=0_V$ for all $v\in V$
2. Additive identity axiom and additive inverse axiom : for every $v,w\in V$, there exists $a\in V$ such that $v+a=w$
3. Additive identity axiom : vector cancellation (for all $v\in V$, $av=bv$ implies $a=b$)
4. Additive identity axiom : exists $v\in V$ such that for all $a\in F$, $av=v$
## PSET II

### **TF**
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

### **SNEU**
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

### **Additional Problems**
1. Find an [[d-group#D Group|Abelian group]] $V$ and field $F$ such that there are two different definitions of a scalar product making $V$ a vector space over $F$.
2. A vector $v=(a_1,\cdots,a_n)\in\mathbb{R}^n$ is strongly positive if $\forall i,a_i>0$. Prove that a subspace $U$ of $\mathbb{R}^n$ contains a strongly positive vector, then $U$ has a basis consisting of strongly positive vectors.