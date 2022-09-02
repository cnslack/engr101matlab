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

.. mchoice:: jh-iteration_06_whileloops_07
    :author: Joe Hummel
    :practice: T
  
    Which loop counts exactly 1, 2, 3, …, 20, and then stops?  Assume i is an integer variable.

    - .. code-block:: cpp
     
         i = 1;
     
         while (i <= 20)
         {
           ...
           i = i + 1;
          }

      - Incorrect. Review the organization of a typical counting pattern and try again!

    - .. code-block:: cpp
       
         i = 1;
     
         while (i != 20)
         {
           ...
           i = i + 1;
          }

      - Incorrect. Review the organization of a typical counting pattern and try again!

    - .. code-block:: cpp
  
         i = 0;
     
         while (i <= 20)
         {
           ...
           i = i + 1;
          }

      + Correct!
    
    - All of the above

      - Incorrect. Review the organization of a typical counting pattern and try again!

.. mchoice:: jh-iteration_06_whileloops_10
  :author: Joe Hummel
  :practice: T
  :answer_a: 1,4,9,16,25,36,49,#
  :answer_b: 4,9,16,25,36,49,#
  :answer_c: 4,16,36,49,#
  :answer_d: 4,16,36,#
  :correct: d
  :feedback_a: Incorrect. Try running the code in C++ and see what you get!
  :feedback_b: Incorrect. Try running the code in C++ and see what you get!
  :feedback_c: Incorrect. Try running the code in C++ and see what you get!
  :feedback_d: Correct!

  I want to write an Add program that adds 2 numbers together.

  .. code-block:: cpp
  
     int  x;
     
     x = 2;
     
     while (x <= 7)
     {
       cout << pow(x, 2) << ",";
       x = x + 2;
      }
     cout << "#"

.. mchoice:: jh-iteration_06_whileloops_12
    :author: Joe Hummel
    :practice: T

    Assume a temperature of 10F. Output the windchill for each wind speed in the range 1..20, using the windchill equation we've defined previously. The better way is to use a loop.  Which of the following computes & outputs the desired wind chills properly?

    - .. code-block:: cpp
  
        T = 10;
        while (W <= 20)
        {
          W = 1;
          windchill = … ;
          cout << … ;
        }

      - Incorrect. Review the organization of a typical counting pattern and try again!

    - .. code-block:: cpp
  
        T = 10;
        while (W <= 20)
        {
          W = 1;
          windchill = … ;
          cout << … ;
          W = W + 1;
        }

      - Incorrect. Review the organization of a typical counting pattern and try again!

    - .. code-block:: cpp
  
          T = 10;
          W = 1;
          windchill = … ;

          while (W <= 20)
          {
            cout << … ;
            W = W + 1;
          }
      
      - Incorrect. Review the organization of a typical counting pattern and try again!

    - .. code-block:: cpp
  
        T = 10;
        W = 1;
     
        while (W <= 20)
        {
          windchill = … ;
          cout << … ;
          W = W + 1;
        }

      + Correct!

.. mchoice:: jh-iteration_07_ifelse_02
  :author: Joe Hummel
  :practice: T
  :answer_a: When both X and Y are negative
  :answer_b: When either X or Y are negative, but not both
  :answer_c: When either X, or Y, or both, are negative
  :answer_d: When both X and Y are zero or positive
  :correct: a
  :feedback_a: Correct!
  :feedback_b: Incorrect. && implies both statements have to be true in the if-condition, so "warning" would print if they both were negative.
  :feedback_c: Incorrect. && implies both statements have to be true in the if-condition, so "warning" would print if they both were negative.
  :feedback_d: Incorrect. && implies both statements have to be true in the if-condition, so "warning" would print if they both were negative.

  The following code outputs the product of X and Y.  However, when does it output “warning” ?

  .. code-block:: cpp
  
     if (X >= 0 && Y >= 0)
     {
       Z = X * Y;
       cout << "answer=" << Z << endl;
      }
     
     else
     {
       cout << "warning" << endl;
      }

.. mchoice:: jh-iteration_07_whileloops_04
    :author: Joe Hummel
    :practice: T

    We are trying to input a score in range 0..100.  Which code fragment ensures we have a valid score once the loop ends?

    - .. code-block:: cpp
  
         cin >> score;
         while (score>=0 && score<=100)
         {
           cout << "try again> ";
           cin >> score;
         }

      + Correct!

    - .. code-block:: cpp
  
         cin >> score;
         while (score<0 && score>100)
         {
           cout << "try again> ";
           cin >> score;
         }
      
      - Incorrect. Review conditional expressions for while loops and try again!
    
    - .. code-block:: cpp
  
         cin >> score;
         while (score != 0..100)
         {
           cout << "try again> ";
           cin >> score;
         }

      - Incorrect. Review conditional expressions for while loops and try again!

    - .. code-block:: cpp
  
         cin >> score;
         while (score<0 || score>100)
         {   
           cout << "try again> ";
           cin >> score;
         }

      - Incorrect. Review conditional expressions for while loops and try again!

.. mchoice:: jh-iteration_07_whileloops_06
  :author: Joe Hummel
  :practice: T
  :answer_a: 5
  :answer_b: 10
  :answer_c: 15
  :answer_d: 21
  :correct: c
  :feedback_a: Incorrect. Try writing out the steps one by one and see what you find!
  :feedback_b: Incorrect. Try writing out the steps one by one and see what you find!
  :feedback_c: Correct!
  :feedback_d: Incorrect. Try writing out the steps one by one and see what you find!

  What is output by this code fragment?

  .. code-block:: cpp
  
     int  x = 1;
     int  y = 0;
     
     while (x <= 5)
     {
       y = y + x;
       x = x + 1;
      }
     cout << y << endl;

