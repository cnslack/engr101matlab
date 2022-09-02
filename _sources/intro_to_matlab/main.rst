.. qnum::
   :prefix: Q
   :start: 1

.. raw:: html

   <link rel="stylesheet" href="../_static/common/css/theme-overrides.css">

.. raw:: html

   <script src="../_static/common/js/common3.js"></script>

.. raw:: html

   <style>
      .btn {
         margin: 0;
      }
      .tab-pane {
         padding: 0;
      }
   </style>

======================
Introduction to MATLAB
======================

.. ^^^^^^^^
.. Welcome!
.. ^^^^^^^^

Welcome to Engr 101! In Engr 101, we will learn basic principles of programming computer code and simple algorithms used to tackle real-world engineering problems. We will learn two programming languages: MATLAB (which is really good at processing data and visualizing it) and C++ (which is really good at automating decisions and creating a process).

**Why are we using Runestone?**

The best way to learn programming is to practice with each new programming skill and concept as it is introduced. This is hard to do in a traditional lecture but easy to do with the Runestone platform. Each Runestone chapter has sections that follow the same general pattern: introduce a concept, show some examples, check your understanding, and practice the concepts. 

We use a variety of approaches for these steps, including short videos, text and images, multiple choice and true/false questions, actual coding practice, and "mixed up code" problems (where you're given the lines of code and you need to arrange the code so that program works correctly). Each question and practice exercise has some type of feedback for you. You can check your answers to true/false and multiple choice questions right away, and Runestone will either tell you whether you are correct or will give you a hint. More complex questions have walkthrough videos that you can watch if you get stuck or want to verify that you've solved the problem correctly. 

**Who Are All These People in the Videos?** 

There are many short, instructional videos woven throughout this Runestone book. These videos have been created especially for Engr 101 by the faculty, GSIs, and IAs. Some of these people are currently teaching Engr 101, and some of them are past members of our Engr 101 teaching team. So, if you see someone you don't recognize, that's okay!  

.. admonition:: Chapter Files

  We'll be using several files throughout this chapter's exercises. It might be helpful to go ahead and download each of them now and move them to your current folder in MATLAB. (It's also a good idea to go ahead and create a new folder for this chapter and use that as your current folder, so that you don't clutter up whatever else you were working on.)

  .. list-table:: 
    :align: left
    :widths: auto

    * - :download:`FuelCalculatorBuggy1.m <../_static/intro_to_matlab/FuelCalculatorBuggy1.m>`

      - .. reveal:: buggy_calculator1
          :showtitle: Preview
          :modal:
          :modaltitle: <code>FuelCalculatorBuggy1.m</code>

          .. literalinclude:: ../_static/intro_to_matlab/FuelCalculatorBuggy1.m
            :language: matlab

      - A buggy fuel calculator script

    * - :download:`FuelCalculatorBuggy2.m <../_static/intro_to_matlab/FuelCalculatorBuggy2.m>`

      - .. reveal:: buggy_calculator2
          :showtitle: Preview
          :modal:
          :modaltitle: <code>FuelCalculatorBuggy2.m</code>

          .. literalinclude:: ../_static/intro_to_matlab/FuelCalculatorBuggy2.m
            :language: matlab

      - A second buggy fuel calculator script

    * - :download:`FuelCalculatorBuggy3.m <../_static/intro_to_matlab/FuelCalculatorBuggy3.m>`

      - .. reveal:: buggy_calculator3
          :showtitle: Preview
          :modal:
          :modaltitle: <code>FuelCalculatorBuggy3.m</code>

          .. literalinclude:: ../_static/intro_to_matlab/FuelCalculatorBuggy3.m
            :language: matlab

      - A third buggy fuel calculator script

    * - :download:`AnnArborTempsAug2019.mat <../_static/intro_to_matlab/AnnArborTempsAug2019.mat>`

      - .. reveal:: annArborTemps_mat_preview
          :showtitle: Preview
          :modal:
          :modaltitle: <code>AnnArborTempsAug2019.mat</code>

          No preview available

      - MATLAB saved workspace for plotting demo

    
  .. reveal:: intro_matlab_download_instructions
    :showtitle: Download Instructions
    :modal:
    :modaltitle: File Download Instructions for MATLAB
    
    .. include:: ../common/matlab_download_instructions.in.rst
      

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
A Quick Tour of MATLAB
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Let's get started with MATLAB! MATLAB is a programming language and environment often used in engineering applications. The term **MATLAB** refers to both the program (that you open on your computer) and the programming language itself. Let's take a quick tour of how it works.

.. youtube:: iFrEd4x8g_k
  :divid: ch01_02_vid_variables_and_expressions
  :height: 315
  :width: 560
  :align: center

.. admonition:: Video Recap

  We've looked at the different components of the MATLAB programming environment, and seen how to change the layout. When you start a new MATLAB program, the first thing you should check is the current folder that you are working in. We looked at a few examples of doing basic math in MATLAB, as well as storing numbers in variables.

Some fundamental tools in programming are literals, variables, and expressions:

* **Literals** are simply data written directly into our code. They might be numbers like :code:`3` or :code:`-2.85`, but we'll also see other kinds of data. For example, text literals can be written with single quotes like :code:`'hello world!'`.

* **Variables** are used to store data in the computer's memory, for example :code:`x`, :code:`ans`, or :code:`fuel_rate`.

  - **Assignment** is used to give a variable a value. In MATLAB, the :code:`=` operator is used for assignment.

  - Variables may be assigned a new value several times, overwriting the old value. Just because we run :code:`x = 5` doesn't mean we won't come back later and run :code:`x = 10` to update it.

* **Expressions** are used to manipulate and compute new data, often by combining variables and literals, or even other sub-expressions. They generally use **operators** like :code:`+`, :code:`*`, etc.

------------------------------------------------------
Exercise: Variables and Expressions
------------------------------------------------------

.. tip::
  By the way, we end up using a lot of terms interchangably to refer to the content of programs, like *code*, *lines of code*, *commands*, *instructions*, *statements*, etc. Likewise, when we "make a program go", we might say we *run* it, *execute* it, or *launch* it. They all mean essentially the same thing and can be used interchangeably.

Consider the following MATLAB code, which might be used to calculate the net income for a server at Proxima Tea, a new drink stand we're planning to open in one of the Proxima b settlements. (If the rate seems weird, that's because it's in Proxima b currency.)


.. code-block:: matlab

  hours = 3 + 0 + 4 + 5 + 3;
  rate = 100.5;
  wage = hours * rate;
  tax = 0.24 * wage;
  net = wage - tax;

|

.. shortanswer:: ch01_02_ex_programming_constructs_01

  Give an example of a *variable* from the code above.

.. shortanswer:: ch01_02_ex_programming_constructs_02

  Give an example of a *literal* from the code above.

.. shortanswer:: ch01_02_ex_programming_constructs_03

  Give an example of an *expression* from the code above.


^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Scripts
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

In MATLAB, a **script** is sequence of commands written out, saved into a file, and then run all at once. We often use a script when we want to write a program that does something non-trivial and that we might run multiple times.

Let's take a look at an example, and along the way we'll write up our first interesting MATLAB program.

----------------------------
Example: A Fuel Calculator
----------------------------

.. youtube:: A1Beuyvju08
  :divid: ch01_03_vid_scripts_01
  :height: 315
  :width: 560
  :align: center

.. admonition:: Video Recap

  For reference, here's the problem discussed in the video:

  .. image:: img/fuel_calculator.png
    :width: 560
    :align: center
    :alt: A screenshot of the fuel calculator problem.

Why would we even *want* to write a program here? Couldn't we just solve this problem by hand a lot faster? Maybe we could solve it for one set of numbers by hand faster than writing a program. But, what if we wanted to solve this problem multiple times, for different fuel rates or different burn times? It would take a long time to solve the problem multiple times by hand, and we can save time by writing a program and automating the process.

We will use an **algorithm** to solve this problem. An algorithm is a formal set of steps for solving a problem that contains enough details to be clear and unambiguous. A good way to check is to think "would someone else understand my solution by reading this?".

.. shortanswer:: ch01_03_ex_fuel_calculator_algorithm

  Briefly describe an algorithm you could use to compute the total amount of fuel needed for the probe, and also give a few examples of *variables* and *expressions* that could be used in a program implementing that algorithm.

Let's look at a couple of algorithms that we could use to implement the fuel calculator.

.. youtube:: Nmg8blikrjY
  :divid: ch01_03_vid_scripts_02
  :height: 315
  :width: 560
  :align: center

.. admonition:: Video Recap

  In the previous video, we considered what variables we would need in our program, as well as a couple of possible algorithms to implement the fuel calculator.

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Debugging
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

In the process of implementing algorithms, sometimes we make coding mistakes; these mistakes are called **bugs**.  A bug is anything that causes a program to not implement an algorithm correctly. Some common bugs are mistyping a variable name, typing the wrong number, or telling the computer to do one thing when you *really* meant that it should do a different thing. **Debugging** is the process we use to narrow down where in our program a bug occurs and then correct the bug. 

.. admonition:: Did you know?

  The terms *bug* and *buggy* are used to decribe defects in programs - small mistakes that can cause a whole system to malfunction. While the terms have been around since the late 1800s, one notable example occurred in 1947 when a moth (a real bug!) managed to infiltrate a Mark II computer and interferred with the operation of one of its relays.

  .. image:: img/bug.jpg
    :width: 560
    :align: center
    :alt: A moth taped to a page from a logbook.

------------------------------------------------------
Exercise: Debugging the Fuel Calculator Script
------------------------------------------------------

To practice debugging, consider three slightly different versions of the fuel calculator script, each containing a bug. You can download these files at the top of this chapter. For each file, download the file, put it in your current MATLAB folder, and run it (by typing the name of the script, e.g. :code:`FuelCalculatorBuggy1`, in the command window). Use your knowledge of the way the script *should* work to help deciper error messages or incorrect results and track down the bug.

.. fillintheblank:: ch01_03_ex_buggy_01

  Which line contains the bug in :code:`FuelCalculatorBuggy1.m`?

  - :15: Correct! Variable names in MATLAB are case sensitive.
    :x: Nope, try again!


.. fillintheblank:: ch01_03_ex_buggy_02

  Which line contains the bug in :code:`FuelCalculatorBuggy2.m`?

  - :11: Correct! :code:`totalHours` should be used instead of :code:`hours`.
    :x: Nope, try again!


.. fillintheblank:: ch01_03_ex_buggy_03

  Which line contains the bug in :code:`FuelCalculatorBuggy3.m`?

  - :12: Correct! There should only be one :code:`60 *` on this line.
    :x: Nope, try again!

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Style Tips
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

As you program, you will likely develop your coding "style" -- how you like to name variables, how much whitespace you put between chunks of code, how you arrange your code. Here are some tips to get you started. 

--------------
Comments
--------------

A **comment** is a brief note in your code to explain what's happening. When the computer runs your code, it ignores all of the comments. The comments are there to document your code for other people (and for yourself, when you come back to your code in a few weeks and forget what you were trying to do!). Here's an example of comments in MATLAB:

.. code:: matlab

  hours = 3 + 0 + 4 + 5 + 3; % This is a short comment!

  %{
  This is a longer comment
  that takes more than one line 
  }%

In general, you don't need to add a comment to every line of code. But, you should use comments to explain more complicated lines of code, as well as to generally document the organization of your program.

--------------
Variable Names
--------------

When naming variables, choose **descriptive** variable names that describe the data being stored. For example, in the fuel calculator program, we have a variable that represents the rate of fuel use. Here are some examples of both undescriptive and descriptive variable names:

.. code:: matlab

  var = 10;         % Bad! Doesn't describe the data
  num = 10;         % Bad! Doesn't describe the data
  rate fuel = 10;   % Error!  You can't use spaces in variable names
  fuelRate = 10;    % Good! This style of capitalization is called "camel case"
  fuel_rate = 10;   % Good! This uses underscores to separate multiple words

--------------------
Operator Spacing
--------------------

When writing expressions, the best style is to pad your binary operators (like :code:`+`, :code:`*`, etc.) with spaces, like this:

.. code:: matlab

  x + y;  % YES
  x+y;    % Maybe
  x+ y;   % NO
  x +y;   % NO

-------------------------
Intermediate Variables
-------------------------

There's a general tradeoff between using *intermediate variables* and using *compound expressions*. From the fuel calculator program, we could calculate the number of seconds using several intermediate variables, like this:

.. code-block:: matlab

  % Algorithm #1 from earlier
  secondsFromDays = 24 * 60 * 60 * days;
  secondsFromHours = 60 * 60 * hours;
  secondsFromMinutes = 60 * minutes;
  seconds = secondsFromDays + secondsFromHours + secondsFromMinutes;

Or we could use one compound expression, like this:

.. code-block:: matlab

  % Algorithm #3 from earlier
  seconds = 24 * 60 * 60 * days + 60 * 60 * hours + 60 * minutes;

Both approaches work equally well in this case, and both are "correct" since they each perform the correct calculations. In your programs, judge which approach best fits the needs of your code and is the easiest to understand. You should also consider whether you need to use any of the intermediate values in other calculations.

-------------------------
Hardcoding
-------------------------

We say a value is **hardcoded** into a program when it appears in an expression as a literal (i.e. without using a variable). Hardcoding is generally okay if the value won't reasonably change. Hardcoding is NOT okay if the value is an input, or if it might change.

Consider this program that uses hardcoding:

.. code:: matlab

  totalHours = 20 * 24 + 6;
  totalMinutes = totalHours * 60 + 43;
  totalTimeInSeconds = 60 * totalMinutes;

In this program, the number of days (20), the number of hours (6), and the number of minutes (43) are hardcoded into the program. But, these are inputs to their program and they might change, so we don't want to hardcode them. Here's a better way to write this program:

.. code :: matlab

  % Inputs for total burn time of fuel
  days = 20;
  hours = 6;
  minutes = 43;

  % calculation
  totalHours = days * 24 + hours;
  totalMinutes = totalHours * 60 + minutes;
  totalTimeInSeconds = 60 * totalMinutes;

It's ok to hardcode the number of hours per day (24) and the number of minutes per hour (60) since these numbers won't change.

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Update Assignments
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Variables in programming are different than variables in math. In math, when you say *x = 1*, you mean it. *x* is equal to 1 and always will be (at least until the next problem!). But in programming, :code:`x = 1` just means "put the value 1 in :code:`x` for now", and its value may be updated later.

We can even update the value of a variable based on its previous value! This is called an **update assignment** (or **update expression**). Let's take a look...

.. youtube:: 2cpC6Uzp0TA
  :divid: ch01_04_vid_update_assignments
  :height: 315
  :width: 560
  :align: center

.. admonition:: Video Recap

  If the variable :code:`x` has already been assigned a value, we can use an **update assignment** to update the value of :code:`x` based on its previous value. This might look like :code:`x = x + 5`.

.. fillintheblank:: ch01_04_ex_buggy_01

  Consider the following code:

  .. code-block:: matlab

    x = 2;
    x = x * x + 1;
    y = x * (x + 1);
    x = y * x;
    disp(x);
    disp(y);

  What values are displayed when this code is run?

  - :150: Correct! The sequence of values for :code:`x` is 2, 5, 150.
    :x: The sequence of values for :code:`x` is 2, 5, 150. Double check which line you have that doesn't match. (Note that line 3 doesn't directly change the value of :code:`x`, although it does change :code:`y`, which will matter for line 4.)

  - :30: Correct! :code:`y` is updated once, based on the value of :code:`x` at line 3, which is 5.
    :x: Try again. Hint: :code:`y` is updated once, based on the value of :code:`x` at line 3, which is 5.

