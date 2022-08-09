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

![1659721700596 (1)](https://user-images.githubusercontent.com/47701869/183133002-bf6db7a4-8250-4299-8d5a-870ba0042cd7.jpg)

We can express the vector $|v_2>$ as $|w>+|x>$ where $|x>$ is a vector in the direction of $|u_1>$ and whose magnitude is the projection of $|v_2>$ unto $|u_1>$, which is simply the inner product $(|v_2>,|u_1>)$, hence:

$$|x>=(|v_2>,|u_1>)|u_1>$$

$$|v_2>=|w>+|x>$$

So the vector $|w>$ we are looking for becomes simply:

$$|w>=|v_2>-(|v_2>,|u_1>)|u_1>$$

Since $|w>$ is a linear combination of { $|u_1>, |v_2>$ }, it is linearly independent of $|u_1>$ (You can check this by referring to the [last post](https://github.com/Anna868/simplified-concepts/blob/main/Linear-Algebra-for-QM-Part1.md) where I discussed the condition for linear independency!). 
Furthermore, $|w>$ is now orthogonal to $|u_1>$. These two conditions are sufficient to say that the set of vectors { $|u_1>, |w>$ } is an orthogonal basis which spans $\mathbf{V^2}$, but is it also an *orthonormal* basis?

The answer is no, since the vector $|w>$ has not been normalized. Recall that $|u_1>$ is already normalized, so the basis is orthonormal if only $|w>$ is also normalized. Let's denote the normalized version of $|w>$ by $|u_2>$ which is given by:

$$|u_2>=\frac{|w>}{||w||}=\frac{|v_2>-(|v_2>,|u_1>)|u_1>}{|||v_2>-(|v_2>,|u_1>)|u_1>||}$$

Now we have a vector basis { $|u_1>, |u_2>$ } which is completely orthonormal and spans $\mathbf{V^2}$. 

Although this formalism in 2 dimensions helps us to understand the orthonormalization process, it may still not be clear how can we generalize this method to higher dimensions, so we will look at the formalism in 3 dimensions because it gives us an idea of how to generalize this method.

### Example 3:
Let's consider now a vector space $\mathbf{V^3}$ which is spanned by the following vector basis { $|u_1>, |u_2>, |v_3>$ } such that { $|u_1>, |u_2>$ }
is th orthonormal basis set discussed in the last example and $|v_3>$ is a third vector which is linearly independent from both $|u_1>$ and $|u_2>$ but which is orthogonal on neither of these two vectors. This can be seen in the figure below:

![1659724740516 (1)](https://user-images.githubusercontent.com/47701869/183141158-8b8c334e-5720-4460-a109-ebbc3b90a4e4.jpg)

The plane drawn represents the vector space $\mathbf{V^2}$; it is created by the two vectors $|u_1>$ and $|u_2>$. The vector $|v_3>$ doesn't belong to the plane $\mathbf{V^2}$ since it is linearly independent of $|u_1>$ and $|u_2>$. Furthermore, the angle $\theta$ which the vector $|v_3>$ makes with the plane $\mathbf{V^2}$ is neither 0 nor 90 degrees since $|v_3>$ is not orthogonal to $|u_1>$ and $|u_2>$.

We want to replace the vector $|v_3>$ with another vector $|y>$ which is orthogonal to the plane formed by $|u_1>$ and $|u_2>$, consequently $|y>$ would be orthogonal to both $|u_1>$ and $|u_2>$ as shown below

![1659729753826 (1)](https://user-images.githubusercontent.com/47701869/183155766-fa10e47f-3b01-42c1-bf3f-3b0373b2e4d0.jpg)

Once again, we can express $|v_3>$ as the sum of $|y>$ and the projection of $|v_3>$  unto the plane $\mathbf{V^2}$ which I will denote by $|p>$ so we can write:

$$|v_3>=|y>+|p>$$

The projection vector $|p>$ is represented as the sum of the projections of $|v_3>$ on $|u_1>$ and $|u_2>$, hence:

$$|p>=(|v_3>,|u_1>)|u_1>+(|v_3>,|u_2>)|u_2>$$

So the orthogonal vector $|y>$ we are looking is given by:

$$|y>=|v_3>-|p>=|v_3>-(|v_3>,|u_1>)|u_1>-(|v_3>,|u_2>)|u_2>$$

Now we have an orthogonal basis set for $\mathbf{V^3}$ which is { $|u_1>, |u_2>, |y>$ }. However, this set is not orthonormal because $|y>$ is not normalized. Let $|u_3>$ be the normalized version of $|y>$ :

$$|u_3>=\frac{|y>}{||y||}=\frac{|v_3>-(|v_3>,|u_1>)|u_1>-(|v_3>,|u_2>)|u_2>}{|||v_3>-(|v_3>,|u_1>)|u_1>-(|v_3>,|u_2>)|u_2>||}$$

We can't really go on with more examples because it is impossible to visualize higher dimensions, but we can already guess (without visualization) what would happen if we want to obtain an orthonormal basis for $\mathbf{V^4}$ from the basis { $|u_1>,|u_2>,|u_3>, |v_4>$ }.
We can guess right away that the new orthonormal basis would be { $|u_1>,|u_2>,|u_3>, |u_4>$ } with:

$$|u_4>=\frac{|v_4>-(|v_4>,|u_1>)|u_1>-(|v_4>,|u_2>)|u_2>-(|v_4>,|u_3>)|u_3>}{|||v_4>-(|v_4>,|u_1>)|u_1>-(|v_4>,|u_2>)|u_2>-(|v_4>,|u_3>)|u_3>||}$$

We can immediately realize the existence of a pattern in this formula which can be generalized to a vector space of **n** dimensions!

### General Formula of Orthonormalization procedure:

Suppose $|v_1>, \dots, |v_n>$ is a general vector basis for some vector space $\mathbf{V^n}$. Then we can use the **Gram-Schmidt Procedure** to obtain a new orthonormal basis set $|u_1>, \dots, |u_n>$ for the same vector space $\mathbf{V^n}$

**Step 1:** Define the first element of the orthonormal basis as:

$$|u_1>=\frac{|v_1>}{||v_1||}$$

**Step 2:** Define the remaining elements of the orthonormal basis iteratively. For some index **k** in range $1\leq k \leq n-1$ define $|u_{k+1}>$ as:

$$|u'>=|v_{k+1}>-\sum_{i=1}^{k}(|u_i>,|v_{k+1}>)|u_i>$$

$$|u_{k+1}>=\frac{|u'>}{||u'||}$$

----

## Outer Product Representation of Linear Operators:

In the last post, [Part I of the Linear Algebra for QM](https://github.com/Anna868/simplified-concepts/blob/main/Linear-Algebra-for-QM-Part1.md) series, we introduced the idea of **Linear Operators** which are mapping functions that generally map a vector **|v>** in the vector space $\mathbf{V}$ to a different vector **|w>** in a different vector space $\mathbf{W}$ in a process symbolized by $\mathbf{A}: \mathbf{V} \rightarrow \mathbf{W}$

In this section, a very useful representation of linear operators will be given using the notation of inner products. Paradoxically, this representation is known as the **Outer product** representation because it utilizes **Ket-Bra** vector multiplications **|v><w|** as well as **Bra-Ket** vector multiplications **<w|v>** 

Suppose **|v>** is a vector in an inner product space $\mathbf{V}$ and **|w>** is a vector in an inner product space $\mathbf{W}$. We want to define the operation $\mathbf{A}: \mathbf{V} \rightarrow \mathbf{W}$ as **|w><v|**. When the newly defined operator **|w><v|** acts on the vector **|v'>** in $\mathbf{V}$ we write it as:

