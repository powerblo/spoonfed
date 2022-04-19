# Primer
This [[primer-0|primer]] tells a few stories on the applications of linear algebra, and give a rundown of the topics for anyone taking linear algebra for the first time.

# I : Vector Spaces
## Primer
As discussed in the heading primer, linear algebra is a field that studies "linear systems". They're any system (equations, functions, algorithms etc.) that *linearly* take take an input to an output, in the fashion of the linear function $y=mx+b$.
In engineering courses, clarifying what this means using hand-on demonstrations; or perhaps first discussing where these systems appear and how to solve them makes sense. A math oriented course delays this for a bit however, by digressing to really dig into the question "but what *is* a linear system"?
We will use the language of set theory; we claim that a "linear system" is "*some linear* function between *some* sets". The question boils down to specifying what *some linear* functions and *some* sets we're precisely talking about.

To define this *linearity*, it's helpful to take another look at the linear function $z=ax+by$. What is this function really doing? It "scales" the input $x$ by $a$, $y$ by $b$, then adds them together. This means that for the *some* sets we're dealing with, at the very least we want to be able to *define the operations* of *scaling* and *addition*. An important distinction is to make sure we don't mistake scaling for multiplication; $y=x*x=x^2$ for example isn't linear.
What happens when we define such operations upon a set is that we obtain a **vector space**, and call its elements **vectors**. The naming is related to the vector from physics, anything with a direction and magnitude; it happens that you can add two vectors together and scale them, so the set of all (physical) vectors forms a (mathematical) vector space.
<br/ >

