=======
History
=======

2.9.2 (2022-07-20)
------------------

* Fix an issue where taking powers of units was backwards-incompatible with previous
  versions of ``unyt`` when the exponent is not zero. See `PR #249
  <https://github.com/yt-project/unyt/pull/249>`_. Thank you to Clément Robert
  (@neutrinoceros on GitHub) for the contribution.
* The import time for ``unyt`` has been reduced by skipping version checking of
  other packages. See `PR #251
  <https://github.com/yt-project/unyt/pull/251>`_. Thank you to Clément Robert
  (@neutrinoceros on GitHub) for the contribution.

2.9.0 (2022-07-14)
------------------

* Dropped support for Python 3.6 and 3.7.
* Added support for Python 3.8, 3.9 and 3.10.
* Fix an issue where SI prefixes of the ``degC`` units would give incorrect
  values in conversions. See `PR #176
  <https://github.com/yt-project/unyt/pull/176>`_. Thank you to Lee Johnston
  (@l-johnston on GitHub) for the contribution.
* Fix an issue when using ``matplotlib_support``, plot an empty unyt array,
  would result in an error when changing units. See `PR #180
  <https://github.com/yt-project/unyt/pull/180>`_. Thank you to Josh Borrow
  (@JBorrow on GitHub) for the contribution.
* Fix an issue where units would be printed twice in formatted strings with
  an ``unyt_array`` embedded. See `PR #188
  <https://github.com/yt-project/unyt/pull/188>`_. Thank you to Clément Robert
  (@neutrinoceros on GitHub) for the contribution.
* Add a method to parse a ``unyt_quantity`` from a string expression. See `PR #191
  <https://github.com/yt-project/unyt/pull/191>`_. Thank you to Clément Robert
  (@neutrinoceros on GitHub) for the contribution.
* Fix an issue where a ``unyt_array`` with dtype int8 could not be converted
  to a different unit. See `PR #197
  <https://github.com/yt-project/unyt/pull/197>`_. Thank you to Clément Robert
  (@neutrinoceros on GitHub) for the contribution.
* The import time for ``unyt`` has been reduced. See `PR #199
  <https://github.com/yt-project/unyt/pull/199>`_. Thank you to Clément Robert
  (@neutrinoceros on GitHub) for the contribution.
* Fix an issue where taking an ``unyt_array`` or ``unyt_quantity`` to a zero
  power would retain the units of the original array or quantity instead of
  converting to a dimensionless array. See `PR #204
  <https://github.com/yt-project/unyt/pull/204>`_. Thank you to Josh Borrow
  (@JBorrow on GitHub) for the contribution.
* Add support for coercing iterables of ``unyt_array`` objects with nonuniform
  dimensionally equivalent units to a single ``unyt_array``. See `PR #211
  <https://github.com/yt-project/unyt/pull/211>`_. Thank you to Nathan Goldbaum
  (@ngoldbaum on GitHub) for the contribution.
* Add the civil engineering units ``pli``, ``plf``, ``psf``, ``kli``, ``klf``,
  and ``ksf``. See `PR #217 <https://github.com/yt-project/unyt/pull/217>`_.
  Thank you to @osnippet on GitHub for the contribution.
* Fix typos in constants and unit prefixes. See `PR #218
  <https://github.com/yt-project/unyt/pull/218>`_. Thank you to Clément Robert
  (@neutrinoceros on GitHub) for the contribution.
* Fix an issue where multiplying a 1-element ``unyt_array`` would return a
  ``unyt_quantity``. See `PR #225 <https://github.com/yt-project/unyt/pull/225>`_.
  Thank you to Clément Robert (@neutrinoceros on GitHub) for the contribution.
* Add the Rydberg constant ``R_∞`` and unit ``Ry``, add the dimension
  ``angular_frequency`` and the unit ``rpm``, and increase the precision of
  Avogadro's number. See `PR #228 <https://github.com/yt-project/unyt/pull/228>`_.
* Fix an issue where ``np.divide.reduce`` would return incorrect units for ``unyt_array``
  instances. See `PR #230 <https://github.com/yt-project/unyt/pull/230>`_.
  Thank you to Kyle Oman (@kyleaoman on GitHub) for the contribution.


2.8.0 (2020-10-05)
------------------

* Dropped support for Python 3.5.
* Add ``delta_degC`` and ``delta_degF`` units to support temperature difference
  arithmetic. See `PR #152
  <https://github.com/yt-project/unyt/pull/152>`_. Thank you to Lee Johnston
  (@l-johnston on GitHub) for the contribution.
