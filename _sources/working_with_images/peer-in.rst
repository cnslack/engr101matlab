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

.. fillintheblank:: aa-workingw/images_10_images_01
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following snippet of code? Assume that there is a colored image with the name 'Batman.png' of size 500 * 500 * 3 in the folder. (If the program will result in an error, put down 'ERROR')

    .. code-block:: matlab
  
     clc; clear;
     pix = 'Batman.png';
     [h,w,c] = size(pix);
     total = h + w + c;
     disp(total);
     disp(str)

  - :12: Correct!
    :x: Incorrect. Check what exactly is 'pix'?

.. fillintheblank:: aa-workingw/images_10_images_02
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following snippet of code? Assume that there is a colored image with the name 'Batman.png' of size 500 * 500 * 3 in the folder. (If the program will result in an error, put down 'ERROR')

    .. code-block:: matlab
  
     clc; clear;
     pix = imread('Batman.png');
     [h, w] = size(pix);
     disp(w);

  - :1500: Correct!
    :x: Incorrect. Note that size(pix) returns the dimensions according to the number of variables used on the left side. So, if you have [h, w, c] then it will return 3 values, and if you have only [h, w], then h will be the number of rows and w will be the number of columns multiplied by total number of matrices. In MATLAB, you get what you ask.

.. fillintheblank:: aa-workingw/images_10_images_03
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following snippet of code? Assume that there is a colored image with the name 'Batman.png' of size 500 * 500 * 3 in the folder. (If the program will result in an error, put down 'ERROR')

    .. code-block:: matlab
  
     clc; clear;
     pix = imread('Batman.png');
     [h,w, ~] = size(pix);
     total = h + w ;
     disp(total)

  - :1000: Correct!
    :x: Incorrect. Here, '~' represents that the third dimension which is number of matrices is not stored in a variable. Therefore, h and w will only be numbers of rows and columns respectively.

.. fillintheblank:: aa-workingw/images_10_images_04
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following snippet of code? Assume that there is a colored image with the name 'Batman.png' of size 500 * 500 * 3 in the folder. (If the program will result in an error, put down 'ERROR')

    .. code-block:: matlab
  
     clc; clear;
     pix = imread('Batman.png');
     blank = uint8(zeros(h,w,c));
     blank(1,1,1) = 255;
     disp(blank(1,1,1));

  - :ERROR: Correct!
    :x: Incorrect. Check how the 'blank' image is defined.

.. fillintheblank:: aa-workingw/images_10_images_05
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   In the following program, how many pixels in the image 'blank' will be red? Assume that there is a colored image with the name 'Batman.png' of size 500 * 500 * 3 in the folder. (If the program will result in an error, put down 'ERROR')

    .. code-block:: matlab
  
     clc; clear;
     pix = imread('Batman.png');
     [h, w, c] = size(pix);
     blank = uint8(zeros(h,w,c));
     blank(1:3, 1:10, 1) = 255;

  - :30: Correct!
    :x: Incorrect. Check how the index values of rows and columns in the last line.

.. mchoice:: aa-workingw/images_10_images_06
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: The function imread() changes the name of the image whereas imshow() displays the image.
  :answer_b: The function imread() converts the image file into a matrix whereas imshow() displays the image.
  :answer_c: The function imread() converts the image file into a matrix whereas imshow() changes the name of the image.
  :answer_d: The function imread() calculates the size of the image whereas imshow() displays the image.
  :correct: b
  :feedback_a: Incorrect. Test these functions in MATLAB.
  :feedback_b: Correct! 
  :feedback_c: Incorrect. Test these functions in MATLAB.
  :feedback_d: Incorrect. Test these functions in MATLAB.
  
   What is the difference between the functions imread(image_name) and imshow(image_name)?

