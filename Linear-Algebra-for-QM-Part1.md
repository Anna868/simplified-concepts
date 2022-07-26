# Linear Algebra For Quantum Mechanics (Part I)
---
If you hear someone speaking a foreign language for the first time, you will be confused, and naturally you will not understand what he is trying to say!

But if you spend a few days with this person, and maybe use an application like Duolingo to help you with the basic vocabulary of the language, then gradually
 you will be able to understand the language when it is spoken!

The native language of Quantum Mechanics is Linear Algebra.
Every sentence written to express a Quantum Mechanical phenomenon is most likely a linear algebraic expression.

So it follows that learning Quantum Mechanics is as easy as learning Linear Algebra, and as it turns out, learning Linear Algebra is pretty easy even
 if you have little to no background on the subject!
 
So what exactly is Linear Algebra?

![linear_algebra](https://user-images.githubusercontent.com/47701869/180783927-55abfb13-c7f4-4ad8-8bec-99352de430b4.png)


It is the language describing vector spaces and the linear operations we can perform on vectors inside those spaces.

(In a previous post, I already talked about vector spaces by giving a quick overview of the topic.
Check it [here](https://github.com/Anna868/simplified-concepts/blob/main/Hilbert-Spaces.md) out if the word “vector spaces” seems new to you!)

As any other language, Linear Algebra has its own vocabulary and grammar which we use to write correct sentences!
We often refer to this linear algebraic grammar as the ‘notation’ of writing down things.

So in this series of posts, we will focus more on the formal notations of Linear Algebra and work through simple exercises together.
Think of this as your first time trying to hold a pen to write your first grammatically correct sentence in the foreign language that you are trying to learn!

Note: Although there were some equations in my previous post on [Hilbert Spaces](https://github.com/Anna868/simplified-concepts/blob/main/Hilbert-Spaces.md), there weren’t any formal introduction to the notations
of linear algebraic expressions in Quantum Mechanics. The equations were beside the point; but in this post they are the main objective.

By the end of this post, you should understand a little bit about this Schrodinger's cat meme!
![image](https://user-images.githubusercontent.com/47701869/180876474-ecdf9c74-af76-442c-ae1a-a2e8493331c4.png)


## Vectors and the Dirac (Bra-Ket Notation):

* In our discussions, we will be dealing with complex vector spaces of finite dimensions.
A capitalized bold letter usually refers to the vector space we are dealing with, and the number of its dimensions is usually written as a superscript to the capital bold letter

$$ \mathbf{V}^n $$

* The elements of any complex vector space are called vectors. Each vector represents a group of complex numbers
$$z_1,..,z_n$$
This is not really how we write vectors down.
As you shall see, there are multiple formal ways to write down vectors. One of them is the column matrix representation:

$$ \begin{pmatrix}
z_1 \\
\vdots \\
z_n
\end{pmatrix} $$

* Beside representations that show the full contents of a vector, there are in-line representations that symbolize the presence of a vector. One such in-line representation for a vector v is given by:

$$ \vec{v} $$

* The above in-line representation is the most common, but it is not the standard representation in QM. Instead, in QM we use the Dirac notation of vectors which is written as:

$$ |v> $$ 

* The notation |v> is also called a **ket** indicating that v is a column vector
* Any vector space contains two special operations: Addition of two vectors and multiplication of a vector by a constant number (a scalar). Let's see each of these operations expressed in the matrix column notation.
* Suppose we want to add two vectors |v> and |z>, this is expressed as adding the respective numbers inside the two vectors together:

$$ \begin{pmatrix}
z_1 \\
\vdots \\
z_n
\end{pmatrix}
+
\begin{pmatrix}
v_1 \\
\vdots \\
v_n
\end{pmatrix} = 
\begin{pmatrix}
v_1+z_1 \\
\vdots \\
v_n+z_n
\end{pmatrix}$$

* Suppose we want to multiply the vector |v> by a constant number z, this is expressed as multiplying each individual number of the vector |v> by this constant number:

$$ z
\begin{pmatrix}
v_1 \\
\vdots \\
v_n
\end{pmatrix} = 
\begin{pmatrix}
zv_1 \\
\vdots \\
zv_n
\end{pmatrix}$$

* In complex vector spaces, the vectors consist of complex numbers. One property of complex numbers is that they have a conjugate. The conjugate is a replica of the complex number with the only difference that the imaginary part has a switched sign. The in-line representation of a conjugate is the asterisk as a superscript:

$$ (1+i)^* =1-i $$

* We can define a conjugate for a complex vector as well. This is represented as:

$$(|v>)^* = (\vec{v})^* =
\begin{pmatrix}
v_1 \\
\vdots \\
v_n
\end{pmatrix}^* = \begin{pmatrix}
v_1^* \\
\vdots \\
v_n^*
\end{pmatrix}
$$

* There is also another operation we can do to the vectors in order to represent them as row matrices instead of the column matrix representation which is the transpose operation. The transpose operation is useful whenever we start multiplying two vectors together. The transpose operation is represented as a superscript T to the vector being transposed:

$$(|v>)^T = (\vec{v})^T =
\begin{pmatrix}
v_1 \\
\vdots \\
v_n
\end{pmatrix}^T = \begin{pmatrix}
v_1 & \dots & v_n
\end{pmatrix}
$$

* The adjoint of a vector is the conjugate transpose of that vector. The adjoint operator is denoted by a dagger superscript to the vector as follows:

$$(|v>)^\dagger = (\vec{v})^\dagger = 
\begin{pmatrix}
v_1 \\
\vdots \\
v_n
\end{pmatrix}^\dagger = \begin{pmatrix}
v_1^* & \dots & v_n^*
\end{pmatrix}
$$
* The adjoint of a vector is also known as the **dual vector** and can be represented by **<v|** in Dirac notation. **<v|** is also known as a **bra**
* Each complex vector space contains a special vector called the zero vector whose elements are all zeros. It is given by:

$$ \mathbf{0}= \begin{pmatrix}
0 \\
\vdots \\
0
\end{pmatrix}$$

* Note that the zero vector has a special notation (a bolded zero **0** ) instead of a ket representation. This is because the ket representation |0> is reserved for another vector in QM literature.

* Two special properties of the zero vector are that any addition of a vector |v> with the zero vector always gives back |v> and any scalar multiplication with the zero vector always gives back the zero vector:

$$ |v> + \mathbf{0} \equiv |v> $$

$$ a\mathbf{0} \equiv \mathbf{0} $$


## Vector Bases and Linear Independence:

* Suppose two vectors |v> and |w> are scalar multiples of one another as expressed below where **a** is the scalar:

$$ |v> = a|w> $$

* The above relation means that the two vectors are **linearly dependent** on one another by a factor of **a**. The dependence is called linear because **a** is a constant number. Here **a** could be any number that belongs to the set of complex numbers deonted by **C**

$$ \forall a \in \mathbf{C} $$

* For any two vectors |v> and |w> which are not linearly dependent (**Linearly Independent**), we can write the following relation for all possible complex constant numbers:

$$ |v> \neq a|w> $$

$$ \forall a \in \mathbf{C} $$

* The above relation means that we cannot express the vector |v> in terms of the vector |w> and vice versa, hence the **independence** term.

* For any complex vector space, there exists a special group of **linearly independent** vectors which we call **A Vector Basis** or just **Basis** for short.
* We use the basis to represent any vector inside the complex vector space as a **linear combination** of the basis vectors.
* Suppose we have a complex vector space which has **n** dimensions, then we can write its vector basis as the group of vectors:

$$ |v_1> \dots |v_n> \equiv |v_i> \forall i \in [1,n] $$

* Any random vector |w> can now be represented in terms of the basis above as:

$$ |w>=a_1|v_1> +a_2|v_2>+ \dots + a_n|v_n> = \sum_i^n a_i|v_i>$$

* In the above expression, it is clear that using the summation is much more compact and informative. The summation has an index **i** that runs from 1 upto **n** which is the number of vectors in the basis (and is also the number of dimensions in the vector space). The constant number $a_i$ is a number to be multiplied by the **ith** vector in the basis. These constant numbers $a_1 \dots a_n$ give us an extra degree of freedom to construct any random vector |w>

* **Example**: For the complex vector space $\mathbf{V}^2$ we can have a basis set which consists of two vectors:

$$ |v_1> = \begin{pmatrix}
1 \\
-1 
\end{pmatrix}$$

$$ |v_2> = \begin{pmatrix}
0 \\
1 
\end{pmatrix}$$

* Any vector in $\mathbf{V}^2$ can now be represented as:

$$ |w>= \sum_{i=1}^{2} a_i|v_i>=a_1|v_1> +a_2|v_2>= \begin{pmatrix}
a_1 \\
a_2-a_1 
\end{pmatrix} \, \forall (a_1,a_2) \in \mathbf{C^2}  $$

* There can be multiple basis sets for the same vector space, for example, another valid basis set for $\mathbf{V}^2$ is:

$$ |v_1> = \begin{pmatrix}
1 \\
0 
\end{pmatrix}$$

$$ |v_2> = \begin{pmatrix}
0 \\
1 
\end{pmatrix}$$

$$ |w>= \sum_{i=1}^{2} a_i|v_i>=a_1|v_1> +a_2|v_2>= \begin{pmatrix}
a_1 \\
a_2
\end{pmatrix} \, \forall (a_1,a_2) \in \mathbf{C^2}  $$

* A basis set cannot have two or more vectors that are linearly dependent. Therefore, we should verify that a particular basis set is valid by checking if all its vectors are **linearly independent**.

* A group of vectors is said to be **linearly dependent** if there exists a group of complex numbers $a_1 \dots a_n$, with at least one non-zero number in it, that satsifies the following equation:

$$ a_1|v_1>+a_2|v_2>+\dots+a_n|v_n>= \mathbf{0} $$

* So if you can prove that the above relation is not true for a group of vectors, then this group of vectors is a basis set which **spans the space**

* **Exercise #1** Verify whether the following group of vectors spans the vector space $\mathbf{V}^3$:

$$|v_1>= \begin{pmatrix}
1 \\
-1
\end{pmatrix}$$

$$|v_2>= \begin{pmatrix}
1 \\
2
\end{pmatrix}$$

$$|v_3>= \begin{pmatrix}
2 \\
1
\end{pmatrix}$$

* **Solution #1** In order for this set of vectors to span the vector space $\mathbf{V}^3$, it has to be a basis set, which means that it should be linearly independent. The check for linear dependency means finding three numbers $a_1, a_2, a_3$ for which the following equation holds:

$$ a_1|v_1>+a_2|v_2>+a_3|v_3>= \mathbf{0} $$

* Suppose we use $a_0=a_1=1$ and $a_2=-1$ in the equation above, so we get:

$$\begin{pmatrix}
1 \\
-1
\end{pmatrix}+
\begin{pmatrix}
1 \\
2
\end{pmatrix}-
\begin{pmatrix}
2 \\
1
\end{pmatrix}=\begin{pmatrix}
0 \\
0
\end{pmatrix}$$

* This leads us to the conclusion that the set of vectors is **linearly dependent** and therefore it cannot be a basis set.

## Linear Operators:
* A linear operator **A** is a function which takes an input vector **|v>** and maps it into a different vector **|w>**. If the vector **|v>** belongs to the vector space $\mathbf{V}$ and the new vector **|w>** belongs to a different vector space $\mathbf{W}$, then we may express this as:

$$ A: \mathbf{V} \rightarrow \mathbf{W} $$

* The linear operator can also map a vector **|v>** to a different vector **|v'>** within the same vector space $\mathbf{V}$. In this case, the linear operator is expressed in the following manner:

$$ A: \mathbf{V} \rightarrow \mathbf{V} $$

* The linearity property of the operator means that the operator is not affected by scalar multiples of input vectors, as it always acts on the input vectors themselves and doesn't act on constant numbers!
* To understand this better let's consider a vector **|v>** which belongs to $\mathbf{V}^3$ space. We can express this vector in terms of the basis set of $\mathbf{V}^3$ as:

$$ |v>=a_1|v_1> +a_2|v_2> +a_3|v_3>$$

* Now, we want to apply on **|v>** the operator **A** which is expressed as follows:

$$ A(|v>)=A(a_1|v_1> +a_2|v_2> +a_3|v_3>)=A(a_1|v_1>) +A(a_2|v_2>) +A(a_3|v_3>)=a_1A(|v_1>) +a_2A(|v_2>) +a_3A(|v_3>)$$

* First notice how we distributed the operator on the individual vector terms regardless of the plus sign (**Distributivity Property**). Next, notice how scalar factors (constant numbers $a_1,a_2,a_3$) are not affected by the operator and so they can be factored out (**Linearity Property**). These two properities are characteristic to operators in vector spaces. These two properties can be expressed in a compact form as:

$$A(\sum_ia_i|v_i>)=\sum_ia_iA(|v_i>)$$

* In standard QM notation, we can denote an operator **A** acting on vector **|v>** by **A|v>** instead of **A(|v>)** so the above equation can be written as:

$$A\sum_ia_i|v_i>=\sum_ia_iA|v_i>$$

* A special operator that acts on all vector spaces is the **Identity Operator** which takes as an input the vector **|v>** and maps it back into itself so it returns **|v>**.
* The identity operator is referred to by the bolded letter **I** and its operation is defined as:

$$ \mathbf{I}: \mathbf{V} \rightarrow \mathbf{V} $$

$$ \mathbf{I} |v> \equiv |v> \forall |v> \in \mathbf{V}^n $$

* Another special operator that acts on all vector spaces is the **Zero Operator** which takes as an input the vector **|v>** and maps it into the vector **0**
* The identity operator is referred to by the bolded letter **0** and its operation is defined as:

$$ \mathbf{0}: \mathbf{V} \rightarrow \mathbf{V} $$

$$ \mathbf{0} |v> \equiv \mathbf{0} \, \forall |v> \in \mathbf{V}^n $$

* Suppose **V**, **W**, and **X** are vector spaces and you have two operators defined by:

$$ \mathbf{A}: \mathbf{V} \rightarrow \mathbf{W} $$

$$ \mathbf{B}: \mathbf{W} \rightarrow \mathbf{X} $$

* Then we can map a vector from space **V** to space **X** by first applying operator **A** on the input vector, then applying the operator **B** on the resulting vector. This cab expressed as:

$$ \mathbf{B}(\mathbf{A}(|v>)) \equiv \mathbf{B}\mathbf{A}|v>$$

## Matrix Representations of Linear Operators:
* Linear operators can be thought of as matrix multplications, and matrices can be thought of linear operators interchangeably.
* Suppose you have an **mxn** matrix **A** as show below:

$$ A=\begin{pmatrix}
A_{11} & \dots & A_{1n} \\
\vdots & \ddots & \vdots \\
A_{m1} & \dots & A_{mn}
\end{pmatrix}$$

* As you can see, you can think of this matrix as **n** number of column vectors stacked beside each other and each vector has **m** group of numbers inside of it. Hence **m** is the number of **rows** in a matrix and **n** is the number of columns

* Recall that when we perform matrix multiplication by multiplying the matrix **A** and matrix **B** together, we must make sure that the **inner dimensions** of the matrices are equal. 
* In other words, we can only multiply matrix **A** with matrix **B** if and only if the number of columns of **A** is equal to the number of rows in **B**. In this case, we produce a new matrix **C** whose dimensions are the **outer dimensions** of **A** and **B**. This can be written as:

$$ \mathbf{A_{mxn}} * \mathbf{B_{nxr}}=\mathbf{C_{mxr}}$$

* The same rules of matrix multiplication apply when we try to multiply a matrix **A** with a vector **|v>** so the inner dimensions of the matrix and vector must match and the output of the multiplication is a new vector **|w>** with the outer dimensions of **A** and **|v>**

$$ \mathbf{A_{mxn}} |v> =|w> \, \forall v \in \mathbf{V^n} \, \forall w \in \mathbf{W^m}$$

* If you multiply a vector **|v>** that belongs to $\mathbf{V}^n$ with the above **mxn** matrix, you produce a new vector **|w>** which has **m** dimensions and belongs to $\mathbf{W}^m$. This is in fact equivalent to saying $\mathbf{A}: \mathbf{V} \rightarrow \mathbf{W}$
* Suppose you have the matrix representation of the operator **A** such that $\mathbf{A}: \mathbf{V} \rightarrow \mathbf{W}$ and the two vector spaces **V** and **W** have the following basis sets

$$\mathbf{V^n}: |v_i>\, \forall i \in [1,n]$$

$$\mathbf{W^m}: |w_j>\, \forall j \in [1,m]$$

* Then we can describe the operation of **A** on the vector **|v>** as:

$$ \mathbf{A}|v_i>=\sum_{j=1}^{m} A_{ji}|w_j> \, \forall i \in [1,n] \, \forall j \in [1,m] $$

* Here, $A_{ji}$ are the matrix elements of the matrix representation of operator **A** such that the index i runs over the columns and index j runs over the rows.

* Note that resulting vector from the multiplication definitvely belongs to the vector space **W** since it is expressed as a linear combination of the vector basis of **W**

* We have introduced an equation which uses the matrix representation of an operator $\mathbf{A}: \mathbf{V} \rightarrow \mathbf{W}$ only when it acts on one vector of the basis set of **V**:

$$ \mathbf{A}|v_i>=\sum_{j=1}^{m} A_{ji}|w_j> \, \forall i \in [1,n] \, \forall j \in [1,m] $$

* We would like to generalize this equation in order to be valid for all vectors which belong to **V** space. That's to say, we would like to generalize it to include linear combinations of the basis set of **V**. This generalization is  done by by using the distributivity and linearity properties of **A** and is expressed as:

$$ \mathbf{A}(\sum_{i=1}^na_i|v_i>)=\sum_{i=1}^na_i\mathbf{A}|v_i>=\sum_{i=1}^na_i\sum_{j=1}^{m} A_{ji}|w_j> \, \forall i \in [1,n] \, \forall j \in [1,m] $$

* **Excercise #2:** Show that the identity operator on a vector space **V** has a matrix which is one along the diagonal sites and zero everywhere else
*  **Solution #2:** Suppose that the vector space is $\mathbf{V^2}. One basis set for this space is given by:

$$ |v_1>= \begin{pmatrix}
0 \\
1
\end{pmatrix}$$

$$ |v_2>=\begin{pmatrix}
1\\
0
\end{pmatrix}$$

* Now, the identity operator matrix representation $\mathbf{I}$ should act on each member of the basis representing the space **V**.
* Note: for this type of problem, it would be confusing to use the generalized equation for linear combinations of the basis; as it would be more useful only when the matrix reprsentation is already known!

$$ \mathbf{I}: \mathbf{V} \rightarrow \mathbf{V}$$

$$ \mathbf{I} |v_1> = \sum_{j=1}^{2}A_{j1}|v_j>=A_{11}|v_1>+A_{21}|v_2> $$

$$ \mathbf{I} |v_2> = \sum_{j=1}^{2} A_{j2}|v_j>=A_{12}|v_1>+A_{22}|v_2>$$

* by the definition of the identity operator, when it acts on a vector, it returns the vector unchanged. So we can also write:

$$ \mathbf{I} |v_1> \equiv |v_1> $$

$$ \mathbf{I} |v_2> \equiv |v_2> $$

* by simple comparison of each two corresponding equations we find that:

$$ A_{11}=A_{22}=1$$

$$ A_{12}=A_{21}=0$$

* We can now write the matrix representation for the identity operator in $\mathbf{V^2}$:

$$I=\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}$$

## Pauli Matrices as Important Linear Operators:

* There are four extremely useful and unique linear operators which we shall encounter many times in our QM studies. These fours operators are known as **Pauli Operators**. Although it is more common to call them **Pauli Matrices** due to the unique properities of their matrix representations.
* We have already seen and dealt with one of the pauli matrices which is the **Identity Matrix** which represents the identity operator and we proved that it had the following form:

$$ I=\sigma_0=\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}$$

* The other three matrices are better known as the **X**, **Y**, and **Z** matrices. The reason for this naming will be clear in the future when we get more into QM calculations. They are given by:

$$ X= \sigma_x=\begin{pmatrix}
0 & 1 \\
1 & 0
\end{pmatrix}$$

$$Y =\sigma_y= \begin{pmatrix}
0 & -i \\
i & 0 
\end{pmatrix}$$

$$Z=\sigma_z=\begin{pmatrix}
1 & 0 \\
0 & -1
\end{pmatrix}$$

* By definition, whenever a matrix $\mathbf{A}$ is multiplied by its inverse $\mathbf{A^{-1}}$, the result is the identity matrix $\mathbf{I}$.
* An interesting property of the Pauli matrices is that every one of them is its own inverse. This is expressed as:

$$ \mathbf{I^2}=\mathbf{X^2}=\mathbf{Y^2}=\mathbf{Z^2}=\mathbf{I}$$

* The Pauli matrices are also **Hermitian Matrices**. Any hermitian matrix by definition is equal to its self-adjoint. This can be expressed as:

$$ \mathbf{A} = \mathbf{A^{\dagger}}=\mathbf{(A^*)^{T}}$$

* Other notable properties is that the pauli matrices **X**, **Y** and **Z** all have a determinant of **-1** and a trace of **0**. Furthermore, the **Eigenvectors** of each of **X**, **Y** and **Z** forms a complete basis for the complex vector space $\mathbf{V^2}$
* We will be seeing pauli matrices again! but for now it suffices to say that they are extremely important!

## Inner Products and Orthonormalized Vector Bases:

* An inner product is a function which takes as an input two vectors **|v>** and **|v'>**, both belonging to the same vector space $\mathbf{V^n}$, and returns an output which is a constant number **v**. 
* Before we discuss the meaning of the constant number **v** which is the output of the inner product, we first need to recall the representations of vectors as straight lines in space with a positive definite length as well as a specific direction.

![image](https://user-images.githubusercontent.com/47701869/180971923-1aa23c78-de5f-4d79-8121-76e529552526.png)
* In this section, we will see how we can define both the magnitude and the direction of a vector **|v>** in the sapce $\mathbf{V^n}$, but for now, let's just keep this idea in mind to understand the role of inner products.
* Now, we can say that output of the inner product between the two vectors **|v>** and **|v'>**, which is the constant number **v** , represents the projection of the vector **|v>** unto the vector **|v'>**.
* The inner product is a measure of how much the vectors **|v>** and **|v'>** overlap together. In other words, it is a measure of how similar their directions are in the vector space $\mathbf{V^n}$

![dotproduct](https://user-images.githubusercontent.com/47701869/180964297-92880fc8-a515-4cbe-a7b1-c2ceb5f8c45a.jpg)

* It is clear that when the angle between the direction of **|v>** and the direction of **|v'>** approaches 90 degrees (i.e. the two vectors are perpendicular on each other), the overlap between them will be zero! In this case we say that **|v>** and **|v'>** are two **orthogonal vectors**
* There are several in-line notations for the inner product of two vectors. The two most frequently used in QM studies are the following:

<img align="center" src='https://user-images.githubusercontent.com/47701869/180967854-6f683db8-ed21-4c7a-952a-59d4f063e0bb.gif'>

* Note that the representation **<v|v'>** uses the Bra-ket Notation in the following manner:

![CodeCogsEqn (1)](https://user-images.githubusercontent.com/47701869/180970022-e7487def-458d-47aa-ade2-c84b00ea7a9b.gif)

* The process of calculating the inner product between **|v>** and **|w>** is given by:

$$ \begin{pmatrix} v_1^* & v_2^* & \dots & v_n^* \end{pmatrix} 
\cdot
\begin{pmatrix}
w_1 \\
\vdots \\
w_n
\end{pmatrix} =(v_1^*  \cdot w_1 )+(v_2^*  \cdot w_2)+\dots+(v_n^*  \cdot w_n)=\sum_{i=1}^{n} v_i^*  \cdot w_i $$

* Any inner product must satisfy three main conditions:

**(1) The inner product must be linear in its second argument and anti-linear in its first argument**
* In order for the inner product to be linear in its second argument, it must satisfy the following equation:

$$ (|v>, |w>) = (|v>, \sum_{i=1}^n a_i|w_i>)=\sum_{i=1}^n(|v>, a_i|w_i>)=\sum_{i=1}^na_i(|v>, |w_i>) $$

(2) The vectors in the inner product do not commute $(|v>, |w>)=(|w>,|v>)^* $ 

(3) The inner product of any vector **|v>** with itself **<v|v>** is a positive definite number  $(|v>, |v>)\geq 0 $ 
