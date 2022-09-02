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

.. mchoice:: jh-inputs_22_indexing_02
  :author: Joe Hummel
  :practice: T
  :answer_a: [0 | 10]
  :answer_b: [0 | 2 | 10]
  :answer_c: [0 | 2 | 4 | 6 | 8 | 10]
  :answer_d: [2 | 2 | 2 | 2 | 2 | 2 | 2 | 2 | 2 | 2]
  :correct: c
  :feedback_a: Incorrect. 
  :feedback_b: Incorrect.
  :feedback_c: Correct! 
  :feedback_d: Incorrect. 

  What is the contents of Z? 
  
  .. code-block:: matlab

    Z = 0:2:10;

.. mchoice:: jh-inputs_22_indexing_03
  :author: Joe Hummel
  :practice: T
  :answer_a: [10]
  :answer_b: [121]
  :answer_c: [10 | 15 | 102]
  :answer_d: Error, you cannot add vector (X) and scalar (3).
  :correct: c
  :feedback_a: Incorrect. 
  :feedback_b: Incorrect.
  :feedback_c: Correct! 
  :feedback_d: Incorrect. 

  What is the contents of Y? 
  
  .. code-block:: matlab
    
    X = [7,12,99];, Y = X + 3;

.. mchoice:: jh-inputs_22_indexing_04
  :author: Joe Hummel
  :practice: T
  :answer_a: Y = [9, 18, 2]
  :answer_b: Y = [1, 0, 0, 1, 0, 1, 0]
  :answer_c: Y = [0, 1, 1, 0, 1, 0, 1]
  :answer_d: Y = 3
  :correct: b
  :feedback_a: Incorrect. 
  :feedback_b: Correct!
  :feedback_c: Incorrect.
  :feedback_d: Incorrect. 

  Suppose X contains [9, 80, 20, 18, 48, 2, 110]. What is the result of executing Y = (X < 20)?

.. mchoice:: jh-inputs_22_indexing_06
    :author: Joe Hummel
    :practice: T
  
    In the project, you need to see if a string is a valid sentence.  You have a function ValidAscii(c) that returns true if c is valid, false if not. What’s your best guess of how to apply this function to every char in a string without using a loop?

    - .. code-block:: matlab
     
         s  = ‘a valid string’;
         s2 = ValidAscii(c);

      - Incorrect. Review the steps one at a time and try again!

    - .. code-block:: matlab
       
         s  = ‘a valid string’;
         s2 = ValidAscii(s);

      + Correct!


    - .. code-block:: matlab
  
         s  = ‘a valid string’;
         s2 = (ValidAscii == s);

      - Incorrect. Review the steps one at a time and try again!

.. mchoice:: aa-indexing_03_conditionals_01
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: Both the lines are same as xyz = 5 and xyz == 5 are assigning a value to a variable.
  :answer_b: Both the lines are different as xyz = 5 is assignment and xyz == 5 is comparison.
  :answer_c: Both the lines are different as xyz = 5 is comparison and xyz == 5 is assignment.
  :answer_d: Both the lines are same as xyz = 5 and xyz == 5 are comparing a value with a variable.
  :correct: b
  :feedback_a: Incorrect. Assignment and comparison differentiate them, check out in MATLAB which is is used to assign a value and which is used to compare it.
  :feedback_b: Correct! 
  :feedback_c: Incorrect. Assignment and comparison differentiate them, check out in MATLAB which is is used to assign a value and which is used to compare it.
  :feedback_d: Incorrect. Assignment and comparison differentiate them, check out in MATLAB which is is used to assign a value and which is used to compare it.

  Choose an option which is true for the following lines of code: 

  .. code-block:: matlab
  
     xyz == 5;
     xyz == 5;

.. mchoice:: aa-indexing_03_conditionals_02
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: && has a priority over ||
  :answer_b: || has a priority over &&
  :answer_c: When it comes to executing a conditions, || and && have same priority
  :answer_d: Sometimes && has priority over || and sometimes || has priority over &&
  :correct: a
  :feedback_a: Correct! You are clear on how conditions are evaluated.
  :feedback_b: Incorrect. Take a complex condition in MATLAB and check which one has the priority.
  :feedback_c: Incorrect. Take a complex condition in MATLAB and check which one has the priority.
  :feedback_d: Incorrect. Take a complex condition in MATLAB and check which one has the priority.

  Which of the following statements is true regarding the use of && (AND) and || (OR) operator is conditions?