## Vector Spaces
Before discussing the formal definition of vectors in linear algebra, here's a quick recap on the intuitive idea of what a vector is.
- **Resource** : The Euclidean vector in Euclidean space is the archetype of vectors, and many of its properties are generalised into abstract ones. Euclidean vectors are frequently described as "an object with magnitude and direction".
- **Resource** : This [video](https://www.youtube.com/watch?v=fNk_zzaMoSs&list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab&index=1) by 3b1b gives two concrete examples and links them to the abstract 'mathematician's' idea of a vector.
- **Resource** : Many instances of data are represented by vectors, as computers are designed to solve problems with linear algebra. In neural networks, input data and output data are considered vectors.
- *Optional* : Vectors have their historical roots in the 'physicist's' idea of a vector, summarised by the aphorism "vectors transform like a vector"; highlighting the intuitive geometric properties of a vector (in relation to a "covector"). Mathematical physics books like Section 1.2 of [[#^533296|Arfken and Weber]] give a rough idea on what this means, but here are some [blogposts](https://www.physicsforums.com/threads/what-does-it-mean-transforms-like-a-vector.699407/post-4431505) and [PSE posts](https://physics.stackexchange.com/questions/155878/what-does-it-mean-to-transform-as-a-scalar-or-vector)) that delve further into this for food for thought.
- *Optional* : In differential geometry, vectors are no longer considered as related to a vector space; instead they're defined through "differential operators". There's a great [article](https://yk-liu.github.io/2018/Vectors-and-One-Forms-on-Manifold/) and [blogpost](https://www.physicsforums.com/threads/tangent-space-in-manifolds-how-do-we-exactly-define.685722/post-4348331) on the topic, and Ch. 12, 14, 15 of [[#^4dff5c|The Road to Reality]] gives a nice introduction to the topic.
<br />

In linear algebra, vectors are *defined* to be an element of a **vector space**.
- **Definition** : [[d-vector-space#D Vector Space|Vector Space]], with [[d-vector-space#Remarks|remarks]]
<br />

A majority of problems in this section consists of either confirming if a given set, scalar and operations *forms a vector space*, or proving if *certain properties* hold in all vector spaces.
- **Statement** : [[s-properties-of-vector-spaces#Summary|Properties of Vector Spaces]], with [[s-properties-of-vector-spaces#Remarks|remarks]]
<br />

The abstract nature of the definition gives several non-intuitive examples of vector spaces, which makes linear algebra greatly applicable.

[[1-matrix-notation|Matrices]] and vectors in Euclidean space are one of the most extensively used examples of vector spaces and vectors. Some notation conventions and definitions are worth mentioning in a linear algebra context. 
- **Resource** : Column vectors are 
- **Resource** : [Einstein notation](https://aditya-sengupta.github.io/expository/einstein.pdf).
<br />

## PSET I
### **TF**
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

### **SNEU**
1. For every $v,w\in V$, there exists $a\in V$ such that $v+a=w$ : for every $v,w\in V$, there exists $a\in V$ such that $w+a=v$ 

These problems are about the [[d-vector-space|vector space axioms]], with an extra step; explain if the two "axioms" A and B can "replace" each other. This means that any vector space that satisfies A', the axioms including A, must also satisfy B', the axioms including B; and vice versa.
Note that this means equivalent statements would indeed be "replacable axioms".
1. Additive inverse axiom : $0v=0_V$ for all $v\in V$
2. Additive identity axiom and additive inverse axiom : for every $v,w\in V$, there exists $a\in V$ such that $v+a=w$
3. Additive identity axiom : vector cancellation (for all $v\in V$, $av=bv$ implies $a=b$)
4. Additive identity axiom : exists $v\in V$ such that for all $a\in F$, $av=v$

## Linear Combination and Bases
A very useful concept that exists in Euclidean space is the "coordinate axis". This allows us to easily assign any point on a map to a set of coordinates and vice versa, which is very advantageous in abstract vector spaces where vectors can be rather fickle to describe otherwise. This also hints at simplifying "coordinate transformations"; instead of rotating the entire space, we can obtain the same result by simply rotating the coordinate axes.

To formalise "coordinate axes", we start off with the easier direction, going from a set of coordinates to a point. Given any *collection of vectors*, a **linear combination** maps a *set of coordinates* to a *specific vector*.
- **Definition** : [[d-linear-combination#D Linear Combination|Linear combination]], with [[d-linear-combination#Remarks|remarks]]
- **Resource** : This [video](https://www.youtube.com/watch?v=k7RM-ot2NWY&list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab&index=2) by 3b1b gives a visual representation on what this means in a Euclidean space context. 
<br />

It's quite clear that not any collection will behave like *coordinate axes*; two reasonable conditions we have are that *every point* in space can be expressed as a linear combination, and that this expression is *unique*. If either fail, mapping a point to a set of coordinates would be impossible. 
In this special case that both hold, we call this collection a **basis** of the vector space.
- **Definition** : Basis
- **Resource** : An [article](https://mikebeneschan.medium.com/how-to-understand-basis-linear-algebra-27a3bc759ae9) that explains bases with an analogy about colour.
<br />

The questions we can ask related to bases are the following;
- Given a collection of vectors, how can we confirm if it's a basis of the vector space?
- What happens to a generating/linearly independent collection of vectors/basis when we add/remove vectors?
- Given a vector space, can we guarantee it has a basis? Is there a systematic method to construct one?
- Can we find a property that all bases of a vector space share?
<br />

### **Generating and Linearly Independent Collections**
Given that we've already defined what a basis is, you could apply it directly to check whether a collection is a basis of the vector space or not. A cleaner and more concise way however, is to consider the "two reasonable conditions" separately; for any collection, if *every point* in the space can be expressed as a linear combination we say it's **generating**, and if every possible expression is *unique* we say it's **linearly independent**.
- **Definition** : Generating Collection
- **Definition** : Linearly Independent Collection
- **Statement** : Equivalent Expressions of Generating and Linearly Independent
<br />

From this, we can conclude a collection of vectors is a *basis if and only if it's generating and linearly independent*.
- **Statement** : Basis Iff Generating and Linearly Independent
<br />

A useful notion to describe the generating property is **span**, which denotes the set of all vectors that *can* be expressed as a linear combination of a collection of vectors. If the span of a collection equals the entire space, it generates the space.
- **Definition** : Span
<br />

Note that while the generating condition explicitly depends on whether the span of the collection equals the *entire* space or not (thus being a *relative* property), linearly independent collections are linearly independent regardless of whatever space they're embedded in (as long as the space actually does contain the collection).
- Embedded spaces
<br />

### **Adding and Removing Vectors to Collections**
Now we are prepared to answer the second question; what happens when we add or remove vectors to a collection of vectors? 
Let us begin by defining an important class of vector spaces; any vector space that can be generated by some finite collection is finite dimensional. 
- **Definition** : [[d-findim-vs#D Finite Dimensional Vector Space|Finite Dimensional]], with [[d-findim-vs#Remark|remarks]]
<br />

We continue by stating a few "obvious" statements; a generating collection upon *adding more vectors is still generating*, and a linearly independent collection upon *removing vectors is still linearly independent*.
- **Statement** : Adding and Removing Vectors to Collections
<br />

Then we state an important lemma that in a linearly dependent collection, there exists an element that can be expressed as a linear combination of the rest, and that removing this element from the collection doesn't change its span. This is the crux of manipulating collections of vectors.
- **Statement** : Linearly Dependent can be Reduced to Linearly Dependent
<br />

The next result is rather surprising; any finite generating collection of vectors can be reduced to a basis. We use exhaustion to cut down the collection until it's linearly independent while keeping its generating property.
- **Statement** : Generating can be Reduced to Basis
<br />

This result implies something even stronger; for any *finite-dimensional* vector space, we can guarantee the *existence of a finite basis*. We simply combine the assumption that the vector space is generated by some finite collection, and the statement above.
- **Statement** : Every Finite Dimensional has a Basis
- *Optional* : What about infinite dimensional spaces? It turns out that there's a [[1-basis-arb-vs|theorem]] that guarantees the existence of a basis for arbitrary vector spaces; the proof involves starkly different methods however, and in many cases (such as the vector space $\mathbb{R}$ over $\mathbb{Q}$) explicitly finding the basis is impossible.
- *Optional* : 
<br />

Similarly, for *finite-dimensional* vector spaces any finite linearly independent collection can be *extended to a basis*. We append to the linearly independent collection a basis of this vector space so it is generating, and use the same lemma as above to remove elements until it becomes a basis.
- **Statement** : Linearly Independent can be Extended to Basis
<br />

To summarise, we have answered the third question; given a finite generating collection of a vector space, we have guaranteed the existence of a basis, and also a method of obtaining it via reducing it to become linearly independent.
<br />

### **Dimension**
The previous section should've hinted to you that length is quite an important property of collections; perhaps even that all bases have the same length. This is a tempting argument to make; in Euclidean space, it makes sense that 2D spaces have two coordinate axes, 3D spaces have three, so on and so forth. It so happens that this is true for finite-dimensional vector spaces, and can even be obtained using the results from the previous section.
- **Statement** : [[s-bases-equal-length#S Bases Have Equal Length|Bases have Equal Length I]]
<br />

A more elegant method is available however; first we state another important lemma that in a finite-dimensional vector space, that any linearly independent collection is shorter or equal in size compared to generating collections.
- **Statement** : Linearly Independent Shorter or Equal than Generating
<br />

Finally, observe that given two bases we can use the inequality above twice to conclude their lengths are equal. 
- **Statement** : [[s-bases-equal-length|Bases have Equal Length II]]
<br />

Because this "length of bases" is no longer dependent on which basis we choose, it is rightfully a property of a finite-dimensional vector space itself, which we call the **dimension** of this vector space.
- **Definition** : [[d-dimension#D Dimension|Dimension]], with [[d-dimension#Remarks|remarks]]
<br />

Dimensions greatly reduce the amount of effort we need to put in say, determining whether a collection is a basis of a vector space or not; the length comparison lemma between linearly independent and generating collections does as well.
We can also prove interesting results about dimensions.
- **Statement** : Linearly Independent of Right Length is Basis
- **Statement** : Generating of Right Length is Basis
<br />

## Subspaces
There's generally one vector space associated with each interpretation of what a vector is. You might have noticed however, that some spaces are subsets of others; this prompts us to ask questions like "can a vector space be reduced/extended to a new vector space?" or "can we check if a subset is a vector space?" Subspaces allow us to ask these questions in a more formal manner.

A **subspace** is a vector space "contained within another", and implicitly shares the operations and scalar field. 
- **Definition** : Subspace
<br />

Because the actual operations are not changed, only a few considerations need to be made to ensure a subset is a subspace.
This is where the condition of *closure* becomes relevant, as it is conceptually possible to have two elements from a subset that map to an element not in that subset (but still in the larger initial space).
- **Statement** : Subspace Test
<br />

Subspaces have a natural connection with the span of a collection of vectors. If the collection were to be linearly independent, then the collection would be a basis of the subspace it generates.
- **Statement** : Span of Collection is Subspace
<br />

### **Direct Sums**
**Direct sums**, are a powerful tool to apply subspaces; a space is a direct sum of two subspaces if every element can be uniquely represented by a sum of an element from each subspace.  A direct sum can be interpreted as "extending a subspace into another dimension", like the direct sum between two subspaces of $\mathbb{R}^3$, $\mathbb{R}^2\oplus\mathbb{R}$.
- **Definition** : [[d-direct-sum|Direct Sum]]
- **Statement** : Direct Sum of Subspaces is Subspace
- **Statement** : Direct Sum Implies Unique Sum Representation
<br />

We can construct new subspaces through direct sums of subspaces, but the surprising fact is that given a subspace, we can decompose the vector space into a direct sum involving this subspace. This decomposition is extremely useful, and as in this [article](https://brilliant.org/wiki/subspace/), the idea of subspaces is prevalent across several areas of math.
- **Statement** : Decomposition into Direct Sum
<br />

Finally, there are equations involving the dimension of the sum of subspaces, which should remind you of the cardinality of the union of sets. 
- **Statement** : [[s-dimension-sum-subspace#Summary|Dimension of Sum of Subspaces]], with [[s-dimension-sum-subspace#Remarks|remarks]]
<br />

## PSET II

### **TF**
1. A basis can contain the zero vector.
2. An empty collection of vectors is linearly independent.
3. An empty collection of vectors cannot be a generating collection.
4. The span of an empty collection of vectors is empty.
5. In the vector space of polynomials with real coefficients up to degree $n$, $\mathcal{P}_n(\mathbb{R})$, any $n$ collection of polynomials with one polynomial for each degree $1\leq i\leq n$ spans $\mathcal{P}_n(\mathbb{R})$.
6. For arbitrary $S_1,S_2\subset V$, $\text{span}(S_1\cup S_2)=\text{span}(S_1)+\text{span}(S_2)$.
7. Let $\beta$ be a basis of $V$. Then $\beta$ spans $V$ but any proper subset of $\beta$ does not.
8. Let $\beta$ be a basis of $V$. Then $\beta$ is linearly independent in $V$ but any proper [[d-set-theory#D Superset|superset]] of $\beta$ is not. 
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
# II : Linear Maps
## Primer
Recall the primer from the previous section; while we have extensively covered the "*some* set" portion, we have yet to give attention to what we mean by "*some linear* function". Here we consider the role of **linear maps**. Maps in linear algebra represent everything from systems of linear equations to expectation values of a random variable, and play an analogous role to functions in calculus.
We are particularly interested in maps that allow us to take advantage of the linear space structure; a good example is rotation of $\mathbb{R}^2$. First note that linear combinations (reprsented by the triangle/parallelogram law as you choose) are preserved under this transformation. Second, note that by simply choosing *where the x-y axes land* after the rotation is enough to characterise the entire rotation. We will take this second property as inspiration to generalise into a definition for linear maps that will hopefully lead to the first property.

Summarising above, we are interested in maps between vector spaces that can be constructed by simply specifying it for the basis vectors of the domain. 
We want to know the value of the map for any arbitrary vector in the domain, but recall that any vector can be expressed as a unique linear combination of the basis vectors; we're already halfway there! 
It might not come as a surprise to you that if this map happens to"preserve this linear combination", we can express the map of an arbitrary vector as a linear combination of the map of basis vectors.
We can do even better! As we expect linear maps to in some way preserve linear independence, we obtain a very useful method to express the range only using basis elements of the domain.

## Linear Maps
What we have discussed in the primer motivates the definition of a linear map, which preserves both addition and scalar multiplication. 
- **Definition** : Linear Map, with remarks
<br />

As expected, this definition leads to us being able to characterise the linear map 

### **Vector Space of Linear Maps**

## Invertibility
### **Kernels and Images**

Surjection and Injection
### **Invertible Maps**

### **Isomorphic Vector Spaces**

## PSET I
### **TF**
1. For linear maps between vector spaces over $\mathbb{R}$, $T(\lambda v)=\lambda T(v)$ is enough to imply linearity.
2. For linear maps between vector spaces over $\mathbb{R}$, $T(v+w)=T(v)+T(w)$ is enough to imply linearity.

Let $V,W$ be fin-dim VSs and $U\leq V$.
4. Let $T\in\mathcal{L}(U,W)$. Then $T$ can be extended to a linear map on $V$; there exists $S\in\mathcal{L}(V,W)$, $\forall u\in U$, $T(u)=S(u)$.
5. There exists $T\in\mathcal{L}(V,W)$ such that 

<br />

### **SNEU**
Let $V,W$ be vector spaces, and $T\in\mathcal{L}(V,W)$.

Fix a collection $\{v_i\}^n_{i=1}$ of vectors $v_i\in V$
1.  $\{v_i\}^n_{i=1}$ spans $V$ : $\{Tv_i\}^n_{i=1}$ spans $\text{im }T$

<br />

## Linear Maps as Matrices
### **Change of Basis**

### **Systems of Linear Equations**

### **Elementary Matrix Operations**

## PSET II
### **TF**
1. For every linear transformation $T\in\mathcal{L}(V)$, there exist bases $\beta,\gamma$ of $V$ such that the matrix $[T]_\beta^\gamma$ is diagonal.
# III : Diagonalisation
## Primer
Now we move on to the second major topic of linear algebra. 

## Eigenvalues and Eigenvectors
### **Invariant Subspaces**

## Diagonalisation

## PSET I
### **TF**
1. Find

<br />

### **SNEU**
1. Let

<br />

### **Geršgorin Disks**


## Normal Forms
### **Generalised Eigenvectors and Algebraic Multiplicity**

### **Decomposition of an Operator**

### **Cayley-Hamilton Theorem**

### **Spectral Mapping Theorem**

### **Jordan Decomposition Theorem**

### **Rational Canonical Form**

## PSET II
### **TF**

# IV : Inner Product Spaces
## Primer
When considering the structure of a vector space, we have taken Euclidean vectors as the archetype and derived all the content of the previous three chapters with the operations of addition and scalar products only. 
By introducing the inner product, we are able to investigate the problem of diagonalisation in much further depth. This chapter will involve many technical 

## Inner Product

### **Orthonormal Bases**

### **Gram-Schmidt Orthonormalisation**

### **Complexification**

### **Riesz Representation Theorem**

## **Operators on Inner Product Spaces**
### **Self-Adjoint and Normal Operators**

### **Unitary and Orthogonal Operators**

### **Spectral Theorem**

### **Positive Operators and Isometries**

### **Polar Decomposition and Singular Value Decomposition**

# V : Duality

## Quotient Spaces

### **The First Isomorphism Theorem**

## Dual Spaces

### **Linear Functionals**

### **Adjoint Maps**

## Multilinear Maps and Tensors

# VI : Topics in Linear Algebra

## Trace and Determinants

## Bilinear and Quadratic Forms

### **Silvester's Law of Inertia**

### **Positive Definite Forms**

## Hilbert Spaces


# Bibliography
1. R. Penrose (2004), The Road to Reality, *Jonathan Cape* ^4dff5c
2. G. B. Arfken, H. J. Weber (2005), Mathematical Methods for Physicists, *Elsevier* ^533296

Exercises used in psets picked from other texts are sourced;
1. S. Axler (2015), Linear Algebra Done Right, *Springer*
2. S. Treil (2017), Linear Algebra Done Wrong, Self-published
3. S. Roman (2008), Advanced Linear Algebra, *Springer*
4. S. H. Friedberg, A. J. Insel, L. E. Spence (1989), Linear Algebra, *Prentice-Hall*