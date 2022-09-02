.. qnum::
   :prefix: Q
   :start: 1

.. raw:: html

   <link rel="stylesheet" href="../_static/common/css/matlab.css">
   <script src="../_static/common/js/common3.js"></script>
   <script src="../_static/common/js/matcrab-exercises2.bundle.js"></script>

------------------------------------------------------
More Practice: 
------------------------------------------------------

.. mchoice:: jh-vectors&matrices_23_vectors_03
  :author: Joe Hummel
  :practice: T 

  When exercising, an equation for your “target heart rate” (THR) is THR = (220 – A ) * 0.6, where A is your age.  Example: for 20-year old, THR = 120.  We want to plot for ages 12 – 102, how would you go about this?

  - .. code-block:: matlab
  
      X = (220 – A) * 0.6;
      Y = 12:102;
      plot(X, Y);

    - Incorrect. Think about how the variables interact in the equation and how we would want to plot the function, and then try again!

  - .. code-block:: matlab
  
      X = 12:102;
      Y = (220 – A) * 0.6;
      plot(X, Y);

    - Incorrect. Think about how the variables interact in the equation and how we would want to plot the function, and then try again!

  - .. code-block:: matlab
  
      THR = (220 – A) * 0.6;
      A = 12:102;
      plot(THR, A);

    - Incorrect. Think about how the variables interact in the equation and how we would want to plot the function, and then try again!
  
  - .. code-block:: matlab
  
      A = 12:102;
      THR = (220 – A) * 0.6;
      plot(A, THR);
    
    + Correct!


.. mchoice:: jh-vectors&matrices_23_vectors_12
  :author: Joe Hummel
  :practice: T

  Exam scores are in the file 'exam01.txt'.  How would you call AnalyzeExamScores to analyze the file and output the results?

  - .. code-block:: matlab
  
      AnalyzeExamScores('exam01.txt');
      fprintf('%f, %d, %d\n', Avg, NumPassed, NumFailed);

    - Incorrect. Think about the steps necessary towards analyzing the file and outputting the results, and try again!

  - .. code-block:: matlab
  
      [avg, P, F] = AnalyzeExamScores('exam01.txt');
      fprintf('%f, %d, %d\n', avg, P, F);

    - Incorrect. Think about the steps necessary towards analyzing the file and outputting the results, and try again!

  - .. code-block:: matlab
  
      scores = load('exam01.txt');
      AnalyzeExamScores(scores);
      fprintf('%f, %d, %d\n', Avg, NumPassed, NumFailed);

    - Incorrect. Think about the steps necessary towards analyzing the file and outputting the results, and try again!

  - .. code-block:: matlab
  
      scores = load('exam01.txt');
      [avg, P, F] = AnalyzeExamScores(scores);
      fprintf('%f, %d, %d\n', avg, P, F);

    + Correct.

.. mchoice:: jh-vectors&matrices_24_matrices_03
  :author: Joe Hummel
  :practice: T
  :answer_a: You cannot compare vectors with < or >
  :answer_b: All values must < or > for condition to be true
  :answer_c: No idea, but based on error message => all if conditions were false --- try a different approach?
  :correct: b
  :feedback_a: Incorrect. Review vector syntax and try again!
  :feedback_b: Correct!
  :feedback_c: Incorrect. Review vector syntax and try again!

  The following code is just trying to set the Trend variable (a good way to start).  But MATLAB gives an error message that “Trend” is never assigned a value.  Why not?

  .. code-block:: matlab
  
     function [Trend, Percentage, MaxChange, Patient] = AnalyzeHRs(file1, file2)
     before = load(file1);
     after  = load(file2);

       if after < before
         Trend = '-';
       end

       if after > before
         Trend = '+';
       end

       if after == before
         Trend = '-';
       end
      
     end

.. mchoice:: jh-vectors&matrices_24_matrices_05
  :author: Joe Hummel
  :practice: T
  :answer_a: Print debugging with disp(var)
  :answer_b: Print debugging with fprintf(…)
  :answer_c: Print debugging by removing “;”
  :answer_d: Work interactively with your code
  :answer_e: All of the above
  :correct: e
  :feedback_a: Incorrect. When things aren’t working, take advantage of what MATLAB has to offer--disp(var) can display contents of any variable, drop the “;” to see what is being computed, and work interactively *before* trying to write functions! 
  :feedback_b: Incorrect. When things aren’t working, take advantage of what MATLAB has to offer--disp(var) can display contents of any variable, drop the “;” to see what is being computed, and work interactively *before* trying to write functions!
  :feedback_c: Incorrect. When things aren’t working, take advantage of what MATLAB has to offer--disp(var) can display contents of any variable, drop the “;” to see what is being computed, and work interactively *before* trying to write functions!
  :feedback_d: Incorrect. When things aren’t working, take advantage of what MATLAB has to offer--disp(var) can display contents of any variable, drop the “;” to see what is being computed, and work interactively *before* trying to write functions!
  :feedback_e: Correct!

  I had a similar solution but it didn’t work…  What could I have done to find the error and fix it?

  .. code-block:: matlab
  
     function [Trend, Percentage, MaxChange, Patient] = AnalyzeHRs(file1, file2)
       before = load(file1);
       after  = load(file2);
       .
       .
       .
     end

.. mchoice:: jh-vectors&matrices_24_matrices_09
  :author: Joe Hummel
  :practice: T
  :answer_a: sum(M)
  :answer_b: V = sum(M, 2); sum(V, 2)
  :answer_c: sum(sum(M))
  :answer_d: V = sum(M, 2); sum(V, 1)
  :correct: d
  :feedback_a: Incorrect. Try running the code again in Matlab and see what you get!
  :feedback_b: Incorrect. Try running the code again in Matlab and see what you get!
  :feedback_c: Incorrect. Try running the code again in Matlab and see what you get!
  :feedback_d: Correct!

  Suppose M=[100 80 62; 59 62 78; 78 88 0; 82 98 0] is a matrix. How do you sum the entire contents of the matrix (i.e. output = 787)?

.. mchoice:: jh-vectors&matrices_24_matrices_10
  :author: Joe Hummel
  :practice: T
  :answer_a: [3]
  :answer_b: [0 0 0; 1 0 0; 0 0 1; 0 0 1]
  :answer_c: [59 0 0]
  :answer_d: [1 1 1; 0 1 1; 1 1 0; 1 1 0]
  :correct: b
  :feedback_a: Incorrect. Try running the code again in Matlab and see what you get!
  :feedback_b: Correct!
  :feedback_c: Incorrect. Try running the code again in Matlab and see what you get!
  :feedback_d: Incorrect. Try running the code again in Matlab and see what you get!

  We create the following matrix and do a search.  What do you think MATLAB assigns to LI?

  .. code-block:: matlab
  
     M = [ [100,80,62]; [59,62,78]; [78,88,0]; [82,98,0] ];
     LI = M < 60;

.. mchoice:: jh-vectors&matrices_27_matrices_03
  :author: Joe Hummel
  :practice: T
  :answer_a: Row vector of 0’s and 1’s
  :answer_b: Column vector of 0’s and 1’s
  :answer_c: Matrix of 0’s and 1’s
  :answer_d: Single number denoting # of positive values in column 1
  :correct: b
  :feedback_a: Incorrect. Try running the code again in Matlab and see what you get!
  :feedback_b: Correct!
  :feedback_c: Incorrect. Try running the code again in Matlab and see what you get!
  :feedback_d: Incorrect. Try running the code again in Matlab and see what you get!

  M is a matrix.  The following builds a logical index from column 1, indicating positive values. What is R?

  .. code-block:: matlab
  
     M = [ [100,80,-9]; [-2,62,178]; [77,0,0]; [0,98,120] ];
     R = (M(:, 1) > 0);

.. mchoice:: jh-vectors&matrices_27_matrices_04
  :author: Joe Hummel
  :practice: T

  M is a matrix.  Extract all values from column 3 that are in the range 100..212, inclusive.  Assign to a vector V.

  - .. code-block:: matlab
  
      M = [ [100,80,-9]; [-2,62,178]; [77,0,0]; [0,98,120] ];
      LI = (100<=M(:,3) & M(:,3)<=212);
      V  = M(LI, 3);
    
    + Correct!

  - .. code-block:: matlab
  
      M = [ [100,80,-9]; [-2,62,178]; [77,0,0]; [0,98,120] ];
      LI = (100<=M(:,3) & M(:,3)<=212);
      V  = M(LI);

    - Incorrect. Try running the code again in Matlab and see what you get!

  - .. code-block:: matlab
  
      M = [ [100,80,-9]; [-2,62,178]; [77,0,0]; [0,98,120] ];
      LI = (100<=M(:,3) | M(:,3)<=212);
      V  = M(LI, 3);

    - Incorrect. Try running the code again in Matlab and see what you get!

  - .. code-block:: matlab
  
      M = [ [100,80,-9]; [-2,62,178]; [77,0,0]; [0,98,120] ];
      LI = (100<=M(:,3) | M(:,3)<=212);
      V  = M(LI);
      
    - Incorrect. Try running the code again in Matlab and see what you get!

.. fillintheblank:: aa-vectors&matrices_08_vectors_01
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
     clc; clear;
     
     vec = [67 21 33 78 39 47 19];
     
     newvec = [vec(2)  vec(1,3)  vec([1, 3])  vec([1 3])];
     
     fprintf('%d ', newvec);

  - :21 33 67 33 67 33: Correct!
    :x: Incorrect. Remember that vec(1,3) means value at row 1 and column 3. Now vec([1,3]) and vec([1 3]) are the same (because in a vector [ ], comma and space both separate a number) and they both refer to values at vec(1) and vec(3).

.. mchoice:: aa-vectors&matrices_08_vectors_02
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: vec(4) = 55;
  :answer_b: vec = [vec(1:3) 55 vec(4:5)];
  :answer_c: vec = [vec(1:4) 55 vec(4:6)];
  :answer_d: vec = [55 vec(1:3) vec(4:6)];
  :correct: b
  :feedback_a: Incorrect. Check out the syntax for vector growing.
  :feedback_b: Correct!
  :feedback_c: Incorrect. Check out the syntax for vector growing.
  :feedback_d: Incorrect. Check out the syntax for vector growing.
  
  Which of the following options represents a correct way to insert number 55 after the first 3 positions in the following vector?

  .. code-block:: matlab
  
     vec = [22 33 44 66 77];

.. fillintheblank:: aa-vectors&matrices_08_vectors_03
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
     clc; clear;
     
     vec = [23 45 67 89 108];
     
     pos = find( max(vec) );
     
     disp( vec(pos) );

  - :23: Correct!
    :x: Incorrect. Remember that find() always need a condition like find(vec == max(vec)) to return positions. If you just have find( max(vec) ), this means find( 108 ) here, which does not tell anything about where the find command is looking for the number 108, thus it will return 1.

.. fillintheblank:: aa-vectors&matrices_08_vectors_04
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
     clc; clear;
     
     vec = [23 89 67 89 108 12];
     
     pos = find( vec  == max(vec), 3);
     
     disp( vec(pos) );

  - :108: Correct!
    :x: Incorrect. Remember that find( condition , n ) indicates that at max it will return ‘n’ number of positions that satisfy the condition of the find() command. Here, since there is only one maximum value, it will just return one position for that.

.. fillintheblank:: aa-vectors&matrices_08_vectors_05
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
     clc; clear;
     
     vec = [33 109 55 109 109 108 109];
     
     pos = find( vec  == max(vec));
     
     disp( vec(pos) + length(pos) );

  - :113 113 113 113: Correct!
    :x: Incorrect. Here vec(pos) will give you the values whereas length(pos) will return the length of pos vector.

.. mchoice:: aa-vectors&matrices_08_vectors_06
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: find( vec == 109 ) = [];
  :answer_b: vec( find(109) ) = [];
  :answer_c: vec( find(vec == 109, 3) ) =[];
  :answer_d: vec( find(vec == 109), 3 ) =[];
  :answer_e: vec( find(vec == 109) ) = [];
  :correct: c
  :feedback_a: Incorrect. Remember that find( condition , n ) indicates that at max it will return first  ‘n’ number of positions that satisfy the condition of the find() command. Here, since we need to delete the first 3 duplicates, we will use 3 in the find() command.
  :feedback_b: Incorrect. Remember that find( condition , n ) indicates that at max it will return first  ‘n’ number of positions that satisfy the condition of the find() command. Here, since we need to delete the first 3 duplicates, we will use 3 in the find() command.
  :feedback_c: Correct!
  :feedback_d: Incorrect. Remember that find( condition , n ) indicates that at max it will return first  ‘n’ number of positions that satisfy the condition of the find() command. Here, since we need to delete the first 3 duplicates, we will use 3 in the find() command.
  :feedback_e: Incorrect. Remember that find( condition , n ) indicates that at max it will return first  ‘n’ number of positions that satisfy the condition of the find() command. Here, since we need to delete the first 3 duplicates, we will use 3 in the find() command.
  
   Which of the following commands will delete all the duplicates of 109 in the following vector except the last one such that the output is [33 55 108 109].

  .. code-block:: matlab
  
     vec = [33 109 55 109 109 108 109];

.. fillintheblank:: aa-vectors&matrices_08_vectors_07
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
     vec = [33 109 55 109 109 108 109];
     
     pos = find(vec == 109);
      
     vec( pos(2:end) ) = [];
     
     disp( vec );

  - :33 109 55 108: Correct!
    :x: Incorrect. Remember, here vec( pos(2:end) ) will ignore the first value in pos vector and only delete for the remaining one.

.. fillintheblank:: aa-vectors&matrices_08_vectors_08
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
     clc; clear;
     
     vec = [33 109 55 109 109 108 109];
     
     pos = find(vec == 108);
     
     vec = [ vec(1:2)  vec(1,2)  vec(pos)  pos ];
     
     disp( vec );

  - :33 109 109 108 6: Correct!
    :x: Incorrect. Check again and try to properly access every value in line 4.

.. fillintheblank:: aa-vectors&matrices_08_vectors_09
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
     clc; clear;
     
     vec = [33 109 55 109 109 108 109];
     
     pos = find(vec == 108);
     
     vec = [ vec(1:2)  vec(2,1)  vec(pos)  pos ];
     
     disp( vec );

  - :ERROR: Correct!
    :x: Incorrect. What will be the value of vec(2,1) here? Think again!

.. fillintheblank:: aa-vectors&matrices_08_vectors_10
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
     clc; clear;
     
     vec = [33 44 55 66];
     
     vec(2) = vec(3);
     
     vec(3) = vec(2);
     
     disp( vec );

  - :33 55 55 66: Correct!
    :x: Incorrect. Execute the lines one by one and see how vec evolves!

.. fillintheblank:: aa-vectors&matrices_08_vectors_11
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
     clc; clear;
     
     vec = [33 44 55 66];
     
     newvec = [vec(1:3) 11];
     
     vec = [22 newvec(2:end)];
     
     disp( vec );

  - :22 44 55 11: Correct!
    :x: Incorrect. Execute the lines one by one and see how vec evolves!

.. fillintheblank:: aa-vectors&matrices_08_vectors_12
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
     clc; clear;
     
     vec = [ 11 22 33 44 55 55 22 33 11];
     
     pos = find( vec == min(vec(2:4)) );
     
     disp( pos );

  - :2 7: Correct!
    :x: Incorrect. Here the find() command will look for the maximum value of vec from 2 to 4 positions in the entire vector.

.. fillintheblank:: aa-vectors&matrices_08_vectors_13
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
     clc; clear;
     
     vec = [ 11 22 33 44 55 55 22 33 11];
     
     pos = find( vec(4:7) == max(vec) );
     
     disp( pos );

  - :2 3: Correct!
    :x: Incorrect. Here the find() command will look for the maximum value of vec which is 55 in vec(4:7) which is [44 55 55 22]. Here vec(4:7) only has 4 positions so find will return the positions according to vec(4:7) and not vec.

.. fillintheblank:: aa-vectors&matrices_08_vectors_14
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
     clc; clear;
     
     vec = [ 11 22 33 44 55 55 22 33 11];
     
     pos = find( vec(1:5) > 22 );
     
     disp( sum(pos) );

  - :12: Correct!
    :x: Incorrect. Check which positions from 1 to 5 in vec are greater than 22 and then add those position numbers.

.. fillintheblank:: aa-vectors&matrices_08_vectors_15
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
     clc; clear;
     
     vec = [ 11 22 33 44 55 55 22 33 11];
     
     pos = find( vec(5:end) > 22 );
     
     disp( sum(pos) );

  - :7: Correct!
    :x: Incorrect. Here since your referencing to vec(5:end) which is [55 55 22 33 11], the positions will be determined by this vec(5:end) and not the original vec.

.. fillintheblank:: aa-vectors&matrices_08_vectors_16
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
     clc; clear;
     
     vec = [33 44 55 66];
     
     temp = vec(2);
     
     vec(2) = vec(3);
     
     vec(3) = temp;
     
     disp( vec );

  - :33 55 44 66: Correct!
    :x: Incorrect. Execute the lines one by one and see how vec evolves!

.. mchoice:: aa-vectors&matrices_08_vectors_17
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: find(vec > 50);
  :answer_b: length( find(vec > 50) ); 
  :answer_c: sum( find(vec> 50) );
  :answer_d: vec( find(vec > 50) );
  :correct: b
  :feedback_a: Incorrect. Check these commands one by one in MATLAB and carefully observe what do you get. Then find out which one is the correct response.
  :feedback_b: Correct!
  :feedback_c: Incorrect. Check these commands one by one in MATLAB and carefully observe what do you get. Then find out which one is the correct response.
  :feedback_d: Incorrect. Check these commands one by one in MATLAB and carefully observe what do you get. Then find out which one is the correct response.
  
   Which of the following commands will return the count of total number of values which are greater than 50 in the following vector:

  .. code-block:: matlab
  
     vec = [ 51 22 21 33 88 991 6 ];

.. fillintheblank:: aa-vectors&matrices_08_vectors_18
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
     clc; clear;

     vec = [33 66];

     vec(5) = 11;

     disp(vec);

  - :33 66 0 0 11: Correct!
    :x: Incorrect. When you assign a number to a position in a vector, then MATLAB puts that number in that position with 0s in positions which are not defined.

.. mchoice:: aa-vectors&matrices_08_vectors_19/20
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: vec( find( vec == max( vec(end-3:end) ) ) ) = [];
  :answer_b: find(vec == max(vec(end-3:end)) ) = [];
  :answer_c: vec( find( vec(end-3:end) == max(vec) ) )= [];
  :answer_d: vec( find(vec == max(vec), 4) ) = [];
  :correct: a
  :feedback_a: Correct!
  :feedback_b: Incorrect. Check these commands carefully and expand them to find out what do they actually refer to.
  :feedback_c: Incorrect. Check these commands carefully and expand them to find out what do they actually refer to.
  :feedback_d: Incorrect. Check these commands carefully and expand them to find out what do they actually refer to.
  
   Which of the following options represents the correct syntax of deleting the maximum value out of the only last 4 values in the following vector:

  .. code-block:: matlab
  
     vec  = [38 63 213 62 32 11 99 44];

.. fillintheblank:: aa-vectors&matrices_12_matrices_01
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
     clc; clear;

     word = 'keyboard';

     temp = word(2);

     word( length(word) - 1) = temp;

     word(2) = word( length(word) - 1 );

     fprintf( '%s', word );

  - :keyboaed: Correct!
    :x: Incorrect. Check it again and execute the lines one by one.

.. fillintheblank:: aa-vectors&matrices_12_matrices_02
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
     clc; clear;

     word = 'program';

     word( [1 6] ) = word( [6 1] );

     fprintf( '%s', word );

  - :arogrpm: Correct!
    :x: Incorrect. Check it again and execute the lines one by one.

.. fillintheblank:: aa-vectors&matrices_12_matrices_03
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
     clc; clear;
     
     word = 'program';
     
     word( [1 3 5] ) = word( [5 3 1] );
     
     fprintf( '%s', word );

  - :rrogpam: Correct!
    :x: Incorrect. Check it again and execute the lines one by one.

.. fillintheblank:: aa-vectors&matrices_12_matrices_04
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
     clc; clear;
     
     word = 'program';
     
     word( [1 3 5] ) = word( [7 3 3] );

     fprintf( '%s', word );

  - :mrogoam: Correct!
    :x: Incorrect. Check it again and execute the lines one by one.