.. mchoice:: jh-iteration_07_whileloops_08
    :author: Joe Hummel
    :practice: T
  
    N! is defined as N * N-1 * N-2 * … 1. Example: 5! = 5*4*3*2*1 = 120. Which code computes N!?

    - .. code-block:: cpp
  
         int  i, N, factrl;
    
         cin >> N;

         i      = N;

         factrl = 1;
     
         while (i > 0)
         {
           factrl = factrl * i;
           i = i – 1;
          }
      
         cout << factrl;
      
      + Correct!

    - .. code-block:: cpp
  
         int  i, N, factrl;
     
         cin >> N;
     
         i      = 1;
     
         factrl = 1;
     
         while (i <= N)
         {
           factrl = factrl * i;
           i = i + 1;
          }
      
         cout << factrl;

      - Incorrect. Look through the code step by step and try again!

    - .. code-block:: cpp
  
         int  N, factrl;
     
         cin >> N;
     
         factrl = 1;
     
         while (N > 0)
         {
           factrl = factrl * N;
           N = N – 1;
          }
      
         cout << factrl;

      - Incorrect. Look through the code step by step and try again!

    - All of the above

      - Incorrect. Look through the code step by step and try again!

.. mchoice:: jh-iteration_08_whileloops_18
  :author: Joe Hummel
  :practice: T
  :answer_a: score = -1;
  :answer_b: score = 0;
  :answer_c: cin >> score;
  :answer_d: cout << score;
  :correct: c
  :feedback_a: Incorrect. Try writing out the steps one by one and see what you find!
  :feedback_b: Incorrect. Try writing out the steps one by one and see what you find!
  :feedback_c: Correct!
  :feedback_d: Incorrect. Try writing out the steps one by one and see what you find!

  For exam score analysis, we have to loop and input the scores.  What’s the initial score to start things off?

  .. code-block:: cpp
  
     int score;
     "Initial Value"

     while (condition)
     {
       "Computation"
       "Advanced"
     } 

.. fillintheblank:: aa-iteration_04_whileloops_01
    :author: Ashish Aggarwal
    :practice: T
    :casei:

    What will be the output of the following code snippet?  (If the program will result in an error or infinite loop, put down ‘ERROR’)

       .. code-block:: matlab
  
         clc; clear;
     
         while n < 10
           n = n + 2;
     
         end
     
         disp(n)

  - :ERROR: Correct!
    :x: Incorrect. We need to define a variable before we start using it.

.. fillintheblank:: aa-iteration_04_whileloops_02
    :author: Ashish Aggarwal
    :practice: T
    :casei:

    What will be the output of the following code snippet?  (If the program will result in an error or infinite loop, put down ‘ERROR’)

       .. code-block:: matlab
  
         clc; clear;
     
         x = 2;
         sum = 2;
     
         while x <= 8
           x = x + sum;
           sum = sum + x;
         end
     
         disp(sum)

  - :16: Correct!
    :x: Incorrect. Change the values of the variables one by one as MATLAB would execute the program and observe how the variables get redefined.

.. fillintheblank:: aa-iteration_04_whileloops_03
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code snippet?  (If the program will result in an error or infinite loop, put down ‘ERROR’)

       .. code-block:: matlab
  
         clc; clear;
     
         x = 2;
         sum = 2;
     
         while x <= 8
           x = x + sum;
           break
           sum = sum + x;
         end
      
         disp(sum)

  - :2: Correct!
    :x: Incorrect. Note, as soon as the break statement executes, the execution directly comes out of the closest while loop. So whatever is written under break statement is not executed.

.. fillintheblank:: aa-iteration_04_whileloops_04
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code snippet?  (If the program will result in an error or infinite loop, put down ‘ERROR’)

       .. code-block:: matlab
  
         clc; clear;
     
         x = 2;
         sum = 2;
     
         while x <= 8
           sum = sum + x;
           continue
           x = x + sum;
         end
     
         disp(sum)

  - :ERROR: Correct!
    :x: Incorrect. Note, continue statement always pushes the execution above to the closest while loop so that the while condition is evaluated again.

.. fillintheblank:: aa-iteration_04_whileloops_05
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code snippet?  (If the program will result in an error or infinite loop, put down ‘ERROR’)

       .. code-block:: matlab
  
         clc; clear;
     
         num = 19;
     
         while true
           while num<100
             if mod(num,3)== 0 || mod(num,4) == 0
               fprintf('%g', num);
               break;
             end
           end
           num = num + 1;
         end

  - :ERROR: Correct!
    :x: Incorrect. Here the inner while-loop has to exhaust first before it increments the value of num by 1.

.. fillintheblank:: aa-iteration_04_whileloops_06
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code snippet?  (If the program will result in an error or infinite loop, put down ‘ERROR’)

       .. code-block:: matlab
  
         clc; clear;
     
         num = 20;
     
         while true
           while num<100
             if mod(num,3)== 0 || mod(num,4) == 0
               fprintf('%g', num);
               break;
             end
           end
           if mod(num,3)== 0 || mod(num,4) == 0
             fprintf('%g', num);
             break;
           end
           num = num + 1;
           fprintf('%g', num)
         end

  - :2020: Correct!
    :x: Incorrect. Note that ‘break statement’ stops the corresponding while loop where it is present in.

.. fillintheblank:: aa-iteration_04_whileloops_07
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code snippet?  (If the program will result in an error or infinite loop, put down ‘ERROR’)

       .. code-block:: matlab
  
         clc; clear;
         x = 41;
     
         while x >= 20
           while x >= 30
             while x >= 40
               if mod(x,4) == 1
                 x = x - 10;
                 break;
               end
             end
             x = x -10;
           end
           x = x - 10;
         end
    
         fprintf('%g', x);

  - :11: Correct!
    :x: Incorrect. Break statement only stops the closest loop, rest of the program still continues its execution.

.. fillintheblank:: aa-iteration_04_whileloops_08
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code snippet?  (If the program will result in an error or infinite loop, put down ‘ERROR’)

       .. code-block:: matlab
  
         clc; clear;
         total = 50;
     
         while total > 10
           if total/10 == 5
             total = total/10;
             total = total^2;
             break;
           end
           total = 5;
           total = 2*total;
         end
     
         fprintf('%g', total);

  - :25: Correct!
    :x: Incorrect. Break statement only the closest loop immediately after it gets executed and the control directly comes out of the loop.

.. fillintheblank:: aa-iteration_04_whileloops_09
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code snippet?  (If the program will result in an error or infinite loop, put down ‘ERROR’)

       .. code-block:: matlab
  
         clc; clear;
         abc = 35;
     
         if abc/7 ~= 5
           fprintf('%g', abc);
      
         else
           while abc>10
             if mod(abc, 7)~=0 || mod(abc, 8)~=0
               abc = abc - 10;
               continue
               abc = 2 * abc;
             end
             break
           end
           abc = abc + 1;
         end
     
         fprintf('%g', abc);

  - :6: Correct!
    :x: Incorrect. Check the execution of the program again line by line.

