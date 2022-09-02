Multiple Choice Exercises
-------------------------

These questions are **completely OPTIONAL**. We provide these exercises to give you more practice with the 
material that you've learned. Additionally, they may be a helpful resource when reviewing for assessments.

.. mchoice:: functions_in_cpp_mcq_1
    :practice: T

    What should be the return type of the function ``convertToCelsius``?

    .. code-block:: cpp

      ______ convertToCelsius (double fahrenheit) {
        double celsius;
        celsius = (fahrenheit - 32) * 5 / 9;
        return celsius;
      }

    - ``int``

      - What variable are we returning in the function, and what is the variable's type? 

    - ``double``

      + The function returns ``celsius``, which is a ``double``.

    - ``string``

      - What variable are we returning in the function, and what is the variable's type? 

    - ``void``

      - Since we are returning something in the function, the function is not ``void``.

.. mchoice:: functions_in_cpp_mcq_2
    :practice: T

    What would be returned by ``secretFunction`` if the input was 14?

    .. code-block:: cpp

      int secretFunction (int input) {
        if (input % 2 == 0) {
          return 3 * input - 2;
        }
        else {
          if (input % 7 == 0) {
            return input;
          }
          return 2 * input + 9;
        }
        return input + 4;
      }  

    - 14

      - Although 14 is divisible by 7, take another look at the conditionals. 

    - 18

      - The flow of code would never reach the last return statement.

    - 36

      - Check your order of operations! 

    - 37

      - Take a closer look at the conditional statements. 

    - 40

      + Since 14 is divisible by 2, the function returns two less than three times 14.

.. mchoice:: functions_in_cpp_mcq_3
    :practice: T

    If we wanted to create a function called ``isPrime`` that returns a ``bool`` and takes an 
    ``int input``, which of the following would be the correct function header?

    - ``boolean isPrime (int input) {``

      - In C++, use the ``bool`` keyword for a boolean. 

    - ``bool isPrime (input) {``

      - In a function header, the type of each variable must be specified in the parameter list.

    - ``bool isPrime (int input) {`` 

      + This is the correct function header for the function.

    - ``int isPrime (bool input) {``

      - Take a closer look at what the return type is.

.. mchoice:: functions_in_cpp_mcq_4
    :practice: T

    What are some benefits of using functions? Select all that are true.

    - Functions make code easier to write and comprehend.

      + You can replace repetitive code with functions.

    - Functions help encapsulate a set of steps that is repeated multiple times.

      + You can make loops simpler by using functions to do the work.

    - Functions will always return something.

      - ``void`` functions do not return anything.

    - Functions make it easier to detect and fix bugs.

      + If your code is broken down into many functions, rather than debugging the entire program, you can isolate the function that is causing issues.

.. mchoice:: functions_in_cpp_mcq_5
    :practice: T

    Suppose you have defined the following function:

    ::

        void fortuneCookie (int a, bool b, char c) {
            if (c < 'm') {
                if (a % 2 == 0) {
                    cout << "An alien of some sort will be appearing to you shortly.";
                }
                else {
                    cout << "The fortune you seek is in another cookie.";
                }
            }
            else if (c < 'r') {
                if (b) {
                    cout << "He who laughs at himself never runs out of things to laugh at.";
                }
                else {
                    cout << "You will be hungry again in one hour.";
                }
            }
            else {
                cout << "Fortune not found? Abort, retry, ignore.";
            }
        }

    What will be your fortune if you run the following code?

    ::

        fortuneCookie(22, true, 'b');

    -   ``An alien of some sort will be appearing to you shortly.``

        +   ``'b' < 'm'`` and ``22 % 2 == 0``, so this is the fortune that will print.

    -   ``The fortune you seek is in another cookie.``

        -   ``22 % 2 == 0``, so you would enter the ``if`` block, not the else.

    -   ``He who laughs at himself never runs out of things to laugh at.``

        -   ``'b'`` is less than ``'m'``, so you would enter the ``if`` block, not the ``else if``.

    -   ``You will be hungry again in one hour.``

        -   ``'b'`` is less than ``'m'``, so you would enter the ``if`` block, not the ``else if``.

    -   ``Fortune not found? Abort, retry, ignore.``

        -   ``'b'`` is less than ``'m'``, so you would enter the ``if`` block, not the ``else``.

.. mchoice:: functions_in_cpp_mcq_6
    :practice: T

    Are there any issues with the code below?

    .. code-block:: cpp

      bool isEven (int num) {
        if (num % 2 == 0) {
          return true;
        }
      }

    - Yes, we have to return either 0 or 1.

      - Returning a 0 or 1 would be returning an ``int``, even though booleans evaluate to 0 or 1.

    - Yes, we cannot pass an ``int`` into a ``bool`` function.

      - The type of variables in the parameter list do not affect the return type.

    - Yes, there is no case for odd numbers.

      + Since we never established an else clause, if the input was an odd number, the function would not return anything despite not being a void function.

    - There are no issues with the code.

      - There is an issue with the code. Can you find it?

.. mchoice:: functions_in_cpp_mcq_7
    :practice: T

    What is the value of ``x`` after the code is run?

    .. code-block:: cpp

      void twice(int num) {
        num = 2 * num;
      }

      int main() {
        int x = 4;
        twice(x);
        twice(x);
      }

    - 16

      - Although that might be what the ``twice`` function hopes to achieve, is that what the value of ``x`` is?

    - 8

      - Take a closer look at what ``twice`` does.

    - 4

      + Since ``num`` is not pass by reference, ``x`` is not actually modified.

    - 2

      - Take another look at the program.

.. mchoice:: functions_in_cpp_mcq_8
    :practice: T

    Are there any issues with the code below?

    .. code-block:: cpp

      void moonWeight (double earth) {
        double moon = 0.165 * earth;
        cout << "You would weigh " << moon << " pounds on the moon." << endl;
        return moon;
      }

    - Yes, we cannot have ``cout`` statements in a function.

      - We are allowed to use ``cout`` statements in a function.

    - Yes, we cannot return anything.

      + ``void`` functions do not have return values, so we cannot return ``moon``.

    - Yes, we need to return the output statement.

      - ``void`` functions do not have return values.

    - There are no issues with the code.

      - There is an issue with the code. Can you find it?