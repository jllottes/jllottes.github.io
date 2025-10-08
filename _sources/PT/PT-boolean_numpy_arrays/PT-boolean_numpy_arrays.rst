
Boolean NumPy arrays
====================

Boolean arrays
--------------

A boolean array is a numpy array with boolean (True/False) values. Such
arrays can be obtained by applying a logical operator to another numpy
array:

.. code:: python

    import numpy as np

    a = np.reshape(np.arange(16), (4,4)) # create a 4x4 array of integers
    print(a)


.. container:: output

    [[ 0  1  2  3]
    \  [ 4  5  6  7]
    \  [ 8  9 10 11]
    \  [12 13 14 15]]


.. code:: python

    large_values = (a > 10) # test which elements of a are greated than 10
    print(large_values)


.. container:: output

    [[False False False False]
    \  [False False False False]
    \  [False False False  True]
    \  [ True  True  True  True]]


.. code:: python

    even_values = (a%2 == 0) # test which elements of a are even
    print(even_values)


.. container:: output

    [[ True False  True False]
    \  [ True False  True False]
    \  [ True False  True False]
    \  [ True False  True False]]


Logical operations on boolean arrays
------------------------------------

Boolean arrays can be combined using logical operators:

+----------+--------------------------+
| operator | meaning                  |
+==========+==========================+
| ``~``    | negation (logical "not") |
+----------+--------------------------+
| ``&``    | logical "and"            |
+----------+--------------------------+
| ``|``    | logical "or"             |
+----------+--------------------------+

.. code:: python

    b = ~(a%3 == 0) # test which elements of a are not divisible by 3

    print('array a:\n{}\n'.format(a))
    print('array b:\n{}'.format(b))


.. container:: output

    array a:
    [[ 0  1  2  3]
    \  [ 4  5  6  7]
    \  [ 8  9 10 11]
    \  [12 13 14 15]]

    array b:
    [[False  True  True False]
    \  [ True  True False  True]
    \  [ True False  True  True]
    \  [False  True  True False]]


.. code:: python

    c = (a%2 == 0) | (a%3 == 0) # test which elements of a are divisible by either 2 or 3

    print('array a:\n{}\n'.format(a))
    print('array c:\n{}'.format(c))


.. container:: output

    array a:
    [[ 0  1  2  3]
    \  [ 4  5  6  7]
    \  [ 8  9 10 11]
    \  [12 13 14 15]]

    array c:
    [[ True False  True  True]
    \  [ True False  True False]
    \  [ True  True  True False]
    \  [ True False  True  True]]


.. code:: python

    d = (a%2 == 0) & (a%3 == 0) # test which elements of a are divisible by both 2 and 3

    print('array a:\n{}\n'.format(a))
    print('array d:\n{}'.format(d))


.. container:: output

    array a:
    [[ 0  1  2  3]
    \  [ 4  5  6  7]
    \  [ 8  9 10 11]
    \  [12 13 14 15]]

    array d:
    [[ True False False False]
    \  [False False  True False]
    \  [False False False False]
    \  [ True False False False]]


Indexing with boolean arrays
----------------------------

Boolean arrays can be used to select elements of other numpy arrays. If
``a`` is any numpy array and ``b`` is a boolean array of the same
dimensions then ``a[b]`` selects all elements of ``a`` for which the
corresponding value of ``b`` is ``True``.

.. code:: python

    a = np.reshape(np.arange(16), (4,4)) # create a 4x4 array of integers
    print(a)


.. container:: output

    [[ 0  1  2  3]
    \  [ 4  5  6  7]
    \  [ 8  9 10 11]
    \  [12 13 14 15]]


.. code:: python

    b = (a%2 == 0) # test which elements of a are even
    print(b)


.. container:: output

    [[ True False  True False]
    \  [ True False  True False]
    \  [ True False  True False]
    \  [ True False  True False]]


.. code:: python

    print(a[b]) # select all even elements of the array a


.. container:: output

    [ 0  2  4  6  8 10 12 14]


We can use this to modify elements of an array that satisfy a logical
condition:

.. code:: python

    a[a%2 == 0] = 100 # set values of all even elements of the array a to 100
    print(a)


.. container:: output

    [[100   1 100   3]
    \  [100   5 100   7]
    \  [100   9 100  11]
    \  [100  13 100  15]]


In the next example we create two numpy arrays, ``x`` and ``y``, and set
all values of ``x`` that are smaller that the corresponding values of
``y`` to -1:

.. code:: python

    x = np.random.random((3,3)) # create a 3x3 array of random numbers
    y = np.random.random((3,3))

    print('array x:\n{}\n'.format(x))
    print('array y:\n{}'.format(y))


.. container:: output

    array x:
    [[ 0.76755354  0.39784664  0.60511187]
    \  [ 0.9584705   0.42498244  0.71316056]
    \  [ 0.30123811  0.2202371   0.64291291]]

    array y:
    [[ 0.58221015  0.09077814  0.26814573]
    \  [ 0.91636671  0.41542893  0.07005894]
    \  [ 0.83128003  0.81483812  0.56582282]]


.. code:: python

    x[x < y] = -1
    print(x)


.. container:: output

    [[ 0.76755354  0.39784664  0.60511187]
    \  [ 0.9584705   0.42498244  0.71316056]
    \  [-1.         -1.          0.64291291]]
