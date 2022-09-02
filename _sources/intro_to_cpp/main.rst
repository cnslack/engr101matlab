.. qnum::
   :prefix: Q
   :start: 1

.. raw:: html

   <link rel="stylesheet" href="../_static/common/css/theme-overrides.css">

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

===================
Introduction to C++
===================


^^^^^^^^^^
Motivation
^^^^^^^^^^
.. section 1


You might be wondering why we use two different programming languages in Engr 101. "We just started to do some really interesting things in MATLAB… why are we switching to something else??" There are many reasons why we switch languages, but one of the most important reasons is that **different programming languages have different strengths**. A programming language is a tool to solve problems using computing, and it's good to have a lot of different tools to pick from when you are solving a problem.

Here are some strengths of MATLAB:

* **Analyzing and presenting data**. There are many MATLAB toolboxes that have been created to help solve engineering problems and perform scientific computing.
* **Rapid prototyping**. With MATLAB, you can quickly try out a bunch of ideas to analyze data or perform computations. The interactive nature of the command window, coupled with breakpoints in functions, allows you to easily trace through your ideas, pause and check on results mid-computation, and determine if this is how you want to solve this problem. MATLAB can help you quickly rule out ways that won't work, which will save you time later on, whether the final version of your program is in MATLAB or in some other language.

However, MATLAB is not so good at other things… remember how awkward dealing with strings was?

C++, on the other hand, does not have the built-in support for vectors and matrices that MATLAB has, but it has other strengths:

* C++ is better for writing **larger, more complex programs**.
* C++ handles **control flow** (branching and iteration) very well, so if your problem requires its computing solution to make a lot of decisions, then C++ might be a better tool to use than a program like MATLAB.

C++ is a well-established and widely-used programming language. Learning C++ will help you to learn more about the way computers work as an engineering tool, and you will learn more about how computer programs really work!

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
C++, Machine Code, and Compilers
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. section 2

Here's a classic program in C++. When you run it, it prints out the message "Hello World!".

.. code-block:: cpp

   #include <iostream>
   using namespace std;

   int main() {
     cout << "Hello World!" << endl;
   }

|

We'll get to the details of how this program works in a bit, but first, we've got a bit of an issue. Your computer can't run C++ code! It only runs a particular dialect of **machine code**, depending on what kind of computer you have. We need some way to translate our **source code**, written in C++, into machine code so that our computer can actually run it. For this, we use a **compiler**...

.. youtube:: IFeUJ15djBo
   :divid: ch11_02_vid_compilers
   :height: 315
   :width: 560
   :align: center

.. admonition:: Video Recap

   MATLAB is an **interpreted** language. MATLAB processes your code *line-by-line*. C++ is a **compiled** language. It uses a **compiler** to translate a **source code** file into an **executable** file (e.g., **machine code**).

.. dragndrop:: ch11_02_ex_compiling
  :match_1: Compile|||Translate a source code file into an executable file (i.e. machine code).
  :match_2: Run|||Take an executable program file and actually run it on the computer.
  :match_3: Source Code|||Program code that someone might actually write to solve a problem.
  :match_4: Machine Code|||Code that can be exectued directly on a computer, but that is not generally human-friendly.
  :match_5: Interpreter|||A program that acts as an intermediary to run source code line-by-line (e.g. MATLAB).

  Match each term with its definition.

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Writing Up The Hello World Program
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. section 3

We recommend using an editor called VS Code to write your C++ source files and a compiler called :code:`g++` to compile your code from your computer **terminal**. Don't worry if you're not sure how to get started or how to use the terminal (or what it even is!). We'll provide some tutorials to get you set up with these!

For now, here's a quick walkthrough of the development process:

.. youtube:: T5IhvQJsPps
   :divid: ch11_03_vid_cpp_first_program
   :height: 315
   :width: 560
   :align: center

.. admonition:: Video Recap

   A key difference in C++ development (vs. MATLAB) is the extra compilation step each time you would like to run your code. Here's a recap of the command you use to compile. (The :code:`g++` command is typed at your computer terminal - again, don't worry, we'll provide tutorials to help you get started working from the terminal.)

   .. figure:: img/cpp1.png
      :width: 500
      :align: center

      ..

      
   .. figure:: img/cpp2.png
      :width: 500
      :align: center

      ..

