Ansible
=======

Installation
------------

.. code-block:: console

    $ virtualenv ansible
    $ source ansible/bin/activate
    $ pip install ansible

.. note::

    On Windows, pycrypto installation fails.
    Install it first using:

    .. code-block:: console

        $ easy_install http://www.voidspace.org.uk/downloads/pycrypto26/pycrypto-2.6.win-amd64-py2.7.exe
        $ pip install ansible
