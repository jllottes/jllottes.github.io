
Wordle
=========================

.. rubric:: due: Saturday, May 21, 11:59 PM

Wordle is a word puzzle game where players have six attempts to guess a five-letter word. With each guess, the player is given feedback in the form of colored tiles that indicate which letters occur in the word and which letters are in the correct position.

 .. image:: wordle.png
       :width: 300px
       :align: center

* Green tiles incidate that the corresponding letter is in the correct position.
* Yellow tiles indicate that the corresponding letter appears in a different position.
* Gray tiles indicate that the corresponding letter does not appear in the word.

The following Python file contains code to play Wordle in Jupyter notebook. 

-   :download:`wordle.py<wordle.py>`

You may download the file and place it into your notebook directory, or use the requests package to automatically do this for you:

.. code:: python

    import requests
    url = 'https://jllottes.github.io/_static/projects/wordle.py'
    with open('wordle.py','wb') as f:
        f.write(requests.get(url).content)
        
The file contains two functions: :code:`wordle_game` which initializes an object for playing Wordle, and :code:`evaluate_guess` which checks a guess against the correct answer to determine the correct tile coloration.
        
You will also need to download the set of words that may appear in Wordle and place into the same directory:


-   :download:`wordle_words.txt<wordle_words.txt>`

        
Once the files are downloaded into the same directory as your notebook, you can play the game in Jupyter notebook with the following code:

.. code:: python

    %matplotlib notebook
    from wordle import *
    
    with open('wordle_words.txt','r') as f:
        words = f.read().split()
        
    game = wordle_game(words)
    game.play()
    
The :code:`wordle_game` function takes in a list of acceptable words, randomly selects one to be the correct answer, and returns an object that will play the Wordle game using the :code:`.play()` method.


Project
-------

**Part 1.** 
We will first assume that no letter is ever repeated in any Wordle word.
Write a function :code:`get_possible_words(guess_word,evaluation,words)` that takes in a word guess and it's evaluation (obtained from the function :code:`evaluate_guess`) along with a list of permissible words, and returns a list of all words that could possibly be correct (assuming no letter is ever duplicated). The correct word should only be used to generate the evaluation, **NOT** to generate the list of possible words.

**Part 2.**
Write a function :code:`solve_wordle(correct_word,guess_word,words)` that will automatically solve a Wordle puzzle given a designated correct word and an initial guess along with a list of permissible words. 
The correct word should only be used to generate the evaluations, **NOT** to solve the puzzle. 
Your function should return the solution, along with the number of guesses made before the answer was obtained.
You can test the function by inputting a randomly selected correct word using the :code:`wordle_game` class:

.. code:: python
    
    guess_word = <initial guess>
    game = wordle_game(words)
    correct_word = game.correct_word
    solution, num_guesses = solve_wordle(correct_word, guess_word, words)

**Part 3.**
Modify the function :code:`get_possible_words` to allow for words with repeated letters.

**Part 4.**
Explore how different starting guesses affect the number of guesses before a Wordle puzzle is solved.
For inspiration, you may wish to view this excellent video by YouTuber 3Blue1Brown:
`Solving Wordle using information theory <https://www.youtube.com/watch?v=v68zYyaEmEA>`_.