^^^^^^^^^^^^^^^^^^^^
C++ Syntax and Types
^^^^^^^^^^^^^^^^^^^^
.. section 5

Let's look at some of the basic rules for C++, including syntax, variables, and expressions. We'll also see a few key differences from MATLAB, including the way *data types* play a more pronounced role in C++:

.. youtube:: lLG5wqwLNT0
   :divid: ch11_05_vid_cpp_variables_and_types
   :height: 315
   :width: 560
   :align: center

.. admonition:: Video Recap

   Like in MATLAB, our programs are built of **statements** of code, but in C++, all statements must end with a semi-colon.

   When you first use a variable in C++, you must **declare** it by telling the compiler its name, its type, and (optionally) an initializer expression. Some common data types are ints, doubles, bools, chars, and strings. When you declare a variable, the variable takes up space in memory - different types of variables take up different amounts of space. If you don't initialize a variable, then the value of the variable is based on whatever memory junk was in that memory location previously.

   We also have **expressions** in C++ that perform computations on variables and other data.

   Single-line comments use :code:`//` and block comments use :code:`/*` and :code:`*/`.

-------
Lobster
-------

.. raw:: html

  <div class="container-fluid">
   <table><tbody>
      <tr>
         <td style="width:175px; text-align: center">
            <img src="../_static/common/img/happylobster.jpg" style="width: 150px" />
         </td>
         <td>
            For C++, we'll use a web-based program visualization tool called "Lobster". Lobster allows you to write and run C++ code in your web browser, including for your Runestone exercises in this and future chapters. Once you've written the code, you can click the "Simulate" button, and Lobster will show you line-by-line what is going on so that you can get a better feel for what your code actually does. Lobster can also track checkpoints as you work through exercsies and analyze your code to help you spot common bugs.
         </td>
      </tr>
   </tbody></table>
  </div>

|

Let's take a closer look at the interface for Lobster and how you can use it to step through your code line-by-line.

.. youtube:: bvKhl8iPc7I
   :divid: ch12_01_vid_lobster
   :height: 315
   :width: 560
   :align: center

.. admonition:: Video Recap

   We walked through the Lobster interface in this video. Lobster has two main tabs - the Source Code tab, where you can write your code, and the Simulation tab, where you can step through your code line-by-line.

Here's the Lobster example we just went through in the video. You don't have to do anything with it, but you're welcome to play around with it if you like.

.. raw:: html

   <div class="lobster-ex" style="width: 600px; margin-left: auto; margin-right: auto">
      <div class="lobster-ex-project-name">ch12_01_ex</div>
   </div>

-------------------------------
Exercise: Variable Declarations
-------------------------------

For this exercise, add some lines of code so that these five variables are declared and initialized:

1. :code:`numPieces` -- an integer representing the number of pieces of candy you have (5)
2. :code:`cost` -- a double representing the cost per piece of candy (3.25)
3. :code:`name` -- a string representing the name of the candy ("peeps")
4. :code:`category` -- a character representing the category of the candy ('K')
5. :code:`isGood` -- a boolean representing whether the candy tastes good (false)

.. raw:: html

   <div class="lobster-ex" style="width: 600px; margin-left: auto; margin-right: auto">
      <div class="lobster-ex-project-name">ch11_01_ex</div>
      <div class="lobster-ex-complete-message">
         Well done! The secret word is "electricity".
      </div>
   </div>

.. fillintheblank:: ch11_01_ex_variableDeclarations
  :casei:

  Complete the Lobster exercise to reveal the *secret word*. Enter it here.
  
  |blank|

  - :electricity: Correct.
    :x: Incorrect. If you finished the exercise, please double check your spelling.


^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
User Input/Output (:code:`cin` and :code:`cout`)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. section 6

We've seen that the terminal can be used to compile and run programs. It can also be used to interact with a program while it's running.

