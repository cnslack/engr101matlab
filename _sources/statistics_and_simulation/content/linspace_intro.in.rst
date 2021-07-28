The examples we've been working with have mostly been about analyzing existing data. We tend to follow a similar pattern each time:

1. Read data in from a file
2. Look for some characteristics/process the data
3. Plot the data to see trends, patterns, extremes, etc.

MATLAB is also widely used to simulate data. When we simulate data, we also tend to follow a similar pattern each time:

1. Convert the math equations into a computer program
2. Create a starter set of data and use the computer program from step 1 to generate predicted data
3. Look for some things / process data / plot data to see trends, etc.

Math equations tend to look something like this:

.. math::

  y = sin(x)

We know that this equation is really saying: :math:`y` is equal to the sine of :math:`x` for all possible values of :math:`x`, no matter how big or small or precise those numbers are. You might be able to type

.. math::

  plot(sin)

into a graphing calculator and get a plot containing a sine wave because the graphing calculator knows that you probably mean: show me a plot of the values of the sine of :math:`x` vs. :math:`x` for all possible values of :math:`x`, no matter how big or small or precise those numbers are. But if we type

.. math::

  plot(sin)

into MATLAB, we get an error message because MATLAB doesn't know that we mean :code:`sin` to really mean :math:`sin(x)` and :math:`x` to be a variable with all possible values of :math:`x`. So MATLAB says " ¯\\_(ツ)_/¯ lol whatever" and gives us an error message.

To run a simulation in MATLAB, we first need to create a *starter set of data*. In Chapter 2, we created vectors and matrices, and we saw that range notation (:code:`start:step:last`) was quite convenient for creating a starter set of data. In our earlier attempt to plot :math:`sin(x)`, we noted that the plot function requires a set of ordered pairs, e.g. (x\ :sub:`1`,y\ :sub:`1`), (x\ :sub:`2`,y\ :sub:`2`), (x\ :sub:`3`,y\ :sub:`3`), etc. We can generate these easily using vectorized code!

.. raw:: html

  <div class="container-fluid">
    <style>
      .matcrab-wide-cells .matlab-scalar {
        width: 3em;
      }
    </style>
    <div class="matcrab-example matcrab-wide-cells" style="font-size: 8pt">
      <table><tbody>
        <tr>
          <td style="text-align: center">
            <img src="../_static/common/img/crabster.jpg" style="height: 35px" />
            <br />
            <a role="button" class="btn btn-success matcrab-run">Run</a>
            <br />
            <a role="button" class="btn btn-warning matcrab-reset">Reset</a>
          </td>
          <td>
            <div class="matcrab-workspace list-group matlab-vars"></div>
          </td>
        </tr>
        <tr>
          <td>
            <textarea class="form-control matcrab-entry" style="resize: none">
              x = 1:10;
              y = sin(x);
            </textarea>
          </td>
          <td>
            <div class="matcrab-vis" style="height: auto; width: auto">
            </div>
          </td>
        </tr>
      </tbody></table>
    </div>
  </div>

|

Now, if we call :code:`plot(x,y)`, we get a plot of :code:`sin(x)` using these values of :code:`x`.

.. figure:: img/Sine_1.png
  :width: 450
  :align: center
  :alt: A plot of sin(x) applied to the range x = 1:10.

To create a smoother plot of a math function, just use more data points. To do this with range notation, decrease the step size from the default of 1 to a new value, 0.1:

.. code-block:: matlab

  x = 1:0.1:10;
  y = sin(x);
  plot(x,y);

.. figure:: img/Sine_2.png
  :width: 450
  :align: center
  :alt: A plot of sin(x) applied to the range x = 1:0.1:10.

Another useful way to create a starter set of data is with the :code:`linspace` function. The :code:`linspace` function provides an alternate way to create evenly spaced vectors of numbers. Here is a comparison between linspace and range notation:

.. figure:: img/RangeNotationVsLinspace.png
  :width: 450
  :align: center
  :alt: A plot of sin(x) applied to the range x = 1:0.1:10.