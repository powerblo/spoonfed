#pset
# PSET I
## **TF**
1. In any vector space, for all $v\in V$, $av=bv$ implies $a=b$.
2. In any vector space, for all $a\in\mathbb{F}$, $av=aw$ implies $v=w$.
3. For vector spaces over $\mathbb{C}$, it suffices to 
4. The set of all finite sequences equipped with component-wise addition and scalar multiplication is a vector space.
5. A vector space must contain at least one element.
6. A vector space must containt at least two elements.

Let $(V,+,\cdot)$ over $\mathbb{F}$ be a vector space. These problems are about alternative operations.

1. Let $\mathbb{F}=\mathbb{C}$. Define a new scalar multiplication $\cdot|_{\mathbb{R}}$, a restriction of the scalar multiplication on the scalar field $\mathbb{R}$. Then $(V,+,\cdot_\mathbb{R})$ is a vector space.
2. Define a new addition $+^\prime$, such that $a+^\prime b=c\cdot a+c\cdot b$ for some scalar $c$. Then $(V,+^\prime,\cdot)$ is a vector space.
<br />

## **SNEU**
1. For every $v,w\in V$, there exists $a\in V$ such that $v+a=w$ : for every $v,w\in V$, there exists $a\in V$ such that $w+a=v$ 

These problems are about the [[d-vector-space|vector space axioms]], with an extra step; explain if the two "axioms" A and B can "replace" each other. This means that any vector space that satisfies A', the axioms including A, must also satisfy B', the axioms including B; and vice versa.
Note that this means equivalent statements would indeed be "replacable axioms".
1. Additive inverse axiom : $0v=0_V$ for all $v\in V$
2. Additive identity axiom and additive inverse axiom : for every $v,w\in V$, there exists $a\in V$ such that $v+a=w$
3. Additive identity axiom : vector cancellation (for all $v\in V$, $av=bv$ implies $a=b$)
4. Additive identity axiom : exists $v\in V$ such that for all $a\in F$, $av=v$