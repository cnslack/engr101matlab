.. qnum::
   :prefix: Q
   :start: 1

.. raw:: html

   <script src="../_static/common/js/common3.js"></script>

.. include:: ../common/include_lobster_exercises.in.rst

.. raw:: html

   <style>
      .btn {
         margin: 0;
      }
      .tab-pane {
         padding: 0;
      }
   </style>

------------------------------------------------------
More Practice: 
------------------------------------------------------

.. fillintheblank:: aa-strings&cells_09_strings_01
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
         clc; clear;
         str = 'parabola';
         str([1 3]) = [];
         str(1:3) = 'a';
         str(1,4) = 'b';
         str(end:-1:end-1) = 'c';
         disp(str);

  - :aaabcc: Correct!
    :x: Incorrect. Perform all the operations one by one on str and then observe how str evolves!

.. fillintheblank:: aa-strings&cells_09_strings_02
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
         clc; clear;
         str = 'parabola';
         str( find(str == 'a', 2) ) =[];
         str = [str(1:3) str(7) 'a'];
        disp(str);

  - :ERROR: Correct!
    :x: Incorrect. Check line number 4 and see how will MATLAB access str(7)!

.. fillintheblank:: aa-strings&cells_09_strings_03
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
         clc; clear;
         str = 'parabola';
         x = find(str <= 'c');
         disp(sum(x));

  - :19: Correct!
    :x: Incorrect. Here str <='c' will look for all the letters which come before 'c'.

.. fillintheblank:: aa-strings&cells_09_strings_04
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
         clc; clear;
         first = 'matlab';
         second = 'java';
         first = 'second';
         second = first;
         disp(second)

  - :second: Correct!
    :x: Incorrect. Carefully check every line, when something is in single quotes, then the variable stores that string.

.. fillintheblank:: aa-strings&cells_09_strings_05
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
         clc; clear;
         word = 'quad';
         word(6) = 'X';
         word(5:-2:1) = [];
         disp(word);

  - :udX: Correct!
    :x: Incorrect. Execute the code line by line and check it again!

.. fillintheblank:: aa-strings&cells_09_strings_06
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
         clc; clear;
         let = 'CDE';
         let(3:5) = 'F';
         let = let - 2;
         fprintf('%s', let);

  - :ABDDD: Correct!
    :x: Incorrect. Execute the code line by line and check it again!

.. fillintheblank:: aa-strings&cells_09_strings_07
   :author: Ashish Aggarwal
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
         str = 'afaeadacab';
         str( find(str == 'a') ) = [];
         str = str(length(str):-1:1);
         disp(str);

  - :bcdef: Correct!
    :x: Incorrect. Execute the code line by line and check it again!

.. mchoice:: aa-strings&cells_09_strings_08
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: str = str(end:-1:1);
  :answer_b: str = str(length(str):-1:1)
  :answer_c: str = str(6:-1:1);
  :answer_d: str(end:-1:1) = str(end:-1:1); 
  :answer_e: str= str([6 5 4 3 2 1]);
  :correct: d
  :feedback_a: Incorrect. Check all these options one by one in MATLAB and see how they are interpreted.
  :feedback_b: Incorrect. Check all these options one by one in MATLAB and see how they are interpreted.
  :feedback_c: Incorrect. Check all these options one by one in MATLAB and see how they are interpreted.
  :feedback_d: Correct! 
  :feedback_e: Incorrect. Check all these options one by one in MATLAB and see how they are interpreted.
  
   Which of the following options represents an incorrect way of reversing the string?

  .. code-block:: matlab
  
     str = 'matlab';

.. fillintheblank:: aa-strings&cells_09_strings_09
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
         str = 'paparazzi';
         str(1) = str(2);
         str([2 4]) = [];
         str(3) = str(4);
         disp(str)

  - :apaazzi: Correct!
    :x: Incorrect. Execute the code line by line carefully and check it again!

.. fillintheblank:: aa-strings&cells_09_strings_10
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
         str = 'matlab';
         str(1:3) = str(end:-1:4);
         str(4:1:end) = str(1:3);
         disp(str)

  - :balbal: Correct!
    :x: Incorrect. Execute the code line by line carefully and check it again!

.. fillintheblank:: aa-strings&cells_09_strings_11
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
         word = 'matlab';
         word(2) = word(3);
         word(3) = word(2);
         disp(word)

  - :mttlab: Correct!
    :x: Incorrect. Execute the code line by line carefully and check it again!

.. fillintheblank:: aa-strings&cells_09_strings_12
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
         word = 'matlab';
         temp = word(2)
         word(2) = word(3);
         word(3) = temp;
         disp(word)

  - :mtalab: Correct!
    :x: Incorrect. Check it again!

