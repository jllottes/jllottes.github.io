
Address book
============

.. rubric:: due: Tuesday, May 3, 11:59 PM

The `Faculty and Staff Directory <http://pharmacy.buffalo.edu/faculty-staff.html>`_
webpage of the UB School of Pharmacy lists names of faculty and staff members of
the school. The name of each person is linked to a webpage with information about
that person.


Project
-------

Using requests and regular expressions write code that retrieves name, office
address, phone number, and e-mail of each person listed in the staff and faculty
directory. Your code should print this information for each person (in alphabetical
order) in a format similar to the following:


|

.. container:: output

    Brown, Alice
    B5-123A NYS Center of Excellence
    Buffalo, NY
    (716) 555-1234
    abrown123\@buffalo.edu


    Chase, Joseph
    555 Kapoor Hall
    Buffalo, NY 14214-8033
    (716) 555-3210
    josech\@buffalo.edu


The sample listings above are made up, they do not correspond to the real information
posted on the School of Pharmacy website.



**Note 1.**  Reports that print contact information that was manually entered into
the report code are not acceptable.

**Note 2.** Your code needs to handle the following issues:


* Individual pages of some people are missing some or all contact information.
  In such cases the listing you produce should indicate it e.g. as follows:

|

.. container:: output

    Brown, Alice
    No Address
    (716) 555-1234
    abrown123\@buffalo.edu


    Chase, Joseph
    No Address
    No Phone
    No E-mail


* The number of lines in the office address can vary, depending on a person.

* Phone numbers are listed on web pages in different formats:
  `(716) 555-1234 <http://pharmacy.buffalo.edu/faculty-staff.html?CFC__target=nTCQYXcvSDinYfrnhrtEjjKQCI-http%3A%2F%2Fwww.pharm.buffalo.edu%2FFaculty_Directory%2Fpages%2Fubcms_profile.php%3FID%3D8>`_,
  or `716-555-1234 <http://pharmacy.buffalo.edu/faculty-staff.html?CFC__target=6J6Cs5aGiYNipNG6RNe71qCSgU-http%3A%2F%2Fwww.pharm.buffalo.edu%2FFaculty_Directory%2Fpages%2Fubcms_profile.php%3FID%3D247>`_,
  or `7165551234 <http://pharmacy.buffalo.edu/faculty-staff.html?CFC__target=kdUKUu4pX7WVGJqbfZ69anCX1g-http%3A%2F%2Fwww.pharm.buffalo.edu%2FFaculty_Directory%2Fpages%2Fubcms_profile.php%3FID%3D227>`_
  etc. Your code should capture all phone numbers regardless how they were entered,
  and print them out in the format (716) 555-1234.

**Note 3.**  This is a programming project. Your project report does not need
include narrative, beyond comments explaining how your code works. The project will
be graded according to the following rubrics:

* Code that successfully decrypts the text file: 70%
* Report organization and code documentation: 30%
