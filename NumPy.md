<h1 align='center'><u>Basic Numpy</u></h1> 


```python
import numpy as np
```

<h2 align='center'>A.Creating Numpy Arrays</h2>

### 1.By converting lists to np arrays


```python
x = np.array([1,2,3,4,5])
print(f'x={x}')
```

    x=[1 2 3 4 5]



```python
# We print information about x
print('x has dimensions:', x.shape)
print('x is an object of type:', type(x))
print('The elements in x are of type:', x.dtype)
```

    x has dimensions: (5,)
    x is an object of type: <class 'numpy.ndarray'>
    The elements in x are of type: int64



```python
# We create a rank 1 ndarray that only contains strings
x = np.array(['Hello', 'World'])

# We print x
print()
print('x = ', x)
print()

# We print information about x
print('x has dimensions:', x.shape)
print('x is an object of type:', type(x))
print('The elements in x are of type:', x.dtype)
```

    
    x =  ['Hello' 'World']
    
    x has dimensions: (2,)
    x is an object of type: <class 'numpy.ndarray'>
    The elements in x are of type: <U5



```python
# We create a rank 1 ndarray from a Python list that contains integers and strings
x = np.array([1, 2, 'World'])

# We print the ndarray
print()
print('x = ', x)
print()

# We print information about x
print('x has dimensions:', x.shape)
print('x is an object of type:', type(x))
print('The elements in x are of type:', x.dtype)
#Note the output whole array is of one single data type
```

    
    x =  ['1' '2' 'World']
    
    x has dimensions: (3,)
    x is an object of type: <class 'numpy.ndarray'>
    The elements in x are of type: <U21



```python
# We create a rank 2 ndarray that only contains integers
Y = np.array([[1,2,3],[4,5,6],[7,8,9], [10,11,12]])

# We print Y
print()
print('Y = \n', Y)
print()

# We print information about Y
print('Y has dimensions:', Y.shape)
print('Y has a total of', Y.size, 'elements')
print('Y is an object of type:', type(Y))
print('The elements in Y are of type:', Y.dtype)
```

    
    Y = 
     [[ 1  2  3]
     [ 4  5  6]
     [ 7  8  9]
     [10 11 12]]
    
    Y has dimensions: (4, 3)
    Y has a total of 12 elements
    Y is an object of type: <class 'numpy.ndarray'>
    The elements in Y are of type: int64


### Even though NumPy automatically selects the dtype of the ndarray,
### NumPy also allows you to specify the particular dtype you want to assign to the elements of the ndarray. 
### You can specify the dtype when you create the ndarray using the keyword dtype in the np.array() function. 


```python
# We create a rank 1 ndarray of floats but set the dtype to int64
x = np.array([1.5, 2.2, 3.7, 4.0, 5.9], dtype = np.int64)

# We print x
print()
print('x = ', x)
print()

# We print the dtype x
print('The elements in x are of type:', x.dtype)
```

    
    x =  [1 2 3 4 5]
    
    The elements in x are of type: int64


### Saving numpy arrays into file and loading it(saved as .npy)


```python
# We create a rank 1 ndarray
x = np.array([1, 2, 3, 4, 5])

# We save x into the current directory as 
np.save('my_array', x)
```


```python
# We load the saved array from our current directory into variable y
y = np.load('my_array.npy')

# We print y
print()
print('y = ', y)
print()

# We print information about the ndarray we loaded
print('y is an object of type:', type(y))
print('The elements in y are of type:', y.dtype)
```

    
    y =  [1 2 3 4 5]
    
    y is an object of type: <class 'numpy.ndarray'>
    The elements in y are of type: int64


### 2.Using Built-in Functions

### numpy.zeros(shape, dtype=float, order='C')


```python
X = np.zeros((3,4),dtype=int)
print(X)
```

    [[0 0 0 0]
     [0 0 0 0]
     [0 0 0 0]]


### numpy.ones(shape, dtype=None, order='C')


```python
X = np.ones((3,2))
print(X)
```

    [[1. 1.]
     [1. 1.]
     [1. 1.]]


### numpy.full(shape, fill_value, dtype=None, order='C')


```python
X = np.full((2,3), 5)#takes datatype of input value
print(X)
print()
Y= np.full((2,3), [1,'ishan',2]) #note number of columns must be equal to fill_value array size
print(Y)
```

    [[5 5 5]
     [5 5 5]]
    
    [['1' 'ishan' '2']
     ['1' 'ishan' '2']]