.. mchoice:: aa-workingw/images_10_images_07
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: The matrix 'mix' is a matrix which can take any mathematical values but matrix 'pix' can only take values from 0 to 255.
  :answer_b: The matrix 'mix' is a matrix which can only take values from 0 to 255 but matrix 'pix' can take any mathematical value.
  :answer_c: The matrix 'mix' has all the values as zeros but matrix 'pix' has all the values as 255.
  :answer_d: There is no difference between both the matrices as they can take any value.
  :correct: a
  :feedback_a: Correct!
  :feedback_b: Incorrect. Note that the addition of uint8 restricts the values which a matric can take.
  :feedback_c: Incorrect. Note that the addition of uint8 restricts the values which a matric can take.
  :feedback_d: Incorrect. Note that the addition of uint8 restricts the values which a matric can take.
  
   What is the difference between the following 2 matrices?

   .. code-block:: matlab
  
     mix = zeros(5,5,3);
     
     pix = uint8(zeros(5,5,3));

.. mchoice:: aa-workingw/images_10_images_08
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: It will show the image 'Batman.png'
  :answer_b: It will return an ERROR 
  :correct: b
  :feedback_a: Incorrect. Note that whenever you write the name, it has to be in single quotes.
  :feedback_b: Correct!
  
   What will be the output of the following snippet of code? Assume that there is a colored image with the name 'Batman.png' of size 500 * 500 * 3 in the folder.

   .. code-block:: matlab
  
     clc; clear;
     
     imshow(Batman.png);

.. mchoice:: aa-workingw/images_10_images_09
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: It will show the image 'Batman.png'
  :answer_b: It will return an ERROR 
  :correct: a
  :feedback_a: Correct!
  :feedback_b: Incorrect. Note that whenever the name of the image is stored in a variable, we just use that variable name without single quotes.
  
   What will be the output of the following snippet of code? Assume that there is a colored image with the name 'Batman.png' of size 500 * 500 * 3 in the folder. (If the program will result in an error, put down 'ERROR')

   .. code-block:: matlab
  
     clc; clear;
     
     filename = 'Batman.png'
     
     imshow(filename);

.. fillintheblank:: aa-workingw/images_10_images_10
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   In the following program, how many pixels in the image 'blank' will be red? Assume that there is a colored image with the name 'Batman.png' of size 500 * 500 * 3 in the folder. (If the program will result in an error, put down 'ERROR')

    .. code-block:: matlab
  
     clc; clear;
     pix = imread('Batman.png');
     [h, w, c] = size(pix);
     blank = uint8(zeros(h,w,c));
     blank(:, :, :) = 255;
     blank(end, :, [2 3]) = 0;

  - :500: Correct!
    :x: Incorrect. Check how the index values of rows and columns in the last line.

.. mchoice:: aa-workingw/images_10_images_11
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: pix(250, 250, :) = blank(400, 400, :);
  :answer_b: blank(250, 250, :) = pix(400, 400, :);
  :answer_c: blank(400, 400, : ) = pix(250, 250, :);
  :answer_d: pix(400, 400, :) = blank(250, 250, :);
  :correct: c
  :feedback_a: Incorrect. Note that position of the receiver is on the left and the assigned value is always on the right.
  :feedback_b: Incorrect. Note that position of the receiver is on the left and the assigned value is always on the right.
  :feedback_c: Correct!
  :feedback_d: Incorrect. Note that position of the receiver is on the left and the assigned value is always on the right.
  
   For the following snippet of code, assume that there is a colored image with the name 'Batman.png' of size 500 * 500 * 3 in the folder. If we want to copy the RGB colors from the position 250, 250 in 'pix' to the position 400, 400 in 'blank', which of the following commands will we use?

   .. code-block:: matlab
  
     clc; clear;
     
     pix = imread('Batman.png');
     
     [h, w, c] = size(pix);
     
     blank = uint8(zeros(h,w,c));

