#solution
# SOLS I
Note the [[r-notation-conventions#^47625b|remark]] on conventions regarding definition of a vector space in psets.
## **TF**
1. For all $v\in V$, $av=bv$ implies $a=b$.
**False** : $v$ can be the zero vector.
**Pf.** Cex. : for some $a\neq b$, if $v=0_V$, $av=bv=0_V$.

2. For all $a\in\mathbb{F}$, $av=aw$ implies $v=w$.
**False** : $a$ can be the zero scalar.
**Pf.** Cex. : for some $v\neq w$, if $a=0$, $av=aw=0_V$.

3. The set of all finite sequences equipped with component-wise addition and scalar multiplication is a vector space.
**True** : closure test on $\mathbb{R}^\infty$.
**Pf.** The set of all sequences $\mathbb{R}^\infty$ is a VS. The subset of finite sequences is closed under addition and scalar products. Due to the subspace test, the subset is a VS.

4. A vector space must contain at least one element.
**True** : the null set is not a VS.
**Pf.** The null set does not satisfy the [[d-vector-space#^31a50e|existence of identity]] axiom.

5. A vector space must containt at least two elements.
**False** : the set $\{0_V\}$ is a vector space.
**Pf.** With the relations $0_V+0_V=0_V$ and $a0_V=0_V$, the vector space axioms are all satisfied.


Let $(V,+,\cdot)$ be a vector space over $\mathbb{F}$. These problems are about alternative operations.

6. Let $\mathbb{F}=\mathbb{C}$. Define a new scalar multiplication $\cdot|_{\mathbb{R}}$, a restriction of the scalar multiplication on the scalar field $\mathbb{R}$. Then $(V,+,\cdot_\mathbb{R})$ is a vector space.
**True**
**Pf.** For any axiom involving a single scalar, if $a\in\mathbb{R}$, then $a\in\mathbb{C}$, and thus it holds. For the scalar product associativity axiom, because $\mathbb{R}$ is a subfield of $\mathbb{C}$ closed under multiplication, for any $a,b\in\mathbb{R}$, $ab\in\mathbb{R}$, and thus $a(bv)=(ab)v$ is well defined in the new operation.

7. Define a new addition $+^\prime$, such that $a+^\prime b=c\cdot a+c\cdot b$ for some scalar $c$. Then $(V,+^\prime,\cdot)$ is a vector space.
**True**
**Pf.** 

<br />

## **SNEU**
1. For every $v,w\in V$, there exists $a\in V$ such that $v+a=w$ : for every $v,w\in V$, there exists $a\in V$ such that $w+a=v$ 


## Additional Problems
These problems are about alternate axiom systems. For each pair, determine if replacing the [[d-vector-space#D Vector Space|axiom]] with the alternative leads to an alternative formulation of vector spaces.
Note this doesn't necessarily mean the two statements are equivalent; it's the "alternative vectors" obtained from *all the axioms together* that must be inspected.

1. Additive inverse axiom : $0v=0_V$ for all $v\in V$


2. Additive identity axiom and additive inverse axiom : for every $v,w\in V$, there exists $a\in V$ such that $v+a=w$


3. Additive identity axiom : vector cancellation (for all $v\in V$, $av=bv$ implies $a=b$)


4. Additive identity axiom : exists $v\in V$ such that for all $a\in F$, $av=v$

