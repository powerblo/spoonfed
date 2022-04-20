#definition
# D : Sum of Subsets
(Let $S_1$ and $S_2$ be two subsets of a vector space $V$.) The **sum** of the two subsets is $S_1+S_2=\{s_1+s_2:s_1\in S_1,s_2\in S_2\}$.
The definition holds for any collection of subsets $\{S_i\}_{i\in I}$; the sum of this collection is the set of all finite sums from the union, $\sum_{i\in I}S_i=\{s_1+\cdots+s_n:s_j\in\bigcup_{i\in I} S_i\}$.

# D : Direct Sum
(Let $U$ and $W$ be two subspaces of a vector space $V$.) The sum of the two subspaces $U+W$ is a **direct sum** if $U\cap W=\{0\}$.
If the sum is a direct sum, the notation $U\oplus W$ is used to signify it is a direct sum.
The definition holds for any collection of subspaces $\{U_i\}_{i\in I}$ if for each $i\in I$, $U_i\cap(\sum_{j\neq i}U_j)=\{0\}$. The notation $\bigoplus_{i\in I}U_i$ is used to express it is a direct sum.

# D : Internal Direct Sum
A vector space $V$ is the **internal direct sum** of subspaces $U$ and $W$ if $V=U\oplus W$.
The definition holds for any collection of subspaces $\{U_i\}_{i\in I}$ if $V=\bigoplus_{i\in I}U_i$.