### numpy.eye(N, M=None, k=0, dtype=<class 'float'>, order='C')


```python
X = np.eye(5,dtype=int)
print(X)
```

    [[1 0 0 0 0]
     [0 1 0 0 0]
     [0 0 1 0 0]
     [0 0 0 1 0]
     [0 0 0 0 1]]


### numpy.diag(v, k=0)
kint, optional

Diagonal in question. The default is 0. Use k>0 for diagonals above the main diagonal, and k<0 for diagonals below the main diagonal.



```python
X = np.diag([10,20,30,50])
print(X)
```

    [[10  0  0  0]
     [ 0 20  0  0]
     [ 0  0 30  0]
     [ 0  0  0 50]]


### numpy.arange([start, ]stop, [step, ]dtype=None)


```python
x = np.arange(10)

print(x)
print()

y = np.arange(4,10)

print(y)
print()

z = np.arange(1,14,3)

print(z)
print()
```

    [0 1 2 3 4 5 6 7 8 9]
    
    [4 5 6 7 8 9]
    
    [ 1  4  7 10 13]
    


### even though the np.arange() function allows for non-integer steps, such as 0.3, the output is usually inconsistent, due to the finite floating point precision. 

### numpy.linspace(start, stop, num=50, endpoint=True, retstep=False, dtype=None, axis=0)


```python
# We create a rank 1 ndarray that has 10 integers evenly spaced between 0 and 25.
x = np.linspace(0,25,10)

# We print the ndarray
print()
print('x = \n', x)
print()
```

    
    x = 
     [ 0.          2.77777778  5.55555556  8.33333333 11.11111111 13.88888889
     16.66666667 19.44444444 22.22222222 25.        ]
    


### np.reshape(ndarray, new_shape)


```python
x = np.reshape(x, (5,2))

print(x)
print()

Y = np.arange(20).reshape(4, 5)

print(Y)
```

    [[ 0.          2.77777778]
     [ 5.55555556  8.33333333]
     [11.11111111 13.88888889]
     [16.66666667 19.44444444]
     [22.22222222 25.        ]]
    
    [[ 0  1  2  3  4]
     [ 5  6  7  8  9]
     [10 11 12 13 14]
     [15 16 17 18 19]]


### np.random.random(shape)
with random floats in the half-open interval [0.0, 1.0)


```python
X = np.random.random((3,3))

print(X)
```

    [[0.61853248 0.32213218 0.39086456]
     [0.7180341  0.9293746  0.77943849]
     [0.57602494 0.69117078 0.07740787]]


### np.random.randint(start, stop, size = shape)
random integers in the half-open interval [start, stop)


```python
X = np.random.randint(4,15,size=(3,2))
print(X)
```

    [[11 10]
     [ 4  9]
     [ 5 14]]


In some cases, you may need to create ndarrays with random numbers that satisfy certain statistical properties. For example, you may want the random numbers in the ndarray to have an average of 0. NumPy allows you create random ndarrays with numbers drawn from various probability distributions. The function np.random.normal(mean, standard deviation, size=shape), for example, creates an ndarray with the given shape that contains random numbers picked from a normal (Gaussian) distribution with the given mean and standard deviation. Let's create a 1,000 x 1,000 ndarray of random floating point numbers drawn from a normal distribution with a mean (average) of zero and a standard deviation of 0.1.


```python
X = np.random.normal(0, 0.1, size=(1000,1000))

print()
print('X = \n', X)
print()

# We print information about X
print('X has dimensions:', X.shape)
print('X is an object of type:', type(X))
print('The elements in X are of type:', X.dtype)
print('The elements in X have a mean of:', X.mean())
print('The maximum value in X is:', X.max())
print('The minimum value in X is:', X.min())
print('X has', (X < 0).sum(), 'negative numbers')
print('X has', (X > 0).sum(), 'positive numbers')
```

    
    X = 
     [[-0.04263308 -0.02294358  0.12837799 ...  0.07377007  0.18564738
      -0.12834024]
     [ 0.04318837 -0.14493155  0.01587642 ...  0.08378954 -0.1026855
      -0.11827792]
     [-0.0913915   0.14842814 -0.05293135 ... -0.01925517  0.06544787
      -0.11646424]
     ...
     [ 0.03422818 -0.09721159  0.06133823 ... -0.0273124   0.03284017
      -0.1017433 ]
     [-0.04687082 -0.09635745 -0.19078807 ...  0.08339463 -0.03262759
      -0.03174562]
     [-0.0440551  -0.00469147  0.02960465 ...  0.15276602  0.19640379
       0.1113167 ]]
    
    X has dimensions: (1000, 1000)
    X is an object of type: <class 'numpy.ndarray'>
    The elements in X are of type: float64
    The elements in X have a mean of: 9.73572160453743e-06
    The maximum value in X is: 0.49855043341077726
    The minimum value in X is: -0.47138648302414243
    X has 499877 negative numbers
    X has 500123 positive numbers


