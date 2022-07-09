# Hilbert Spaces

The following post is intended for people with a little bit of interest in anything related to quantum mechanics and who have a teeny tiny (secondary school level)
mathematical background.

Today’s topic aims to explain a jargon term that gets thrown around a lot when trying to describe quantum mechanical states mathematically.

The objective is that by the end of this post, you and I pass by this jargon term in our readings without being annoyed by it because we grasp the gist of what it
means.

---

If you decide to study any topic related to quantum mechanics, you are going to read the words "Hilbert space" a lot. That’s our annoying jargon term.

For example, if we were to give the shortest possible definition of a qubit (if you decide to get into quantum computing), we would say
"A qubit is a vector that belongs to an N dimensional Hilbert space"

So what is a Hilbert space? and what is a mathematical space in general?

---

## Mathematical Spaces:

Let's give a real-life analogy to understand the definition of a mathematical space:

Assume the Opera House in your city announces a concert and you want to buy a ticket to attend the concert.

![Metropolitan_Opera_House,_a_concert_by_pianist_Josef_Hofmann_-_NARA_541890_-_Edit](https://user-images.githubusercontent.com/47701869/177996645-d7cc9778-11fc-470f-af74-02450c9835d5.jpg)

**What are the conditions imposed on you to be able to get the ticket?**
 
1. You have to have enough money to buy the ticket
2. You have to have formal attire in your wardrobe
3. You have to be free at the time of the concert
4. You have to have a transportation method to and from the opera house

If you fulfill all these conditions, then you are eligible to be a member of the audience that could attend the concert (under the assumption that the opera house
is so big that it would never run out of seats!)

**Once you are inside the opera house, there are certain rules to follow:**

1. You are not allowed to sit at any other seat except the one you reserved with your ticket
2. You may not talk loudly to any member of the audience except during breaks
3. At all times, you must remain at a certain distance from the platform on which the performance is given.

In our analogy, the space is the Opera House where the audience is chosen according to a set of conditions and the audience members interact with each other
and with the environment according to certain rules.

The same analogy can be applied with your coworkers in your office at work, or with your family members at home, etc. 
(You can think about the rules that define your eligibility to be at your workplace/home and the rules that define your interaction with your
coworkers/family members and write them down!)

Furthermore, the opera house and your workplace and your home are all contained in an even bigger space which is your city.
Your city has broader criteria to choose its citizens from and the rules that define how citizens interact together are more malleable and diverse.

But even your city is contained in your country and your country is contained within a continent and a continent is contained within planet Earth and so on. So general big spaces can contain more
specific smaller spaces.

![1557923401_Friendship_diagram-Final-01 (1) resized](https://user-images.githubusercontent.com/47701869/178000385-d12cd75e-d247-44b0-85a3-22ae558bdf6e.jpg)

So the word 'space' in the analogies above refers to:

1. A physical space in which similar people are gathered together according to some criteria. 
2. Once the people are in this place together, there are specific rules to control the way they interact with each other.
3. On top of that, broad spaces with malleable general rules contain inside of them more well defined narrow spaces. (e.g. opera house contained in a city)

In mathematics, a space is not necessarily a physical space. Generally, it is a concept that groups similar mathematical objects together and defines
the way they are related to each other by a set of rules.

The mathematical space describes a physical space only when it is geometrical. A geometrical space contains mathematical objects like points and vectors
(i.e. lines with direction). 

It defines the relationship between these objects using metrics like distance and displacement (i.e. distance with direction) or using transformations
like projection (i.e. how well two vectors overlap on top of each other).

Geometrical spaces are the most intuitive to our minds because we happen to be living in a 3D geometrical space! (More on that later)

We know from before that general big spaces can contain more specific smaller spaces. This also applies to the different types of geometrical spaces.

So when mathematicians constructed different types of geometrical spaces, they created a structure of Russian dolls, where the biggest Russian doll
contains inside it the next big Russian doll and so on:

(Topological spaces contain Metric Spaces and Vector Spaces. Their intersection contains Normed Vector Spaces which contain Inner Product
Vector Spaces which contain Hilbert Spaces)

The Russian doll we are interested in (the Hilbert Space) unfortunately lies a couple of levels deep, so we have to pop open some dolls
before we can get to it.

![VjI8T](https://user-images.githubusercontent.com/47701869/178000512-4f782284-f79e-4125-ae8c-251eab3dc5c2.png)


Bear in mind that this is a very simplistic view of the actual detailed discussion of mathematical geometrical spaces. A detailed diagram would look more
like the figure below! So this is just a reminder that we are scratching the surface of things very lightly and very slowly!

![g7CYc_resized](https://user-images.githubusercontent.com/47701869/178001723-01aa0fa3-94ba-4539-bd81-35a1bd3807fb.jpg)


---

## Geometrical Spaces:

### 1) Topological spaces:

* A topological space is the broadest and most general type of geometrical spaces.

* Its eligible members are called points. Think of each point as a set of one or more numbers. 

* Any point can be a member of the topological space (it doesn't matter if its values are positive or negative, complex or real).

* In a topological space, we can describe qualitatively the closeness of one point to all other points (whether they are near or
far from each other) using a set of rules which are shown in the image below. (If you don't understand them you can skip them for now!)

![Topological-space](https://user-images.githubusercontent.com/47701869/178003351-7cfba1fd-3919-4f16-beb7-bc68a77e605e.png)

* In a topological space, we can’t know exactly how far or close the points are in numbers.

* So in topological spaces, we can't necessarily define a notion of distance between points to quantify their closeness to each other.

* If we can define a notion of distance between points, then we are in a special subset of topological spaces called Metric spaces.


### 2) Metric spaces:

* Metric spaces are a family of topological spaces.

* They are special because they allow us to measure the distance between any two points inside of them.

* If the points inside the metric space are represented by N numbers then the metric space is N dimensional,
For example: if the points are represented by 2 numbers then the metric space is two dimensional and so on.

*  Each metric space contains a function which takes two points in the metric space and computes a distance between them.
Two very popular distance functions are the Euclidean distance and the Minkowski distance. 

![metric](https://user-images.githubusercontent.com/47701869/178008178-ac9208e9-01a2-4d08-99f1-c81b63940220.jpg)

* There are very simple rules imposed on the distance between points inside metric spaces. Suppose you are going to walk from point A towards point B
along a straight line inside a metric space, the following statements are rules imposed on the distance you will walk:

1. The distance between points A and B can only be a positive number or zero, You can’t walk a negative distance!

2. The shortest distance between points A and B is always a straight line. Any other path you take which involves a 3rd point or more and doesn't
form a straight line will cause you to walk a longer distance.

3. The shortest distance between points A and B is the same as the shortest distance between points B and A so the direction in which you walk does not matter!

4. The shortest distance between A and B is zero if and only if A is the same point as B.
If A and B are the same point and you are looking for the optimal route with shortest distance, then you won’t move from your spot so you won’t walk at all!

5. The distance from A to B and then from B back to A is positively valued, so it doesn’t matter that your walk starts at a point and ends at the same point! 

* Generally, Metric spaces don’t contain the concept of direction so you can’t specify whether your destination is point A or point B in the previous example.

* If we can define directions in a Metric space, then this Metric space is special because it also happens to be a Vector space.



### 3) Vector spaces:
* Vector spaces are a subset of topological spaces. They are special because they allow us to use the concept of direction.

* Some vector spaces are a subset of metric spaces as well. They allow us to use the concept of direction as well as distance and are better known as **Normed Vector Spaces**.

* In this section, we first discuss Vector Spaces, then move on to Normed Vector Spaces.

* For an N dimensional vector space, we have N unique directions to use. For example, in 3D vector space, we have 3 unique directions:
1. Up or Down (let’s call it z direction - it expresses the height dimension)
2. Left or Right (let’s call it y direction - it expresses the width dimension)
3. Forwards or Backwards (let’s call it x direction - it expresses the depth dimension)

![3d-coordinate-axis-vector-7814714](https://user-images.githubusercontent.com/47701869/178013395-59bb424d-4fd7-45ce-b3bf-be2ab5180e27.jpg)

* The N unique directions in the N dimensional vector space are known as the basis of the vector space. So for 3D vector space, the basis directions are x, y and z directions from above.

* We use the basis directions to define the members of the vector space which are called vectors.

* A vector is just a straight line between two points but it has a specific starting point and a specific ending point, so it has a specific direction.
It also has a length (often called a magnitude) which is defined as the shortest distance between the starting point and the ending point

![magnitude-of-a-vector](https://user-images.githubusercontent.com/47701869/178015829-b42d96aa-d09a-46b9-872c-8789ad771963.png)

* Any vector within a vector space can be completely described by the vector space basis. Let’s give a real-life analogy here:

Assume you work in a fast food delivery service and you want to deliver a pizza from the restaurant at point A to the customer residence at point B.

You don’t know the shortest path between points A and B so you ask your manager to describe the path for you.

However, your manager can only describe the path in terms of (right-left),(forward-backward), and (ascend-descend) operations.

So your manager tells you that to walk the shortest distance between points A and B, you have to:

1. walk forward 2 kilometers,
2. then a further 1 km to the right
3. and finally ascend 100 meters by taking the stairs!

This can be rewritten as:

1. walk 2 units along x direction
2. walk 1 unit along y direction
3.  walk 0.1 units along z direction

This is expressed by the following equation:
$$ \vec{AB}= 2 \hat{x}+ 1 \hat{y}+0.1 \hat{z}$$

---

* As with all geometrical spaces, there are certain rules to be imposed on the vectors in a vector space. These rules are:

1. If you want to add 2 vectors together to get a new vector, then the addition must be **commutative**.
This means that the order of addition doesn't matter. Consider two vectors a and b, then:

$$ a + b = b + a $$

$$ (a_x + b_x)\hat{x}+(a_y + b_y)\hat{y}+(a_z + b_z)\hat{z} = (b_x + a_x)\hat{x}+(b_y + a_y)\hat{y}+(b_z + a_z)\hat{z}$$

2. If you want to add 3 or more vectors together to get a new vector, then the addition must be **Associative**.
You always have to start the addition process with two vectors, and the result is added to another vector and so on.
So associativity tells you that the order of addition doesn't matter.
For example if you have 3 vectors a, b and c then it doesn't matter if you start with a+b then add c or if you start with b+c then add a !

$$ (a+b)+c=a+(b+c)$$

3. You can change the length/magnitude of a vector by multiplying its components along the basis directions with a constant number.
The constant number could be a real positive or a real negative number in which case the vector space is called a **Real Vector Space**.
The constant number could also be a complex number, in which case the vector space is called a **Complex Vector Space**
This constant number is usually known as a **scalar**. The image below shows an example of scalar multiplication in a **Real Vector Space**

![vector_r](https://user-images.githubusercontent.com/47701869/178024580-8068000a-7ecf-4a4e-a8d5-09a2b14e3845.jpg)

4. Multiplying an addition of vectors with a scalar must be **distributive**. So if you have vectors a and b and multiplied their sum by a scalar, then it is equivalent 
to multiplying a and b individually with the same scalar:

$$ \alpha (a+b)= \alpha a + \alpha b $$

5. You can subtract two vectors a and b from each other by multiplying one of them by a scalar that is equal to -1. This can be stated as follows:

$$ a - b = a + (-1 * b)$$

6. The vector space is closed. Meaning that any vector that results from an operation of addition/subtraction/scalar multiplication still belongs to the same vector space as the operands
---

### 4) Normed Vector Spaces:

* Normed Vector Spaces are vector spaces equipped with functions that calculate:
1. the length/magnitude of a vector
2. the distance between any two vectors in the vector space.

* The norm functions take an input vector $\vec{u}$ which has as many numbers as the basis vectors of the vector space, and then map it to a single real positive number ||u|| which represents the vector's length/magnitude

* The distance between any two vectors $u$ and $v$ can be calculated through the following steps:
1. get the difference between the two vectors  $$\vec{d}=\vec{u}-\vec{v}$$
2. get the magnitude of the difference vector $\vec{d}$ which is ||d|| 
3. ||d|| is equivalent to the distance between the two vectors

* In case the vector is mulitiplied by a constant number (scalar), the magnitude of the vector is also scaled by the same number. This can be expressed as:
$$ || \gamma \vec{d} ||= |\gamma| . ||\vec{d}|| $$
Generally, $\gamma$ could be a real or a complex number. In case of complex numbers, we have to use their magnitude. This is the reason why the scalar is denoted as $|\gamma|$ is because it could be a complex number in the case of **Complex Vector Spaces**. 

* For a vector space with a finite number of dimensions N, a vector's norm/length/magnitude is calculated simply by following formula:
$$ ||x||= (\sum_{i=1}^{N} (x_i)^p)^{1/p}$$

If you are not familiar with mathematical notations like these, don't panic just yet! This is actually a very easy equation. 

Let's do a little real life example to understand the equation:

Suppose after delivering the pizza from the restaurant at point A to the customer residence at point B, you wish to calculate exactly the shortest distance between the two points A and B. You know from before that the vector $\vec{AB}$ is given by:

$$ \vec{AB}= 2 \hat{x}+ 1 \hat{y}+0.1 \hat{z}$$

You can now apply the equation above by taking each number in the vector and raising it to the power p, so you get $2^p$ , $1^p$ and $0.1^p$

Next you sum all these numbers together, so you get:
$$ s= 2^p + 1^p + 0.1^p$$

Finally, the magnitude ||AB|| can be obtained by:
$$||AB|| = s^{1/p} =(2^p + 1^p + 0.1^p)^{1/p}$$

If you take $p=2$, this distance function will be very familiar:

$$||AB||=\sqrt{2^2+1^2+0.1^2}=\sqrt{4+1+0.01}=2.34$$

It becomes the Euclidean distance we dealt with a lot in high school !

* There are 3 most notable cases for the number $p$ you should be aware of:
1. When $p=1$ then we are computing a norm called the Manhattan Norm,
2. When $p=2$ then we are computing a norm the Euclidean Norm,
3. We can generalize the norm equation by using p greater than 2 with no upper limit on p so that $ p \rightarrow \infty$ is a possible limit (in other words p could get very big!). In this case we are computing a norm called the Minkowski Norm.

* When $p \rightarrow \infty$ , then the norm becomes simply the largest number in the vector. So in the last example, if the vector is given by
$$ \vec{AB}= 2 \hat{x}+ 1 \hat{y}+0.1 \hat{z}$$
and we will compute the Manhattan Norm with $p \rightarrow \infty$ so ||AB||=2

* Let's try to visualize the norm equation to get more sense of what is going on.

We will compute norms for a 2D vector space. And suppose in this space, we want to find all the vectors who length/magnitude/norm is equal to 1, so we need to solve the following equation:

$$ 1= (\sum_{i=1}^{N} (x_i)^p)^{1/p}$$

If we vary the value of $p$ to be $p=1$, $p=2$, $p=3$ and $p \rightarrow \infty$, we will get the shapes shown in the image below.

![lp_norms_2d](https://user-images.githubusercontent.com/47701869/178084458-d9eb3a4d-e2bc-4adb-a2a3-25692b93ed7e.jpg)

This means that any vector that starts from the origin point (0,0) and ends on the shape boundary has a norm that is equal to 1. 
so for example, if $p=1$, then any vector which starts at the center and ends on the diamond shape has a length of 1 unit. And if $p=2$, then any vector which starts at the center and ends on the circle has a length of 1 unit. As p increases above $p=2$, the circle flattens slowly till it becomes a square for $p=100$ which is considered $p \rightarrow \infty$

We can repeat the same visualization for a 3D vector space so we get 3D surfaces instead of 2D shapes. Any vector which starts at the point (0,0,0) and ends on any 3D surface corresponding to $p=1$, $p=2$, $p=3$ and $p \rightarrow \infty$ has a length of 1 unit.
![lp_norms_3d](https://user-images.githubusercontent.com/47701869/178084559-b25420b2-bdcb-4dc2-8cf0-c48f995a92d2.jpg)

* By now you might be wondering if there any conditions on the value of p. Turns out that there is!
For our chosen p, the norm equation must fulfill what is known as the triangle inequality. This inequality is defined as follows for two vectors x and y as:

$$ ||\vec{x}+ \vec{y} || \leq ||\vec{x}||+ ||\vec{y} ||$$

This inequality simply states that no side in a triangle formed by 3 vectors can have a length that is greater than the sum of the other two sides. This is visualized in the image below:
![300px-Vector-triangle-inequality svg (1)](https://user-images.githubusercontent.com/47701869/178085520-bd067010-4abf-4d27-ab53-afc23d9fcc03.png)

for $0 \leq p  < 1$ the triangle inequality is not fulfilled and so $p$ must be larger than 1!

* One final note on Normed Vector Spaces is that they needn't have finite dimensions. They can have inifinite dimensions, that is, $N \rightarrow \infty$. This is actually a very interesting case in many mathematical and physical problems especially in continuous-variable quantum mechanics.

In this case, our vectors become continuous functions and we need to map them to a single real number which is the function's norm by the following equation:

$$ ||f||= (\int_a^b |f(x)|^p dx)^{1/p}$$

---

### 5) Inner Product Vector Spaces (Pre-Hilbert Spaces):

* We saw that in Vector spaces, we can add together two vectors and we can also multiply vectors by scalars. In Normed Vector Spaces, we can do all that and also caluclate the length of a vector or the distance between any two vectors.

* In Inner Product Vector Spaces, we can do every operation we can do inside a Normed Vector Space, but with the ability to multiply two vectors together!

* Suppose you have two vectors called v and w, their inner product is expressed in the following notation <v, w> in angled brackets.

* As always, there are rules imposed on the inner product of any two vectors. These rules must be respected in any Inner Product Vector Spaces:

1. **Distributivity of Vector Muliplication:** This simply means that multiplying the vector v+w with u is equivalent to multiplying v with u and w with u then adding the two resulting vectors. This can written as: <v+w, u>= <v,u> +<w,u>

2. **Distributivity of Scalar Multiplication:**  This simply means that multiplying the vector av with u when a is a scalar (constant number) is equivalent to multiplying v with u and then multiply the resulting vector with the scalar a. This can written as: <av, u>= a<v,u>

3. **Commutativity of Vector Multiplication:** This simply means that the order of multiplication doesn't matter so <u,v>=<v,u>. However, this is only true for **Real Vector Spaces**. In **Complex Vector Spaces** the commutative property is rewritten to be: ![image](https://user-images.githubusercontent.com/47701869/178099833-57195c49-8bc8-4cc5-82ce-898ec5b11165.png). Here the bar denotes the complex conjugate of the resulting vector. An inner product vector space that satisfies the latter condition for complex vector is known as a **Hermitian Inner Product Space**. Keep that name in mind as you will read it a lot in literature as well 

4. **Inner Products must be positive-definite:** This means that if you take the inner product of a vector v with itself,  you will get a number that is greater than or equal to zero <v,v> $\geq 0 $. This inner product is zero if and only if v is a zero vector (meaning that all its components are zero.