.. mchoice:: aa-inputsoutputs_04_whileloops_10
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: while abc < 10 && abc > 0
  :answer_b: while abc > 0 && abc < 10
  :answer_c: while abc < 10 || abc < 20
  :answer_d: while 0 < abc < 10
  :answer_e: while abc~=0
  :correct: d
  :feedback_a: Incorrect. Check the way we write conditions in MATLAB.
  :feedback_b: Incorrect. Check the way we write conditions in MATLAB.
  :feedback_c: Incorrect. Check the way we write conditions in MATLAB.
  :feedback_d: Correct!
  :feedback_e: Incorrect. Check the way we write conditions in MATLAB.
  
  Which of the following while conditions is incorrect?

.. mchoice:: aa-inputsoutputs_04_whileloops_11
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: Press Ctrl+Z in the command window
  :answer_b: Press Ctrl+X in the command window
  :answer_c: Press Ctrl+C in the command window
  :answer_d: Press Ctrl+V in the command window
  :correct: c
  :feedback_a: Incorrect. Write a program having an infinite loop and try these commands in MATLAB.
  :feedback_b: Incorrect. Write a program having an infinite loop and try these commands in MATLAB.
  :feedback_c: Correct! 
  :feedback_d: Incorrect. Write a program having an infinite loop and try these commands in MATLAB.
  
  How can we stop an execution of a program when it is stuck in a while-loop?

.. fillintheblank:: aa-iteration_04_whileloops_12
   :author: Ashish Aggarwal
   :casei:

   What will be the output of the following code snippet?  (If the program will result in an error or infinite loop, put down ‘ERROR’)

       .. code-block:: matlab
  
         clc; clear;
         foo = 12;
         foo = (2*foo) / (foo/2) ;
     
         while foo>=3
           if mod(foo,2) > 0
             foo = foo - 1;
           elseif mod(foo, 3) > 0
             foo = foo - 2;
             continue
             foo = 2 * foo;
           end
           foo = foo - 1;
         end
         fprintf('%g', foo);

  - :2: Correct!
    :x: Incorrect. Check the execution of the program again line by line. The continue statement always pushes the execution above to the condition of nearest while loop.

.. fillintheblank:: aa-iteration_04_whileloops_13
   :author: Ashish Aggarwal
   :casei:

   What will be the output of the following code snippet?  (If the program will result in an error or infinite loop, put down ‘ERROR’)

       .. code-block:: matlab
  
         clc; clear;
         num = 19;
     
         while true
           while num<100
             if mod(num,3)== 0 || mod(num,4) == 0
               break;
             end
             num = num + 1;
           end
           num = num + 1;
           break;
         end
     
         fprintf('%g', num);

  - :21: Correct!
    :x: Incorrect. Check the execution of the program again line by line. Break statement stops the closest loop.

.. fillintheblank:: aa-iteration_04_whileloops_14
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code snippet?  (If the program will result in an error or infinite loop, put down ‘ERROR’)

       .. code-block:: matlab
  
         x = 15;
     
         while x > 10
           if x < 15
             x = x-3;
           elseif x > 0
             x = x-1;
             continue
           end
         end
     
         fprintf('%g', x)

  - :8: Correct!
    :x: Incorrect. Check the execution of the program again line by line.

.. mchoice:: aa-inputsoutputs_04_whileloops_15
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: Always evaluated as logical 1
  :answer_b: Always evaluated as logical 0
  :answer_c: Always returns an ERROR
  :answer_d: Always runs the loop for exactly one iteration
  :correct: a
  :feedback_a: Correct! 
  :feedback_b: Incorrect. The keyword ‘true’ is always evaluated as logical 1.
  :feedback_c: Incorrect. The keyword ‘true’ is always evaluated as logical 1.
  :feedback_d: Incorrect. The keyword ‘true’ is always evaluated as logical 1.
  
  A ‘while true’ condition is:

.. mchoice:: aa-inputsoutputs_04_whileloops_16
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: Stops all the loops present in the program.
  :answer_b: Stops all the if-else conditions
  :answer_c: Stops the closest loop
  :answer_d: Stops the closest if-elseif-else condition
  :correct: c
  :feedback_a: Incorrect. Refer back to the rules of the 'break' statement.
  :feedback_b: Incorrect. Refer back to the rules of the 'break' statement.
  :feedback_c: Correct! 
  :feedback_d: Incorrect. Refer back to the rules of the 'break' statement.
  
  The ‘break’ statement:

.. mchoice:: aa-inputsoutputs_04_whileloops_17
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: Pushes the execution above to the corresponding while condition
  :answer_b: Pushes the execution below to the next closest while condition
  :answer_c: Pushes the execution above to the top while condition of the program
  :answer_d: Pushes the execution below to the next if-condition
  :correct: a
  :feedback_a: Correct!
  :feedback_b: Incorrect. Refer back to the rules of the 'continue' statement.
  :feedback_c: Incorrect. Refer back to the rules of the 'continue' statement.
  :feedback_d: Incorrect. Refer back to the rules of the 'continue' statement.
  
  The ‘continue’ statement:

.. fillintheblank:: aa-iteration_04_whileloops_18
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code snippet?  (If the program will result in an error or infinite loop, put down ‘ERROR’)

       .. code-block:: matlab
  
         clc; clear;
         y = 23;
     
         while y > 5
           while y > 10
             while y > 15
               while y > 20
                 y = y - 15;
                 break;
               end
               y = y - 5;
             end
             break
           end
           y = y - 2;
         end
     
         fprintf('%g', y);

  - :1: Correct!
    :x: Incorrect. Execute the program line by line again.

.. fillintheblank:: aa-iteration_04_whileloops_19
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code snippet?  (If the program will result in an error or infinite loop, put down ‘ERROR’)

       .. code-block:: matlab
  
         clc; clear;
         y = 23;
     
         while y > 5
           while y > 10
             while y > 15
               while y > 20
                 y = y - 20;
                 continue;
               end
               continue;
             end
             continue;
           end
           continue;
           y = y - 2;
           break;
         end
     
         fprintf('%g', y);

  - :3: Correct!
    :x: Incorrect. Execute the program line by line again. Remember, continue always pushes the execution above to the corresponding loop condition.