.. mchoice:: aa-workingw/images_10_images_12
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: pix(:, 3:10, 3) = 255;
  :answer_b: pix(3:10, :, 2) = 255;
  :answer_c: pix(3:10, 50, 3) = 255;
  :answer_d: pix(3:10, :, 3) = 255;
  :answer_e: pix(3, 10, 3) = 255;
  :correct: d
  :feedback_a: Incorrect. Check these statements in MATLAB and observe what do they exactly do.
  :feedback_b: Incorrect. Check these statements in MATLAB and observe what do they exactly do.
  :feedback_c: Incorrect. Check these statements in MATLAB and observe what do they exactly do.
  :feedback_d: Correct!
  :feedback_e: Incorrect. Check these statements in MATLAB and observe what do they exactly do.
  
   For a defined image 'pix' which of the following options will color all the columns in the rows from 3 to 10 as blue?

   .. code-block:: matlab
  
     clc; clear;
     
     pix = uint8(zeros(50, 50, 3));

.. mchoice:: aa-workingw/images_10_images_13
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: pix(1:5, 3:10, 1) = 255;
  :answer_b: pix(3:10, 1:5, 1) = 255;
  :answer_c: pix(3:10, 5, 1) = 255;
  :answer_d: pix(:, 3:10, 1) = 255;
  :correct: b
  :feedback_a: Incorrect. Check these statements in MATLAB and observe what do they exactly do.
  :feedback_b: Correct!
  :feedback_c: Incorrect. Check these statements in MATLAB and observe what do they exactly do.
  :feedback_d: Incorrect. Check these statements in MATLAB and observe what do they exactly do.
  
   For a defined image 'pix' which of the following options will color only the columns from 1 to 5 in the rows from 3 to 10 as red?

   .. code-block:: matlab
  
     clc; clear;
     
     pix = uint8(zeros(50, 50, 3));

.. mchoice:: aa-workingw/images_10_images_14
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: imwrite( pix, 'Correct.png');
  :answer_b: imwrite( 'pix', Correct.png);
  :answer_c: imwrite( 'pix', 'Correct.png');
  :answer_d: imwrite( 'Correct.png', pix);
  :correct: a
  :feedback_a: Correct!
  :feedback_b: Incorrect. The syntax to use imwrite() is imwrite( image_variable, image_name).
  :feedback_c: Incorrect. The syntax to use imwrite() is imwrite( image_variable, image_name).
  :feedback_d: Incorrect. The syntax to use imwrite() is imwrite( image_variable, image_name).
  
   Which of the following options saves the image 'pix' with the name 'Correct.png'?

.. mchoice:: aa-workingw/images_10_images_15
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: It displays a complete black image
  :answer_b: It displays an image having alternating rows and columns as black and white in the form of a grid
  :answer_c: It displays a complete white image
  :answer_d: It displays an image having alternating black rows and blue columns in the form of a grid
  :correct: d
  :feedback_a: Incorrect. Check the indices used in the for-loop again.
  :feedback_b: Incorrect. Check the indices used in the for-loop again.
  :feedback_c: Incorrect. Check the indices used in the for-loop again.
  :feedback_d: Correct!
  
   What does the following code snippet display?

   .. code-block:: matlab
  
     clc; clear;
     
     pix = uint8(zeros(50,50,3));
     
     pix(:, :, :) = 255;
     
     for ii = 1:2:50
      pix(ii, :, : ) = 0;
      pix(:, ii, [1 2]) = 0;
     end
     
     imshow(pix)

.. mchoice:: aa-workingw/images_10_images_16
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: pix(25, 25, 3) = 255;
  :answer_b: pix(1:25, 25, 3) = 255;
  :answer_c: pix(1:25, 1:25, 3) = 255;
  :answer_d: pix(1:25, 1:25, 3) = 255;
  :correct: c
  :feedback_a: Incorrect. Check the indices again for rows and columns in the options provided.
  :feedback_b: Incorrect. Check the indices again for rows and columns in the options provided.
  :feedback_c: Correct!
  :feedback_d: Incorrect. Check the indices again for rows and columns in the options provided.
  
   Which of the following options will put a blue box in the top-left half (1st quadrant) of the image 'pix'?

   .. code-block:: matlab
  
     clc; clear;
     
     pix = uint8(zeros(50,50,3));