.. youtube:: BkWAf-G0d_U
   :divid: ch11_06_vid_cin_and_cout
   :height: 315
   :width: 560
   :align: center

.. admonition:: Video Recap

   :code:`cout` can be used to print a message to the terminal (e.g. "Hello World!"). :code:`cin` can be used to pause a program and wait for input from the user. To send the input, the user just types something and hits the <enter> key.

------------------------------------
Exercise: User Input via :code:`cin`
------------------------------------

Let's write a program that asks the user about their favorite candy. Below is an example of interacting with the program for someone who likes peeps. The :code:`$` symbol indicates the "prompt" at the terminal - the lines with :code:`$` are wherever you would have typed something and hit <enter>. This includes compiling with :code:`g++`, running the program with :code:`./candy`, *and* typing input whenever the program paused on a :code:`cin` line.

.. code-block::

   $ g++ candy.cpp -o candy
   $ ./candy
   What is your favorite candy?
   $ peeps
   How many would you buy right now?
   $ 5
   How much does each piece cost?
   $ 3.25
   5 peeps will cost you 16.25

.. parsonsprob:: ch11_06_ex_cin_and_cout

   Arrange the lines of code below to write the program. Make sure to place the blocks at the right indentation levels!

   -----
   #include &lt;iostream&gt;
   =====
   using namespace std;
   =====
   int main()
   =====
   {
   =====
     cout << "What is your favorite candy?" << endl;
   =====
     string name;
     cin >> name;
   =====
     cout << "How many would you buy right now?" << endl;
   =====
     int numPieces;
     cin >> numPieces;
   =====
     cout << "How much does each piece cost?" << endl;
   =====
     double cost;
     cin >> cost;
   =====
     cout << numPieces << " " << name;
     cout << " will cost you " << numPieces * cost << endl;
   =====
   }
   =====

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Compile Errors and Runtime Errors
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. section 7

When the compiler translates your program to machine code, it also acts as a proofreader and can catch many errors at **compile-time**. These are errors where the compiler can't figure out what you mean, or where your program would ultimately crash if you ran it, so the compiler is doing us a favor by warning us ahead of time.

.. youtube:: b_xL25S9qo0
   :divid: ch11_07_vid_compile_errors
   :height: 315
   :width: 560
   :align: center

.. admonition:: Video Recap   

   Some types of compiler errors include syntax errors, semantic errors, and type errors. C++ is able to catch many type errors at compile-time, because C++ is a **statically typed** language, which means that a variable's type is known at compile-time and doesn't change. This is in contrast to MATLAB, a **dynamically typed** language, where a variable's type can change at runtime.

Even though the compiler is very good at catching certain kinds of errors (e.g. syntax errors, missing variable declarations, type mismatches, etc.), there are some errors that occur at **runtime** and that the compiler generally can't catch! Why not? For example, what if an error only happens when a user enters bad data? The compiler can't be expected to predict the future!

.. youtube:: h-lRHUX-qwo
   :divid: ch11_07_vid_runtime_errors
   :height: 315
   :width: 560
   :align: center

.. admonition:: Video Recap

   Runtime errors are errors that the compiler isn't able to predict at compile-time. For example, if a user enters two numbers to divide, and the denominator is a zero, the program will crash because it can't divide by zero!

------------------------------------
Exercise: Compile and Runtime Errors
------------------------------------

.. dragndrop:: ch11_07_ex_compiling
   :match_1: undeclared variable|||semantic error (compile-time error)
   :match_2: missing curly brace|||syntax error (compile-time error)
   :match_3: cannot divide by zero|||runtime error
   :match_4: string value cannot be assigned to an int variable|||type error (compile-time error)

   Match the error to which category of error it is.


^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Application: Temperature Converter
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. section 8

Let's apply what we've learned so far to create our first *useful* C++ program - a temperature converter that takes an input temperature in degrees Celsius through :code:`cin` and then prints out the equivalent temperature in degrees Fahrenheit.

Here's the formula to convert Celsius (C) to Fahrenheit (F): F = 9/5 * C + 32.

Your program should:

* Prompt the user for a temperature in Celsius.
* Read the temperature from the standard input stream (i.e., :code:`cin`).
* Compute the temperature in Fahrenheit, and print it.

If you've got C++ set up on your computer, try to compile/run the code!

.. code :: c++

   #include <iostream>
   using namespace std;

   int main() {
      // Your code here
   }

|

.. shortanswer:: ch11_08_ex_temperature_converter

   Include a draft program in the box below. Please don't worry too much about getting it exactly right, but take enough time to think through and attempt to solve the problem. Then, watch the video below.

Let's walk through the process of writing this program, as well as some general tips for writing, testing, and debugging your code.

.. youtube:: CGPk9xOOZas
   :divid: ch11_08_vid_temperature_converter
   :height: 315
   :width: 560
   :align: center

.. admonition:: Video Recap

   This was Laura's first attempt at the temperature converter:

   .. code-block:: cpp

      #include <iostream>
      using namespace std;

      int main() {
      cout << "Enter a temperature in Celsius: ";
      
      int c;
      cin >> c;

      int f = 9 / 5 * c + 32;
      cout << f << " degrees Fahrenheit.";

      }

Based on Laura's first attempt at the temperature converter, answer these review questions.

.. mchoice:: ch11_08_ex_temp_convert_debug_01
  :answer_a: True
  :answer_b: False
  :correct: a
  :feedback_a: Correct! Temperatures are a continuous variable, therefore we need to store the temperature in Celsius as a double, not an int.
  :feedback_b: Incorrect. Temperatures are a continuous variable, therefore we need to store the temperature in Celsius as a double, not an int.

  The :code:`c` variable should be declared as a :code:`double`.

.. mchoice:: ch11_08_ex_temp_convert_debug_02
  :answer_a: True
  :answer_b: False
  :correct: a
  :feedback_a: Correct! Temperatures are a continuous variable, therefore we need to store the temperature in Fahrenheit as a double, not an int.
  :feedback_b: Incorrect. Temperatures are a continuous variable, therefore we need to store the temperature in Fahrenheit as a double, not an int.

  The :code:`f` variable should be declared as a :code:`double`.

.. mchoice:: ch11_08_ex_temp_convert_debug_03
  :answer_a: True
  :answer_b: False
  :correct: b
  :feedback_a: Incorrect. Re-watch the video to find why this expression for f is not quite correct.
  :feedback_b: Correct! The 9 / 5 is evaluated as integer division because 9 and 5 are both integers. So 9 / 5 = 1.8, but only the integer part (the 1) is kept. Change 9 / 5 to 9.0 / 5.0 and we force the expression to do "regular division" which is what we want in this case.

  The calculation :code:`f = 9 / 5 * c + 32` works for all values of :code:`c` (the temperature in Celsius).
  

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Summary
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

This is the end of the chapter! Here is a summary of what we covered in this chapter: 

* MATLAB is a great programming language for analyzing and presenting data, as well as rapid prototyping. C++ is better for writing larger, more complex programs, and it handles control flow very well.
* To run a C++ program, first we must **compile** our **source code**, turning it into **machine code**. Then, we must **run** the executable file. In contrast, MATLAB uses an **interpreter** to run code. We will use g++ to compile our C++ code.
* In C++, variables must be **declared** before they are used (specifying their name, type, and optional initializer expression). Some common data types are ints, doubles, bools, chars, and strings. When you declare a variable, the variable takes up space in memory.
* We can do single-line comments in C++ using :code:`//` and block comments using :code:`/*` and :code:`*/`.
* :code:`cout` is used to print a message to the terminal. :code:`cin` is used to get input from a user.
* When you compile C++ code, the compiler is able to catch many errors at compile-time. Some errors that the compiler can catch are syntax errors, semantic errors, and type errors.
* Not all errors can be caught at compile time. Some are caught at runtime.
* C++ is **statically typed** because a variable's type is known at compile-time. In contrast, in a **dynamically typed** language, a variable's type can change at runtime.

You can double check that you have completed everything on the "Assignments" page. Click the icon that looks like a person, go to "Assignments", select the chapter, and make sure to scroll all the way to the bottom and click the "Score Me" button.
