:orphan:

Code breakers
=============

.. rubric:: due: Sunday, November 17th ats 11:59 PM


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
words is available `here <https://raw.githubusercontent.com/en-wl/wordlist/master/alt12dicts/5desk.txt>`__,
and all words used as secret keys are listed in this dictionary. Write
code that decrypts the file assigned to you.


**Note.**  This is a programming project. Your project report does not need
include narrative, beyond comments explaining how your code works. The project will
be graded according to the following rubrics:

* Code that successfully decrypts the text file: 70%
* Report organization and code documentation: 30%

- :download:`akuhn.txt<akuhn.txt>`
- :download:`changcha.txt<changcha.txt>`
- :download:`colinhen.txt<colinhen.txt>`
- :download:`ctobrien.txt<ctobrien.txt>`
- :download:`cwmccann.txt<cwmccann.txt>`
- :download:`dsbyrnes.txt<dsbyrnes.txt>`
- :download:`dsmalsch.txt<dsmalsch.txt>`
- :download:`eeheintz.txt<eeheintz.txt>`
- :download:`elyhfenn.txt<elyhfenn.txt>`
- :download:`gentigas.txt<gentigas.txt>`
- :download:`huazhouq.txt<huazhouq.txt>`
- :download:`hyeonseo.txt<hyeonseo.txt>`
- :download:`hzahra.txt<hzahra.txt>`
- :download:`hzhuang2.txt<hzhuang2.txt>`
- :download:`ianmcivo.txt<ianmcivo.txt>`
- :download:`jfatorma.txt<jfatorma.txt>`
- :download:`jiongliu.txt<jiongliu.txt>`
- :download:`jjkim35.txt<jjkim35.txt>`
- :download:`kaczmar3.txt<kaczmar3.txt>`
- :download:`lucyhene.txt<lucyhene.txt>`
- :download:`maungoma.txt<maungoma.txt>`
- :download:`milaniai.txt<milaniai.txt>`
- :download:`mortalak.txt<mortalak.txt>`
- :download:`ogrich.txt<ogrich.txt>`
- :download:`peterlov.txt<peterlov.txt>`
- :download:`rileytot.txt<rileytot.txt>`
- :download:`tjiang24.txt<tjiang24.txt>`
- :download:`yuhanhu.txt<yuhanhu.txt>`