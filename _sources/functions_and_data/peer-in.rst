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

.. mchoice:: jh-functionsanddata_21_functions_02
  :author: Joe Hummel
  :practice: T

  Write a MaxSpeed function that takes the length of a sailboat (in feet) and returns the maximum speed of that boat (in MPH). Equation: 1.3 * sqrt(L)
  
  - .. code-block:: matlab

      function S = MaxSpeed(L)
         S = 1.3 * sqrt(L);
      end

    - Incorrect. Try running the program in Matlab and see what you get!

  - .. code-block:: matlab

      function MaxSpeed(L)
        MaxSpeed = 1.3 * sqrt(L);
      end

    + Correct!

  - .. code-block:: matlab
  
      function MaxSpeed(L, S)
        S = 1.3 * sqrt(L);
      end

    - Incorrect. Try running the program in Matlab and see what you get!

  - .. code-block:: matlab
  
      function MaxSpeed(L)
        S = 1.3 * sqrt(L);
        return S;
      end

    - Incorrect. Try running the program in Matlab and see what you get!


.. mchoice:: jh-functionsanddata_21_functions_03
  :author: Joe Hummel
  :practice: T 

  Suppose Analyze is a function that takes the name of a file containing exam scores, and returns min, max and average. How would you call the function to process exam01.txt ?
  
  .. code-block:: matlab
  
      function [Min, Max, Avg] = Analyze(filename)
        scores = load(filename);
        Min = min(scores);
        Max = max(scores);
        Avg = mean(scores);
      end


  - .. code-block:: matlab

      Analyze(‘exam01.txt’);

    - Incorrect. Try running the program in Matlab and see what you get!

  - .. code-block:: matlab

      Min = Analyze(‘exam01.txt’);
      Max = Analyze(‘exam01.txt’);
      Avg = Analyze(‘exam01.txt’);
   
    - Incorrect. Try running the program in Matlab and see what you get!
   
  - .. code-block:: matlab
  
      [Min,Max,Avg] = Analyze(‘exam01.txt’);

    + Correct!
  
  - .. code-block:: matlab
  
      [Min,Max,Avg] = Analyze(exam01.txt);
  
    - Incorrect. Try running the program in Matlab and see what you get!


.. mchoice:: jh-functionsanddata_21_functions_11
  :author: Joe Hummel
  :practice: T

  Suppose x, y, and z are vectors (1D arrays) of equal length.  Sum the corresponding elements of x and y, storing the results in z.  Which of the following do you think will work?

  .. code-block:: matlab
  
     x = [ 1.0, 2.2, 9.6, 10.2, … ];
     +
     y = [ 3.9, 1.0, 0.1, 88.6, … ];

  
  - .. code-block:: matlab

      for i=0:length(x)-1
         z(i) = x(i) + y(i);
      end
   
    + Correct!
  
  
  - .. code-block:: matlab

      for i=1:length(x)
         z(i) = x(i) + y(i);
      end

    - Incorrect. Try running the program in Matlab and see what you get!
  
  - .. code-block:: matlab
  
      z = x + y;

    - Incorrect. Try running the program in Matlab and see what you get!
  
  - .. code-block:: matlab
  
      z = sum(x, y)

    - Incorrect. Try running the program in Matlab and see what you get!

