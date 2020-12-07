npreadtext
==========

Read text files (e.g. CSV or other delimited files) into a NumPy array.

Dependencies
------------

Requires NumPy::

    pip install -r requirements.txt

To run the numpy test suite via ``compat/`` you'll also need some of the
numpy testing dependencies, namely ``pytest`` and ``hypothesis``::

    pip install -r test_requirements.txt

Build/Install
-------------

To see the compiler output while building/installing,
``python setup.py build_ext -i`` or ``python setup.py install``.

If you don't want to see compiler output and just want a quick install step
(e.g. to test changes), ``pip install .``

Testing
-------

There are three sets of tests:

 - C-tests::

       cd src/ctests && source build_runtests.sh
       ./runtests

 - npreadtxt test suite::

       pytest .

 - Compatibility with ``np.loadtxt``::

       python compat/check_loadtxt_compat.py -t numpy.lib.tests.test_io::TestLoadTxt
