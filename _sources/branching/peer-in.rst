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

.. mchoice:: jh-branching_04_runtimeerror_04
    :author: Joe Hummel
    :practice: T
  
    We want to prevent the runtime error, and instead output “cannot divide”. Which is correct?

    - .. code-block:: cpp
     
         int main() 
         { 
           int  x, y, z; 
           cin >> x; 
           cin >> y; 
           z = x / y; 
         
           if (y == 0) 
           { 
           cout << "cannot divide"; 
           } 
           else 
           { 
            cout << z << endl; 
           } 
           return 0; 
         } 

      + This code is correct.

    - .. code-block:: cpp
       
         int main()
         {
            int  x, y, z;
            
            if (y == 0)
            {
              cout << "cannot divide";
            }
            else
            { 
              cin >> x;
              cin >> y;
              
              z = x / y;
              
              cout << z << endl;
            }
            return 0;
         }

      - Incorrect. Review the steps one at a time and try again!


    - .. code-block:: cpp
  
         int main()
         {
            int  x, y, z;
        
            cin >> x;
            cin >> y;
        
            if (y == 0)
            {
              cout << "cannot divide";
            }
            else
            { 
              z = x / y;
              cout << z << endl;
            }
            return 0;
         }

      - Incorrect. Review the steps one at a time and try again!


.. mchoice:: jh-branching_04_sequences_09
  :author: Joe Hummel
  :practice: T
  :answer_a: grow in size to handle more and more digits past the decimal point
  :answer_b: compress the digits into the same memory space in order to store more and more digits
  :answer_c: store an exact value when possible, otherwise store an approximate value
  :answer_d: always stores the exact value because computers support "infiniteness"
  :correct: c
  :feedback_a: Incorrect. Computers have limitations and are not be able to hold infinite memory.
  :feedback_b: Incorrect. Computers have limitations and are not be able to hold infinite memory.
  :feedback_c: Correct! 
  :feedback_d: Incorrect. Computers have limitations and are not be able to hold infinite memory.

  Since there are an infinite number of real numbers, this implies that variables of type double…