<h2 align = 'center'>B.Inserting/Deleting in numpy arrays</h2>

### numpy arrays are mutable and hence can be changed after assignment

### 1.Accessing elements


```python
x = np.array([1, 2, 3, 4, 5])

print(x[0])
print()
print(x[-1])
```

    1
    
    5


### 2.Modifying Elements


```python
x[0] = 6
print(x)
```

    [6 2 3 4 5]



```python
X = np.array([[1,2,3],[4,5,6],[7,8,9]])
print(X)

print()

print(X[0][0])

print()

X[0][0] = 10

print(X)
```

    [[1 2 3]
     [4 5 6]
     [7 8 9]]
    
    1
    
    [[10  2  3]
     [ 4  5  6]
     [ 7  8  9]]


### numpy.delete(arr, obj, axis=None)
<h3 style='color:green'>axis=0 implies x-axis<br>axis=1 implies y-axis</h3>


```python
x = np.array([1, 2, 3, 4, 5])
print(x)

x = np.delete(x,[0,4])#deletes first and last element
print()
print(x)
print()

Y = np.array([[1,2,3],[4,5,6],[7,8,9]])
print(Y)
print()

# We delete the first row of y
w = np.delete(Y, 0, axis=0)
print(w)
print()

# We delete the first and last column of y
v = np.delete(Y, [0,2], axis=1)
print(v)

```

    [1 2 3 4 5]
    
    [2 3 4]
    
    [[1 2 3]
     [4 5 6]
     [7 8 9]]
    
    [[4 5 6]
     [7 8 9]]
    
    [[2]
     [5]
     [8]]


### numpy.append(arr, values, axis=None)


```python
x = np.array([1, 2, 3, 4, 5])

print(x,end='\n\n')

x = np.append(x, 6)

print(x)
print()

x = np.append(x, [7,8])

print(x)
print()

Y = np.array([[1,2,3],[4,5,6]])
print(Y)
print()

v = np.append(Y, [[7,8,9]], axis=0)
print(v)
print()

q = np.append(Y,[[9],[10]], axis=1)#note this
print(q)

```

    [1 2 3 4 5]
    
    [1 2 3 4 5 6]
    
    [1 2 3 4 5 6 7 8]
    
    [[1 2 3]
     [4 5 6]]
    
    [[1 2 3]
     [4 5 6]
     [7 8 9]]
    
    [[ 1  2  3  9]
     [ 4  5  6 10]]


### numpy.insert(arr, obj, values, axis=None)


```python
x = np.array([1, 2, 5, 6, 7])
print(x)
print()

x = np.insert(x,2,[3,4])#at 2nd index
print(x)
print()

Y = np.array([[1,2,3],[7,8,9]])
print(Y)
print()

# We insert a row between the first and last row of y
w = np.insert(Y,1,[4,5,6],axis=0)
print(w)
print()

# We insert a column full of 5s between the first and second column of y
v = np.insert(Y,1,5, axis=1)
print(v)
```

    [1 2 5 6 7]
    
    [1 2 3 4 5 6 7]
    
    [[1 2 3]
     [7 8 9]]
    
    [[1 2 3]
     [4 5 6]
     [7 8 9]]
    
    [[1 5 2 3]
     [7 5 8 9]]


### NumPy also allows us to stack ndarrays on top of each other, or to stack them side by side. The stacking is done using either the np.vstack() function for vertical stacking, or the np.hstack() function for horizontal stacking. It is important to note that in order to stack ndarrays, the shape of the ndarrays must match.


```python
x = np.array([1,2])

Y = np.array([[3,4],[5,6]])
print(Y)
print()
z = np.vstack((x,Y))
print(z)
print()

w = np.hstack((Y,x.reshape(2,1)))
print(w)

```

    [[3 4]
     [5 6]]
    
    [[1 2]
     [3 4]
     [5 6]]
    
    [[3 4 1]
     [5 6 2]]


### slicing
#### 1. ndarray[start:end]
#### 2. ndarray[start:]
#### 3. ndarray[:end]


