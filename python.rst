python
======

setuptools
----------

`setuptools <http://pythonhosted.org/setuptools/>`_ is the de-facto standard
library for Python projects packaging.

setuptools provides the ``easy_install`` tool.

* On Windows, use the Cygwin package ``python-setuptools`` or ``python3-setuptools``.


pip
---

`pip <https://pip.pypa.io/>`_ is the de-facto standard package manager in the Python ecosystem.
We install it using setuptools' easy_install:

.. code-block:: console

    $ easy_install-3.4 pip
    $ easy_install-2.7 pip


virtualenv
----------

`virtualenv <https://virtualenv.pypa.io>`_ is a tool to create isolated Python
environments.

Installation:

.. code-block:: console

    $ pip2 install virtualenv

.. note::

    virtualenv is integrated with Python >= 3.3.
    Use the ``pyvenv-3.4`` command.


Sphinx
------

`Sphinx <http://sphinx-doc.org/>`_ is a tool to build documentations written
in `reStructuredText <http://docutils.sourceforge.net/rst.html>`_.

Installation:

.. code-block:: console

    $ pip3 install sphinx rstcheck
    $ pip2 install sphinx rstcheck

.. note::

    rstcheck is a static checker for reStructuredText documents,
    used by vim's syntastic plugin.
