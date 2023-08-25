# MULTI DIMENSIONAL ARRAYS - MASTERING THE MATRIX

## What are arrays?

Arrays are data structures in which:
 * elements are stored in sequential order. The position of each element is its index.
 * A contiguous block of memory which means that each element of the array are stored in the memory such that there are no gaps between their memory addresses.
 * The elements are typically of the same datatpye. 
 * Elements are mutable 

 ## Multi dimensional arrays (MD array)

 * Each element of a multi dimensional array is a one-dimensionsional or a multi dimensional array
 * Can be visualised as a matrix where index of each element is its position in the matrix
 * **While it may seem like the elements in the array are not contiguous as they are stored in a matrix-like form, it is not the case.**

## BUT WHY BOTHER?

* Multi dmensional arrays or arrays in general may seem very trivial but they have immense applications in both the computing and the "real" world
* Matrix manipulation and operation on matrices is an obvious application. With the ever-increasing demand of data science, it is essential to master this tool to perform even the very basic data manipulation tasks.
* Image and video processing - images are often viewed as a 2-dimensinal grid of data which is essentially a MD array
* These are just a few examples, you can literally think of any data related task and chances are that the core data structure is a MD array. 
* Perhaps the most striking featur of MD arrays is that it enables us to break the shackles of imagination and perceptions. If there are more than 10 features to a particular model, it is not possible to interpret physicallly or graphically. For instance, the first 3 features can be easily plotted, the 4th feature may be represented by colour of point and so on..but sooner than later a limit will be reach to effectively express it. Here comes **matrix manipulation which can effortlessly calculate and manipulate data of more than 1000s of features**.

# Overhead

While it may seem like ALL IS WELL but MD arrays have their fair share of negatives as well
* Element addition and deletion
* Memory allocation and utilisation

---

## Arrays in Python

* Python is like that one kid who has every single possible type of candy in his backpack
* There is a special type of array called Lists in python which can have elements of different data types.

`a = ['1',2,5.2,3]`

This may look very appealing but it is a headache for the compiler to keep additional data like object type of each element which makes it inefficient for calculations.

Here a library called NumPy comes handy. It has a method called array which allows homogeneous ie. same type of elements in array.

```
import numpy as np

arr = np.array([1, 2, 3, 4, 5])
```

To access elements, simply the index of the element is used:

```
a = arr[0]
```

Now each dimension of the MD array is known as an axis and the tuple containing the number of elements in each dimension is called the shape of the array.

```
#creating empty array with all elements 0
empty_array = np.empty((3,4),0)

#creating custom array with lists
l1 = [2,3,4]
l2  = [3,4,5]
new_array = np.array([l1,l2])
```

To access elements from multidimensional arrays, the position in each dimension(axes) must be mentioned in a single bracket after arrayname seperated by ','.

```
2nd_el_1st_row = new_array[0,1] #prints 3
last_el_last_row = new_array[-1,-1] #prints 5
```

## Some useful functions:

```
array.ndim #tells no. of dimensions(axes) in array
array.size #tells no. of elements in array
array.shape #tells the number of elements stored along each dimension of the array
array.reshape #changes shape of array as demonstrated
a = np.array([1,2,3,4,5,6])
a.reshape(3,2) # a = [[1,2,3],[4,5,6]]
 
```
![Visualising_MD_arrays](https://miro.medium.com/v2/resize:fit:828/format:webp/1*sxnhgeSptW8Jfol8XUyP-Q.png)


## Slicing

A powerful tool in Python is list slicing, which basically means to get a portion of a list kind of like a substring

```
#for a general list
a = [1,2,3,4,5]
b = a[1:4] # b = [2,3,4]

#for numpy array
a = np.array([1,2,3,4,5])
a[0:3] #array([1,2,3])
```
![Array Slicing](https://scipy-lectures.org/_images/numpy_indexing.png)


Using expressions for slicing lists

a = a[a < 5] # a  = [1,2,3,4]

# Functions for array manipulation

Addition :

```
arr = np.array([[18, 25, 37], [5, -7, 15]])
arr1 = np.array([[4, 8, 12], [-13, 24, 17]])
arr2 = np.add(arr, arr1) #Adds element-wise
```

Multiplication :

```
np.dot(array a, array b)   #scalar/dot product of two arrays
np.matmul(array a, array b)   #the matrix product of two arrays
np.multiply(array a, array b)  #element-wise matrix multiplication of two arrays
```
You can check this site to get a pretty good basic understanding of array multiplication:

[Multiplication of arrays](https://www.educative.io/blog/numpy-matrix-multiplication)


Divison


```
#both a1 and a2 need to be of same shape for divison to be performed
a1 = np.array([[2,6,5],[3,4,8]])
a2 = np.array([[1,7,2],[10,9,4]])
res = np.divide(a1,a2) 
```

# Time to Matrix-tically wrap this up!

I hope the reader has got a basic understanding of what MD arrays are. See you in the binary sunset!


![Siuuuu](https://media.makeameme.org/created/whenevr-you-watch.jpg)
