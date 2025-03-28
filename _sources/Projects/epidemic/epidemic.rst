:orphan:

Epidemic
========

.. rubric:: due: Tuesday, December 10th, 11:59pm

In this project we will be working with the following model of a spread of
a contagious disease.

We start with a rectangular grid of cells (i.e. small squares).
Each cell has an associated numerical value, which indicates the status
of the cell:

+------------+-----------------------------------------+
| Value      | Meaning                                 |
+============+=========================================+
| 0          | the cell is healthy                     |
+------------+-----------------------------------------+
| 1          | the cell is sick                        |
+------------+-----------------------------------------+
| 2          | the cell was sick, but is now recovered |
+------------+-----------------------------------------+


The grid with cell values describes spread of a disease in the population
of cells:

.. figure:: epidemic-1.svg
   :width: 450px
   :align: center

   *Healthy, sick, and healed cells.*

In order to model how the disease evolves from one day to the next, we
select two numbers: :math:`p_I` and :math:`p_R`, both in the range between
0 and 1. The number :math:`p_I` is the probability of infection - it indicates
how likely is a sick cell to infect healthy neighboring cells.
The number :math:`p_R` is the probability of recovery of a sick cell.

Given these two numbers, the disease spread changes according to the following rules:

- if a cell is healthy one day, then the probability that it will get sick the
  following day is :math:`1 - (1-p_I)^k`, where :math:`k` is the number of neighbors
  of the cell which are sick. A neighbor of a cell is any cell which shares with it
  either an edge or a corner. For example, on the picture below all black cells are neighbors of the orange cell.

.. figure:: epidemic-2.svg
   :width: 250px
   :align: center

   *A cell and its neighbors*

- if a cell is sick one day then the probability that it will be healed
  the next day is :math:`p_R`.

- if a cell is healed, then it stays healed - it won't get sick again.


Project
-------

**Part 1.** Consider a 200x200 cells grid, starting with 16 (4x4 grid) infected cells at its center.
Develop a functions `update_spread` that takes a 200x200 grid of cells with given states (0,1,2) and returns the grid showing the states of the cells on the next days.

**Part 2.** The following code produces an animation.

.. code:: python


	%matplotlib qt

	import numpy as np
	import matplotlib.pyplot as plt
	from matplotlib.animation import FuncAnimation

	x = np.zeros((200,200), dtype = int)

	fig = plt.figure()
	im = plt.imshow(x,vmin=0,vmax=1)
    
	def animate(i):    
	    x[:,:] = np.random.random(x.shape)
	    im.set_data(x)
	    return im

	anim = FuncAnimation(fig,animate)
	plt.show()
    
Modify the code to produce an animation of the evolving epidemic.

**Part 3.** Explore the effect the model parameters :math:`p_I` and :math:`p_R` on the spread of the disease.

**Part 4.** Suppose that a vaccine has been invented for the disease. A vaccinated
cell will have the value -1, and such cell will never get sick.

.. figure:: epidemic-3.svg
   :width: 450px
   :align: center

   *Healthy, sick, healed, and vaccinated cells.*

Investigate how the spread of the disease will be affected if a given percentage
of randomly selected cells in the population gets vaccinated.