.. fillintheblank:: aa-iteration_04_whileloops_20
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code snippet?  (If the program will result in an error or infinite loop, put down ‘ERROR’)

       .. code-block:: matlab
  
         clc; clear;
         y = 23;
     
         while y > 5
           if y/5 ~=0
             y = y-5;
             break;
             y = y - 3;
           else
             y = y + 2;
             continue;
             y = y +3;
           end
         end

         fprintf('%g', y);

  - :18: Correct!
    :x: Incorrect. Execute the program line by line again carefully.

.. fillintheblank:: aa-iteration_05_foorloops_01
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code snippet?  (If the program will result in an error or infinite loop, put down ‘ERROR’)

       .. code-block:: matlab
  
         clc; clear;
     
         ii = 3;
     
         for ii = 1:1:ii
           for ii = ii:-1:1
             fprintf('%g',ii)
           end
         end

  - :121321: Correct!
    :x: Incorrect. Remember that the list of numbers generated by a statement like ‘for ii = 1:1:3’ is fixed (which is [1,2,3]) and the value of variable ii is reassigned according to the list when it executes.

.. fillintheblank:: aa-iteration_05_foorloops_02
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code snippet?  (If the program will result in an error or infinite loop, put down ‘ERROR’)

       .. code-block:: matlab
  
         clc; clear;
     
         fprintf('28');
     
         for ii = 1:1:3
           for kk = 3:1:1
             fprintf('%g',ii+kk)
           end
         end

  - :28: Correct!
    :x: Incorrect. Remember that the list of numbers generated by a statement like ‘for ii = 3:1:1’ is blank [] because you cannot start at 3 and increment by 1 to finish at 1.

.. fillintheblank:: aa-iteration_05_foorloops_03
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code snippet?  (If the program will result in an error or infinite loop, put down ‘ERROR’)

       .. code-block:: matlab
  
         clc; clear;
     
         for ii = 1:1:3
           for jj = 1:1:3
             fprintf('%g',ii+jj)
           end
      
           for kk = 3:1:1
             fprintf('%g',ii+kk)
           end
         end

  - :234345456: Correct!
    :x: Incorrect. Remember that the list of numbers generated by a statement like ‘for ii = 3:1:1’ is blank [] because you cannot start at 3 and increment by 1 to finish at 1.

.. fillintheblank:: aa-iteration_05_foorloops_04
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code snippet?  (If the program will result in an error or infinite loop, put down ‘ERROR’)

       .. code-block:: matlab
  
         clc; clear;
     
         x = 0;
     
         while x < 5
           x = x+3;
           for x = 1:3:5
             fprintf('x')
             x = x+2;
           end
           fprintf('x')
         end

  - :xxx: Correct!
    :x: Incorrect. Carefully execute the program line by line and check what are you printing, is it a number or an alphabet? Also note that the variable x takes a new value whenever it is redefined.

.. fillintheblank:: aa-iteration_05_foorloops_05
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code snippet?  (If the program will result in an error or infinite loop, put down ‘ERROR’)

       .. code-block:: matlab
  
         clc; clear;
     
         x = 0;
     
         while x < 5
           x = x+3;
           for x = 1:3:5
             fprintf('x')
           end
           fprintf('x')
         end

  - :ERROR: Correct!
    :x: Incorrect. Carefully execute the program line by line and note that the variable x takes a new value whenever it is redefined.

.. fillintheblank:: aa-iteration_05_foorloops_06
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code snippet?  (If the program will result in an error or infinite loop, put down ‘ERROR’)

       .. code-block:: matlab
  
         clc; clear;
     
         x = 4;
     
         while x < 5
           x = x+3;
           for x = 1:3:x
             fprintf('x')
           end
           continue
           fprintf('x')
         end

  - :xxx: Correct!
    :x: Incorrect. Carefully execute the program line by line and note that the variable x takes a new value whenever it is redefined.

.. fillintheblank:: aa-iteration_05_foorloops_07
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code snippet?  (If the program will result in an error or infinite loop, put down ‘ERROR’)

       .. code-block:: matlab
  
         clc; clear;
         x = 4;
     
         while x < 5
           x = x+3;
           for x = 1:3:x
             fprintf('x')
             break
           end
           continue
           fprintf('x')
         end

  - :ERROR: Correct!
    :x: Incorrect. Carefully execute the program line by line and note that the variable x takes a new value whenever it is redefined.

.. fillintheblank:: aa-iteration_05_foorloops_08
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code snippet?  (If the program will result in an error or infinite loop, put down ‘ERROR’)

       .. code-block:: matlab
  
         clc; clear;
         x = 1;
     
         while x < 5
           x = x+3;
           for x = x:-1:1
             fprintf('x')
           end
           fprintf('x')
         end

  - :ERROR: Correct!
    :x: Incorrect. Carefully execute the program line by line and note that the variable x takes a new value whenever it is redefined.

.. fillintheblank:: aa-iteration_05_foorloops_09
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code snippet?  (If the program will result in an error or infinite loop, put down ‘ERROR’)

       .. code-block:: matlab
  
         clc; clear;
     
         for ii = 3:3:5
           jj = ii;
           while jj < 5
             fprintf('%g', ii);
             jj = jj + 1;
           end
         end

  - :33: Correct!
    :x: Incorrect. Check it again!

.. fillintheblank:: aa-iteration_05_foorloops_10
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code snippet?  (If the program will result in an error or infinite loop, put down ‘ERROR’)

       .. code-block:: matlab
  
         clc; clear;
     
         for ii = 3:3:7
           jj = ii;
           while jj < 5
             jj = jj + 1;
             continue;
             fprintf('%g', jj);
           end
           jj = jj + 2;
           break;
         end
         fprintf('%g', jj)

  - :7: Correct!
    :x: Incorrect. Continue and break statements execute for the corresponding loops, irrespective of whether it is a for-loop or while-loop.

.. fillintheblank:: aa-iteration_05_foorloops_11
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code snippet?  (If the program will result in an error or infinite loop, put down ‘ERROR’)

       .. code-block:: matlab
  
         clc; clear;
     
         for ii = 3:3:6
           jj = ii;
           while jj < 5
             fprintf('%g', ii);
             break;
             jj = jj + 1;
           end
           jj = jj + 2;
           break;
         end
         fprintf('%g', jj)

  - :35: Correct!
    :x: Incorrect. Continue and break statements execute for the corresponding loops, irrespective of whether it is a for-loop or while-loop.