.. mchoice:: aa-indexing_03_conditionals_03
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: If x>20 && x<100
  :answer_b: If 20<x && 100>x
  :answer_c: If 20<x<100
  :answer_d: If x<100 and x>20
  :answer_e: If 100>x && 20<x
  :correct: c
  :feedback_a: Incorrect. Take some sample value of x and y and try it yourself in MATLAB. You will come to know which one is not correct.
  :feedback_b: Incorrect. Take some sample value of x and y and try it yourself in MATLAB. You will come to know which one is not correct.
  :feedback_c: Correct! 
  :feedback_d: Incorrect. Take some sample value of x and y and try it yourself in MATLAB. You will come to know which one is not correct.
  :feedback_e: Incorrect. Take some sample value of x and y and try it yourself in MATLAB. You will come to know which one is not correct.

  Which of the following is not a correct way of writing an if-condition?

.. mchoice:: aa-indexing_03_conditionals_04
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: Yes, they are same and having parenthesis will make no difference in how they are evaluated.
  :answer_b: The way conditions are evaluated will depend on the values of x and y.
  :answer_c: No, they are not same as having parenthesis will impact the way the conditions are evaluated.
  :correct: c
  :feedback_a: Incorrect. Check yourself and try these conditions in MATLAB by taking x = 2 and y = 2.
  :feedback_b: Incorrect. Check yourself and try these conditions in MATLAB by taking x = 2 and y = 2.
  :feedback_c: Correct! 

  Are the two following if-conditions same? 

  .. code-block:: matlab
  
     Condition 1: if x == 2 || x == 3 && y == 2  || y == 3 
     Condition 2: if ( x == 2 || x == 3 ) && ( y == 2 || y == 3 )

.. fillintheblank:: aa-indexing_03_conditionals_05
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code snippet? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
      clc; clear;
     
      x = 20;
     
      if mod(x,4) ~= 0 && mod(x,5) == 0
       fprintf('4');

      elseif mod(x,5) ~= 0 || mod(x,4) == 0
       fprintf('5');

      elseif mod(x,4) == 0 && mod(x,5) == 0
       fprintf('45');
     
      end

  - :5: Correct!
    :x: Incorrect. Note that conditions are evaluated from top to bottom, however, if a condition is true then the other conditions below it will never be checked.

.. fillintheblank:: aa-indexing_03_conditionals_06
   :author: Ashish Aggarwal
   :casei:

   What will be the output of the following code snippet? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
      clc; clear;
     
      x = 20;
     
      if mod(x,4) ~= 0
       fprintf('4');
      
      elseif mod(x,5) ~= 0
       fprintf('5');
      
      elseif mod(x,4) == 0 || mod(x,5) == 0
       fprintf('45');
      
      end
     
      if mod(x,4) == 0 && mod(x,5) == 0
       fprintf('45');
      
      end

  - :4545: Correct!
    :x: Incorrect. This code snippet has two separate blocks of if statements which are independent of each other.

.. fillintheblank:: aa-indexing_03_conditionals_07
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code snippet? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
      clc; clear;
     
      x = 20;
     
      if mod(x,4) ~= 0
       fprintf('4');
      
      elseif mod(x,5) == 0
     
      if mod(x,4) == 0
       fprintf('54');
      
      end
       fprintf(’4’);
      
      elseif mod(x,4) == 0 || mod(x,5) == 0
       fprintf('45');
      
      else
       fprintf(’4545’);
      
      end

  - :544: Correct!
    :x: Incorrect. This code snippet has nested if-conditions. Check it carefully and execute this code line by line.

.. fillintheblank:: aa-indexing_03_conditionals_08
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code snippet? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
      clc; clear;
      num = 24;
     
      fprintf('X');
     
      if mod(num,8) == 0
       fprintf('Z');
      
      if num/3 == 8
       fprintf('Y');
      
      end
     
      fprintf('V');
     
      end
     
      fprintf('W');

  - :XZYVW: Correct!
    :x: Incorrect. Check it carefully and execute this code line by line.

