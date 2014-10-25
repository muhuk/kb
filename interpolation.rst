Interpolation
=============


Linear Interpolation
--------------------

1D
~~

.. math::

    x = (1 - r) x_a + r x_b \qquad (0 < r < 1, \quad x_a < x_b)


:math:`x_a` and :math:`x_b` are the values we are interpolating between,
:math:`r` is the interpolation factor.


2D
~~

.. math::

    z = z_{00} + x (z_{10} - z_{00}) + y (z_{01} - z_{00}) + x y (z_{00} - z_{01} - z_{10} + z_{11}) \qquad (0 < x < 1, \quad 0 < y < 1)


:math:`z_{00}, z_{01}, z_{10}, z_{11}` represent the corners of our area
sampled. :math:`x` and :math:`y` are the factors for x and y axes.