* Fix an issue where a subsequent load of the unit registry with units that are
  equal but not identical leads to a crash. See `PR #158
  <https://github.com/yt-project/unyt/pull/158>`_. Thank you to Matthew Turk
  (@matthewturk on GitHub) for the initial bug report and fix.
* Add force unit ``kip`` and pressure unit ``psi``. Thank you to P. Talley
  (@otaithleigh on GitHub) for the contribution. See `PR #162
  <https://github.com/yt-project/unyt/pull/162>`_.
* Fix an issue where arithmetic operations on units defined in different
  registries and having the conversion defined in one direction would lead to a
  crash.  See `PR #164 <https://github.com/yt-project/unyt/pull/164>`_. Thank
  you to Clément Robert (@neutrinoceros on GitHub) for the initial bug report
  and fix.


2.7.2 (2020-06-29)
------------------

* The ``unyt.returns`` and ``unyt.accepts`` decorators now work correctly for
  functions that accept or return data with dimensionless units. See `PR #146
  <https://github.com/yt-project/unyt/pull/146>`_. Thank you to Simon Schopferer
  (@simfinite on GitHub) for the initial bug report and fix.
* Data used in the tests are packaged with the source distribution and
  ``unyt.test()`` is now itself run as part of unyt's continuous integration
  tests. See `PR #149 <https://github.com/yt-project/unyt/pull/149>`_ and `PR
  #150 <https://github.com/yt-project/unyt/pull/150>`_. Thank you to Miguel de
  Val-Borro (@migueldvb on GitHub) for the initial bug report and fix.
* The ``degC`` and ``degF`` units now render as ``°C`` and ``°F`` by default,
  ``°C`` and ``°F`` are now recognized as valid unit names as well. Thank you to
  Lee Johnston (@l-johnston on GitHub) for the contribution.
* Use a more canonical representation of the micro symbol when printing units
  with the micro prefix, avoiding issues with displaying unit names in
  Matplotlib plot labels. See `PR #153
  <https://github.com/yt-project/unyt/pull/153>`_. Thank you to Matthew Turk
  (@matthewturk on GitHub) for the bug report and fix.
* Add more alternative spellings for solar units. See `PR #155
  <https://github.com/yt-project/unyt/pull/155>`_. Thank you to Clément Robert
  (@neutrinoceros on GitHub) for the initial bug report.


2.7.1 (2020-02-17)
------------------

* Fix compatibility with ``unyt_array`` subclasses that do not have the new
  ``name`` argument in their initializer. See `PR #140
  <https://github.com/yt-project/unyt/pull/140>`_.
* Fix an issue where custom units added to a unit registry were not restored
  correctly when reloading a unit registry from a JSON or pickle
  representation. See `PR #140 <https://github.com/yt-project/unyt/pull/140>`_.

2.7.0 (2020-02-06)
------------------

* The ``unyt_array`` and ``unyt_quantity`` classes now have a new, optional
  ``name`` attribute. The primary purpose of this attribute is to enable
  automatic generation of matplotlib plot labels. The ``name`` attribute is
  propagated through unit conversions and copies but is not propagated through
  mathematical operations. See `PR #129
  <https://github.com/yt-project/unyt/pull/129>`_ and the documentation for
  details.
* Add support for the ``Neper`` and ``Bel`` units with logarithmic
  dimensions. This includes support for the ``decibel`` unit. Note that
  logarithmic units can only be used with other logarithmic units and must be
  applied and stripped manually. See `PR #133
  <https://github.com/yt-project/unyt/pull/133>`_ and `PR #134
  <https://github.com/yt-project/unyt/pull/134>`_.
* Add support for the SI unit of inductance, ``H``. See `PR #135
  <https://github.com/yt-project/unyt/pull/135>`_.
* Fix formatting of error message produced when raising a quantity to a power
  with units. See `PR #131
  <https://github.com/yt-project/unyt/pull/131>`_. Thank you to Lee Johnston
  (@l-johnston on GitHub) for all of the above contributions.
* Fix incorrect unit metadata when loading a pickled array saved by
  ``yt.units``. See `PR #137 <https://github.com/yt-project/unyt/pull/137>`_.


2.6.0 (2020-01-22)
------------------

