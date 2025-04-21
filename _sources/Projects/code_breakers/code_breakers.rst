Code breakers
=============

.. rubric:: due: Monday, April 28th ats 11:59 PM


ASCII codes
-----------

Each character on a computer keyboard is assigned an `ASCII code <http://www.theasciicode.com.ar>`_, which
is an integer in the range 0-127. The ASCII code of a character can be
obtained using the ``ord()`` function:


.. code:: python

    for c in "This is MTH 337":
        print('{:>3} {}'.format(ord(c), "'"+c+"'"))

.. container:: output

      \  84 'T'
      104 'h'
      105 'i'
      115 's'
      \  32 ' '
      105 'i'
      115 's'
      \  32 ' '
      \  77 'M'
      \  84 'T'
      \  72 'H'
      \  32 ' '
      \  51 '3'
      \  51 '3'
      \  55 '7'



Conversely, the function ``chr()`` converts ASCII codes into characters:

.. code:: python

    char_list = []
    for n in [104, 101, 108, 108, 111]:
        char_list.append(chr(n))
        txt = ''.join(char_list)
    print(txt)


.. container:: output

    hello


Text encryption
---------------

In order to securely send a confidential message one usually needs to
encrypt it in some way to conceal its content. Here we consider the following
encryption scheme:

-  One selects a secret key, which is sequence of characters. This key is used
   to both encrypt and decrypt the message.
-  Characters of the secret key and characters of the message are converted
   into ASCII codes. In this way the key is transformed into a
   sequence of integers :math:`(k_1, k_2, \dots, k_r)`, and the message becomes
   another sequence of integers :math:`(m_1, m_2, \dots, m_s)`. If :math:`r < s`
   then the secret key sequence is extended by repeating it as many times as
   necessary until it matches the length of the message.
-  Let :math:`c_i` be the reminder from the division of
   :math:`m_i+k_i` by 128. The sequence of numbers
   :math:`(c_1, c_2, \dots, c_s)` is the encrypted message.

For example, if the message is 'Top secret!' and the secret key is 'buffalo'
then the encrypted message is:

.. math:: \tt{54,100,86,6,84,81,82,84,90,90,7}



In order to decrypt the message we work backwards: for each number :math:`c_i`
we compute the reminder from the division of :math:`c_i-k_i` by 128. This
number is equal to :math:`m_i`, so converting it into a character
we get the :math:`i`-th letter of the message.

Project
-------

Each file listed below contains text (a fragment of a book in English)
encrypted using the method described above. The secret key used to encrypt
the text is a word, different for each file. A dictionary of over 60,000 English
words is available here (:download:`dictionary.txt<dictionary.txt>`) and all words used as secret keys are listed in this dictionary. 
Write code that decrypts the file assigned to you.


**Note.**  This is a programming project. Your project report does not need
include narrative, beyond comments explaining how your code works. The project will
be graded according to the following rubrics:

* Code that successfully decrypts the text file: 70%
* Report organization and code documentation: 30%

- :download:`aevicker.txt<txtfiles/aevicker.txt>`
- :download:`alecjens.txt<txtfiles/alecjens.txt>`
- :download:`amritaga.txt<txtfiles/amritaga.txt>`
- :download:`anrao4.txt<txtfiles/anrao4.txt>`
- :download:`asnewbur.txt<txtfiles/asnewbur.txt>`
- :download:`azumpano.txt<txtfiles/azumpano.txt>`
- :download:`cmpretna.txt<txtfiles/cmpretna.txt>`
- :download:`cr226.txt<txtfiles/cr226.txt>`
- :download:`ctrennel.txt<txtfiles/ctrennel.txt>`
- :download:`dheredia.txt<txtfiles/dheredia.txt>`
- :download:`eliascol.txt<txtfiles/eliascol.txt>`
- :download:`elifelds.txt<txtfiles/elifelds.txt>`
- :download:`emilytap.txt<txtfiles/emilytap.txt>`
- :download:`gsrich.txt<txtfiles/gsrich.txt>`
- :download:`ianmcmee.txt<txtfiles/ianmcmee.txt>`
- :download:`jiongliu.txt<txtfiles/jiongliu.txt>`
- :download:`msmith37.txt<txtfiles/msmith37.txt>`
- :download:`omarjaff.txt<txtfiles/omarjaff.txt>`
- :download:`qmgibbon.txt<txtfiles/qmgibbon.txt>`
- :download:`ramateja.txt<txtfiles/ramateja.txt>`
- :download:`rmortiz2.txt<txtfiles/rmortiz2.txt>`
- :download:`rtsaucke.txt<txtfiles/rtsaucke.txt>`
- :download:`ryansaab.txt<txtfiles/ryansaab.txt>`
- :download:`skylagre.txt<txtfiles/skylagre.txt>`
- :download:`sswu2.txt<txtfiles/sswu2.txt>`
- :download:`xichenzh.txt<txtfiles/xichenzh.txt>`
- :download:`xtstanto.txt<txtfiles/xtstanto.txt>`
- :download:`yuleisim.txt<txtfiles/yuleisim.txt>`