.. mchoice:: aa-iteration_05_forloops_12
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: [2 5 7]
  :answer_b: [2 4 7]
  :answer_c: [2 5]
  :answer_d: [2 5 8]
  :answer_e: ERROR
  :correct: c
  :feedback_a: Incorrect. Refer back to the rules of lists.
  :feedback_b: Incorrect. Refer back to the rules of lists.
  :feedback_c: Correct! 
  :feedback_d: Incorrect. Refer back to the rules of lists.
  :feedback_e: Incorrect. Refer back to the rules of lists.
  
  What list of number is generated by the following statement: for ii = 2:3:7

.. mchoice:: aa-inputsoutputs_05_forloops_13/14
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: [7 4]
  :answer_b: []
  :answer_c: [5 2]
  :answer_d: [7 10]
  :answer_e: ERROR
  :correct: b
  :feedback_a: Incorrect. Here since the starting value is 7, increment is 3 and the end value is 2 there is no way that 7 can be incremented by 3 to reach 2. So no numbers will be generated. But it will not give an error, you’ll simply have a list of no numbers.
  :feedback_b: Correct!
  :feedback_c: Incorrect. Here since the starting value is 7, increment is 3 and the end value is 2 there is no way that 7 can be incremented by 3 to reach 2. So no numbers will be generated. But it will not give an error, you’ll simply have a list of no numbers.
  :feedback_d: Incorrect. Here since the starting value is 7, increment is 3 and the end value is 2 there is no way that 7 can be incremented by 3 to reach 2. So no numbers will be generated. But it will not give an error, you’ll simply have a list of no numbers.
  :feedback_e: Incorrect. Here since the starting value is 7, increment is 3 and the end value is 2 there is no way that 7 can be incremented by 3 to reach 2. So no numbers will be generated. But it will not give an error, you’ll simply have a list of no numbers.
  
  What list of number is generated by the following statement: for ii = 7:3:2

.. mchoice:: aa-iteration_05_foorloops_15
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: The statement ‘for ii=3:3:-1” will give an error.
  :answer_b: The break statement works differently in for and while-loop.
  :answer_c: Continue statement only executes in while-loop and not in for-loop.
  :answer_d: A for-loop can be always converted into a while-loop but a while-loop cannot always be converted into a for-loop.
  :correct: d
  :feedback_a: Incorrect. Note that a for-loop is always a special case of a while-loop.
  :feedback_b: Incorrect. Note that a for-loop is always a special case of a while-loop.
  :feedback_c: Incorrect. Note that a for-loop is always a special case of a while-loop.
  :feedback_d: Correct! 
  
  Which of the following statements is true?

.. mchoice:: aa-iteration_05_foorloops_16
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: x = n + ii;
  :answer_b: x = x + n;
  :answer_c: n = n + ii;
  :answer_d: x = x + ii;
  :answer_e: n = x + ii;
  :correct: d
  :feedback_a: Incorrect. Try to observe what do you want to add and to which variable, and loud bells should ring.
  :feedback_b: Incorrect. Try to observe what do you want to add and to which variable, and loud bells should ring.
  :feedback_c: Incorrect. Try to observe what do you want to add and to which variable, and loud bells should ring.
  :feedback_d: Correct!
  :feedback_e: Incorrect. Try to observe what do you want to add and to which variable, and loud bells should ring.
  
  The following program should print the sum of 'n' whole numbers starting from 1 to n. Which of the following options should be present in the blank (inside the for-loop) in order to make the program work correctly.

  .. code-block:: matlab
  
     clc; clear;
     
     n = input('Enter the number: ');
     x = 0;
     
     for ii = 1:1:n
     	___________________________
       end
     
     fprintf('The sum is %g', x);

.. mchoice:: aa-iteration_05_foorloops_17
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: p = p * (p*2);
  :answer_b: p = p * (2^ii);
  :answer_c: p = 2 * (2^ii);
  :answer_d: p = p * (p^ii);
  :answer_e: p = ii * (2^ii);
  :correct: b
  :feedback_a: Incorrect. Try to observe what do you want to add and to which variable, and extremely loud bells should ring.
  :feedback_b: Correct! 
  :feedback_c: Incorrect. Try to observe what do you want to add and to which variable, and extremely loud bells should ring.
  :feedback_d: Incorrect. Try to observe what do you want to add and to which variable, and extremely loud bells should ring.
  :feedback_e: Incorrect. Try to observe what do you want to add and to which variable, and extremely loud bells should ring.
  
  The following program calculates the product of the sequence given below till 'x' terms. Which of the options should be present in the blank (inside the for-loop) in order to make the program work correctly. p = 2 * 4 * 8 * 16 * 32 * 64 * 128 * ..................….

  .. code-block:: matlab
  
     x = input('Enter the number of terms: ');
     
     p = 1;
     
     for ii = 1:1:x
     ___________________________
     end
     
     fprintf('The product is %g', p);

.. mchoice:: aa-iteration_05_foorloops_18
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: In line 3, it should be total = 0 instead of total = 5
  :answer_b: In line 5, it should 'for ii = 1:1:terms-1' instead of 'for ii = 1:1:terms'
  :answer_c: In line 5, it should 'for ii = 2:1:terms' instead of 'for ii = 1:1:terms'
  :answer_d: In line 6, it should 'total  = total +  terms/(ii*5)' instead of 'total  = total +  ii/(ii*5)'
  :answer_e: In line 6, it should 'total  = total +  ii/(ii*total)' instead of 'total  = total +  ii/(ii*5)'
  :correct: c
  :feedback_a: Incorrect. Check it again by generating the terms in the program and then observe them.
  :feedback_b: Incorrect. Check it again by generating the terms in the program and then observe them.
  :feedback_c: Correct! 
  :feedback_d: Incorrect. Check it again by generating the terms in the program and then observe them.
  :feedback_e: Incorrect. Check it again by generating the terms in the program and then observe them.
  
  The following program calculates the product of the sequence given below till 'x' terms. Which of the options is correct in order to make the program work correctly. total = 5 + (2/10) + (3/15) +  (4/20)  + (5/25) + .............… 

  .. code-block:: matlab
  
     1. clc; clear;
     2. terms = input('Enter the number of terms: ');
     3. total = 5;
     4. 
     5. for ii = 1:1:terms
     6. total = total + ii/(ii*5);
     7. end
     8. 
     9. fprintf( 'The total is %g', total);

.. mchoice:: aa-iteration_05_foorloops_19
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: A while-loop because we don’t exactly know how many terms we need to run the loop
  :answer_b: A for-loop because we don’t exactly know how many terms we need to run the loop
  :answer_c: A for-loop because it will be able to generate the terms easily
  :answer_d: A while-loop because we exactly know how many terms we need to run the loop
  :correct: a
  :feedback_a: Correct! 
  :feedback_b: Incorrect. Remember that for-loop should only be used when you know the number of times you want to run the loop.
  :feedback_c: Incorrect. Remember that for-loop should only be used when you know the number of times you want to run the loop.
  :feedback_d: Incorrect. Remember that for-loop should only be used when you know the number of times you want to run the loop.
  
  If you are asked to write a program to calculate the number of terms required for the following sequence to reach just above 10000: sequence: 5 + (5^2) + (5^3) + (5^4) + ................................…. Which loop should you prefer to use and why?

.. mchoice:: aa-iteration_05_foorloops_20
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: A while-loop because we don’t exactly know how many terms we need to run the loop
  :answer_b: A for-loop because we don’t exactly know how many terms we need to run the loop
  :answer_c: A for-loop because we exactly know how many terms we need to run the loop
  :answer_d: A while-loop because it will be able to generate the terms easily
  :correct: c
  :feedback_a: Incorrect. Remember that for-loop should be preferred when you know the number of times you want to run the loop.
  :feedback_b: Incorrect. Remember that for-loop should be preferred when you know the number of times you want to run the loop.
  :feedback_c: Correct! 
  :feedback_d: Incorrect. Remember that for-loop should be preferred when you know the number of times you want to run the loop.
  
  If you are asked to write a program to calculate the sum of first 100 terms of the follow

.. fillintheblank:: aa-iteration_06_seriesandpatterns_01
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code snippet?  (If the program will result in an error or infinite loop, put down ‘ERROR’)

       .. code-block:: matlab
  
         clc; clear;
     
         sum = 0;
     
         while true
           while sum < 10
             sum = sum + 10;
             while sum <20
               sum = sum + 10;
               break
             end
             break;
             sum = sum + 10;
           end
           sum = sum + 10;
           disp(sum)
           break;
         end

  - :30: Correct!
    :x: Incorrect. Remember that the break statement executes for the corresponding loop in which the statement is present in.
  
.. fillintheblank:: aa-iteration_06_seriesandpatterns_02
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code snippet?  (If the program will result in an error or infinite loop, put down ‘ERROR’)

       .. code-block:: matlab
  
         clc; clear;
     
         sum = 0;
     
         while true
           while sum < 10
             sum = sum + 10;
             continue
             sum = sum + 10;
           end
           break;
           sum = sum + 1;
         end
         disp(sum)

  - :10: Correct!
    :x: Incorrect. Remember that when a continue or break statement executes, it goes up (for continue) or comes out (for break) immediately as soon as it is executed.

.. fillintheblank:: aa-iteration_06_seriesandpatterns_03
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code snippet?  (If the program will result in an error or infinite loop, put down ‘ERROR’)

       .. code-block:: matlab
  
         clc; clear;
         sum = 0;
     
         while true
           while sum < 10
             sum = sum + 10;
             if sum == 10
               fprintf('%g',sum);
               break
               sum = sum + 10;
             else
               ontinue
             end
           end
           if sum >10
		         sum = sum + 1;
           else
		         break;
		         sum = sum + 2;
	         end
	         sum = sum + 3;
         end
         fprintf('%g',sum);

  - :1010: Correct!
    :x: Incorrect. Remember that continue and break statements are only related to loops, so they execute for the corresponding loop only in which the statement is present in.

.. fillintheblank:: aa-iteration_06_seriesandpatterns_04
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code snippet?  (If the program will result in an error or infinite loop, put down ‘ERROR’)

       .. code-block:: matlab
  
         clc; clear;
     
         sum = 42;
     
         while sum > 10
           if mod(sum, 2) ~= 0
             break;
	         else
		         sum = sum -7;
		         continue
	         end
	         while sum > 0
		         sum = sum -5;
	         end
         end
         fprintf('%g',sum);

  - :35: Correct!
    :x: Incorrect. Note that as soon as the break statement executes, the execution comes out of the corresponding loop.

.. fillintheblank:: aa-iteration_06_seriesandpatterns_05
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code snippet?  (If the program will result in an error or infinite loop, put down ‘ERROR’)

       .. code-block:: matlab
  
         clc; clear;
         num = 1 ;
     
         for ii = 1:1:3
	         while num <15
		         if mod(num,3) == 0
			         %num = num + 2;
			         break
		         else
			         num = num + 5;
			         continue
		         end
	         end
	         num = num +4;
         end 
         disp(num)

  - :23: Correct!
    :x: Incorrect. Note that continue and break statements execute for the corresponding loops, irrespective of whether it is a for-loop or while-loop.

.. fillintheblank:: aa-iteration_06_seriesandpatterns_06
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code snippet?  (If the program will result in an error or infinite loop, put down ‘ERROR’)

       .. code-block:: matlab
  
         clc; clear;
         num = 1 ;

         for ii = 1:1:5
	         for jj = 1:1:5
		         num = num + 1;
		         continue;
	         end
	         break;
	         num = num +1 ;
         end
         fprintf(‘%g’, num);

  - :6: Correct!
    :x: Incorrect. Note that continue and break statements execute for the corresponding loops, irrespective of whether it is a for-loop or while-loop.

.. fillintheblank:: aa-iteration_06_seriesandpatterns_07
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code snippet?  (If the program will result in an error or infinite loop, put down ‘ERROR’)

       .. code-block:: matlab
  
         clc; clear;
         num = 10 ;

         if num > 10
	         disp(num)
	         break;
         else
	         num = num + 1;
         end

  - :ERROR: Correct!
    :x: Incorrect. Note that continue and break statements are valid only with loops.

