Code breakers
=============

.. Comment
    .. rubric:: due: Friday, May 1st at 11:59 PM


ASCII codes
-----------

Each character on a computer keyboard is assigned an `ASCII code <http://www.theasciicode.com.ar>`_, which
is an integer in the range 0-127. The ASCII code of a character can be
obtained using the ``ord()`` function:


.. code:: python

    for c in "This is MTH 337":
        print("'{}'  ->  {}".format(c, ord(c)))

.. container:: output

      'T'  ->  84
      'h'  ->  104
      'i'  ->  105
      's'  ->  115
      ' '  ->  32
      'i'  ->  105
      's'  ->  115
      ' '  ->  32
      'M'  ->  77
      'T'  ->  84
      'H'  ->  72
      ' '  ->  32
      '3'  ->  51
      '3'  ->  51
      '7'  ->  55



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
   :math:`m_i+k_i` by :math:`128`. The sequence of numbers
   :math:`(c_1, c_2, \dots, c_s)` is the encrypted message.

For example, if the message is 'Top secret!' and the secret key is 'buffalo'
then the encrypted message is:

.. math:: \tt{54,100,86,6,84,81,82,84,90,90,7}



In order to decrypt the message we work backwards: for each number :math:`c_i`
we compute the reminder from the division of :math:`c_i-k_i` by :math:`128`. This
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

- :download:`aasamit.txt<txtfiles/aasamit.txt>`
- :download:`ajparlat.txt<txtfiles/ajparlat.txt>`
- :download:`bgdykas.txt<txtfiles/bgdykas.txt>`
- :download:`bli55.txt<txtfiles/bli55.txt>`
- :download:`bmoreira.txt<txtfiles/bmoreira.txt>`
- :download:`bpdalfon.txt<txtfiles/bpdalfon.txt>`
- :download:`catsum.txt<txtfiles/catsum.txt>`
- :download:`cduong2.txt<txtfiles/cduong2.txt>`
- :download:`dilyetda.txt<txtfiles/dilyetda.txt>`
- :download:`ecemkucu.txt<txtfiles/ecemkucu.txt>`
- :download:`gecollin.txt<txtfiles/gecollin.txt>`
- :download:`iahidalg.txt<txtfiles/iahidalg.txt>`
- :download:`isaachos.txt<txtfiles/isaachos.txt>`
- :download:`isiahsmi.txt<txtfiles/isiahsmi.txt>`
- :download:`jamesjud.txt<txtfiles/jamesjud.txt>`
- :download:`krbrydal.txt<txtfiles/krbrydal.txt>`
- :download:`lching.txt<txtfiles/lching.txt>`
- :download:`masudkab.txt<txtfiles/masudkab.txt>`
- :download:`maxkoan.txt<txtfiles/maxkoan.txt>`
- :download:`mjmeacha.txt<txtfiles/mjmeacha.txt>`
- :download:`mshafiul.txt<txtfiles/mshafiul.txt>`
- :download:`omargeba.txt<txtfiles/omargeba.txt>`
- :download:`ryanmaig.txt<txtfiles/ryanmaig.txt>`
- :download:`summerti.txt<txtfiles/summerti.txt>`
- :download:`sunbinmo.txt<txtfiles/sunbinmo.txt>`
- :download:`tanatale.txt<txtfiles/tanatale.txt>`
- :download:`taseenis.txt<txtfiles/taseenis.txt>`
- :download:`wjiang8.txt<txtfiles/wjiang8.txt>`
- :download:`wyang48.txt<txtfiles/wyang48.txt>`
- :download:`zsdoxtat.txt<txtfiles/zsdoxtat.txt>`




