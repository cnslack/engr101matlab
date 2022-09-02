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

.. mchoice:: jh-plotting&figures_26_plotting_03
    :author: Joe Hummel
    :practice: T
    
    How would you design the function?

    - .. code-block:: matlab
  
         function PlotRainfall()
          .
          .
          .
         end
      
      - Incorrect. Take a look at how we would plot a function and try again!

    - .. code-block:: matlab
  
         function PlotRainfall(matrix)
          .
          .
          .
         end

      - Incorrect. Take a look at how we would plot a function and try again!
 
    - .. code-block:: matlab
  
         function PlotRainfall(filename)
          .
          .
          .
         end
      
      + Correct!

    - .. code-block:: matlab
  
         function PlotRainfall(filename, matrix)
          .
          .
          .
         end
      
      - Incorrect. Take a look at how we would plot a function and try again!

.. mchoice:: jh-plotting&figures_26_plotting_04
  :author: Joe Hummel
  :practice: T 
  :answer_a: 1
  :answer_b: 2
  :answer_c: 3
  :answer_d: 4
  :correct: b
  :feedback_a: Incorrect. Review vector syntax and try again!
  :feedback_b: Correct!
  :feedback_c: Incorrect. Review vector syntax and try again!
  :feedback_d: Incorrect. Review vector syntax and try again!

  How many lines would you change to generalize this code?

  .. code-block:: matlab
  
     function PlotRainfall(filename)
       matrix   = load('midway.csv');
       rainfall = matrix(1:85, 2:13);
       totals   = sum(rainfall, 2);  %% sum each row:

       x = 1929:2013;    %% plot in ascending order: 
       y = flip(totals); %% reverse to match years:

       plot(x, y);
       ylim([0 50]);  %% start Y axis at 0
     end

