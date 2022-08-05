# Linear Algebra for Quantum Mechanics Part2
----
## Gram-Schmidt Orthonormalization Procedure:

In the last post, [Part I of the Linear Algebra for QM](https://github.com/Anna868/simplified-concepts/blob/main/Linear-Algebra-for-QM-Part1.md) series,
we introduced the idea of vector bases and what it means for a set of vectors to span or cover an entire vector space.

We also introduced what it means for a vector to be normalized (i.e. its magnitude is always 1) and what it means for to vectors to be orthogonal to
each other (i.e. they do not overlap with each other and so their overlapping length is always 0)

In this section, we want to combine these ideas together to obtain a vector basis in which every vector is normalized and at the same time it is also orthogonal
to all other vectors in the basis set.
Such a basis set is better known as an **orthonormal vector basis** and it is very useful in simplifying quantum mechanical calculations.

So the objective of this section is to describe a linear algebraic procedure which converts a generic vector basis into an orthonormal basis for the same
vector space. This procedure is known as the **Gram-Schmidt Procedure**

Instead of presenting a rigorous proof of this procedure, I prefer to rpresent it through a set of examples which makes the logic of the method easier to grasp
and to abstract in higher dimensions of vector spaces.

### Example 1:
Let's consider a one dimensional vector space $\mathbf{V^1}$ which geometrically represents a single line in space that can be represented by a single vector
$|v_1>$ so the entire basis for $\mathbf{V^1}$ is contained in the set ${|v_1>}$

In this case, how can we convert the basis ${| v_1 >}$ into an orthonormal basis?
Well, it's simple! Let's define a new vector $| u_1 >$ such that:

$$|u_1>=\frac{|v_1>}{|| v_1 ||}$$

This way, we have normalized $|v_1>$, but what about the orthogonality condition in this case?
Remember that the definition of orthogonality was that the vector $|v_1>$ shouldn't overlap with any other vector in the basis set. However, the basis set
is completely defined by $|v_1>$ so the orthogonality condition is automatically fulfilled!

So for the one dimensional case, the entire orthonormal basis set is simply given by ${|u_1>}$ as defined above.

### Example 2:
Let's consider a more complicated example with two dimensions, so we have a vector space $\mathbf{V^2}$ which is spanned by the basis set
{ ${|u_1>,|v_2>}$ } with $|u_1>$ the vector representing the orthonormal basis for $\mathbf{V^1}$ from the last example and $|v_1>$ is a generic vector
which is neither normalized nor orthogonal to $|u_1>$

Note that for { ${|u_1>,|v_2>}$ } to form a basis set for $\mathbf{V^2}$, both vectors must be linearly independent, which means that they must have different directions in space as depicted below. To geneeralize the argument, the angle $\theta$ between the two vectors is neither 0 nor is it 90 degrees.

![1659717063860 (3)](https://user-images.githubusercontent.com/47701869/183122089-5f8b6bdd-8cfa-49b2-a0c7-235e6ffac2bd.jpg)

We wish to replace $|v_2>$ with another vector $|w>$ which is orthogonal to $|u_1>$ as shown below:
