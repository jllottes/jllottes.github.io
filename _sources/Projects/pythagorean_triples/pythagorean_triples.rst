Pythagorean triples
===================

.. rubric:: due: Sunday, March 2nd at 11:59 PM

The Pythagorean Theorem says that positive numbers :math:`a`,
:math:`b`, :math:`c` are lengths of sides of a right triangle if and
only if :math:`a^2 + b^2 = c^2`.

.. image:: pythagorean_triples-1.svg
   :width: 170px
   :align: center


An interesting problem is to determine which triples of integers satisfy
this equation.

**Definiton.** A triple of positive integers :math:`(a, b, c)` such that
:math:`a^2 + b^2 = c^2` is called a *Pythagorean triple*.

**Example.** :math:`(3, 4, 5)` is a Pythagorean triple since
:math:`3^2 + 4^2 = 5^2`.

**Note.** In order to find a Pythagorean triple it is enough to
find a couple of positive integers :math:`(a, b)` such that
:math:`\sqrt{a^2 + b^2}` is also an integer. This gives a
Pythagorean triple :math:`(a, b, c)` where
:math:`c = \sqrt{a^2 + b^2}`. We will say in such case that
:math:`(a, b)` is a *Pythagorean tuple*.

The goal of this project is to investigate the structure of Pythagorean
triples.

Project
-------

**Part 1.** Write a function ``get_ptriples(n)`` that takes as its argument
a number :math:`n` and returns a list of all  Pythagorean triples :math:`(a, b, c)`
where :math:`1 \leq a, b \leq n`:



.. code:: python

    get_ptriples(20)




.. container:: output

    [[3, 4, 5],
    [4, 3, 5],
    [5, 12, 13],
    [6, 8, 10],
    [8, 6, 10],
    [8, 15, 17],
    [9, 12, 15],
    [12, 5, 13],
    [12, 9, 15],
    [12, 16, 20],
    [15, 8, 17],
    [15, 20, 25],
    [16, 12, 20],
    [20, 15, 25]]



**Part 2.** Plot all Pythagorean tuples :math:`(a, b)` where
:math:`1\leq a, b \leq n` for various values of :math:`n`.

**Part 3.** Describe and analyze the structure of Pythagorean tuples.

**Note.** There are many possible directions to take to analyze the structure of Pythagorean tuples. One possibility is to look into "primitive Pythagorean tuples", which we will discuss in class.