.. mchoice:: aa-workingw/images_10_images_17
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: It creates an image matrix which initially has all values as zeros and where all the numbers can only take values from 0 to 255
  :answer_b: It creates a matrix which initially has all values as zeros and where all the numbers can take any numeric value
  :answer_c: It creates a matrix which can either have 0s or 1s
  :answer_d: It returns an error
  :correct: b
  :feedback_a: Incorrect. Check your notes to understand how do we define an image.
  :feedback_b: Correct!
  :feedback_c: Incorrect. Check your notes to understand how do we define an image.
  :feedback_d: Incorrect. Check your notes to understand how do we define an image.
  
   What is the functionality of the command zeros()?

.. fillintheblank:: aa-workingw/images_10_images_18
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   How many total number of pixels are present in the image 'pix'?

    .. code-block:: matlab
  
     clc; clear;
     pix = uint8(zeros(500,500,3));

  - :250000: Correct!
    :x: Incorrect. Note that the color of a pixel is combination of three colors.

.. fillintheblank:: aa-workingw/images_10_images_19
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following snippet of code? (If the program will result in an error, put down 'ERROR')

    .. code-block:: matlab
  
     clc; clear;
     pix = uint8(zeros(10, 10, 3));
     pix(1, 1, :) = 1000;
     disp( pix(1, 1, 1) );

  - :255: Correct!
    :x: Incorrect. Note that the values in an image matrix only varies from 0 to 255.

.. fillintheblank:: aa-workingw/images_10_images_20
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following snippet of code? (If the program will result in an error, put down 'ERROR')

    .. code-block:: matlab
  
     clc; clear;
     pix = zeros(10, 10, 3);
     pix(1, 1, :) = 1000;
     disp( pix(1, 1, 1) );

  - :1000: Correct!
    :x: Incorrect. Note that here,  the matrix pix is not an image matrix since it does not have uint8, thus it can take any value.

.. fillintheblank:: aa-workingw/images_11_images_01
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following snippet of code? (If the program will result in an error, put down 'ERROR')

    .. code-block:: matlab
  
     clc; clear;
     x = uint8(100);
     x = x * 5;
     disp(x)

  - :255: Correct!
    :x: Incorrect. Note that the number 100 is bounded by the uint8 constraint by which they can only go from o to 255. Therefore, if the number is manipulated through any mathematical operation, its range will only be able to vary from 0 to 255.

.. fillintheblank:: aa-workingw/images_11_images_02
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following snippet of code? (If the program will result in an error, put down 'ERROR')

    .. code-block:: matlab
  
     clc; clear;
     pix = uint8(zeros(50,50,3));
     pix(1, 1, 1) = 250;
     total = pix(1, 1, 1) * 2;
     disp(total)

  - :255: Correct!
    :x: Incorrect. Note that the numbers in the image matrix are bounded by the uint8 constraint by which they can only go from o to 255. Therefore, if the number is manipulated through any mathematical operation, its range will only be able stretch from 0 to 255.

.. fillintheblank:: aa-workingw/images_11_images_03
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following snippet of code? (If the program will result in an error, put down 'ERROR')

    .. code-block:: matlab
  
     clc; clear;
     x = uint8(100);
     x = double(x * 5);
     disp(x)

  - :255: Correct!
    :x: Incorrect. Note that the number 'x' has to be converted to double(to remove any constraint) before it is multiplied with 5, otherwise it is still in the unit8 constraint.