.. fillintheblank:: aa-strings&cells_09_strings_13
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
         word = 'matlab';
         word(2) = '';
         word(3) = '';
         word(4) = '';
         disp(word)

  - :mta: Correct!
    :x: Incorrect. Execute the code line by line carefully and check it again!

.. fillintheblank:: aa-strings&cells_09_strings_14
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
         word = 'matlab';
         word([2 3 4]) = '';
         disp(word)

  - :mab: Correct!
    :x: Incorrect. Execute the code line by line carefully and check it again!

.. mchoice:: aa-strings&cells_09_strings_15
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: phr(end) =  '  ';
  :answer_b: phr = [phr '  '];
  :answer_c: phr(length(phr) + 1) =  '  ';
  :answer_d: phr(end + 1) =  '  ';
  :correct: a
  :feedback_a: Correct! 
  :feedback_b: Incorrect. Check these options one by one in MATLAB.
  :feedback_c: Incorrect. Check these options one by one in MATLAB.
  :feedback_d: Incorrect. Check these options one by one in MATLAB.
  
   Which of the following options represents an incorrect way of adding a space at the end of a phrase 'phr'?

.. mchoice:: aa-strings&cells_09_strings_16
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: str(4) = 'X';
  :answer_b: str = [str 'X' str];
  :answer_c: str = [str(1:3) 'X' str(4:6)];
  :answer_d: str = [str(1:3) 'X' str(5:7)];
  :correct: c
  :feedback_a: Incorrect. Check these options one by one in MATLAB.
  :feedback_b: Incorrect. Check these options one by one in MATLAB.
  :feedback_c: Correct!
  :feedback_d: Incorrect. Check these options one by one in MATLAB.
  
   Which of the following options represents the correct way of adding a letter 'X' in the middle of the following string?

   .. code-block:: matlab
  
     str = 'abcdef';

.. mchoice:: aa-strings&cells_09_strings_17
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: For all letters which become > 'z', add 26
  :answer_b: For all letters which become < 'z', add 26
  :answer_c: For all letters which become > 'z', subtract 26
  :answer_d: For all letters which become < 'z', subtract 26
  :correct: c
  :feedback_a: Incorrect. When we add 3 to letters, it is possible that some values go beyond 'z'. Therefore, to bring them in range, we would subtract 26 from the letters which go beyond 'z'. 
  :feedback_b: Incorrect. When we add 3 to letters, it is possible that some values go beyond 'z'. Therefore, to bring them in range, we would subtract 26 from the letters which go beyond 'z'. 
  :feedback_c: Correct!
  :feedback_d: Incorrect. When we add 3 to letters, it is possible that some values go beyond 'z'. Therefore, to bring them in range, we would subtract 26 from the letters which go beyond 'z'. 
  
   With respect to Caesar Cipher, lets say we have a string 'str' whose individual letters are added by 3 to shift them by 3 positions. Which of the following statements is correct in this context?

.. fillintheblank:: aa-strings&cells_09_strings_18
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
         clc; clear;
         phrase = 'Go Gators Greater!';
         pso = find(phrase == '  ');
         phrase( pso(1):1:pso(end) ) = phrase( pso(end):-1:pso(1) );
         disp( phrase(pso(1)+1:pso(end)-1) );

  - :srotaG: Correct!
    :x: Incorrect. Decouple the syntax in line 3 and check what does it values does it actually refer to from pos

.. mchoice:: aa-strings&cells_09_strings_19
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: str = upper(str(1));
  :answer_b: str(1) = upper(str);
  :answer_c: str(1) = upper(str(1));
  :answer_d: str = upper(str)
  :correct: c
  :feedback_a: Incorrect. Remember that we need to only capitalize the first letter so we should only change str(1).
  :feedback_b: Incorrect. Remember that we need to only capitalize the first letter so we should only change str(1).
  :feedback_c: Correct!
  :feedback_d: Incorrect. Remember that we need to only capitalize the first letter so we should only change str(1).
  
   Which of the following options represents the correct syntax to capitalize only the first letter of the following string?

   .. code-block:: matlab
  
     str = 'matlab';

.. fillintheblank:: aa-strings&cells_09_strings_20
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
         clc; clear;
         str = 'optimistic';
         str(1:3) = str(end:-1:end-2);
         str = [ str(3:-1:1) 'X' str(1:2:5) ];

         disp(str)

  - :ticXctm: Correct!
    :x: Incorrect. Execute the code line by line carefully and check it again!