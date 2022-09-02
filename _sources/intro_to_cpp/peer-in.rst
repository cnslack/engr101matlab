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

------------------------------------
More Practice:
------------------------------------

.. mchoice:: jh-inputs_02_variables_04
  :author: Joe Hummel
  :practice: T
  :answer_a: No inputs
  :answer_b: 1
  :answer_c: 2
  :answer_d: 3
  :correct: c
  :feedback_a: Incorrect. The equation has two inputs--T and W.
  :feedback_b: Incorrect. The equation has more than one input--T and W.
  :feedback_c: Correct! The equation has two inputs--T and W.
  :feedback_d: Incorrect. The equation has only two inputs--T and W.

  I want to write a program to compute windchill. How many inputs are there to the program? :code:`windchill = 35.7 + (0.6 * T) - (35.7 * pow(W, 0.16) + (0.43 * T * pow(W, 0.16))` 

.. mchoice:: jh-inputs_02_variables_06
  :author: Joe Hummel
  :practice: T
  :answer_a: 4
  :answer_b: 3
  :answer_c: 2
  :answer_d: 1
  :correct: c
  :feedback_a: Incorrect. The equation doesn't have four variables, there are only two--T and W.
  :feedback_b: Incorrect. The equation doesn't have three variables, there are only two--T and W.
  :feedback_c: Correct! The equation has two variables--T and W.
  :feedback_d: Incorrect. The equation has more than one variable--T and W.

  How many variables are there to the program? 

  .. code-block:: cpp
  
     `windchill = 35.7 + (0.6 * T) - (35.7 * pow(W, 0.16) + (0.43 * T * pow(W, 0.16))` 

.. mchoice:: jh-cincout_05_cincout_02
  :author: Joe Hummel
  :practice: T
  :answer_a: 19,19
  :answer_b: 19,20
  :answer_c: 20,20
  :answer_d: 20,19
  :correct: d 
  :feedback_a: Incorrect. While the output of y becomes 19, we see that the output of x becomes 20 with the incrementation line.
  :feedback_b: Incorrect. The output of y becomes 19, and we see that the output of x becomes 20 with the incrementation line.
  :feedback_c: Incorrect. While we see that the output of x becomes 20 with the incrementation line, the output of y becomes 19 instead of 20.
  :feedback_d: Correct! The output of x becomes 20 and the output of y becomes 19. 

  What does this program output? Assume the user inputs 19. 

  .. code-block:: cpp
  
     #include &lt;iostream&gt;
     using namespace std;
     
     int main()
     {
        int x, y;
        cin >> x;
        y = x++;
        cout << x; 
        << ",";
        << y:
        << endl;
        return 0; 
      }
  

.. mchoice:: jh-cincout_05_cincout_03
  :author: Joe Hummel
  :practice: T
  :answer_a: My friend PI!
  :answer_b: Just a real number
  :answer_c: <<no output>>
  :answer_d: My friend PI! Just a real number.
  :correct: b
  :feedback_a: Incorrect. The input was 3.1415926, not 3.14159, so the loop flows to else and prints "Just a real number."
  :feedback_b: Correct! Since 3.1415926 does not satisfy the first part of the if statement, the loop flows to else and prints "Just a real number."
  :feedback_c: Incorrect. There is an output for this input--try running it in a compiler and seeing!
  :feedback_d: Incorrect. The input of 3.1415926 will not print both statements--if-else statements are meant to print either one statement or another. 

  The program below checks to see if the user has input PI. Suppose the user inputs 3.1415926. What is output?

  .. code-block:: cpp
  
     #include &lt;iostream&gt;
     using namespace std;
     
     int main()
     {
        double x;
        cin >> x;
        
        if (x == 3.14159)
        {
           cout << "My friend PI!" << endl;
        }
        else
        {
           cout << "Just a real number" << endl;
         }
         
        return 0; 
      }