.. fillintheblank:: aa-workingw/images_11_images_04
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following snippet of code? (If the program will result in an error, put down 'ERROR')

    .. code-block:: matlab
  
     clc; clear;
     pix = uint8(zeros(50,50,3));
     pix(1, 1, 1) = 250;
     total = double(pix(1, 1, 1)) * 2;
     disp(total)

  - :500: Correct!
    :x: Incorrect. Note that here, double() converts pix(1, 1, 1) to a normal numeric value only for calculation purposes and then it is multiplied by 2.

.. mchoice:: aa-workingw/images_11_images_05
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: It helps in identifying which pixels of the image are being thresholded so that the thresholding condition can be changed accordingly
  :answer_b: It helps in creating a black and white image
  :answer_c: It helps in identifying the center of the thresholded object
  :answer_d: It helps in the position of the thresholded object
  :correct: a
  :feedback_a: Correct!
  :feedback_b: Incorrect. Note that the primary use of binary image is to know which all pixels got thresholded so that you can improve the thresholding condition.
  :feedback_c: Incorrect. Note that the primary use of binary image is to know which all pixels got thresholded so that you can improve the thresholding condition.
  :feedback_d: Incorrect. Note that the primary use of binary image is to know which all pixels got thresholded so that you can improve the thresholding condition.
  
   In the thresholding example videos you have watched, what do you think is the primary purpose of using a binary image?