```python
X = np.arange(20).reshape(4, 5)
print(X)
print()

# We select all the elements that are in the 2nd through 4th rows and in the 3rd to 5th columns
Z = X[1:4,2:5]#row,cloumn
print(Z)
print()

# We select all the elements that are in the 1st through 3rd rows and in the 3rd to 4th columns
Y = X[:3,2:5]
print(Y)
print()

# We select all the elements in the 3rd row
v = X[2,:]
print(v)#note it prints 1d array
print()

# We select all the elements in the 3rd column but return a rank 2 ndarray
R = X[:,2:3]
print(R)
print()


```

    [[ 0  1  2  3  4]
     [ 5  6  7  8  9]
     [10 11 12 13 14]
     [15 16 17 18 19]]
    
    [[ 7  8  9]
     [12 13 14]
     [17 18 19]]
    
    [[ 2  3  4]
     [ 7  8  9]
     [12 13 14]]
    
    [10 11 12 13 14]
    
    [[ 2]
     [ 7]
     [12]
     [17]]
    


### It is important to note that when we perform slices on ndarrays and save them into new variables, as we did above, the data is not copied into the new variable. 
#### Z = X[1:4,2:5]
### the slice of the original array X is not copied in the variable Z. Rather, X and Z are now just two different names for the same ndarray. We say that slicing only creates a view of the original array. This means that if you make changes in Z you will be in effect changing the elements in X as well.


```python
X = np.arange(20).reshape(4, 5)
print(X)
print()

Z = X[1:4,2:5]
print(Z)
print()

Z[2,2] = 555

print(X)
```

    [[ 0  1  2  3  4]
     [ 5  6  7  8  9]
     [10 11 12 13 14]
     [15 16 17 18 19]]
    
    [[ 7  8  9]
     [12 13 14]
     [17 18 19]]
    
    [[  0   1   2   3   4]
     [  5   6   7   8   9]
     [ 10  11  12  13  14]
     [ 15  16  17  18 555]]


### np.copy()


```python
X = np.arange(20).reshape(4, 5)
print(X)
print()

W = X[1:4,2:5].copy()

W[2,2] = 444

print(X)
```

    [[ 0  1  2  3  4]
     [ 5  6  7  8  9]
     [10 11 12 13 14]
     [15 16 17 18 19]]
    
    [[ 0  1  2  3  4]
     [ 5  6  7  8  9]
     [10 11 12 13 14]
     [15 16 17 18 19]]


### It is often useful to use one ndarray to make slices, select, or change elements in another ndarray. Let's see some examples:


```python
# We create a 4 x 5 ndarray that contains integers from 0 to 19
X = np.arange(20).reshape(4, 5)

# We create a rank 1 ndarray that will serve as indices to select elements from X
indices = np.array([1,3])

# We print X
print()
print('X = \n', X)
print()

# We print indices
print('indices = ', indices)
print()

# We use the indices ndarray to select the 2nd and 4th row of X
Y = X[indices,:]

# We use the indices ndarray to select the 2nd and 4th column of X
Z = X[:, indices]

# We print Y
print()
print('Y = \n', Y)

# We print Z
print()
print('Z = \n', Z)
```

    
    X = 
     [[ 0  1  2  3  4]
     [ 5  6  7  8  9]
     [10 11 12 13 14]
     [15 16 17 18 19]]
    
    indices =  [1 3]
    
    
    Y = 
     [[ 5  6  7  8  9]
     [15 16 17 18 19]]
    
    Z = 
     [[ 1  3]
     [ 6  8]
     [11 13]
     [16 18]]


### np.diag(arr,k=0)
### np.unique(arr)

### Boolean indexing


```python
# We create a 5 x 5 ndarray that contains integers from 0 to 24
X = np.arange(25).reshape(5, 5)

# We print X
print()
print('Original X = \n', X)
print()

# We use Boolean indexing to select elements in X:
print('The elements in X that are greater than 10:', X[X > 10])
print('The elements in X that less than or equal to 7:', X[X <= 7])
print('The elements in X that are between 10 and 17:', X[(X > 10) & (X < 17)])

# We use Boolean indexing to assign the elements that are between 10 and 17 the value of -1
X[(X > 10) & (X < 17)] = -1

# We print X
print()
print('X = \n', X)
print()
```

    
    Original X = 
     [[ 0  1  2  3  4]
     [ 5  6  7  8  9]
     [10 11 12 13 14]
     [15 16 17 18 19]
     [20 21 22 23 24]]
    
    The elements in X that are greater than 10: [11 12 13 14 15 16 17 18 19 20 21 22 23 24]
    The elements in X that less than or equal to 7: [0 1 2 3 4 5 6 7]
    The elements in X that are between 10 and 17: [11 12 13 14 15 16]
    
    X = 
     [[ 0  1  2  3  4]
     [ 5  6  7  8  9]
     [10 -1 -1 -1 -1]
     [-1 -1 17 18 19]
     [20 21 22 23 24]]
    