* Matplotlib support is no longer enabled by importing ``unyt``. Instead, it is
  now necessary to use the ``unyt.matplotlib_support`` context manager in code
  where you want unyt to automatically generate plot labels. Enabling Matplotlib
  support by default in the previous release caused crashes in previously
  working code for some users so we have decided to make the plotting support
  optional. See the documentation for more details. We are sorry for introducing
  a new feature that broke some user's code. See `PR #126
  <https://github.com/yt-project/unyt/pull/126>`_. Thank you to Lee Johnston
  (@l-johnston on GitHub) for the contribution.
* Updated the contribution guide to include more details about setting up
  multiple Python versions for the ``tox`` tests.

2.5.0 (2020-01-20)
------------------

* Importing unyt now registers unyt with Matplotlib's interface for handling
  units. See the `Matplotlib
  <https://matplotlib.org/gallery/units/units_scatter.html>`_ and `unyt
  <https://unyt.readthedocs.io/en/latest/usage.html#plotting-with-matplotlib>`_
  documentation for more details. See `PR #122
  <https://github.com/yt-project/unyt/pull/122>`_ and `PR #124
  <https://github.com/yt-project/unyt/pull/124>`_. Thank you to Lee Johnston
  (@l-johnston on GitHub) for the contribution.
* Updated the LaTeX formatting of solar units so they do not get rendered
  italicized. See `PR #120
  <https://github.com/yt-project/unyt/pull/120>`_. Thank you to Josh Borrow
  (@JBorrow on GitHub) for the contribution.
* Reduce floating point round-off error when data are converted from integer to
  float dtypes. See `PR #119 <https://github.com/yt-project/unyt/pull/119>`_.

2.4.1 (2020-01-10)
------------------

* Add support for the latest releases of h5py, sympy, NumPy, and PyTest. See `PR
  #115 <https://github.com/yt-project/unyt/pull/115>`_.
* Fix the hash implementation so that identical units cannot have distinct
  hashes. See `PR #114 <https://github.com/yt-project/unyt/pull/114>`_ and `PR
  #117 <https://github.com/yt-project/unyt/pull/114>`_. Thank you to Ben Kimock
  (@saethlin on GitHub) for the contribution.

2.4.0 (2019-10-25)
------------------

* Improve performance for creating quantities or small arrays via multiplication
  with a unit object. Creating an array or quantity from data that does not have
  a numeric dtype will now raise ``UnitOperationError`` instead of
  ``UnitDtypeError``, which has been removed. See `PR #111
  <https://github.com/yt-project/unyt/pull/111>`_.
* Comparing data with units that have different dimensions using the ``==`` and
  ``!=`` operators will no longer raise an error. Other comparison operators
  will continue to raise errors. See `PR #109
  <https://github.com/yt-project/unyt/pull/109>`_.
* Fixed a corner case in the implementation of ``clip``. See `PR #108
  <https://github.com/yt-project/unyt/pull/108>`_. Thank you to Matthew Turk
  (@matthewturk on GitHub) for the contribution.
* Added ``%`` as a valid dimensionless unit with a value of ``0.01``, also
  available under the name ``percent``. See `PR #106
  <https://github.com/yt-project/unyt/pull/106>`_. Thank you to Thomas Hisch for
  the contribution.
* Added ``bar`` to the default unit lookup table. See `PR #103
  <https://github.com/yt-project/unyt/pull/103>`_. Thank you to Thomas Hisch
  (@thisch on GitHub) for the contribution.

2.3.1 (2019-08-21)
------------------

* Added support for the ``clip`` ufunc added in NumPy 1.17. See `PR #102
  <https://github.com/yt-project/unyt/pull/102>`_.

2.3.0 (2019-08-14)
------------------

* Added ``unyt.dimensions.accepts`` and ``unyt.dimensions.returns``, decorators
  that can be used to ensure that data passed into a decorated function has
  units that are dimensionally consistent with the function's expected
  inputs. See `PR #98 <https://github.com/yt-project/unyt/pull/94>`_. Thank you
  to Andrei Berceanu (@berceanu on GitHub) for the contribution.
* Added ``unyt.allclose_units`` and improved documentation for writing tests for
  code that uses ``unyt``. This is a wrapper for ``numpy.allclose`` that also
  checks the units of the input arrays. See `PR #94
  <https://github.com/yt-project/unyt/pull/94>`_. Thank you to Andrei Berceanu
  (@berceanu on GitHub) for the contribution.

2.2.2 (2019-07-03)
------------------

