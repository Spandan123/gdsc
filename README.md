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
```