.. admonition:: Walkthrough

  .. reveal:: ch01_04_revealwt_update_assignments

    .. youtube:: vaVU87KQ-y8
      :divid: ch01_04_wt_update_assignments
      :height: 315
      :width: 560
      :align: center



^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Functions
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Expressions in MATLAB can also use **functions** to compute results or perform operations. MATLAB has *many* built-in functions for math, data analysis, and engineering applications. You can even write your own!

.. youtube:: hURLCeTwpGk
  :divid: ch01_05_vid_intro_to_functions
  :height: 315
  :width: 560
  :align: center

.. admonition:: Video Recap

  A **function** is an abstraction over a chunk of computation (data goes in, gets processed, new data comes out). We call data going *into* a function **parameters**, and data coming *out* of a function **return variables**. We can use a function by **calling** it, passing it some parameters, and storing its return variables.

  Scripts and functions are related, but have different uses. The terminology is also slightly different: you **run** a script, but **call** a function.

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
So what else can MATLAB do?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

MATLAB is way more than just a really fancy calculator. We will cover a lot more of what MATLAB can do as we go through the course, but let’s take a quick look to see how powerful MATLAB can be!

A key strength of MATLAB is support for working with vectors and matrices just as easily as scalar values. A **scalar** is a regular number, like 12 or 97.4. 

