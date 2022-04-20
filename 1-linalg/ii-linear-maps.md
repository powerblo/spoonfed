#notes
[[i-vector-spaces|<- Vector Spaces]]    [[iii-diagonalisation|Diagonalisation ->]]
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

As expected, this definition leads to us being able to uniquely characterise the linear map if we know its values for the basis of the domain.
- **Statement** : Characterisation of Linear Map via Basis

## Invertibility
### **Kernels and Images**
Linear maps are intimately related to the domain and range space it maps on.
The **kernel** or **null space** of a linear map is the set of all vectors in the domain in which the map equals 0; as the name suggests, it forms a subspace of the domain.
- **Definition** : Kernel, with remarks
- **Statement** : Kernel is Subspace
The kernel is intimately related to injectivity of a linear map.
- **Statement** : Injectivity Iff Trivial Null Space

The **image** of a linear map is the set of all vectors in the range that the domain maps to, which forms a subspace of the range.
- **Definition** : Image

A major result involving the relation between a linear map and its domain and range is the **rank-nullity theorem**. Rank and nullity simply refers to the dimension of the image and kernel. 
This theorem states that a sense of "conservation of dimensionality" occurs for every linear map; a vector is either "conserved" (and is mapped to the image) or is "compressed" (and belongs to the kernel).
- **Definition** : Rank and Nullity
- **Theorem** : Rank-Nullity
- **Resources** : The famed [[#^29dcba|diagram]] on dimensionality. 
- **Resources** : [MSE](https://math.stackexchange.com/a/208400), 

This theorem allows us to state the limitations on the properties of a linear map by simply looking at the dimensions of the domain and range.
- **Statement** : Map to Lesser Dimension not Injective
- **Statement** : Map to Greater Dimension not Surjective
- **Statement** : Existence of Injection if Range Greater Dimension
- **Statement** : Existence of Surjection if Range Lesser Dimension

### **Invertible Maps**
Finally, we reach the 

### **Isomorphic Vector Spaces**

## PSET III

[[pset-iii|PSET Link]]

## Linear Maps as Matrices
### **Space of Linear Maps and Linear Maps as Matrices**
In the case of linear maps between finite dimensional vector spaces, maps can be represented in the form of matrices. This gives us the advantage of being able to express many of the results in the previous section using more natural language, whether it be proofs involving linear combinations or the properties of linear maps themselves.

To begin with, we state an interesting property of linear maps; by equipping the entire set of linear maps between two vector spaces with component-wise addition and scalar multiplication, we can give this set a vector space structure itself.

Next, we observe that for linear maps between finite dimensional vector spaces, the property of the linear map being uniquely determined by its values at basis vectors of the domain is intimately connected with the representation of a linear map as a matrix.

### **Change of Basis**

### **Systems of Linear Equations**

### **Elementary Matrix Operations**

### **RREF and Gauss-Jordan Elimination**

Many proofs we have investigated involving manipulation of linear combinations can be considerably simplified if we 
- **Statement** : Alternative Proofs Using Gauss-Jordan Form
  Brilliant wiki

## PSET IV

[[pset-iv|PSET Link]]

[[i-vector-spaces|<- Vector Spaces]]    [[iii-diagonalisation|Diagonalisation ->]]