### set operations


```python
# We create a rank 1 ndarray
x = np.array([1,2,3,4,5])

# We create a rank 1 ndarray
y = np.array([6,7,2,8,4])

# We print x
print()
print('x = ', x)

# We print y
print()
print('y = ', y)

# We use set operations to compare x and y:
print()
print('The elements that are both in x and y:', np.intersect1d(x,y))
print('The elements that are in x that are not in y:', np.setdiff1d(x,y))
print('All the elements of x and y:',np.union1d(x,y))
```

    
    x =  [1 2 3 4 5]
    
    y =  [6 7 2 8 4]
    
    The elements that are both in x and y: [2 4]
    The elements that are in x that are not in y: [1 3 5]
    All the elements of x and y: [1 2 3 4 5 6 7 8]


### sort



```python
# We create an unsorted rank 1 ndarray
x = np.random.randint(1,11,size=(10,))

# We print x
print()
print('Original x = ', x)

# We sort x and print the sorted array using sort as a function.
print()
print('Sorted x (out of place):', np.sort(x))

# When we sort out of place the original array remains intact. To see this we print x again
print()
print('x after sorting:', x)


```

    
    Original x =  [4 9 2 9 1 9 9 6 8 6]
    
    Sorted x (out of place): [1 2 4 6 6 8 9 9 9 9]
    
    x after sorting: [4 9 2 9 1 9 9 6 8 6]



```python
# We create an unsorted rank 1 ndarray
x = np.random.randint(1,11,size=(10,))

# We print x
print()
print('Original x = ', x)

# We sort x and print the sorted array using sort as a method.
x.sort()

# When we sort in place the original array is changed to the sorted array. To see this we print x again
print()
print('x after sorting:', x)
```

    
    Original x =  [5 2 4 6 8 1 1 6 3 9]
    
    x after sorting: [1 1 2 3 4 5 6 6 8 9]



```python
# We create an unsorted rank 2 ndarray
X = np.random.randint(1,11,size=(5,5))

# We print X
print()
print('Original X = \n', X)
print()

# We sort the columns of X and print the sorted array
print()
print('X with sorted columns :\n', np.sort(X, axis = 0))

# We sort the rows of X and print the sorted array
print()
print('X with sorted rows :\n', np.sort(X, axis = 1))
```

    
    Original X = 
     [[ 4  4  6  9  2]
     [ 1  1  1  6  9]
     [ 3  8  6  3  8]
     [ 4  6  3 10 10]
     [ 2  5  8  1  2]]
    
    
    X with sorted columns :
     [[ 1  1  1  1  2]
     [ 2  4  3  3  2]
     [ 3  5  6  6  8]
     [ 4  6  6  9  9]
     [ 4  8  8 10 10]]
    
    X with sorted rows :
     [[ 2  4  4  6  9]
     [ 1  1  1  6  9]
     [ 3  3  6  8  8]
     [ 3  4  6 10 10]
     [ 1  2  2  5  8]]



```python
X = np.arange(1,26).reshape(5,5)
print(X)

X = X[X%2!=0]

print(X)
```

    [[ 1  2  3  4  5]
     [ 6  7  8  9 10]
     [11 12 13 14 15]
     [16 17 18 19 20]
     [21 22 23 24 25]]
    [ 1  3  5  7  9 11 13 15 17 19 21 23 25]


### Arithmetic operations