A **vector** is a one-dimensional sequence of numbers:

.. image:: img/vector.png
  :width: 200
  :align: center
  :alt: A row vector containing [1, 3, 6, 7, 9].

|

A **matrix** is a two-dimensional grid of numbers:

.. image:: img/matrix.png
  :width: 150
  :align: center
  :alt: A 2-by-3 matrix containing [7, 3, 9 ; 5, 7, 2].

|

We use vectors and matrices to represent real-world data and quickly analyze that data to help make decisions about things. We need to know things like the biggest value, or the smallest value, or the most common value. MATLAB has a lot of built-in functions that can help us analyze data. 

We also often want to visualize how one set of data relates to another. MATLAB has a staggeringly large number of ways to plot data. We will cover some of the most common plotting styles in this class, as well as ways to make your plots clear and professional.

Watch the demo below to see examples of how we can use MATLAB to manipulate data. You can download the workspace file :code:`AnnArborTempsAug2019.mat` at the top of the chapter.

.. youtube:: mO9a57T8NJg
  :divid: ch01_06_vid_what_else
  :height: 315
  :width: 560
  :align: center

.. admonition:: Video Recap

  You can save all the variables in your MATLAB workspace to a file using the :code:`save` command, and restore a saved workspace using the :code:`load` command. The load and save commands are also available from the MATLAB menu. All workspace files use the :file:`.mat` file extension.

  In the video, we showed some examples of data analysis and plotting (much more to come in later chapters!).

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Summary
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

