# Here we will try answering some important questions like:

1. What are Channels and Kernels (according to EVA)?

Channels: 
Kernels:

In CNN dictionary, Kernel = filters = feature detector.

2. Why should we only (well mostly) use 3x3 Kernels?



3. How many times do we need to perform 3x3 convolution operation to reach 1x1 from 199x199 (show calculations)

We need to perform 199-2 = 197 iterations. So let do it:

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
 


Feeling after manually doing the above calcuation:
 


 
![alt text](https://media.giphy.com/media/FoH28ucxZFJZu/giphy.gif)
