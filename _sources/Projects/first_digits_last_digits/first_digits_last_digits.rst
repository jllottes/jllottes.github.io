:orphan:

First digits, last digits
=========================

.. rubric:: due: Wednesday, May 11, 11:59 PM

The goal of this project is to look for some patterns (or lack of patterns) in data. 
More precisely, you will investigate how often various digits appear as the first digit and the last 
digit of numerical data of various kinds.

**Exercise 1.**
Write a function ``fd`` that for a (positive or negative) number returns the integer which is the 
first non-zero digit of that number. 
If there are no non-zero digits the function should return 0.

.. code:: python

    fd(123.45)
    
.. container:: output

    1
    
.. code:: python

    fd(-75)
    
.. container:: output

    7
    
.. code:: python

    fd(0.00345)
    
.. container:: output

    3
    
.. code:: python

    fd(0.0)
    
.. container:: output

    0
    
**Exercise 2.**
Write a function ``ld`` that for a (positive or negative) number returns the integer which is the last 
non-zero digit of that number. 
If there are no non-zero digits the function should return 0.

.. code:: python

    ld(-123.45)
    
.. container:: output

    5
    
.. code:: python

    ld(42000.00)
    
.. container:: output

    2
    
.. code:: python

    ld(0.0)
    
.. container:: output

    0

Project
-------

#. Below are links to csv files containing numerical data coming from various sources. Analyze how often each non-zero digit apprears as the first digit of the data. You don’t need to use all files, but you should analyze several of them. Observe and investigate any patterns that may appear. Perform the same analysis for the last non-zero digits. Use bar graphs (or other plots) to illustrate results of your computations.
  
    * | :download:`NYSE_2016_03_25.csv` 
      | This file contains information about trades of stocks listed on the New York Stock Exchange on March 25, 2016. Interesting data to analyze are stock prices (opening price, closing price, low and high price during the day, high and low during the preceding 52 weeks - you can select one or more of these) and trading volume of stocks. This data was obtained  from `The Wall Street Journal <https://www.wsj.com/market-data)>`_.
    
    * | :download:`country_areas.csv` 
      | This file lists land areas of countries in square kilometers and in square miles. The data was obtained from the website of `The World Bank <https://data.worldbank.org/indicator/AG.LND.TOTL.K2>`__.
    
    * | :download:`country_populations.csv` 
      | This file lists populations of countries for several years. You can choose to analyze data for one or more years. This data was obtained from the website of `The World Bank <https://data.worldbank.org/indicator/SP.POP.TOTL>`__.
    
    * | :download:`airports.csv` 
      | This file contains information ab out airports and heliports around the world. Interesting numerical dta here are elevations of airports abvoe the sea level. This data was obtained from the website `ourairports.com <https://ourairports.com/data/>`_.
    
    * | :download:`library_survey_2013.csv` 
      | This file contains results of the 2013 survey of public libraries in the United States. There is a lot of data here. Column headings are explained in :download:`this file<library_survey_2013_masthead.pdf>`. Interesting data to analyze includes the total number of print materials owned by each library (column BKVOL), the total number of annual library visits (column VISITS), the total annual library circulation (column TOTCIR), library operating expenditures (column TOTOPEXP) etc. Another interesting option is to extract building numbers from library street addresses (column ADDRESS). This data was obained from the website of the `Institute of Museum and Library Services <https://imls.gov/>`_.
    
    * | :download:`capital_distances.txt` 
      | This file lists distances (in  kilometeres) between capitals of countries. This data was obtained frmo the website of `prof. Kristian Skrede Gleditsch <http://ksgleditsch.com/data-5.html)>`_.
    
#. Below is a link to a file with text of all articles published by New York Times on June 1, 2010.  Find all numbers appearing in the text, and analyze frequency of first and last non-zero digits in these numbers. Compare this with the results you obtained in part 1. 
  
    * :download:`NYT_2010_06_01.txt`