.. fillintheblank:: aa-vectors&matrices_12_matrices_05
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
     clc; clear;

     word = 'waffles';

     word(1:2:5) = word(5:-2:1);

     fprintf( '%s', word );

  - :laffwes: Correct!
    :x: Incorrect. Check it again and execute the lines one by one.
     
.. fillintheblank:: aa-vectors&matrices_12_matrices_06
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
     clc; clear

     word = 'aiaas';

     jj = length(word);

     for ii = 1:2:length(word)
       word(jj) = word(ii);
        word(ii) = word(jj);
       jj = jj - 2;
     end
     disp(word)

  - :aiaaa: Correct!
    :x: Incorrect. Check it again and execute the lines one by one.

.. mchoice:: aa-vectors&matrices_12_matrices_07
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: kryboard
  :answer_b: kryboaed
  :answer_c: keyboaed
  :answer_d: keyboard
  :correct: b
  :feedback_a: Incorrect. Check it again and execute the lines one by one.
  :feedback_b: Correct!
  :feedback_c: Incorrect. Check it again and execute the lines one by one.
  :feedback_d: Incorrect. Check it again and execute the lines one by one.
  
   Which of the following options is the output of the following code snippet?

  .. code-block:: matlab
  
     clc; clear;
     
     word = 'keyboard';
     
     temp = word(2);
     
     word(2) = word( length(word) - 1 );
     
     word( length(word) - 1) = temp;
     
     disp(word)

.. mchoice:: aa-vectors&matrices_12_matrices_08
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: a & z
  :answer_b: y & z
  :answer_c: b & y
  :answer_d: a & b
  :correct: d
  :feedback_a: Incorrect. Recall the concept of ciphers in the class and see what we need to be careful of when we are adding or subtracting values from letters.
  :feedback_b: Incorrect. Recall the concept of ciphers in the class and see what we need to be careful of when we are adding or subtracting values from letters.
  :feedback_c: Incorrect. Recall the concept of ciphers in the class and see what we need to be careful of when we are adding or subtracting values from letters.
  :feedback_d: Correct!
  
   The following program shifts any given letter by subtracting 2 to decrypt it into another letter from 'a' to 'z'. This program will work for all the lowercase letters given by the user except ___________?

  .. code-block:: matlab
  
     clc; clear;
     
     word = input('Enter a single letter in lowercase: ' , 's')
     
     word = word - 2;
     
     fprintf( '%s', word );

.. mchoice:: aa-vectors&matrices_12_matrices_09
    :author: Ashish Aggarwal
    :practice: T 

    The following program shifts any given letter by adding 5 to encrypt it into another letter from 'a' to 'z'. Which code snippet from the following options is required to be added to the program in order to make it work for all the letters?

        .. code-block:: matlab
  
         clc; clear;
     
         word = input('Enter a single letter in lowercase: ' , 's')
     
         word = word + 5;
     
         fprintf( '%s', word );

  
    - .. code-block:: matlab
        
           if word < 'a'
             word = word + 5;
           end

      - Incorrect. Recall the concept of ciphers in the class and see what we need to be careful of when we are adding or subtracting values from letters.

    - .. code-block:: matlab

           if word < 'a'
             word = word + 26;
           end

      - Incorrect. Recall the concept of ciphers in the class and see what we need to be careful of when we are adding or subtracting values from letters.

    - .. code-block:: matlab

           if word > 'z'
             word = word + 26;
           end

      - Incorrect. Recall the concept of ciphers in the class and see what we need to be careful of when we are adding or subtracting values from letters.

    - .. code-block:: matlab

           if word > 'z'
             word = word - 26;
           end

      + Correct!

.. fillintheblank:: aa-vectors&matrices_12_matrices_10
   :author: Ashish Aggarwal
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
      clc; clear;

      vec = [97 98 99 100];

      fprintf('%s', vec + 3);

  - :defg: Correct!
    :x: Incorrect. Check it again and execute the lines one by one.

