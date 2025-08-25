Project Report Guide
====================

.. Comment
    `Example report <../../_static/projects/twin_primes.html>`_

Checklist
---------

Before submitting your report, please check the following list.

 * You have restarted the kernel and run all cells top-to-bottom with no errors.
 * You have included markdown cells before each code cell that explains (i) what the code does, (ii) how it serves the needs of the report, and (iii) how it works.
 * You have used LaTeX ($) for math equations and variables in your markdown cells.
 * You have used backticks (`) when referring to Python functions and variables in your markdown cells.
 * You have defined any relevant terms that are necessary for the report.
 * You have included an Introduction and Conclusion, with additional sections as appropriate to make up the body.

Collaboration
--------------

You are free to discuss projects with your classmates. However, each project report
must be solely your own work: it must be written by you in its entirety, including
all Python code. Plagiarism of any kind (copying from other students, or permitting
someone to copy your work, copying from the internet etc.) will result at the minimum
in the failing grade on a report, and possibly in additional sanctions (an F grade for
the course, an academic disciplinary action etc.).




Using external resources
------------------------

There are two types of resources that may be relevant. 
First, there are plenty of books and websites devoted to Python programming. 
You should take advantage of this. 
There are many Python features that we will not have time to cover in class.
If you have a programming question then in most cases a quick google search will get you an answer.

**Note**: You must understand and be able to explain in detail what your code does and how it works.
You must not copy code snippets that you found somewhere and that somehow seem to be doing what you need.
Any code that you cannot fully explain will result in an F on the project.

Second, most of the projects you will be working on are based on mathematical problems and ideas that are described somewhere. 
However, you should not start your work on a project by doing a web or library search. 
The goal of each project is for you to explore a problem on your own. 
Descriping your exploration and experimentation must be the main part of your project report. 
The projects are open-ended so there is no “complete solution” you should be looking for. 
Have fun, explore, and put in the report what you came up with.


Report grading rubrics
----------------------

Project reports will be graded as follows. Each element listed in the
table below will be graded on the A-F scale. These letter grades will be then
converted into numerical scores (A = 4.0, A- = 3.67 etc.), multiplied by the
corresponding weights, and added together. The resulting score will give the
letter grade for the whole report.

Bonus (if any) will be indicated by either 'X' or 'XX'. The 'X' bonus will increase
the overall report grade to the next higher grade (from B to B+, from B+ to A- etc.).
The 'XX' bonus will increase the report grade by two grades (e.g from B to A-).
A report grade with a bonus may be higher than A, and will be indicated by either
A+ or A++.

+----------------------+-----------+--------------------------------------------+
| Element              | Weight    |  What will be graded                       |
+======================++==========+============================================+
| Report Content       | 40%       | |Content|                                  |
+----------------------+-----------+--------------------------------------------+
| Python Code          | 40%       | |Code|                                     |
+----------------------+-----------+--------------------------------------------+
| Presentation         | 20%       | |Presentation|                             |
+----------------------+-----------+--------------------------------------------+
| Bonus                |           | |Bonus|                                    |
+----------------------+-----------+--------------------------------------------+

.. |Content| replace:: Work done on developing the project. Your analysis, insights,
   observations, and interpretations. Quality of the narrative of the report.

.. |Code| replace:: Quality of the Python code included in the report. Relevance
   of the code to the project. Code organization. Documentation of code
   by code comments.

.. |Presentation| replace:: Organization of the report. Text formatting.
   Use of LaTeX to typeset mathematics. Formatting of code output.
   Quality of graphs and plots.

.. |Bonus| replace:: Extra credit for excellent work that exceeds
   expectations.

* A more detailed breakdown for each element can be found here: :download:`Project Rubrics <./_static/project_rubrics.pdf>`


Report Style Guide
------------------


Report introduction
~~~~~~~~~~~~~~~~~~~

A report must begin with an introduction section. It should explain the project
and the goals of the report in a way which is engaging and understandable to
person who does not take this course.
The introduction of a report must not be limited to a list of tasks you want
to accomplish. While explaining the project use your own words, do not copy
the project description posted on this website.


.. toctree::
   :maxdepth: 0

   Example <./Report_guide/report6>


Report conclusions
~~~~~~~~~~~~~~~~~~

The final section of the report must summarize your results and conclusions as well as the process of obtaining them.


Report organization
~~~~~~~~~~~~~~~~~~~

Beside the introduction and conclusions, the body of the
report should be logically organized into sections. Each section 
should have a meaningful title.



References
~~~~~~~~~~

If you used books, articles, websites etc. while preparing the report, they should
be listed at the end of the report.



Math formatting
~~~~~~~~~~~~~~~

Use LaTeX to format all mathematical symbols and formulas.

.. toctree::
   :maxdepth: 0

   Example <./Report_guide/report4>



Code structure
~~~~~~~~~~~~~~

Python code should be split into possibly short code cells that accomplish a single,
well defined task.  In particular, you should not define several functions in one cell
or define a function and execute it in the same cell.

You should introduce each block of code (even if very briefly) with the purpose of the code along with where it fits into the project plan as a whole. As a rule, you should not have in a report two consecutive code cells without any text between them.


.. toctree::
   :maxdepth: 0

   Example <./Report_guide/report7>


Code sequencing
~~~~~~~~~~~~~~~

All Python code in the report must be presented in such order that it can be read
and executed sequentially, from the beginning to the end of the report. For example,
you should not use a Python function in your report prior to defining this function.


.. toctree::
   :maxdepth: 0

   Example <./Report_guide/report5>


Code comments
~~~~~~~~~~~~~

Code comments should be used to explain workings of the code.


.. toctree::
   :maxdepth: 0

   Example <./Report_guide/report9>


Execution errors
~~~~~~~~~~~~~~~~

All code included in your report must work. Do not submit reports with execution errors.


.. toctree::
   :maxdepth: 0

   Example <./Report_guide/report8>


Output size
~~~~~~~~~~~

Your report should contain only code output that serves some purpose
and that you expect someone to read. As a general rule, do not print more
than 30 lines of output unless you have a very good reason for it.


.. toctree::
   :maxdepth: 0

   Example <./Report_guide/report1>


Output formatting
~~~~~~~~~~~~~~~~~

Format code output in a way that makes it easy to read.


.. toctree::
   :maxdepth: 0

   Example <./Report_guide/report3>


Graphs and plots
~~~~~~~~~~~~~~~~

Graphs and plots must be well formatted. They should have titles and, if appropriate,  axis labels, a legend etc.


.. toctree::
   :maxdepth: 0

   Example <./Report_guide/report2>