This is the end of the chapter! Here is a summary of what we covered in this chapter: 

* The term **MATLAB** refers to both the program (that you open on your computer) and the programming language itself.
* **Literals** are data written directly into code. **Variables** are used to store data in the computer’s memory. **Expressions** are used to manipulate and compute new data.
* The **assignment operator** (:code:`=`) stores a value into a variable.
* In MATLAB, a **script** is sequence of commands written out, saved into a file, and then run all at once. 
* An **algorithm** is a formal set of steps for solving a problem that contains enough details to be clear and unambiguous. 
* A **bug** is anything that causes a program to not implement an algorithm correctly. **Debugging** is the process we use to narrow down where in our program a bug occurs and then correct the bug.
* A **comment** is a brief note in your code to explain what’s happening.
* When naming variables, choose **descriptive** variable names that describe the data being stored.
* We say a value is **hardcoded** into a program when it appears in an expression as a literal (i.e. without using a variable).
* You can update the value of a variable based on its previous value using an **update assignment** (or **update expression**). 
* A **function** is an abstraction over a chunk of computation. There are built-in functions and functions that you write yourself. We call data going into a function **parameters**, and data coming out of a function **return variables**. We can use a function by **calling** it, passing it some parameters, and storing its return variables.
* MATLAB is really good at working with vectors and matrices and processing data.

You can double check that you have completed everything on the "Assignments" page. Click the icon that looks like a person, go to "Assignments", select the chapter, and make sure to scroll all the way to the bottom and click the "Score Me" button.
