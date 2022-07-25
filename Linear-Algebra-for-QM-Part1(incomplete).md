# Linear Algebra For Quantum Mechanics (Part I)
---
If you hear someone speaking a foreign language for the first time, you will be confused, and naturally you will not understand what he is trying to say!

But if you spend a few days with this person, and maybe use an application like Duolingo to help you with the basic vocabulary of the language, then gradually
 you will be able to understand the language when it is spoken!
 
 ![language_barrier](https://user-images.githubusercontent.com/47701869/180783165-15eca8af-7649-4db1-a386-9ab0efe7830c.jpg)


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

Note: Although there were some equations here and there in my previous post on [Hilbert Spaces]((https://github.com/Anna868/simplified-concepts/blob/main/Hilbert-Spaces.md), there wasn’t any formal introduction to the notations
of linear algebraic expressions in Quantum Mechanics. The equations were beside the point; but in this post they are the main objective.


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

* The notation |v> is also called a **ket** indicating the v is a column vector
* Any vector space contains two special operations: Addition of two vectors and multiplication of a vector by a constant number (a scalar). Let's see each of these operation expressed in the matrix column notation.
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

* In complex vector spaces, the vectors consist of complex numbers. One property of complex numbers is that they have a conjugate. The conjugate is a replica of the complex number with the only difference that the imaginary part has a switched sign. The in-line representation of a conjugate is the astrisk as a superscript:

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