* Fix erroneous conversions of E&M units to their "native" unit system,
  for example, converting Gauss to CGS units would return Tesla and converting
  Tesla to MKS units would return Gauss. See `PR #96
  <https://github.com/yt-project/unyt/pull/96>`_.

2.2.1 (2019-07-02)
------------------

* Add support for loading JSON unit registries saved by ``yt.units``.
  See `PR #93 <https://github.com/yt-project/unyt/pull/93>`_.
* Correct the value of the ``light_year`` unit.
  See `PR #93 <https://github.com/yt-project/unyt/pull/93>`_.
* It is now possible to define a ``UnitSystem`` object with a quantity.
  See `PR #86 <https://github.com/yt-project/unyt/pull/86>`_.
* Incorrect units for Planck units have been fixed.
  See `PR #85 <https://github.com/yt-project/unyt/pull/85>`_. Thank you to
  Nathan Musoke (@musoke on GitHub) for the contribution.
* Updated value of Newton's constant to latest CODATA value.
  See `PR #84 <https://github.com/yt-project/unyt/pull/84>`_.

2.2.0 (2019-04-03)
------------------

* Several performance optimizations. This includes a slight change to the behavior
  of MKS/CGS E&M unit conversions that makes the conversion rules slightly more relaxed.
  See `PR #82 <https://github.com/yt-project/unyt/pull/82>`_.

2.1.1 (2019-03-27)
------------------

* Fixed an issue with restoring unit registries from JSON output. See `PR #81
  <https://github.com/yt-project/unyt/pull/81>`_.

2.1.0 (2019-03-26)
------------------

This release includes a few minor new features and bugfixes for the 2.0.0 release.

* Added support for the matmul ``@`` operator. See `PR #80
  <https://github.com/yt-project/unyt/pull/80>`_.
* Allow defining unit systems using ``Unit`` instances instead of string unit
  names. See `PR #71 <https://github.com/yt-project/unyt/pull/71>`_. Thank you
  to Josh Borrow (@JBorrow on GitHub) for the contribution.
* Fix incorrect behavior when ``uhstack`` is called with the ``axis``
  argument. See `PR #73 <https://github.com/yt-project/unyt/pull/73>`_.
* Add ``"rsun"``, ``"lsun"``, and ``"au"`` as alternate spellings for the
  ``"Rsun"``, ``"Lsun"``, and ``"AU"`` units. See `PR #77
  <https://github.com/yt-project/unyt/pull/77>`_.
* Improvements for working with code unit systems. See `PR #78
  <https://github.com/yt-project/unyt/pull/78>`_.
* Reduce impact of floating point round-off noise on unit comparisons. See `PR
  #79 <https://github.com/yt-project/unyt/pull/79>`_.

2.0.0 (2019-03-08)
------------------

``unyt`` 2.0.0 includes a number of exciting new features as well as some
bugfixes. There are some small backwards incompatible changes in this release
related to automatic unit simplification and handling of dtypes. Please see the
release notes below for more details. If you are upgrading from ``unyt 1.x`` we
suggest testing to make sure these changes do not siginificantly impact you. If
you run into issues please let us know by `opening an issue on GitHub
<https://github.com/yt-project/unyt/issues/new>`_.

* Dropped support for Python 2.7 and Python 3.4. Added support for Python 3.7.
* Added ``Unit.simplify()``, which cancels pairs of terms in a unit expression
  that have inverse dimensions and made it so the results of ``unyt_array``
  multiplication and division will automatically simplify units. This means
  operations that combine distinct dimensionally equivalent units will cancel in
  many situations. For example

  .. code-block::

     >>> from unyt import kg, g
     >>> print((12 * kg) / (4 * g))
     3000.0 dimensionless

  older versions of ``unyt`` would have returned ``4.0 kg/g``. See `PR #58
  <https://github.com/yt-project/unyt/pull/58>`_ for more details. This change
  may cause the units of operations to have different, equivalent simplified
  units than they did with older versions of ``unyt``.
* Added the ability to resolve non-canonical unit names to the equivalent
  canonical unit names. This means it is now possible to refer to a unit name
  using an alternative non-canonical unit name when importing the unit from the
  ``unyt`` namespace as well as when a unit name is passed as a string to
  ``unyt``. For example:

  .. code-block::

     >>> from unyt import meter, second
     >>> data = 1000.0 * meter / second
     >>> data.to("kilometer/second")
     unyt_quantity(1., 'km/s')
     >>> data.to("metre/s")
     unyt_quantity(1000., 'm/s')

  The documentation now has a table of units recognized by ``unyt`` along with
  known alternative spellings for each unit.
