unittest2six
============

.. image:: https://secure.travis-ci.org/msabramo/unittest2six.png
   :target: http://travis-ci.org/msabramo/unittest2six

Simple meta package to easily get unittest2_ functionality in both Python 2 and
Python 3.

**Note: You probably don't need this package anymore**. The unittest2_ package supports Python 3 since version 0.6.0 (released 2014-10-28).

This provides stuff that was added to unittest in the Python 2.7 stdlib and
backported to Python 2.6 with unittest2_. e.g.:

- ``assertIn``/``assertNotIn``
- ``assertIsInstance``/``assertNotIsInstance``
- ``assertRaises`` as a context manager
-  etc...

This module has no code. It's just a meta package that ``install_requires`` the
proper dependency:

- On Python 2, this ``install_requires`` unittest2_.
- On Python 3, this ``install_requires`` unittest2py3k_.

This is handy to have one dependency that you can use on both Python 2 and
Python 3 and not have to have separate pip requirements files and tox targets.


Compatibility
-------------

Results from Tox_::

    $ make test
    ...
    [TOX] py25: commands succeeded
    [TOX] py26: commands succeeded
    [TOX] py27: commands succeeded
    [TOX] py30: commands succeeded
    [TOX] py31: commands succeeded
    [TOX] py32: commands succeeded
    [TOX] congratulations :)
    ...
      py26: commands succeeded
      py27: commands succeeded
      py32: commands succeeded
      py33: commands succeeded
      py34: commands succeeded
      pypy: commands succeeded
      congratulations :)


See also
--------

- https://github.com/msabramo/unittest2/pull/1 -- This is a GitHub pull request
  for changes that I proposed to make to unittest2 to make it work in Python 3.


.. _unittest2: https://pypi.python.org/pypi/unittest2
.. _unittest2py3k: https://pypi.python.org/pypi/unittest2py3k
.. _Tox: http://tox.testrun.org/
