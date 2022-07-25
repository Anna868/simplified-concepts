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


