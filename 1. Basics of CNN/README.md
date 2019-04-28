**Background**

DNN - When the great minds said all human should look within to find the answers of most difficult problems, we never took it seriously. Now interestingly most of AI is built around replicating GOD's most beautiful wonder that is us. Scientist and researchers are still in awe of how our minds work and it performs such complex operation with such smoothness. DNN which stands for Deep Neural Network is a similar approach in trying to replicate how our brain works. So this whole course will be about learning DNN.


CNN - Convolution neural network is a branch of DNN through which we process images and try to learn the pattern so that we can make a better prediction in the future. 

Convolution is a technique where we try to reduce the size of an image without losing key/important features of it. It's just like how when our mom asks us to clean our room, we remove the unnecessary stuff but keep only the relevant items like books, games cd, etc. We have reduced the items in our room but we never lost anything important.

Let's use below 3x3 convolution and see with an example: 

$ \begin{bmatrix}
    1      & 0 & 1  \\
    0      & 1 & 0  \\
    1      & 0 & 1  
\end{bmatrix} $


![alt text](https://i.stack.imgur.com/9Iu89.gif)

Above is a 3x3 convolution on a 5x5 matrix and the result is a 3x3 matrix(the result matrix is always 2 less than the original matrix, for example, if we have a 7x7 matrix and run a convolution matrix of 3x3 over it, we will have a 5x5 matrix).

Remember,

![alt text](https://s3.scoopwhoop.com/anj/morpheus/884813517.gif =500x350)

Now lets do some programming using above concepts.

# Now, we will try answering some important questions like:

1. What are Channels and Kernels (according to EVA)?

Kernels: A unit. You can think of it as an atom(the smallest particle of a chemical element that can exist). 

Channels: Collection of kernels. you can think of it as a molecule(Every combination of atoms is a molecule).

In CNN dictionary, Kernel = filters = feature detector.

2. Why should we only (well mostly) use 3x3 Kernels?

We will split this question into 2 parts:

a. How to choose between smaller and larger filter size?
b. Why 3x3 and not any other filter like 5x5?

How to choose between smaller and larger filter size?

* Smaller filter looks at very few pixels at a time hence it has small receptive field. Where as large filter will look at lot of pixel hence it will have large receptive field

* When we work with smaller filters, we focus on every minute details and capture smaller complex features from Image, where as when we work with larger filters we tends to search for generic features which will give us basic components.

* After capturing smaller/ minute features from Image we can make use of them later in the processing. We loose this benefit with large filters as they focus on generics not specific features.

Why 3x3 and not any other filter like 5x5?

* 

3. How many times do we need to perform 3x3 convolution operation to reach 1x1 from 199x199 (show calculations)

We need to perform 199-2 = 100 iterations. So let do it:

199, 197, 195, 193, 191, 
189, 187, 185, 183, 181, 
179, 177, 175, 173, 171, 
169, 167, 165, 163, 161, 
159, 157, 155, 153, 151, 
149, 147, 145, 143, 141, 
139, 137, 135, 133, 131, 
129, 127, 125, 123, 121, 
119, 117, 115, 113, 111, 
109, 107, 105, 103, 101,  
 99,  97,  95,  93,  91,  
 89,  87,  85,  83,  81,  
 79,  77,  75,  73,  71,  
 69,  67,  65,  63,  61,  
 59,  57,  55,  53,  51, 
 49,  47,  45,  43,  41,  
 39,  37,  35,  33,  31,  
 29,  27,  25,  23,  21,  
 19,  17,  15,  13,  11,   
 9,   7,   5,   3,   1
 


Me after manually doing the above calcuation:


 
![alt text](https://media.giphy.com/media/FoH28ucxZFJZu/giphy.gif)
