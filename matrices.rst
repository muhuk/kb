Matrices
========

Identity Matrix
---------------

.. math::

    I_1 = \begin{bmatrix}
    1 \end{bmatrix}
    ,\
    I_2 = \begin{bmatrix}
    1 & 0 \\
    0 & 1 \end{bmatrix}
    ,\
    I_3 = \begin{bmatrix}
    1 & 0 & 0 \\
    0 & 1 & 0 \\
    0 & 0 & 1 \end{bmatrix}
    ,\ \cdots ,\
    I_n = \begin{bmatrix}
    1 & 0 & \cdots & 0 \\
    0 & 1 & \cdots & 0 \\
    \vdots & \vdots & \ddots & \vdots \\
    0 & 0 & \cdots & 1 \end{bmatrix}


Matrix Multiplication
---------------------

Also known as matrix product.

To be able to multiply two matrices, column count of the first matrix must be
equal to the row count of the first matrix.

.. math::

    [M \times P] * [P \times N] = [M \times N]


Resulting matrix has as many rows as the first operand and as many columns as
the second operand:

.. math::

    A = \begin{bmatrix}
    a_{0:0} & a_{0:1} & a_{0:2} \\
    a_{1:0} & a_{1:1} & a_{1:2} \\
    \end{bmatrix} \qquad B = \begin{bmatrix}
    b_{00} & b_{01} \\
    b_{10} & b_{11} \\
    b_{20} & b_{21} \\
    \end{bmatrix}

    C = A * B

    c_{i:j} = \sum_{k=1}^{3} a_{j:k} \, b_{k:j}

    C = \begin{bmatrix}
    \sum\limits_{k=1}^{3} a_{0:k} \, b_{k:0} & \sum\limits_{k=1}^{3} a_{0:k} \, b_{k:1} \\
    \sum\limits_{k=1}^{3} a_{1:k} \, b_{k:0} & \sum\limits_{k=1}^{3} a_{1:k} \, b_{k:1} \\
    \end{bmatrix}

Matrix multiplication is not a commutative operation.

.. math::

    A * B \neq B * A


Transposition
-------------

.. math::

   \forall x, y \quad M_{(x, y)}^T = M_{(y, x)}


Inversion
---------

To be invertible a matrix:

- Must be square. (Must have equal number of rows and column.)
- Determinant must **not** be zero.


Multiplying a matrix with its inverse yields identity matrix:

.. math::

   M * M^{-1} = M^{-1} * M = I


Gauss-Jordan Method
~~~~~~~~~~~~~~~~~~~

Elementary row operations are:

#. Swap rows.
#. Multiply (or divide) each element in a row with a constant
#. Add a multiple of another row to a row.

Gauss-Jordan method is applying elementary row operations to a matrix :math:`M`
until it is equal to identity vector and applying the same operations to identity
vector which ends up being :math:`M^{-1}`.

#. Ensure, for each column pivot (:math:`1`\ 's in identity matrix) is non-zero.
#. For each row set non-pivot values to zero.
#. Scale each pivot to one.

Example:

.. math::

    \begin{bmatrix}
    3 & 0 & 2 \\
    2 & 0 & -2 \\
    0 & 1 & 1 \\
    \end{bmatrix} \qquad \begin{bmatrix}
    1 & 0 & 0 \\
    0 & 1 & 0 \\
    0 & 0 & 1 \\
    \end{bmatrix}


Swap rows 1 & 2:

.. math::

    \begin{bmatrix}
    3 & 0 & 2 \\
    0 & 1 & 1 \\
    2 & 0 & -2 \\
    \end{bmatrix} \qquad \begin{bmatrix}
    1 & 0 & 0 \\
    0 & 0 & 1 \\
    0 & 1 & 0 \\
    \end{bmatrix}


All pivots are non-zero now. Add row 2 to row 0:

.. math::

    \begin{bmatrix}
    5 & 0 & 0 \\
    0 & 1 & 1 \\
    2 & 0 & -2 \\
    \end{bmatrix} \qquad \begin{bmatrix}
    1 & 1 & 0 \\
    0 & 0 & 1 \\
    0 & 1 & 0 \\
    \end{bmatrix}


Add to row 1, row 2 divided by 2:

.. math::

    \begin{bmatrix}
    5 & 0 & 0 \\
    1 & 1 & 0 \\
    2 & 0 & -2 \\
    \end{bmatrix} \qquad \begin{bmatrix}
    1 & 1 & 0 \\
    0 & 0.5 & 1 \\
    0 & 1 & 0 \\
    \end{bmatrix}


Add to row 1, row 0 multiplied by -0.2:

.. math::

    \begin{bmatrix}
    5 & 0 & 0 \\
    0 & 1 & 0 \\
    2 & 0 & -2 \\
    \end{bmatrix} \qquad \begin{bmatrix}
    1 & 1 & 0 \\
    -0.2 & 0.3 & 1 \\
    0 & 1 & 0 \\
    \end{bmatrix}


Add to row 2, row 0 multiplied by -0.4

.. math::

    \begin{bmatrix}
    5 & 0 & 0 \\
    0 & 1 & 0 \\
    0 & 0 & -2 \\
    \end{bmatrix} \qquad \begin{bmatrix}
    1 & 1 & 0 \\
    -0.2 & 0.3 & 1 \\
    -0.4 & 0.6 & 0 \\
    \end{bmatrix}


Multiply row 0 with 0.2 and row 2 with -0.5

.. math::

    \begin{bmatrix}
    1 & 0 & 0 \\
    0 & 1 & 0 \\
    0 & 0 & 1 \\
    \end{bmatrix} \qquad \begin{bmatrix}
    0.2 & 0.2 & 0 \\
    -0.2 & 0.3 & 1 \\
    0.2 & -0.3 & 0 \\
    \end{bmatrix}


Result:

.. math::

    \begin{bmatrix}
    3 & 0 & 2 \\
    2 & 0 & -2 \\
    0 & 1 & 1 \\
    \end{bmatrix}
    *
    \begin{bmatrix}
    0.2 & 0.2 & 0 \\
    -0.2 & 0.3 & 1 \\
    0.2 & -0.3 & 0 \\
    \end{bmatrix}
    =
    \begin{bmatrix}
    1 & 0 & 0 \\
    0 & 1 & 0 \\
    0 & 0 & 1 \\
    \end{bmatrix}