.. mchoice:: aa-workingw/images_11_images_06
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: pix = binary(50, 50);
  :answer_b: binary = false(50, 50); 
  :answer_c: binary = zeros(50, 50);
  :answer_d: pix = binary(zeros(50,50);
  :correct: b
  :feedback_a: Incorrect. Check these individual statements in MATLAB and see what do they do.
  :feedback_b: Correct!
  :feedback_c: Incorrect. Check these individual statements in MATLAB and see what do they do.
  :feedback_d: Incorrect. Check these individual statements in MATLAB and see what do they do.
  
   Which of the following is the correct way to define a binary image?

.. mchoice:: aa-workingw/images_11_images_07
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: A binary image has three matrices which have the value of 0.
  :answer_b: A binary image can take any numeric value.
  :answer_c: A binary image can only take values ranging from 0 to 255.
  :answer_d: A binary image can only take the value of either 0 or 1.
  :correct: d
  :feedback_a: Incorrect. Remember that a binary image has 1 matrix whose values can either have 0 or 1.
  :feedback_b: Incorrect. Remember that a binary image has 1 matrix whose values can either have 0 or 1.
  :feedback_c: Incorrect. Remember that a binary image has 1 matrix whose values can either have 0 or 1.
  :feedback_d: Correct!
  
   Which of the following statement is true regarding a binary image?

.. mchoice:: aa-workingw/images_11_images_08
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: value = double( pix(1, 1, 1) * 2 );
  :answer_b: value = double(2) * pix(1, 1, 1);
  :answer_c: value = double( pix(1, 1, 1) ) * 2; 
  :answer_d: value = double( 2 * pix(1, 1, 1) );
  :correct: c
  :feedback_a: Incorrect. Note that the number pix(1, 1, 1) has to be converted to double(remove any constraint) before it is multiplied with 2, otherwise it is still in the unit8 constraint.
  :feedback_b: Incorrect. Note that the number pix(1, 1, 1) has to be converted to double(remove any constraint) before it is multiplied with 2, otherwise it is still in the unit8 constraint.
  :feedback_c: Correct!
  :feedback_d: Incorrect. Note that the number pix(1, 1, 1) has to be converted to double(remove any constraint) before it is multiplied with 2, otherwise it is still in the unit8 constraint.
  
   Which of the following is the correct way to use double() when multiplying the value of pix(1, 1, 1) with 2 at the end of the code snippet given below?   

   .. code-block:: matlab
  
     clc; clear;
     
     pix = uint8(zeros(50,50,3));
     
     pix(:, :, : ) = 255;

.. fillintheblank:: aa-workingw/images_11_images_09
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following snippet of code? (If the program will result in an error, put down 'ERROR')

    .. code-block:: matlab
  
     clc; clear;
     binary = false(50, 50);
     binary(1, 1) = 50;
     disp( binary(1, 1) );

  - :1: Correct!
    :x: Incorrect. Note that a binary image has 1 matrix whose values can either have 0 or 1. So if you try to assign it any value other than 0, it will take it as 1.

.. fillintheblank:: aa-workingw/images_11_images_10
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following snippet of code? (If the program will result in an error, put down 'ERROR')

    .. code-block:: matlab
  
     clc; clear;
     binary = false(50, 50);
     binary(1, : ) = true;
     disp( binary(1, 1) )

  - :1: Correct!
    :x: Incorrect. Note that here, 'binary(1, : ) = true'  changes all the values in the first row as 1 because true represents logical 1.

.. fillintheblank:: aa-workingw/images_11_images_11
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following snippet of code? (If the program will result in an error, put down 'ERROR')

    .. code-block:: matlab
  
     clc; clear;
     binary = false(50, 50);
     binary(1:2, : ) = true;
     value = length(find(binary == 1));
     disp(value);

  - :100: Correct!
    :x: Incorrect. Note that here 2 rows are changed to 1s, so length( find() ) tells you how many values have 1 in the binary matrix.

.. fillintheblank:: aa-workingw/images_11_images_12
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following snippet of code? (If the program will result in an error, put down 'ERROR')

    .. code-block:: matlab
  
     clc; clear;
     binary = false(50, 50);
     binary(end, end) = true;
     value = length(find(binary == 1));
     disp(value);

  - :1: Correct!
    :x: Incorrect. Check the indexes again.

.. fillintheblank:: aa-workingw/images_11_images_13
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following snippet of code? (If the program will result in an error, put down 'ERROR')

    .. code-block:: matlab
  
     clc; clear;
     pix = uint8(zeros(50,50,3));
     pix(: ,: ,: ) = 255;
     sum = pix(1, 1, 1) + pix(end, end, 1);

  - :255: Correct! 
    :x: Incorrect. Note that here both values are uint8 values which cannot exceed 255.

.. fillintheblank:: aa-workingw/images_11_images_14
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following snippet of code? (If the program will result in an error, put down 'ERROR')

    .. code-block:: matlab
  
     clc; clear;
     pix = uint8(zeros(50,50,3));
     pix(: ,: ,: ) = 255;
     sum = double( pix(1, 1, 1) ) + pix(end, end, 1);
     disp( sum )

  - :255: Correct! 
    :x: Incorrect. Note that here one value is still present in uint8 format, the total sum cannot exceed 255.

.. fillintheblank:: aa-workingw/images_11_images_15
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following snippet of code? (If the program will result in an error, put down 'ERROR')

    .. code-block:: matlab
  
     clc; clear;
     pix = uint8(zeros(50,50,3));
     pix(: ,: ,: ) = 255;
     sum = double( pix(1, 1, 1) ) + double( pix(end, end, 1) );
     disp( sum )

  - :510: Correct! 
    :x: Incorrect. Note that here both the values are converted into double before being added.

.. mchoice:: aa-workingw/images_11_images_16
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: It is converting all the black pixels in 'pix' to white
  :answer_b: It is converting all the blue pixels in 'pix' to white
  :answer_c: It is converting all the green pixels in 'pix' to white
  :answer_d: It is converting all the red pixels in 'pix' to white
  :correct: d
  :feedback_a: Incorrect. Check the if-condition in the program again.
  :feedback_b: Incorrect. Check the if-condition in the program again.
  :feedback_c: Incorrect. Check the if-condition in the program again.
  :feedback_d: Correct!
  
   What is the following program doing for a given image 'Random.png' ?

   .. code-block:: matlab
  
     clc; clear;
     
     pix = imread('Random.png');
     
     [h, w, c] = size(pix);
     
     for ii = 1:1:h  
      for jj = 1:1:w  
         red = pix(ii, jj, 1);
         green = pix(ii, jj, 2);
         blue = pix(ii, jj, 3);
         if red == 255 && green == 0 and blue == 0
            pix(ii, jj, : ) = 255;
         end
      end
     end

.. mchoice:: aa-workingw/images_11_images_17
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: It is counting all the black pixels in 'pix'
  :answer_b: It is counting all the blue pixels in 'pix'
  :answer_c: It is counting all the green pixels in 'pix'
  :answer_d: It is counting all the red pixels in 'pix'
  :correct: c
  :feedback_a: Incorrect. Check the if-condition in the program again.
  :feedback_b: Incorrect. Check the if-condition in the program again.
  :feedback_c: Correct!
  :feedback_d: Incorrect. Check the if-condition in the program again.
  
   What is the following program doing for a given image 'Random.png' ?

   .. code-block:: matlab
  
     clc; clear;
     
     pix = imread('Random.png');
     
     [h, w, c] = size(pix);
     
     count = count + 1;
     
     for ii = 1:1:h
      for jj = 1:1:w
         red = pix(ii, jj, 1);
         green = pix(ii, jj, 2);
         blue = pix(ii, jj, 3);
         if red == 0 && green == 255 and blue == 0
            count = count + 1;
         end
      end
     end

.. mchoice:: aa-workingw/images_11_images_18
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: It is thresholding all the yellow pixels in 'pix'
  :answer_b: It is thresholding all the blue pixels in 'pix'
  :answer_c: It is thresholding all the green pixels in 'pix'
  :answer_d: It is thresholding all the red pixels in 'pix'
  :correct: a
  :feedback_a: Correct!
  :feedback_b: Incorrect. Check the if-condition in the program again.
  :feedback_c: Incorrect. Check the if-condition in the program again.
  :feedback_d: Incorrect. Check the if-condition in the program again.
  
   What is the following program doing for a given image 'Random.png' ?

   .. code-block:: matlab
  
     clc; clear;
     
     pix = imread('Random.png');
     
     [h, w, c] = size(pix);
     
     binary = false(h, w);
     
     for ii = 1:1:h
      for jj = 1:1:w
         red = pix(ii, jj, 1);
         green = pix(ii, jj, 2);
         blue = pix(ii, jj, 3);
         if red == 255 && green == 255 and blue == 0
            binary(ii, jj) = 1;
         end
      end
     end

.. mchoice:: aa-workingw/images_11_images_19
  :author: Ashish Aggarwal
  :practice: T
  :answer_a: It will return an ERROR
  :answer_b: It will display a black image
  :answer_c: It will display a white image
  :answer_d: It will neither display anything nor it will return an ERROR
  :correct: c
  :feedback_a: Incorrect. Here, true will put 1 in all the values of the binary image and thus the image will be white.
  :feedback_b: Incorrect. Here, true will put 1 in all the values of the binary image and thus the image will be white.
  :feedback_c: Correct!
  :feedback_d: Incorrect. Here, true will put 1 in all the values of the binary image and thus the image will be white.
  
   What will be the output of the following code snippet?

   .. code-block:: matlab
  
     clc; clear;
     
     binary = true(50, 50);
     
     imshow(binary);

.. fillintheblank:: aa-workingw/images_11_images_20
   :author: Ashish Aggarwal
   :practice: T
   :casei:

   What will be the output of the following snippet of code? (If the program will result in an error, put down 'ERROR')

    .. code-block:: matlab
  
     clc; clear;
     x = uint8(200);
     y = double(x) * 2;
     disp(x*2);

  - :255: Correct! 
    :x: Incorrect. Note, here y does convert the value of x when it is multiplied by 2, but that does not change the value/format of x. It is only for the calculation purposes that we use double(). But it does not change the format of the number x from uint8 to double.