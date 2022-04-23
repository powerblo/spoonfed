#pset
# PSET I
## **TF**
1. Find

<br />

## **SNEU**
1. Let

<br />

## Wedderburn-Artin Theorem
In Linear Maps as Matrices, we showed that the space of finite-dimensional linear maps have a matrix representation. This process can be generalised however, and applied to a much wider variety of mathematical objects that behave like linear maps.
The Wederburn-Artin Theorem not only concerns understanding diagonalisable matrices in a different light, but also is related to results about decomposition in fields like representation theory.

As a warm-up, let us investigate a link between linear algebra and ring theory.
Let $T$ be a **simple operator** if the only invariant subspaces under $T$ are $\{0\}$ and $V$.
Let an $R$-module $M$ be a **simple module** if $M$ has no non-trivial proper $R$-submodules. A ring $R$ is a **simple ring** if it is simple as an $R$-module.

1. Let $V$ be finite-dimensional, and $\mathcal{V}\leq\mathcal{L}(V)$ such that for all $S\in\mathcal{L}(V)$ and $T\in\mathcal{V}$, $ST\in\mathcal{V}$ and $TS\in\mathcal{V}$. Prove that $\mathcal{V}=\{0\}$ or $\mathcal{L}(V)$.
   (Prove that the ring of operators has no non-trivial proper ideals, or is a simple ring.)

Let $T$ be a **semi-simple operator** if every invariant subspace of $T$ has a [[s-decomposition-direct-sum|complementary]] invariant subpsace of $T$.
Define the **minimal polynomial** of $T$ to be the monic polynomial of minimal degree such that $p(T)=0$.
1. Prove $T$ is semi-simple if and only if the minimal polynomial is square free.
2. Let $\mathbb{F}$ be algebraically closed. Prove $T$ is semi-simple if and only if it is diagonalisable.

Let an $R$-module $M$ be a **semi-simple module** if every $R$-submodule $N$ of $M$ is an $R$-module direct summand of $M$; $\exists P$, $M=N\oplus P$. 
A ring $R$ is a **semi-simple ring** if it is semi-simple as an $R$-module.
1. Prove $R$ is semi-simple if and only if it is the direct sum of minimal ideals.
2. Prove the subspace of semi-simple operators forms a semi-simple ring.
3. (Wedderburn-Artin Theorem) Prove $R$ is semi-simple if and only if it is isomorphic to a finite product of matrix rings (each over some division ring).
4. Prove that 

## **Geršgorin Disks**
