Mayfly model
============

.. rubric:: due: Sunday, March 23rd at 11:59 PM

Population models
-----------------

An interesting problem in mathematics is to try to predict changes in
populations of people, animals, insects, bacteria etc. How many people
will live in the United States in 20 years? If a cell culture in a lab
is started with :math:`x` cells how many cells will it consist of in 24
hours? Mathematical models used to make such predictions are often
complex and involve many factors. Here we will consider a simple
population model that may be applicable e.g. to predicting population
changes of `mayflies <https://en.wikipedia.org/wiki/Mayfly>`__. These
insects spend a year (or a few years - depending on species) at the
bottom of a river, then over a course of a few days emerge from the
water, mate, lay eggs and die. In effect only one generation of mayflies
is alive at any time. We will assume that the size of population of
mayflies in a given year depends only on the size of population in the
previous year. If :math:`x_n` denotes the size of population in year
:math:`n` then we can write:

.. math:: x_{n} = g(x_{n-1})\cdot x_{n-1} \ \ \ \ \ \ \ \ \ \ \ (\ast)

where :math:`g(x_{n-1})` is the growth rate of the population (which may
depend on :math:`x_{n-1}`). Properties of this model will depend of
course on what the function :math:`g(x)` is.

The simplest case: constant growth rate
---------------------------------------

The simplest model is obtained by assuming that :math:`g` is a constant
function: :math:`g(x) = a` for some fixed number :math:`a`. In such case
we get:

.. math:: x_n = ax_{n-1}

For example, if :math:`a=2` then population doubles each year.
Inductively this formula gives :math:`x_n = a^n x_{0}`. This describes
an exponential growth for :math:`a>1` and exponential decay for
:math:`a<1`:

.. image:: mayfly_model-1.svg
   :width: 500 px
   :align: center


The exponential model may reflect reality in a short run, but it is not
realistic in a long range since it predicts that a population will
either grow to infinity, or it will collapse to zero.

Mayfly model: linear growth rate
--------------------------------

In order to improve on the exponential model we can reason as follows.

-  In a small population there is little competition for resources such
   as food, space etc. This allows for fast population growth. As the
   population increases the competition for these resources increases as
   well, and we can expect that the growth rate will go down. This means
   that the function :math:`g(x)` describing the growth rate should be a
   decreasing function.

-  It is also reasonable to assume that the population can grow only up
   to some maximal size :math:`M`. As the population size approaches
   :math:`M` the growth rate should approach :math:`0`. In effect we can
   assume that :math:`g(M) = 0` (meaning that there will be no new generation).

The simplest function satisfying the above conditions is the linear
function

.. math:: g(x) = a(M-x)

for some :math:`a>0`.

.. image:: mayfly_model-2.svg
   :width: 250 px
   :align: center


If we use this function then the equation :math:`(\ast)` becomes

.. math:: x_n = a(M-x_{n-1})x_{n-1} \ \ \ \ \ \ \ \ \ \ (\ast\ast)

This equation involves two parameters: :math:`M` and :math:`a`. We can
reduce them to one parameter as follows. Define

.. math:: y_n = \frac{x_n}{M}

The equation :math:`(\ast\ast)` now becomes

.. math:: M y_n = a(M- My_{n-1}) My_{n-1}

Simplifying we obtain

.. math:: y_n = aM(1-y_{n-1})y_{n-1}

If we denote :math:`b = aM` then we get

.. math:: y_n = b(1-y_{n-1})y_{n-1}

for some :math:`b\geq 0`. This is the equation we will be interested in.
We will call the population model described by this equation the *mayfly
model*.

**Note.**

1. In the mayfly model meaningful values of :math:`y_n` are
   the ones between :math:`0` and :math:`1` since :math:`y_n = x_n/M` and
   by assumption :math:`0\leq x_n \leq M`.

2. For :math:`b\geq 0` the maximal value of the function :math:`b(1-y)y`
   is attained at :math:`y=1/2` and it is equal to :math:`b/4`. This
   means that the mayfly model may break if :math:`b>4`, since in such
   case for :math:`y_n = 1/2` we will get :math:`y_{n+1} = b/4 > 1`. To
   avoid such problems we will assume that :math:`0\leq b \leq 4`.

3. Notice that beside the choice of :math:`b` the model depends also on
   the value of the initial population :math:`y_0`.

**Exercise 1.** Modify the Lissajous curve slider code (from class, see 
`week06_notebook <../_static/weekly_notebooks/week06_notebook.html>`_) to 
plot the mayfly population with sliders for the initial population :math:`y0`
and growth rate :math:`b`. This interactive plot does not need to appear in
your project report, but it is useful for exploring the mayfly model dynamics.

Project
-------

Analyze behavior of the mayfly model for various values of :math:`b` and
:math:`y_0`. Describe your findings, observations and conclusions.

**Suggestions:** 

1. It will be helpful to look for equilibrium populations, that is, populations 
where :math:`y_n` is constant. How do these depend on :math:`y_0` and :math:`b`?
How do they relate to our observations?

2. If you decide to include an interactive plot in your report, then you should
explain clearly in markdown cells what you want the reader to see. That is,
you should explain how the sliders should be manipulated to lead the reader in
making specific observations and conclusions. Alternatively, you can write code
to animate an interactive plot so that the reader doesn't need to manually move
the sliders, or you can simply use subplots to compare between different choices
of :math:`y_0` and :math:`b`.