.. mchoice:: aa-indexing_03_conditionals_09
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: 2
  :answer_b: 0.5
  :answer_c: 30
  :answer_d: 60
  :answer_e: ERROR
  :correct: c
  :feedback_a: Incorrect. Remember that mod(x,y) gives you the remainder when x is divided by y. So what will be the remainder when 30 is divided by 60? You can definitely find it!
  :feedback_b: Incorrect. Remember that mod(x,y) gives you the remainder when x is divided by y. So what will be the remainder when 30 is divided by 60? You can definitely find it!
  :feedback_c: Correct! 
  :feedback_d: Incorrect. Remember that mod(x,y) gives you the remainder when x is divided by y. So what will be the remainder when 30 is divided by 60? You can definitely find it!
  :feedback_e: Incorrect. Remember that mod(x,y) gives you the remainder when x is divided by y. So what will be the remainder when 30 is divided by 60? You can definitely find it!

  What is mod(30,60)?

.. mchoice:: aa-indexing_03_conditionals_10
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: If x == A and y ~= Z
  :answer_b: If x ~= A and y == Z
  :answer_c: If x == ‘A’ and y ~= ‘Z’ 
  :answer_d: If x ~= ‘A’ and y == ‘Z’
  :correct: c
  :feedback_a: Incorrect. Remember that when comparing with letters, we put single quotes around the letter being compared. This differentiates a symbol from it being a variable. 
  :feedback_b: Incorrect. Remember that when comparing with letters, we put single quotes around the letter being compared. This differentiates a symbol from it being a variable. 
  :feedback_c: Correct! 
  :feedback_d: Incorrect. Remember that when comparing with letters, we put single quotes around the letter being compared. This differentiates a symbol from it being a variable. 
  
  Which of the following conditions checks if variable x is same as letter A and variable y is different from letter Z?

.. mchoice:: aa-indexing_03_conditionals_11
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: variable = input('Enter a letter: ');
  :answer_b: variable = input('Enter a letter: ' , 's');
  :answer_c: variable = fprintf('Enter a letter: ');
  :answer_d: variable = input('Enter a letter: ' , %s);
  :answer_e: variable = input();
  :correct: b
  :feedback_a: Incorrect. Remember that to take a string/letter as input, we put ‘s’ in the input statement after the input prompt. This implies that input will be of string type and not a number.
  :feedback_b: Correct! 
  :feedback_c: Incorrect. Remember that to take a string/letter as input, we put ‘s’ in the input statement after the input prompt. This implies that input will be of string type and not a number.
  :feedback_d: Incorrect. Remember that to take a string/letter as input, we put ‘s’ in the input statement after the input prompt. This implies that input will be of string type and not a number.
  :feedback_e: Incorrect. Remember that to take a string/letter as input, we put ‘s’ in the input statement after the input prompt. This implies that input will be of string type and not a number.
  
  Which of the following options is the correct syntax to take a letter as input from a user?

.. fillintheblank:: aa-indexing_03_conditionals_12
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code snippet? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
      clc; clear;
     
      y = 1;
     
      if y > 0
       y = 3;
      
      elseif y == 3
       y = y + 2;
      
      else
       y = y - 1;
     
      end
     
      fprintf ('%.2f%g', 3*y, y);

  - :9.003: Correct!
    :x: Incorrect. Execute this program line by line carefully and make sure you correctly look at the format specifiers used in the fprintf() statement.

