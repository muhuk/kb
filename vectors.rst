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

Vec3 operator + (const Vec3<T> &v) const { return Vec3<T>(x + v.x, y + v.y, z + v.z); }
Vec3 operator * (const T &val) const { return Vec3<T>(x * val, y * val, z * val); }
Vec3 operator / (const T &val) const { T invVal = T(1) / val; return Vec3<T>(x * invVal, y * invVal, z * invVal); }
Vec3 operator / (const Vec3<T> &v) const { return Vec3<T>(x / v.x, y / v.y, z / v.z); }
Vec3 operator * (const Vec3<T> &v) const { return Vec3<T>(x * v.x, y * v.y, z * v.z); }
Vec3 operator - (const Vec3<T> &v) const { return Vec3<T>(x - v.x, y - v.y, z - v.z); }
Vec3 operator - () const { return Vec3<T>(-x, -y, -z); }

.. math::

    \vec{C} & = \vec{A} + \vec{B} \\
    \vec{C}.x & = \vec{A}.x + \vec{B}.x \\
    \vec{C}.y & = \vec{A}.y + \vec{B}.y \\
    \vec{C}.z & = \vec{A}.z + \vec{B}.z


.. math::

    \vec{C} & = \vec{A} - \vec{B} \\
    \vec{C}.x & = \vec{A}.x - \vec{B}.x \\
    \vec{C}.y & = \vec{A}.y - \vec{B}.y \\
    \vec{C}.z & = \vec{A}.z - \vec{B}.z


Multiplication and Division
---------------------------

.. math::

    \vec{B} & = \vec{A} \, k \\
    \vec{B}.x & = \vec{A}.x \, k \\
    \vec{B}.y & = \vec{A}.y \, k \\
    \vec{B}.z & = \vec{A}.z \, k


.. math::

    \vec{C} & = \vec{A} \, \vec{B} \\
    \vec{C}.x & = \vec{A}.x \, \vec{B}.x \\
    \vec{C}.y & = \vec{A}.y \, \vec{B}.y \\
    \vec{C}.z & = \vec{A}.z \, \vec{B}.z


.. math::

    \vec{B} & = \frac{\vec{A}}{k} \\
    \vec{B}.x & = \frac{\vec{A}.x}{k} \\
    \vec{B}.y & = \frac{\vec{A}.y}{k} \\
    \vec{B}.z & = \frac{\vec{A}.z}{k}


.. math::

    \vec{C} & = \frac{\vec{A}}{\vec{B}} \\
    \vec{C}.x & = \frac{\vec{A}.x}{\vec{B}.x} \\
    \vec{C}.y & = \frac{\vec{A}.y}{\vec{B}.y} \\
    \vec{C}.z & = \frac{\vec{A}.z}{\vec{B}.z}


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