.. fillintheblank:: aa-vectors&matrices_12_matrices_11
   :author: Ashish Aggarwal
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
      clc; clear;
     
      vec = [11 12 22 14 23 12 11];
     
      vec = length( find( vec(2:1:end-1) < 15 ) );
     
      disp(vec);

  - :3: Correct!
    :x: Incorrect. Check the find command again, it uses only a certain segment of vec.

.. fillintheblank:: aa-vectors&matrices_12_matrices_12
   :author: Ashish Aggarwal
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
     clc; clear;
     
     x = zeros(1, 2);
     
     x(3) = 4;
     
     jj = 4;
     
     for ii = 1:1:2
      if mod(ii,2) == 1
         x = cat(2,7,x);
      end
     end
     disp(x(4))

  - :4: Correct!
    :x: Incorrect. Execute the program step by step and make sure you do the correct concatenation.

.. fillintheblank:: aa-vectors&matrices_12_matrices_13
   :author: Ashish Aggarwal
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
     clc; clear;
     word = 'program';
     word(1:3) = word(end:-4:1);
     fprintf('%s', word);

  - :ERROR: Correct!
    :x: Incorrect. Execute the program step by step and look at the number of elements on both sides.

.. fillintheblank:: aa-vectors&matrices_12_matrices_14
   :author: Ashish Aggarwal
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
     clc; clear;
     mat = cat(2, cat(1, [11 33 55],  [88]), [22 44]);
     mat(1,2) = mat(2,3);
     disp(mat(1,2) + mat(2));

  - :ERROR: Correct!
    :x: Incorrect. Check the dimensions of the array and unpack the commands one by one.

.. fillintheblank:: aa-vectors&matrices_12_matrices_15
   :author: Ashish Aggarwal
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
     clc; clear;
     mat = cat(2, [33; 44], cat(1, [12 32], [59 23]));
     mat(1,2) = mat(2,3);
     disp(mat(1,2) + mat(2));

  - :67: Correct!
    :x: Incorrect. Unpack the cat commands one by one.

.. fillintheblank:: aa-vectors&matrices_12_matrices_16
   :author: Ashish Aggarwal
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
     clc; clear;
     mat = cat(2, zeros(2,2), zeros(2,2));
     mat(1,3) = 5;
     mat(2, 1) = mat(1, 3);
     disp(mat(1,3) + mat(2));

  - :10: Correct!
    :x: Incorrect. Check the program again.

.. fillintheblank:: aa-vectors&matrices_12_matrices_17
   :author: Ashish Aggarwal
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
     clc; clear;
     mat = cat(2, zeros(2,2), zeros(2,3));
     mat(3,2) = 51;
     mat(4) = 6;
     mat(2,3) = mat(2,2);
     disp( mat(6) );

  - :51: Correct!
    :x: Incorrect. Check the program again. Remember if we assign a value at a particular position, then MATLAB puts that value there.

.. fillintheblank:: aa-vectors&matrices_12_matrices_18
   :author: Ashish Aggarwal
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
     clc; clear;
     mat = cat(2, zeros(2,2), zeros(2,2));
     mat(5) = 78;
     mat(3,1) = 87;
     mat(5) = mat(1,5) + mat(5);
     disp( mat(3) );

  - :ERROR: Correct!
    :x: Incorrect. Check the program again. Remember if we assign a value at a particular position, then MATLAB puts that value there.

.. fillintheblank:: aa-vectors&matrices_12_matrices_19
   :author: Ashish Aggarwal
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
     clc; clear;
     vec = [11 12 22 14 23 12 11];
     vec = length( find( vec(3:1:10) < 15 ) );
     disp(vec);

  - :ERROR: Correct!
    :x: Incorrect. Check the dimensions of vec(3:1:10).

.. fillintheblank:: aa-vectors&matrices_12_matrices_20
   :author: Ashish Aggarwal
   :casei:

   What will be the output of the following code? (If the program will result in an error, put down ‘ERROR’)

    .. code-block:: matlab
  
     clc; clear;
     vec = [11 12 22 14 23 44 11];
     vec = sum( find( vec(end:-1:end-3) < 15 ) );
     disp(vec);

  - :5: Correct!
    :x: Incorrect. Here, since only a segment of vec is considered, the numbering of position will be done according to vec(end:-1:end-3) and not the original vec.