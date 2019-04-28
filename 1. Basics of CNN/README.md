**Background**

DNN - When the great minds said all humans should look within themselves to find the answers of most difficult problems, we never took it seriously. Now interestingly most of the AI is built around replicating GOD's most beautiful wonder which is us. Scientist and researchers are still in awe of how our minds work and it performs such complex operation with such ease. DNN which stands for Deep Neural Network is a similar approach in trying to replicate how our brain functions. So throughout the series(yes this is just the beginning), we will be learning about DNN that means whatever we will learn going forward is a branch of DNN.

Today we will discuss Images and CNN. But before that let me ask you a question, have you ever thought how modern photo apps like Instagram provides those filters? What is the logic behind those filters? Let's find the answer.

CNN - Convolution neural network is a branch of DNN through which we process images and try to learn the pattern so that we can make a better prediction in the future. FYI Though it is famous for Image progressing it can be used in other scenarios as well. Now lets again take the example of our brain, do you know how our brain process Images? It uses an edge detector to detect the edges and forms an image based on that. So when an Images comes to the brain it uses edge detector to find the edges and then those edges are converted to part of an object and then in the final step they are converted to object.

![alt text](https://ujwlkarn.files.wordpress.com/2016/08/screen-shot-2016-08-10-at-12-58-30-pm.png)

Let's take another example, have you ever try reading something when there is no electricity? CNN also works in the same way. You move your torch from left to right to read lines and same logic goes behind convolution as well.

![alt text](https://thumbs.gfycat.com/PresentGreedyHornshark-size_restricted.gif) 

Convolution is a technique where we try to reduce the size of an image without losing key/important features of it. Well, it makes sense to do so because if we are detecting whether an Image is of CAT or DOG, what is the whole point of doing it in the original image which might be of MB's.

![alt text](https://i.stack.imgur.com/9Iu89.gif)

Above is a 3x3 convolution on a 5x5 matrix and the result is a 3x3 matrix(In case 3x3 convolution/ filter the result matrix is always 2 less than the original matrix, for example, if we have a 7x7 matrix and run a convolution matrix of 3x3 over it, we will have a 5x5 matrix).

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

Why 3x3 and not any other filter like 5x5 or 7x7?

* Less filter less computation, big filter more computation.

* It learns large complex features easily, where as large filters learns simple features. 

* Output Layers will be less when we use 3x3 filters as compared to 5x5 or bigger filters. 

* Also since there will be more output layers when using 3x3 filters more memory will be required to store them as compared to 5x5 or bigger filters. 

3. How many times do we need to perform 3x3 convolution operation to reach 1x1 from 199x199 (show calculations)

We need to perform 100 iterations. So let do it:

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
