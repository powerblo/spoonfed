#definition 
# D : Ring
A **field** is a set $F$ with two operations, addition and multiplication, that the following properties hold;
- The set $F$ with addition is an [[d-group#D Group|Abelian group]].
- The set $F\setminus\{0\}$ with multiplication is a [[d-algebraic-structure#^844fee|monoid]].

## Unity and Units
- If a ring has a multiplicative identity, it is called **unity**. ^0690fd
- Whether a ring must contain unity or not depends on convention. Authors that include unity in the ring axioms call "rings without unity" as **rngs**. This text does not include existence of unity in the ring axioms.
- An element with a multiplicative inverse in a ring is called a **unit**. ^c498e6
- A ring is a **commutative** ring if it is commutative under multiplication.

## Prime and Irreducible Elements
These definitions hold for commutative rings. Let $R$ be a commutative ring, and $p\in R$ be a nonzero, nonunit element.
- $p\in R$ is **prime** if whenever $p$ divides $ab$ (for some $a,b\in R$), $p$ divides either $a$ or $b$. ^6b8d00
- $p\in R$ is **irreducible** if it is not the product of two nonunit elements.