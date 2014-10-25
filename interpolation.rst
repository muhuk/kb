Interpolation
=============


General Form
------------

.. math::

    v = \mathrm{F}(a, b, r) \qquad & a \le \mathrm{F}(a, b, r) \le b, \\
                                   & 0 \le r \le 1


:math:`\mathrm{F}`
  Interpolation function.

:math:`a, b`
  Values to interpolate between.

:math:`r`
  Interpolation factor.


To Interpolate in n dimensions, apply 1D interpolation recursively to collapse
them one by one. Until there is only a scalar value:

.. math::

    v_n = \mathrm{F}(\mathrm{F}(\cdots, \cdots, r_{n-1}),\mathrm{F}(\cdots, \cdots, r_{n-1}), r_n)

This would mean :math:`2^n-1` applications of :math:`\mathrm{F}`.


Linear Interpolation
--------------------

1D
~~

.. math::

    x = (1 - r) x_a + r x_b \qquad & 0 \le r \le 1, \\
                                   & x_a \le x_b


:math:`x_a, x_b`
  Values to interpolate between.

:math:`r`
  Interpolation factor.


2D
~~

.. math::

    z = z_{00} + x (z_{10} - z_{00}) + y (z_{01} - z_{00}) + x y (z_{00} - z_{01} - z_{10} + z_{11}) \qquad & 0 \le x \le 1, \\
                                                                                                            & 0 \le y \le 1


:math:`z_{00}, z_{01}, z_{10}, z_{11}`
  Values to interpolate between.

:math:`x, y`
  Interpolation factors.


Cosine Interpolation
--------------------

1D
~~


.. math::

    x = x_a + \frac{1 - \cos(\pi r)}{2} (x_b - x_a) \qquad 0 \le r \le 1


:math:`x_a, x_b`
  Values to interpolate between.

:math:`r`
  Interpolation factor.


2D
~~

.. math::
    :nowrap:

    \begin{align*}
    z = & \frac{z_{0} (1 + \cos(\pi x) + z_{1} (1 - \cos(\pi x)}{2} \\
    z_0 = & \frac{z_{00} (1 + \cos(\pi y) + z_{01} (1 - \cos(\pi y)}{2} \\
    z_1 = & \frac{z_{10} (1 + \cos(\pi y) + z_{11} (1 - \cos(\pi y)}{2} \\
    & 0 \le x \le 1 \\
    & 0 \le y \le 1
    \end{align*}


:math:`z_{00}, z_{01}, z_{10}, z_{11}`
  Values to interpolate between.

:math:`x, y`
  Interpolation factors.


Cubic Interpolation
-------------------

.. math::
    :nowrap:

    \begin{align*}
    x = & A r^3 + B r^2 + C r + D \\
    A = & (x_3 - x_2) - (x_0 - x_1) \\
    B = & (x_0 - x_1) - A \\
    C = & x_2 - x_0 \\
    D = & x_1 \\
    & 0 \le r \le 1 \\
    & x_0 \le x_1 \le x \le x_2 \le x_3
    \end{align*}


:math:`x_0, x_1, x_2, x_3`
  Values to interpolate between.

:math:`r`
  Interpolation factor.


Bezier Curve
------------


.. math::

    x = (1 - r)^3 x_0 + 3 (1 - r)^2 r x_1 + 3 (1 - r) r^2 x_2 + r^3 x_3


Optimized:

.. math::
    :nowrap:

    \begin{align*}
    x = & A r^3 + B r^2 + C r + D \\
    A = & x_3 - 3 x_2 + 3 x_1 - x_0 \\
    B = & 3 x_2 - 6 x_1 + 3 x_0 \\
    C = & 3 x_1 - 3 x_0 \\
    D = & x_0 \\
    & 0 \le r \le 1 \\
    & x_0 \le x_1 \le x \le x_2 \le x_3
    \end{align*}

:math:`x_0, x_1, x_2, x_3`
  Values to interpolate between.

:math:`r`
  Interpolation factor.