.. mchoice:: jh-cincout_05_cincout_05
  :author: Joe Hummel
  :practice: T
  :answer_a: 19,19
  :answer_b: 19,20
  :answer_c: 20,20
  :answer_d: 20,19
  :correct: d 
  :feedback_a: Incorrect. While the output of y becomes 19, we see that the output of x becomes 20 with the incrementation line.
  :feedback_b: Incorrect. The output of y becomes 19, and we see that the output of x becomes 20 with the incrementation line.
  :feedback_c: Incorrect. While we see that the output of x becomes 20 with the incrementation line, the output of y becomes 19 instead of 20.
  :feedback_d: Correct! The output of x becomes 20 and the output of y becomes 19. 

  What does this program output? Assume the user inputs 19. 

  .. code-block:: cpp
  
     if ( condition )
     {
        S1;
        S2;
     }
     else
     {
        S3;
        S4;
      }


.. mchoice:: jh-cincout_05_cincout_06
    :author: Joe Hummel
    :practice: T

    The following are all equivalent, except for one.  Which one is not like the others?

    - .. code-block:: cpp
  
         if (x > 0)
          {
            cout << x;
          }
      
      - Incorrect. Review the rules of if-else statements and try again!

    - .. code-block:: cpp
  
         if (x > 0)
          cout << x;

      - Incorrect. Review the rules of if-else statements and try again!

    - .. code-block:: cpp
  
         if (x > 0);
          cout << x;

      - Incorrect. Review the rules of if-else statements and try again!

    - .. code-block:: cpp
  
         if (x > 0)
          {
            cout << x;
          }
         else
          {
          }

      + Correct!

.. mchoice:: jh-cincout_05_cincout_07
  :author: Joe Hummel
  :practice: T
  :answer_a: B
  :answer_b: BC
  :answer_c: BCD
  :answer_d: BCF
  :answer_e: BF
  :correct: c
  :feedback_a: Incorrect. While the input satisifies the output of B, the code will print all the letters that the input will satisfy.
  :feedback_b: Incorrect. The code will print out all the letters that the input will satisfy, not just BC.
  :feedback_c: Correct! The output will be BCD.
  :feedback_d: Incorrect. The if-else statement will not print out both options from the if statements AND the else statetment--it's either or. 
  :feedback_e: Incorrect. The if-else statement will not print out both options from the if statements AND the else statetment--it's either or. 

  Suppose input is 82. What does the program output?

  .. code-block:: cpp
  
     #include &lt;iostream&gt;
     using namespace std;
     
     int main()
     {
        int score;
        
        cin >> score;
        
        if (score >= 90)
        {
           cout << "A";
         }
           
        if (score >= 80)
        {
           cout << "B";
         }
        
        if (score >= 70)
        {
           cout << "C";
         }
         
        if (score >= 60)
        {
           cout << "D";
         }
         
        else
        {
           cout << "F";
         }
         
         return 0; 
      }

.. mchoice:: jh-cincout_05_cincout_09
  :author: Joe Hummel
  :practice: T
  :answer_a: B
  :answer_b: BC
  :answer_c: BCD
  :answer_d: BCF
  :answer_e: BF
  :correct: a
  :feedback_a: Correct! Now the program is written to print out the single letter corresponding to the input.
  :feedback_b: Incorrect. The code will no longer print out multiple letters.
  :feedback_c: Incorrect. The code will no longer print out multiple letters.
  :feedback_d: Incorrect. Not only will the code no longer print out multiple letters, the if-else statement will not print out both options from the if statements AND the else statetment--it's either or. 
  :feedback_e: Incorrect. Not only will the code no longer print out multiple letters, the if-else statement will not print out both options from the if statements AND the else statetment--it's either or. 

  Suppose someone writes a different version as shown below... Suppose input is 82. What does this version output?

  .. code-block:: cpp
  
     #include &lt;iostream&gt;
     using namespace std;
     
     int main()
     {
        int score;
        
        cin >> score;
        
        if (score >= 90)
        {
           cout << "A";
        }
        
        else if (score >= 80)
        {
           cout << "B";
         }
         
        else if (score >= 70)
        {
           cout << "C";
         }
        
        else if (score >= 60)
        {
           cout << "D";
         }
         
        else
        {
           cout << "F";
         }
      
      return 0; 

     }

