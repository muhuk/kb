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
