:orphan:

Message decryption
==================

Message encryption is necessary to ensure safe transmission of data.


Messages can be encrypted by changing the order of the characters in the message.


Consider the example: 'Luke, I am your father'

The encryption is done following these steps:

-  An integer number **c** is chosen at random. (say c=3)

-  The message is then written in a **n x c  array** (extra characters '&' might be needed if the string is too short). The dimension **n** is determined by the length of the string and the value of **c**. So the corresponding array for our message looks like this:

+---+---+---+
| L | u | k |
+---+---+---+
| e | , |   |
+---+---+---+
| I |   | a |
+---+---+---+
| m |   | y |
+---+---+---+
| o | u | r |
+---+---+---+
|   | f | a |
+---+---+---+
| t | h | e |
+---+---+---+
| r | & | & |
+---+---+---+

-  The encrypted message is obtained from the transpose array (after removing the extra characters '&'):

+---+---+---+---+---+---+---+---+
| L | e | I | m | o |   | t | r |
+---+---+---+---+---+---+---+---+
| u | , |   |   | u | f | h | & |
+---+---+---+---+---+---+---+---+
| k |   | a | y | r | a | e | & |
+---+---+---+---+---+---+---+---+

**Encrypted message**: 'LeImo tru,  ufhk ayrae'

Project
-------

Each file listed below contains text (a fragment of a book in English)
encrypted using the method described above choosing **c** at random in the [25,100] interval. 

Write a function **decrypt('txtfile')** that decrypts the file corresponding to your UB Person Number modulo
30 and print the decrypted message. The function should take as a variable the name of your .txt file.

A dictionary of English words is available here :download:`dictionary<dictionary.txt>`


**Note.**  This is a programming project. Your project report does not need
include narrative, beyond comments explaining how your code works. The project will
be graded according to the following rubrics:

* Code that successfully decrypts the text file: 70%
* Report organization and code documentation: 30%

0.  :download:`text0.txt<text0.txt>`
1.  :download:`text1.txt<text1.txt>`
2.  :download:`text2.txt<text2.txt>`
3.  :download:`text3.txt<text3.txt>`
4.  :download:`text4.txt<text4.txt>`
5.  :download:`text5.txt<text5.txt>`
6.  :download:`text6.txt<text6.txt>`
7.  :download:`text7.txt<text7.txt>`
8.  :download:`text8.txt<text8.txt>`
9.  :download:`text9.txt<text9.txt>`
10. :download:`text10.txt<text10.txt>`
11. :download:`text11.txt<text11.txt>`
12. :download:`text12.txt<text12.txt>`
13. :download:`text13.txt<text13.txt>`
14. :download:`text14.txt<text14.txt>`
15. :download:`text15.txt<text15.txt>`
16. :download:`text16.txt<text16.txt>`
17. :download:`text17.txt<text17.txt>`
18. :download:`text18.txt<text18.txt>`
19. :download:`text19.txt<text19.txt>`
20. :download:`text20.txt<text20.txt>`
21. :download:`text21.txt<text21.txt>`
22. :download:`text22.txt<text22.txt>`
23. :download:`text23.txt<text23.txt>`
24. :download:`text24.txt<text24.txt>`
25. :download:`text25.txt<text25.txt>`
26. :download:`text26.txt<text26.txt>`
27. :download:`text27.txt<text27.txt>`
28. :download:`text28.txt<text28.txt>`
29. :download:`text29.txt<text29.txt>`
