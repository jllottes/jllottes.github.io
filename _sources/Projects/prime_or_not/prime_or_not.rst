A prime or not a prime
======================

`Example report <../../_static/projects/Project01_example.html>`_
    
.. rubric:: due: Friday, February 14th at 11:59 PM

Prime numbers
-------------

A *prime number* is an integer greater than 1 which is divisible only by
1 and by itself. For example, 5 is a prime but 6 is not since 6 is
divisible by 1, 2, 3, and 6. There are infinitely many prime numbers.
Here is the list of all primes smaller than 50:

.. math:: 2, 3, 5, 7, 11, 13, 17, 19, 23, 29, 31, 37, 41, 43, 47

Prime numbers are the building blocks of integers: any integer
:math:`n>1` can be written in a unique way as a product of
primes

.. math:: n = p_{1}\cdot p_{2} \cdot {\dots} \cdot p_{m}

such that :math:`p_{1} \leq p_{2} \leq {\dots} \leq p_{m}`. This
product called the *primary decomposition* of :math:`n`. For example:
:math:`12 = 2\cdot 2\cdot 3`, :math:`25 = 5\cdot 5`,
:math:`90 = 2\cdot 3\cdot 3\cdot 5`.


**Exercise 1.** Write a Python function ``my_primes(n)`` that returns the
list of all primes smaller or equal to ``n``, ordered from the smallest
to the largest:

.. code:: python

    my_primes(10)


.. container:: output

    [2, 3, 5, 7]


.. code:: python

    my_primes(29)

.. container:: output

    [2, 3, 5, 7, 11, 13, 17, 19, 23, 29]


**Exercise 2.** Write a Python function ``primary(n)`` that for each
integer ``n`` greater than 1 returns a list

.. math:: [p_{1}, p_{2}, \dots, p_{m}]

where :math:`p_{1}, \dots, p_{m}` are primes such that
:math:`p_{1} \leq p_{2} \leq {\dots} \leq p_{m}` and
:math:`n = p_{1}\cdot p_{2} \cdot {\dots} \cdot p_{m}`:

.. code:: python

    primary(10)

.. container:: output

    [2, 5]



.. code:: python

    primary(90)

.. container:: output

    [2, 3, 3, 5]



Primes and false primes
-----------------------

Prime numbers are important in mathematics as well as in some practical
applications. For example, they are used to encrypt data (credit card
numbers etc.) so that it can be transmitted securely. For this reason it
is interesting to look for new methods that can help us recognize which
numbers are prime and which are not. Here we will explore one such
possible method.

Congruences
~~~~~~~~~~~

Given integers :math:`m, n` and :math:`k` we say that :math:`m` and
:math:`n` are *congruent modulo* :math:`k` if the reminder from dividing
:math:`m` by :math:`k` is the same as the reminder from dividing
:math:`n` by :math:`k`. In such situation we write
:math:`m \equiv n \ (\text{mod } 7)`. For example
:math:`19 \equiv 47 \ (\text{mod } 7)` since

.. math:: 19 = 2\cdot 7 + 5 \ \ \ \ \ \ \ 47 = 6\cdot 7 + 5

so the reminder from division of both 19 and 47 by 7 is 5.


**Note.** The congruence relation is preserved by the arithmetic
operations: if :math:`m_{1} \equiv n_{1} \ (\text{mod } k)` and
:math:`m_{2} \equiv n_{2} \ (\text{mod } k)` then
:math:`m_{1}+ m_{2} \equiv n_{1}+n_{2} \ (\text{mod } k)` and
:math:`m_{1}m_{2} \equiv n_{1}n_{2} \ (\text{mod } k)`.

Congruences and prime numbers
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Here is a basic fact in number theory that relates prime numbers and
congruences:

**Theorem** (Fermat's little theorem). If :math:`p` is a prime number then

.. math:: a^{p} \equiv a \ (\text{mod } p)

for any integer :math:`0 \leq a < p`.

For example, for :math:`p=3` we have

.. math:: 1^{3} = \phantom{2}1  \equiv 1 \ (\text{mod } 3)

.. math:: 2^{3} = \phantom{2}8  \equiv 2 \ (\text{mod } 3)

.. math:: 3^{3} = 27 \equiv 3 \ (\text{mod } 3)

.. math:: 4^{3} = 64 \equiv 4 \ (\text{mod } 3)

which shows that the formula :math:`a^{3} \equiv a \ (\text{mod } 3)`
holds for :math:`a= 1, 2, 3, 4`.

The formula from the above theorem does not hold in general if :math:`p`
is not a prime number. For example for :math:`p = 4` and :math:`a = 2`
we have :math:`2^{4}= 16` which is not congruent to 2 modulo 4.

If it would turn out that the only numbers :math:`p` that satisfy the
formula :math:`a^{p} \equiv a \ (\text{mod } p)` for all :math:`0 \leq a < p` are
prime numbers we would get a new way of recognizing which numbers are
prime. It turns out, however, that there are numbers :math:`p\geq 2` such that:

-  :math:`p` is not a prime
-  the formula :math:`a^{p} \equiv a \ (\text{mod } p)` holds for all
   :math:`0 \leq a < p`

We will call such numbers *false primes*. The smallest number (besides 1) which is a
false prime is 561.


Project
-------

**Part 1.** Write a Python script to find the first 20 false primes.

**Hint.** Call a number :math:`p` *prime-like* if :math:`p\geq 2` and the formula
:math:`a^{p} \equiv a \ (\text{mod } p)` holds for all :math:`0 \leq a < p`.
You can start your work on part 1  by writing a function ``is_prime_like(n)`` that returns ``True`` if ``n`` is
prime-like and returns ``False`` otherwise. Once you know that an integer is prime-like you just need to
check that it is not a prime number.

**Part 2.** Compute the primary decomposition of each false prime you found.

**Part 3.** What can you say or conjecture about properties of false
primes?

**Note.** In order to compute with Python the reminder from division of
the number :math:`a^{n}` by :math:`k` we can use the command
``(a**n)%k``. For example:

.. code:: python

    print(7**2 % 5)


.. container:: output

    4


This method is however inefficient, since Python computes first
:math:`a^{n}`, which can be a very large number, and only then
calculates the reminder from division by :math:`k`. A much faster way of
performing the same computation is by using the function ``pow()`` which
uses modular arithmetic to compute the power and the reminder at the
same time. The result of the command ``pow(a,n,k)`` is exactly the same
as that of ``(a**n)%k``:

.. code:: python

    print(pow(7, 2, 5))


.. container:: output

    4


The function ``pow()`` can be also used with two arguments. The command
``pow(a,n)`` returns simply the power :math:`a^{n}`.

.. code:: python

    print(pow(7, 2))


.. container:: output

    49