.. fillintheblank:: aa-iteration_06_seriesandpatterns_08
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code snippet?  (If the program will result in an error or infinite loop, put down ‘ERROR’)

       .. code-block:: matlab
  
         clc; clear;
     
         a = 5;
         b = 10;

         for ii = 1:1:5
	         c = a + b + c;
         end
         disp(c);

  - :ERROR: Correct!
    :x: Incorrect. Note that variables have to be declared before you can use them.

.. fillintheblank:: aa-iteration_06_seriesandpatterns_09
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code snippet?  (If the program will result in an error or infinite loop, put down ‘ERROR’)

       .. code-block:: matlab
  
         clc; clear;
         a = 1;

         for ii = 1:1:3
	         for jj = 1:1:2
		         fprintf('%g',a);
	         end
	         a = a + 1;
         end

  - :112233: Correct!
    :x: Incorrect. Check the program again and execute it step by step.

.. fillintheblank:: aa-iteration_06_seriesandpatterns_10
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code snippet?  (If the program will result in an error or infinite loop, put down ‘ERROR’)

       .. code-block:: matlab
  
         clc; clear;
         ii = 1;

         while ii <= 3
	         while ii <= 2
		         fprintf('ii');
		         ii = ii + 1;
	         end
         end

  - :iiii: Correct!
    :x: Incorrect. Check carefully to see what are you printing.

.. mchoice:: aa-iteration_06_seriesandpatterns_11
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: This program prints 10 consecutive multiples of 2 which are obtained by multiplying 2 with 1,2,3……..10.
  :answer_b: This program prints 10 consecutive exponents of 2 which are obtained by 2 to the power of 1,2,3……..10.
  :answer_c: This program adds the values of 1 to ‘a’, 10 times.
  :answer_d: This program multiplies the value of ‘a’ with ‘a’, 10 times.
  :correct: b
  :feedback_a: Incorrect. Iterate the program step by step using a pen and paper and then see what you get.
  :feedback_b: Correct! 
  :feedback_c: Incorrect. Iterate the program step by step using a pen and paper and then see what you get.
  :feedback_d: Incorrect. Iterate the program step by step using a pen and paper and then see what you get.
  
  What is the following program trying to do? Choose one of the following options.

  .. code-block:: matlab
  
     clc; clear;
     
     a = 1;
     
     for ii = 1:1:10
      a = a + a;
      disp(a);
     end

.. mchoice:: aa-iteration_06_seriesandpatterns_12
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: This program prints 10 consecutive multiples of 2 which are obtained by multiplying 2 with 1,2,3……..10.
  :answer_b: This program prints 10 consecutive exponents of 2 which are obtained by 2 to the power of 1,2,3……..10.
  :answer_c: This program adds the values of 1 to ‘a’, 10 times.
  :answer_d: This program multiplies the value of ‘a’ with ‘a’, 10 times.
  :correct: c
  :feedback_a: Incorrect. Iterate the program step by step using a pen and paper and then see what you get.
  :feedback_b: Incorrect. Iterate the program step by step using a pen and paper and then see what you get.
  :feedback_c: Correct!
  :feedback_d: Incorrect. Iterate the program step by step using a pen and paper and then see what you get.
  
  What is the following program trying to do? Choose one of the following options.

  .. code-block:: matlab
  
     clc; clear;
     
     a = 0;
     x = 1;
     
     for ii = 1:1:10
      a = a + x;
      disp(a);
     end

.. mchoice:: aa-iteration_06_seriesandpatterns_13
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: It prints the sum of series: (1*2*3) + (2*3*4) + (3*4*5) + (4*5*6) + (5*6*7)
  :answer_b: It prints the sum of series: (1*2*3) + (1*2*3) + (1*2*3) + (1*2*3) + (1*2*3)
  :answer_c: It prints the sum of series: (1*2*2) + (2*2*2) + (3*2*2) + (4*2*2) + (5*2*2)
  :answer_d: It prints the sum of series: (1*2*3) + (2*2*3) + (3*2*3) + (4*2*3) + (5*2*3)
  :correct: d
  :feedback_a: Incorrect. Iterate the program step by step using a pen and paper and then see what you get.
  :feedback_b: Incorrect. Iterate the program step by step using a pen and paper and then see what you get.
  :feedback_c: Incorrect. Iterate the program step by step using a pen and paper and then see what you get.
  :feedback_d: Correct!
  
  What is the following program trying to do? Choose one of the following options.

  .. code-block:: matlab
  
     clc; clear;
     
     sum = 0;
     
     for ii = 1:1:5
      fun = ii;
      num = 2;
      for jj = 1:1:2
        fun = fun * num;
        num = num + 1;
      end
      sum = sum + fun;
     end

.. mchoice:: aa-iteration_06_seriesandpatterns_14
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: It prints the sum of series: (1*2*3) + (2*3*4) + (3*4*5) + (4*5*6) + (5*6*7)
  :answer_b: It prints the sum of series: (1*2*3) + (1*2*3) + (1*2*3) + (1*2*3) + (1*2*3)
  :answer_c: It prints the sum of series: (1*2*2) + (2*2*2) + (3*2*2) + (4*2*2) + (5*2*2)
  :answer_d: It prints the sum of series: (1*2*3) + (2*2*3) + (3*2*3) + (4*2*3) + (5*2*3)
  :correct: a
  :feedback_a: Correct!
  :feedback_b: Incorrect. Iterate the program step by step using a pen and paper and then see what you get.
  :feedback_c: Incorrect. Iterate the program step by step using a pen and paper and then see what you get.
  :feedback_d: Incorrect. Iterate the program step by step using a pen and paper and then see what you get.
  
  What is the following program trying to do? Choose one of the following options.

  .. code-block:: matlab
  
     clc; clear;
     
     sum = 0;
     
     for ii = 1:1:5
      fun = ii;
      num = ii+1;
      for jj = 1:1:2
        fun = fun * num;
        num = num + 1;
      end
      sum = sum + fun;
     end