* Added support for unicode unit names, including ``μm`` for micrometer and ``Ω``
  for ohm. See `PR #59 <https://github.com/yt-project/unyt/pull/59>`_.
* Substantially improved support for data that does not have a ``float64``
  dtype. Rather than coercing all data to ``float64`` ``unyt`` will now preserve
  the dtype of data. Data that is not already a numpy array will be coerced to a
  dtype by calling ``np.array`` internally. Converting integer data to a new
  unit will convert the data to floats, if this causes a loss of precision then
  a warning message will be printed. See `PR #55
  <https://github.com/yt-project/unyt/pull/55>`_ for details. This change may
  cause data to be loaded into ``unyt`` with a different dtype. On Windows the
  default integer dtype is ``int32``, so data may begin to be recognized as
  ``int32`` or converted to ``float32`` where before it was interpreted as
  ``float64`` by default.
* Unit registries are now associated with a unit system. This means that it's
  possible to create a unit registry that is associated with a non-MKS unit
  system so that conversions to "base" units will end up in that non-MKS
  system. For example:

  .. code-block::

     >>> from unyt import UnitRegistry, unyt_quantity
     >>> ureg = UnitRegistry(unit_system="cgs")
     >>> data = unyt_quantity(12, "N", registry=ureg)
     >>> data.in_base()
     unyt_quantity(1200000., 'dyn')

  See `PR #62 <https://github.com/yt-project/unyt/pull/62>`_ for details.
* Added two new utility functions, ``unyt.unit_systems.add_constants`` and
  ``unyt.unit_systems.add_symbols`` that can populate a namespace with a set of
  unit symbols in the same way that the top-level ``unyt`` namespace is
  populated. For example, the author of a library making use of ``unyt`` could
  create an object that users can use to access unit data like this:

  .. code-block::

      >>> from unyt.unit_systems import add_symbols
      >>> from unyt.unit_registry import UnitRegistry
      >>> class UnitContainer:
      ...     def __init__(self):
      ...         add_symbols(vars(self), registry=UnitRegistry())
      ...
      >>> units = UnitContainer()
      >>> units.kilometer
      km
      >>> units.microsecond
      μs

  See `PR #68 <https://github.com/yt-project/unyt/pull/68>`_.
* The ``unyt`` codebase is now automatically formatted by `black
  <https://github.com/ambv/black>`_. See `PR #57
  <https://github.com/yt-project/unyt/pull/57>`_.
* Add missing "microsecond" name from top-level ``unyt`` namespace. See `PR
  #48 <https://github.com/yt-project/unyt/pull/48>`_.
* Add support for ``numpy.argsort`` by defining ``unyt_array.argsort``. See `PR
  #52 <https://github.com/yt-project/unyt/pull/52>`_.
* Add Farad unit and fix issues with conversions between MKS and CGS
  electromagnetic units. See `PR #54
  <https://github.com/yt-project/unyt/pull/54>`_.
* Fixed incorrect conversions between inverse velocities and ``statohm``. See
  `PR #61 <https://github.com/yt-project/unyt/pull/61>`_.
* Fixed issues with installing ``unyt`` from source with newer versions of
  ``pip``. See `PR #63 <https://github.com/yt-project/unyt/pull/62>`_.
* Fixed bug when using ``define_unit`` that caused crashes when using a custom
  unit registry. Thank you to Bili Dong (@qobilidob on GitHub) for the pull
  request. See `PR #64 <https://github.com/yt-project/unyt/pull/64>`_.

We would also like to thank Daniel Gomez (@dangom), Britton Smith
(@brittonsmith), Lee Johnston (@l-johnston), Meagan Lang (@langmm), Eric Chen
(@ericchen), Justin Gilmer (@justinGilmer), and Andy Perez (@sharkweek) for
reporting issues.

1.0.7 (2018-08-13)
------------------

Trigger zenodo archiving.

1.0.6 (2018-08-13)
------------------

Minor paper updates to finalize JOSS submission.

1.0.5 (2018-08-03)
------------------