```python
# We create two rank 1 ndarrays
x = np.array([1,2,3,4])
y = np.array([5.5,6.5,7.5,8.5])

# We print x
print()
print('x = ', x)

# We print y
print()
print('y = ', y)
print()

# We perfrom basic element-wise operations using arithmetic symbols and functions
print('x + y = ', x + y)
print('add(x,y) = ', np.add(x,y))
print()
print('x - y = ', x - y)
print('subtract(x,y) = ', np.subtract(x,y))
print()
print('x * y = ', x * y)
print('multiply(x,y) = ', np.multiply(x,y))
print()
print('x / y = ', x / y)
print('divide(x,y) = ', np.divide(x,y))
```

    
    x =  [1 2 3 4]
    
    y =  [5.5 6.5 7.5 8.5]
    
    x + y =  [ 6.5  8.5 10.5 12.5]
    add(x,y) =  [ 6.5  8.5 10.5 12.5]
    
    x - y =  [-4.5 -4.5 -4.5 -4.5]
    subtract(x,y) =  [-4.5 -4.5 -4.5 -4.5]
    
    x * y =  [ 5.5 13.  22.5 34. ]
    multiply(x,y) =  [ 5.5 13.  22.5 34. ]
    
    x / y =  [0.18181818 0.30769231 0.4        0.47058824]
    divide(x,y) =  [0.18181818 0.30769231 0.4        0.47058824]



```python
# We create a rank 1 ndarray
x = np.array([1,2,3,4])

# We print x
print()
print('x = ', x)

# We apply different mathematical functions to all elements of x
print()
print('EXP(x) =', np.exp(x))
print()
print('SQRT(x) =',np.sqrt(x))
print()
print('POW(x,2) =',np.power(x,2)) # We raise all elements to the power of 2
```

    
    x =  [1 2 3 4]
    
    EXP(x) = [ 2.71828183  7.3890561  20.08553692 54.59815003]
    
    SQRT(x) = [1.         1.41421356 1.73205081 2.        ]
    
    POW(x,2) = [ 1  4  9 16]



```python
# We create a 2 x 2 ndarray
X = np.array([[1,2], [3,4]])

# We print x
print()
print('X = \n', X)
print()

print('Average of all elements in X:', X.mean())
print('Average of all elements in the columns of X:', X.mean(axis=0))
print('Average of all elements in the rows of X:', X.mean(axis=1))
print()
print('Sum of all elements in X:', X.sum())
print('Sum of all elements in the columns of X:', X.sum(axis=0))
print('Sum of all elements in the rows of X:', X.sum(axis=1))
print()
print('Standard Deviation of all elements in X:', X.std())
print('Standard Deviation of all elements in the columns of X:', X.std(axis=0))
print('Standard Deviation of all elements in the rows of X:', X.std(axis=1))
print()
print('Median of all elements in X:', np.median(X))
print('Median of all elements in the columns of X:', np.median(X,axis=0))
print('Median of all elements in the rows of X:', np.median(X,axis=1))
print()
print('Maximum value of all elements in X:', X.max())
print('Maximum value of all elements in the columns of X:', X.max(axis=0))
print('Maximum value of all elements in the rows of X:', X.max(axis=1))
print()
print('Minimum value of all elements in X:', X.min())
print('Minimum value of all elements in the columns of X:', X.min(axis=0))
print('Minimum value of all elements in the rows of X:', X.min(axis=1))
```

    
    X = 
     [[1 2]
     [3 4]]
    
    Average of all elements in X: 2.5
    Average of all elements in the columns of X: [2. 3.]
    Average of all elements in the rows of X: [1.5 3.5]
    
    Sum of all elements in X: 10
    Sum of all elements in the columns of X: [4 6]
    Sum of all elements in the rows of X: [3 7]
    
    Standard Deviation of all elements in X: 1.118033988749895
    Standard Deviation of all elements in the columns of X: [1. 1.]
    Standard Deviation of all elements in the rows of X: [0.5 0.5]
    
    Median of all elements in X: 2.5
    Median of all elements in the columns of X: [2. 3.]
    Median of all elements in the rows of X: [1.5 3.5]
    
    Maximum value of all elements in X: 4
    Maximum value of all elements in the columns of X: [3 4]
    Maximum value of all elements in the rows of X: [2 4]
    
    Minimum value of all elements in X: 1
    Minimum value of all elements in the columns of X: [1 2]
    Minimum value of all elements in the rows of X: [1 3]



```python
# We create a 2 x 2 ndarray
X = np.array([[1,2], [3,4]])

# We print x
print()
print('X = \n', X)
print()

print('3 * X = \n', 3 * X)
print()
print('3 + X = \n', 3 + X)
print()
print('X - 3 = \n', X - 3)
print()
print('X / 3 = \n', X / 3)
```

    
    X = 
     [[1 2]
     [3 4]]
    
    3 * X = 
     [[ 3  6]
     [ 9 12]]
    
    3 + X = 
     [[4 5]
     [6 7]]
    
    X - 3 = 
     [[-2 -1]
     [ 0  1]]
    
    X / 3 = 
     [[0.33333333 0.66666667]
     [1.         1.33333333]]