.. mchoice:: aa-indexing_03_conditionals_13
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: fprintf('You don’t have 80% points');
  :answer_b: fprintf('You don''t have 80% points');
  :answer_c: fprintf('You don''t have 80%% points');
  :answer_d: fprintf('You don't have 80%% points');
  :correct: c
  :feedback_a: Incorrect. Displaying apostrophe or percent sign maybe a little tricky, you put them twice wherever you want them in fprintf() statement.
  :feedback_b: Incorrect. Displaying apostrophe or percent sign maybe a little tricky, you put them twice wherever you want them in fprintf() statement.
  :feedback_c: Correct!
  :feedback_d: Incorrect. Displaying apostrophe or percent sign maybe a little tricky, you put them twice wherever you want them in fprintf() statement.
  
  Which of the following fprintf() will display this statement: You don’t have 80% points.

.. mchoice:: aa-indexing_03_conditionals_14
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: a will be 12 and b will be 24
  :answer_b: a will be 24 and b will be 12
  :answer_c: a will be 12 and b will be 12
  :answer_d: a will be 24 and b will be 24
  :answer_e: ERROR
  :correct: c
  :feedback_a: Incorrect. Check the conditions again, note that only one condition gets executed.
  :feedback_b: Incorrect. Check the conditions again, note that only one condition gets executed.
  :feedback_c: Correct!
  :feedback_d: Incorrect. Check the conditions again, note that only one condition gets executed.
  :feedback_e: Incorrect. Check the conditions again, note that only one condition gets executed.
  
  What will be the values of a and b after the execution of this code? 

  .. code-block:: matlab
  
     clc; clear;
     a = 2;
     a = a*2;
     a = a*3;
     b = 24;
     
     if a < b
      b = b/2;
     
     elseif a == b/2
      a = 2*a;
      b = b/2;

     else 
      a = 2*a;

     end

.. mchoice:: aa-indexing_03_conditionals_5
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: x will be 9
  :answer_b: x will be 8
  :answer_c: x will be 12
  :answer_d: x will be 15
  :answer_e: x will be 5
  :correct: b
  :feedback_a: Incorrect. Check the conditions again, note that only one condition gets executed.
  :feedback_b: Correct! Check the conditions again, note that only one condition gets executed.
  :feedback_c: Incorrect. Check the conditions again, note that only one condition gets executed.
  :feedback_d: Incorrect. Check the conditions again, note that only one condition gets executed.
  :feedback_e: Incorrect. Check the conditions again, note that only one condition gets executed.
  
  What will be the values of a and b after the execution of this code? 

  .. code-block:: matlab
  
     clc; clear;
     x = 15;

     if x <= 15
        x = x - 3;
          if x == 12
            x = x - 3;
          end
     
     elseif x > 0
        x = x - 3;
     end
     
     if x == 6
        x = 5;
     elseif x == 9
        x = 5;
        x = x + 3;
     
     else
        x = x + 15;
     end

.. mchoice:: aa-indexing_03_conditionals_16
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: There can be at most only one elseif clause
  :answer_b: There can be multiple else clauses
  :answer_c: The else clause must be the last clause in the if-elseif-else construct
  :answer_d: The else clause can have a condition
  :correct: c
  :feedback_a: Incorrect. Check the syntax of if-elseif-else conditions again.
  :feedback_b: Incorrect. Check the syntax of if-elseif-else conditions again.
  :feedback_c: Correct! 
  :feedback_d: Incorrect. Check the syntax of if-elseif-else conditions again.
  
  Which of the following statement is true regarding if-elseif-else statements? 

.. mchoice:: aa-indexing_03_conditionals_17
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: Swap the condition of line 9 with line 7
  :answer_b: Swap the condition of line 9 with line 11
  :answer_c: Swap the condition of line 7 with line 5
  :answer_d: Swap the condition of line 11 with line 5
  :answer_e: Swap the condition of line 9 with line 5
  :correct: e
  :feedback_a: Incorrect. The execution of if-elseif-else conditions work in such a way that as soon as one condition is evaluated as true, the following conditions are not even looked at.
  :feedback_b: Incorrect. The execution of if-elseif-else conditions work in such a way that as soon as one condition is evaluated as true, the following conditions are not even looked at.
  :feedback_c: Incorrect. The execution of if-elseif-else conditions work in such a way that as soon as one condition is evaluated as true, the following conditions are not even looked at.
  :feedback_d: Incorrect. The execution of if-elseif-else conditions work in such a way that as soon as one condition is evaluated as true, the following conditions are not even looked at.
  :feedback_e: Correct! 
  
  The following program displays ‘Yes’ only when a given number is divisible by 3 and 7 both. However, the program has an error that can be corrected by swapping two conditions with each other including there fprintf() statement. Which of the given swaps will correct this program? 

  .. code-block:: matlab
  
     clc; clear;
     num = input('Enter the number: ');
     
     if mod(num, 3) == 0
      fprintf('No');
     elseif mod(num, 7) == 0
      fprintF('No');
     elseif mod(num, 3) == 0 && mod(num, 7) == 0
      fprintf('Yes');
     elseif mod(num, 3) == 0 || mod(num, 7) == 0
      fprintf('No');
     end

.. fillintheblank:: aa-indexing_03_conditionals_18
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code snippet? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
      clc; clear;
     
      y = 5;
     
      if y = 5
       y = 5;
      
      else
       y = 6;
      
      end
     
      disp(y);

  - :ERROR: Correct!
    :x: Incorrect. Check the assignment operator again.

.. mchoice:: aa-indexing_03_conditionals_19
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: mod(x,10) ==9 || mod(x,10) == 0
  :answer_b: mod(x,10) ~= 9 && mod(x,10) ~=0
  :answer_c: mod(x,10) ~= 9 || mod(x,10) ~= 0
  :answer_d: mod(x,10) == 9 && mod(x,10) == 0
  :correct: b
  :feedback_a: Incorrect. Very carefully take some example like lets say x = 50 and then check every condition to see what does it display. Also, note that mod() is a very useful function, it can give you the first digit by finding the remainder when a number is divided by 10.
  :feedback_b: Correct! 
  :feedback_c: Incorrect. Very carefully take some example like lets say x = 50 and then check every condition to see what does it display. Also, note that mod() is a very useful function, it can give you the first digit by finding the remainder when a number is divided by 10.
  :feedback_d: Incorrect. Very carefully take some example like lets say x = 50 and then check every condition to see what does it display. Also, note that mod() is a very useful function, it can give you the first digit by finding the remainder when a number is divided by 10.
  
  The following program should display ‘Yes’ if the given number by the user has either 9 or 0 in its ones place. For example 2349, 2340, 39, 40….have either 0 or 9 in their ones place (the first digit from the right). Which condition should be there in line 3 so that the program works correctly?

  .. code-block:: matlab
  
     x = input(‘Enter the number: ‘);
     if ________________________________
      fprintf(‘No’);
     else
      fprintf(‘Yes’);
     end

.. fillintheblank:: aa-indexing_03_conditionals_20
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code snippet? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
      clc; clear;
     
      x = 'A';
     
      if x == 'B'
       fprintf('B');
      
      else
       fprintf('A');
      
      elseif x == 'C'
       fprintf('C')
      
      end

  - :ERROR: Correct!
    :x: Incorrect. Check the placement of the else-clause.

.. fillintheblank:: aa-indexing_03_conditionals_21
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code snippet? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
      clc; clear;
     
      x = 3;
      y = 4;
     
      if x == 2 && y == 3 || y == 4 || y == 5
       fprintf('A');
      
      elseif (x == 3) && (y == 3 || y == 4 || y == 5)
       fprintf('B');
      
      else
       fprintf('C');
      
      end

  - :A: Correct!
    :x: Incorrect. && always have preference over || in evaluating the conditions.

.. mchoice:: aa-indexing_03_conditionals_22
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: MATLAB will execute both the snippets differently as the second code snippet has indented conditions.
  :answer_b: MATLAB will execute both the snippets in the same way as indentation does not really make a difference in the way programs execute.
  :answer_c: MATLAB may execute both the programs differently since there is a nested if-else condition in the second snippet but not in the first code snippet.
  :answer_d: MATLAB will execute both the programs in the same way and output an ERROR.
  :correct: b
  :feedback_a: Incorrect. Remember, indentation makes no difference in how the programs are executed but they are helpful to us in reading and understanding the program. 
  :feedback_b: Correct! 
  :feedback_c: Incorrect. Remember, indentation makes no difference in how the programs are executed but they are helpful to us in reading and understanding the program. 
  :feedback_d: Incorrect. Remember, indentation makes no difference in how the programs are executed but they are helpful to us in reading and understanding the program. 
  
  The following are two separate code snippets. Out of the following given options, choose the correct options.

  .. code-block:: matlab
  
     x = 20;
     if mod(x,5)~=0
      fprintf('Yes');
     elseif mod(x,5) == 0
      if mod(x,4) ~= 0
        fprintf('No');
      else
        fprintf('YesYes');
      end
     else
      fprintf('NoNo');
     end
     
     x = 20;
     if mod(x,5)~=0
      fprintf('Yes');
     elseif mod(x,5) == 0
      if mod(x,4) ~= 0
        fprintf('No');
      else
        fprintf('YesYes');
      end
     else
      fprintf('NoNo');
     end