``unyt`` 1.0.5 includes changes that reflect the peew review process for the
JOSS method paper. The peer reviewers were Stuart Mumfork (`@cadair
<https://github.com/cadair>`_), Trevor Bekolay (`@tbekolay
<https://github.com/tbekolay>`_), and Yan Grange (`@ygrange
<https://github.com/ygrange>`_). The editor was Kyle Niemeyer (`@kyleniemeyer
<https://github.com/kyleniemeyer>`_). The ``unyt`` development team thank our
reviewers and editor for their help getting the ``unyt`` paper out the door as
well as for the numerous comments and suggestions that improved the paper and
package as a whole.

In addition we'd like to thank Mike Zingale, Meagan Lang, Maksin Ratkin,
DougAJ4, Ma Jianjun, Paul Ivanov, and Stephan Hoyer for reporting issues.

* Added docstrings for the custom exception classes defined by ``unyt``. See `PR
  #44 <https://github.com/yt-project/unyt/pull/44>`_.
* Added improved documentation to the contributor guide on how to run the tests
  and what the PR review guidelines are. See `PR #43
  <https://github.com/yt-project/unyt/pull/43>`_.
* Updates to the text of the method paper in response to reviewer
  suggestions. See `PR #42 <https://github.com/yt-project/unyt/pull/42>`_.
* It is now possible to run the tests on an installed copy of ``unyt`` by
  executing ``unyt.test()``. See `PR #41
  <https://github.com/yt-project/unyt/pull/41>`_.
* Minor edit to LICENSE file so GitHub recognizes it. See `PR #40
  <https://github.com/yt-project/unyt/pull/35>`_. Thank you to Kyle Sunden
  (`@ksunden <https://github.com/ksunden>`_) for the contribution.
* Add spatial frequency as a dimension and added support in the ``spectral``
  equivalence for the spatial frequency dimension. See `PR #38
  <https://github.com/yt-project/unyt/pull/38>`_ Thank you to Kyle Sunden
  (`@ksunden <https://github.com/ksunden>`_) for the contribution.
* Add support for Python 3.7. See `PR #37
  <https://github.com/yt-project/unyt/pull/35>`_.
* Importing ``unyt`` will now fail if ``numpy`` and ``sympy`` are not
  installed. See `PR #35 <https://github.com/yt-project/unyt/pull/35>`_
* Testing whether a unit name is contained in a unit registry using the Python
  ``in`` keyword will now work correctly for all unit names. See `PR #31
  <https://github.com/yt-project/unyt/pull/31>`_.
* The aliases for megagram in the top-level unyt namespace were incorrectly set
  to reference kilogram and now have the correct value. See `PR #29
  <https://github.com/yt-project/unyt/pull/29>`_.
* Make it possible to take scalars to dimensionless array powers with a properly
  broadcasted result without raising an error about units. See `PR #23
  <https://github.com/yt-project/unyt/pull/23>`_.
* Whether or not a unit is allowed to be SI-prefixable (for example, meter is
  SI-prefixable to form centimeter, kilometer, and many other units) is now
  stored as metadata in the unit registry rather than as global state inside
  ``unyt``. See `PR #21 <https://github.com/yt-project/unyt/pull/21>`_.
* Made adjustments to the rules for converting between CGS and MKS E&M units so
  that errors are only raised when going between unit systems and not merely
  when doing a complicated unit conversion invoving E&M units. See `PR #20
  <https://github.com/yt-project/unyt/pull/20>`_.
* ``round(q)`` where ``q`` is a ``unyt_quantity`` instance will no
  longer raise an error and will now return the nearest rounded float.
  See `PR #19 <https://github.com/yt-project/unyt/pull/19>`_.
* Fixed a typo in the readme. Thank you to Paul Ivanov (`@ivanov
  <https://github.com/ivanov>`_) for `the fix
  <https://github.com/yt-project/unyt/pull/16>`_.
* Added smoot as a unit. See `PR #14
  <https://github.com/yt-project/unyt/pull/14>`_.

1.0.4 (2018-06-08)
------------------

* Expand installation instructions
* Mention paper and arxiv submission in the readme.

1.0.3 (2018-06-06)
------------------

* Fix readme rendering on pypi

1.0.2 (2018-06-06)
------------------

* Added a paper to be submitted to the Journal of Open Source Software.
* Tweaks for the readme

1.0.1 (2018-05-24)
------------------

* Don't use setup_requires in setup.py

1.0.0 (2018-05-24)
------------------

* First release on PyPI.
* unyt began life as a submodule of yt named yt.units.
* It was separated from yt.units as its own package in 2018.
