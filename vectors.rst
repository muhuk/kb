Vectors
=======

Length of a Vector
------------------

.. math::

    \|\vec{V}\| = \sqrt{{\vec{V}.x}^2 + {\vec{V}.y}^2 + {\vec{V}.z}^2}


Result is a scalar.


Normalizing
-----------

.. math::

     \hat{V} = {\vec{V} \over { \| \vec{V} \| }}


Result is a vector with :math:`length = 1`.


Addition and Subtraction
------------------------

.. math::
    :nowrap:

    \begin{flalign*}
    \vec{C} & = \vec{A} + \vec{B}        & \vec{C} & = \vec{A} - \vec{B} \\
    \vec{C}.x & = \vec{A}.x + \vec{B}.x  & \vec{C}.x & = \vec{A}.x - \vec{B}.x \\
    \vec{C}.y & = \vec{A}.y + \vec{B}.y  & \vec{C}.y & = \vec{A}.y - \vec{B}.y \\
    \vec{C}.z & = \vec{A}.z + \vec{B}.z  & \vec{C}.z & = \vec{A}.z - \vec{B}.z
    \end{flalign*}


Result is a vector.


Multiplication and Division
---------------------------

With a scalar:

.. math::
    :nowrap:

    \begin{flalign*}
    \vec{B} & = \vec{A} \, k      & \vec{B} & = \frac{\vec{A}}{k} \\
    \vec{B}.x & = \vec{A}.x \, k  & \vec{B}.x & = \frac{\vec{A}.x}{k} \\
    \vec{B}.y & = \vec{A}.y \, k  & \vec{B}.y & = \frac{\vec{A}.y}{k} \\
    \vec{B}.z & = \vec{A}.z \, k  & \vec{B}.z & = \frac{\vec{A}.z}{k}
    \end{flalign*}


With another vector:

.. math::
    :nowrap:

    \begin{flalign*}
    \vec{C} & = \vec{A} \, \vec{B}       & \vec{C} & = \frac{\vec{A}}{\vec{B}} \\
    \vec{C}.x & = \vec{A}.x \, \vec{B}.x & \vec{C}.x & = \frac{\vec{A}.x}{\vec{B}.x} \\
    \vec{C}.y & = \vec{A}.y \, \vec{B}.y & \vec{C}.y & = \frac{\vec{A}.y}{\vec{B}.y} \\
    \vec{C}.z & = \vec{A}.z \, \vec{B}.z & \vec{C}.z & = \frac{\vec{A}.z}{\vec{B}.z}
    \end{flalign*}


Result is a vector.


Dot Product
-----------

.. math::

    \vec{A} \cdot \vec{B} = \vec{A}.x * \vec{B}.x + \vec{A}.y * \vec{B}.y + \vec{A}.z * \vec{B}.z


Result is a scalar.

Length can be derived from dot product of vector with itself:

.. math::

    \|\vec{V}\| = \sqrt{\vec{V} \cdot \vec{V}}


Dot product is a commutative operation:

.. math::

    \vec{A} \cdot \vec{B} = \vec{B} \cdot \vec{A}


Dot product of two unit vectors is the cosine of the angle between:

.. math::

    \hat{A} \cdot \hat{B} & = \cos(\theta) \\
    \vec{A} \cdot \hat{B} & = \|\vec{A}\| \cos(\theta) \\
    \vec{A} \cdot \vec{B} & = \|\vec{A}\| \, \|\vec{B}\| \cos(\theta) \\
    \theta & = \arccos(\frac{\vec{A} \cdot \vec{B}}{\|\vec{A}\| \, \|\vec{B}\|})


Cross Product
-------------

.. math::

    \vec{C} & = \vec{A} \times \vec{B} \\
    \vec{C}.x & = \vec{A}.y \, \vec{B}.z - \vec{A}.z \, \vec{B}.y \\
    \vec{C}.y & = \vec{A}.z \, \vec{B}.x - \vec{A}.x \, \vec{B}.z \\
    \vec{C}.z & = \vec{A}.x \, \vec{B}.y - \vec{A}.y \, \vec{B}.x


Result is a vector.

Cross product is anticommutative:

.. math::

    \vec{A} \times \vec{B} \neq \vec{B} \times \vec{A}

    \vec{C} = \vec{A} \times \vec{B} \iff \vec{B} \times \vec{A} = -\vec{C}


Spherical Coordinates
---------------------

:math:`\phi` is the angle that lies on xy plane. :math:`\theta` is the angle
perpendicular to xy plane.

.. math::
    :nowrap:

    \begin{align*}
    \phi & = \arctan\left({y \over x}\right) & 0 \le \phi \le 2\pi \\
    \theta & = \arccos(z) & 0 \le \theta \le \pi
    \end{align*}


Spherical coordinates can be converted to a unit vector using:

.. math::

    x & = cos(\phi) \, sin(\theta) \\
    y & = sin(\phi) \, sin(\theta) \\
    z & = cos(\theta)