.. mchoice:: aa-iteration_06_seriesandpatterns_15
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: It prints the sum of series: (1*2*3) + (2*3*4) + (3*4*5) + (4*5*6) + (5*6*7)
  :answer_b: It prints the sum of series: (1*2*3) + (1*2*3) + (1*2*3) + (1*2*3) + (1*2*3)
  :answer_c: It prints the sum of series: (1*2*2) + (2*2*2) + (3*2*2) + (4*2*2) + (5*2*2)
  :answer_d: It prints the sum of series: (1*2*3) + (2*2*3) + (3*2*3) + (4*2*3) + (5*2*3)
  :correct: c
  :feedback_a: Incorrect. Iterate the program step by step using a pen and paper and then see what you get.
  :feedback_b: Incorrect. Iterate the program step by step using a pen and paper and then see what you get.
  :feedback_c: Correct!
  :feedback_d: Incorrect. Iterate the program step by step using a pen and paper and then see what you get.
  
  What is the following program trying to do? Choose one of the following options.

  .. code-block:: matlab
  
     clc; clear;
     
     sum = 0;
     
     for ii = 1:1:5
      fun = ii;
      num = 2;
      for jj = 1:1:2
        fun = fun * num;
      end
      sum = sum + fun;
     end

.. mchoice:: aa-iteration_06_seriesandpatterns_16
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: Change sum = 1 to sum = 0
  :answer_b: Change for ii=1:1:99 to for ii=1:1:100
  :answer_c: Change sum = sum + (ii  * (ii+1) ) to sum = sum + (ii  * (ii-1) );
  :answer_d: Change for ii=1:1:99 to for ii=2:1:100 
  :correct: d
  :feedback_a: Incorrect. Generate the different terms of the sequence and then observe where is the error.
  :feedback_b: Incorrect. Generate the different terms of the sequence and then observe where is the error.
  :feedback_c: Incorrect. Generate the different terms of the sequence and then observe where is the error.
  :feedback_d: Correct!
  
  The following program calculates the sum of the series till first 100 terms: sum = 1 + (2 * 3) + (3 * 4) + (4 * 5)……… Which of the following changes will correct a mistake in the program such that it calculates the sum correctly?

  .. code-block:: matlab
  
     clc; clear;
     
     sum = 1;
     
     for ii=1:1:99
      sum = sum + (ii  * (ii+1) );
     end
     
     disp(sum)

.. mchoice:: aa-iteration_06_seriesandpatterns_17
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: Change term = 1 to term = 0
  :answer_b: Change for ii=1:1:99 to while sum <= 500
  :answer_c: Change sum = sum + (terms  * (terms+1) ) to  sum = sum + ( (terms-1)  * terms );
  :answer_d: Change for ii=1:1:99 to for ii=2:1:500
  :correct: b
  :feedback_a: Incorrect. Check your notes to see when should we use a for loop and when should we use a while loop.
  :feedback_b: Correct!
  :feedback_c: Incorrect. Check your notes to see when should we use a for loop and when should we use a while loop.
  :feedback_d: Incorrect. Check your notes to see when should we use a for loop and when should we use a while loop.
  
  The program below calculates the number of terms required for the following sequence to just exceed 500: sum = 1 + (2 * 3) + (3 * 4) + (4 * 5)……… Which of the following changes will correct a mistake in the program such that it calculates the number of terms correctly?

  .. code-block:: matlab
  
     clc; clear;
     
     sum = 1;
     
     terms = 1;
     
     for ii=1:1:500
      terms = terms + 1;
      sum = sum + (terms  * (terms+1) );
     end
     
     disp(terms)

.. mchoice:: aa-iteration_06_seriesandpatterns_18
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: Change sum = ii^ii to sum = sum - ii^ii
  :answer_b: Change sum = 5 to sum = 0
  :answer_c: Change for ii=2:1:582 to for ii=1:1:582
  :answer_d: Change for ii=1:1:99 to for ii=2:2:582
  :correct: a
  :feedback_a: Correct!
  :feedback_b: Incorrect. Check the program and generate the terms.
  :feedback_c: Incorrect. Check the program and generate the terms.
  :feedback_d: Incorrect. Check the program and generate the terms.
  
  The program below calculates the sum of the series till first 582 terms: sum = 5 - 2^2 + 5 - 4^4 + 5 - 6^6 + 5 -8^8 ....................…. Which of the following changes will correct a mistake in the program such that it calculates the sum of the series correctly?

  .. code-block:: matlab
  
     clc; clear;
     
     sum = 5;
     counter = 0;
     
     for ii=2:1:582
      if counter == 0
        sum = ii^ii;
        counter = 1;
      else
        sum = sum + 5;
        counter = 0;
      end
     end
     
     disp(terms)

.. mchoice:: aa-iteration_06_seriesandpatterns_19
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: The value of ‘c’ represents the sum of all digits in num.
  :answer_b: The value of ‘c’ represents the total number of digits in num.
  :answer_c: The value of ‘c’ represents the number of times the loop works to make ‘num’ divisible by 10.
  :answer_d: None of the above!
  :correct: b
  :feedback_a: Incorrect. Check the program, generate the terms and see what is the values of ‘c’.
  :feedback_b: Correct!
  :feedback_c: Incorrect. Check the program, generate the terms and see what is the values of ‘c’.
  :feedback_d: Incorrect. Check the program, generate the terms and see what is the values of ‘c’.
  
  What does the value of ‘c’ represents in the following program:

  .. code-block:: matlab
  
     clc; clear;
     
     num = input(‘Enter the number: ‘);
     
     c = 0;
     
     while num > 0
      num = floor(num/10);
      c = c + 1;
     end
     
     disp(c)

.. mchoice:: aa-iteration_06_seriesandpatterns_20
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: The value of ‘c’ represents the sum of all digits in num.
  :answer_b: The value of ‘c’ represents the total number of digits in num.
  :answer_c: The value of ‘c’ represents the number of times the loop works to make ‘num’ divisible by 10.
  :answer_d: None of the above!
  :correct: a
  :feedback_a: Correct!
  :feedback_b: Incorrect. Check the program, generate the terms and see what is the values of ‘c’.
  :feedback_c: Incorrect. Check the program, generate the terms and see what is the values of ‘c’.
  :feedback_d: Incorrect. Check the program, generate the terms and see what is the values of ‘c’.
  
  What does the value of ‘c’ represents in the following program:

  .. code-block:: matlab
  
     clc; clear;
     
     num = input(‘Enter the number: ‘);
     
     c = 0;
     
     while num > 0
      c = c + mod(num, 10);
      num = floor(num/10);
     end
     
     disp(c)

