# Vector Spaces

A **vector space** is a collection of vectors that satisfies specific rules for vector addition and scalar multiplication. These vectors typically belong to $\mathbb{R}^{n}$, meaning they have n real-number components. The space includes all linear combinations of its vectors.

**Key Properties:**

1. **Closure under Addition:** Adding two vectors in the space yields another vector in the same space.
2. **Closure under Scalar Multiplication:** Multiplying a vector by a scalar keeps the result in the space.
3. **Zero Vector:** The space always includes the zero vector.
4. **Distributive and Commutative Laws:** These apply to both vector addition and scalar multiplication.

**Examples:**

- $\mathbb{R}^{2}$: Represents all points in a 2D plane.
- $\mathbb{R}^{3}$: Represents all points in 3D space.
## Rules for Vector Spaces and Subspaces
To qualify as a vector space, a set of vectors VV must satisfy **8 axioms**:
1. **Closure under Addition:**  
    For all $u,v \in V$, the sum $u+v\in V$.
    
2. **Closure under Scalar Multiplication:**  
    For all $v\in V$ and scalars $c\in\mathbb{R},cv\in V$.
    
3. **Commutativity of Addition:**  
    $u+v=v+u$.
    
4. **Associativity of Addition:**  
    $(u+v)+w=u+(v+w)$.
    
5. **Existence of Additive Identity (Zero Vector):**  
    There exists $0\in V$ such that $v+0=v$ for all $v\in V$.
    
6. **Existence of Additive Inverse:**  
    For every $v\in V$, there exists $-v\in V$ such that $v+(-v)=0$.
    
7. **Distributive Property for Scalars over Vector Addition:**  
    $c(u+v)=cu+cv$.
    
8. **Distributive Property for Scalars over Scalar Addition:**  
    $(c+d)v=cv+dv$.
    
9. **Associativity of Scalar Multiplication:**  
    $c(dv)=(cd)v$.
    
10. **Multiplicative Identity:**  
    $1v=v$ for all $v\in V$.
    


---
# Subspaces

A **subspace** is a smaller vector space within a larger vector space. For a set to qualify as a subspace, it must:

1. Include the zero vector.
2. Be closed under addition.
3. Be closed under scalar multiplication.

**Key Insight:** A subspace is always "anchored" to the origin (contains the zero vector). For example:

- A plane passing through the origin in $\mathbb{R}^3$ is a subspace.
- A line passing through the origin in $\mathbb{R}^{2}$ or $\mathbb{R}^{3}$ is a subspace.

## Non-Examples

Planes or lines not passing through the origin are **not subspaces** because they fail to include the zero vector or satisfy closure under scalar multiplication.

## Summary of Key Points

1. **Vector Space:** The full collection of vectors following specific rules in $\mathbb{R}^{n}$.
2. **Subspace:** A subset of vectors within a vector space that satisfies the same rules and includes the origin.
3. **Common Subspaces:** The entire vector space itself, planes through the origin, and lines through the origin.

**Example:**

1. **Vector Space:** $\mathbb{R}^{3}$, containing vectors like (1,2,3)(1, 2, 3)(1,2,3).
2. **Subspace:** A plane $ax+by+cz=0$ passing through the origin in $\mathbb{R}^{3}$.

## Rules for Subspaces

A subset SS of a vector space VV is a **subspace** if:

1. **Contains the Zero Vector:**  
    $0\in S$.
    
2. **Closed under Addition:**  
    For all $u,v\in S,u+v\in S$.
    
3. **Closed under Scalar Multiplication:**  
    For all $v\in S$ and scalars $c\in \mathbb{R},cv\in S$.
    

These three rules can be combined into a single requirement:

- If $u,v\in S$, then every linear combination $cu+dv\in S$, where $c,d$ are scalars.

# Summary of Differences Between Vector Spaces and Subspaces:

- **Vector Space:** A complete set of vectors, e.g., $\mathbb{R}^{n}$.
- **Subspace:** A subset of a vector space that includes the origin and is closed under addition and scalar multiplication.