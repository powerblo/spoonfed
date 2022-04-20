#definition 
# D : Algebraic Structure
An **algebraic structure** consists of a set $A$ (sometimes referred to as the *underlying set*), a collection of operations (of finite [[r-operations#^82ffb3|arity]]), and a finite collection of [[r-axioms|axioms]].

## Common Axioms
Let $\ast$ be some binary operation defined on $A$.
- **Commutativity** : (For all $x,y\in A$) $x\ast y=y\ast x$
- **Associativity** : (For all $x,y,z\in A$) $(x\ast y)\ast z=x\ast(y\ast z)$
- **Existence of Identity** : There exists $e\in A$ (such that for all $x\in A$) $x\ast e=x$ and $e\ast x=x$
- **Existence of Inverse** : (For all $x\in A$) there exists $x^{-1}\in A$ such that $x\ast x^{-1}=e$ and $x^{-1}\ast x=e$
	- A left and right identity/inverse can be defined depending on where the element in question acts from.
Let $+$ be another binary operation defined on $A$.
- **Left Distributivity** : (For all $x,y,z\in A$) $x\ast(y+z)=x\ast y+x\ast z$
- **Right Distributivity** : (For all $x,y,z\in A$) $(y+z)\ast x=y\ast x+z\ast x$
- **Distributivity** holds when both left and right distributivity hold.

## Group-like Structures
- **Magma**/**Groupoid** : Set and a closed binary operation
- **Semigroup** : Associative magma
- **Monoid** : Semigroup with identity ^844fee
- **Group** : Monoid with inverse

## Ring-like Structures
- **Semiring** : Set with two closed binary operations (addition, multiplication), monoid under each operation
- **Ring** : semiring which is Abelian group under addition
	- Whether a ring must contain [[d-ring#^0690fd|unity]] or not depends on convention. Authors that include unity in the ring axioms call "rings without unity" as **rngs**. This text does not include existence of unity in the ring axioms.
- **Commutative Ring** : ring which is commutative under multiplication
	- **Integral Domain** : nonzero commutative ring in which product of any two nonzero elements is nonzero
	- **Unique Factorisation Domain** : ID where every nonzero [[d-ring#^c498e6|nonunit]] element can be written as a product of [[d-ring#^6b8d00|prime elements]], unique up to order and units
	- **Principal Ideal Domain** : ID where every [[d-ideal#D Ideal|ideal]] is [[d-ideal#^a8ccab|principal]]
	- **Euclidean Domain** : ID that can be equipped with a Euclidean function
	- **Noetherian Ring** : ring that satisfies the ascending chain condition on left and right ideals
- **Field** : commutative ring which has multiplicative inverse