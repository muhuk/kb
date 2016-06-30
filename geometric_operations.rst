Geometric Operations
====================

Homogeneous Point
-----------------

Homogeneous coordinates are used to support translation.

.. math::

    P = \begin{bmatrix} x & y & z & 1 \end{bmatrix}


If the fourth component is not 1, the point can be normalized:

.. math::

    \begin{bmatrix} x & y & z & w \end{bmatrix} \to \begin{bmatrix} x \over w & y \over w & z \over w & 1 \end{bmatrix}


Translation
-----------

.. math::

    T(x, y, z) = \begin{bmatrix}
    1 & 0 & 0 & x \\
    0 & 1 & 0 & y \\
    0 & 0 & 1 & z \\
    0 & 0 & 0 & 1 \\
    \end{bmatrix}


Rotation
--------

.. math::

    R_x(\theta) = \begin{bmatrix}
    1 & 0 & 0 & 0 \\
    0 & \cos(\theta) & \sin(\theta) & 0 \\
    0 & -\sin(\theta) & \cos(\theta) & 0 \\
    0 & 0 & 0 & 1 \\
    \end{bmatrix}

    R_y(\theta) = \begin{bmatrix}
    \cos(\theta) & 0 & -\sin(\theta) & 0 \\
    0 & 1 & 0 & 0 \\
    \sin(\theta) & 0 & \cos(\theta) & 0 \\
    0 & 0 & 0 & 1 \\
    \end{bmatrix}

    R_z(\theta) = \begin{bmatrix}
    \cos(\theta) & \sin(\theta) & 0 & 0 \\
    -\sin(\theta) & \cos(\theta) & 0 & 0 \\
    0 & 0 & 1 & 0 \\
    0 & 0 & 0 & 1 \\
    \end{bmatrix}


Scaling
-------

.. math::

    S(x, y, z) = \begin{bmatrix}
    x & 0 & 0 & 0 \\
    0 & y & 0 & 0 \\
    0 & 0 & z & 0 \\
    0 & 0 & 0 & 1 \\
    \end{bmatrix}
