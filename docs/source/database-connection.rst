Setting a database connection
=====
To connect to our databases we use the Python package ``pyodbc``, which will be able to access our existing  :ref:`odbc-ref` ``.odbc.ini``.

.. _installation:

Installation
------------
Set-up your virtual environment
............
Go to your terminal, and type the following:

.. code-block:: console
   source create_virt_env.sh <name_of_your_env>

If you want to install an additional package, you have to activate your virtual environment in your terminal in the following manner:

.. code-block:: console
   source ~/.virtualenvs/<name_of_your_env>/bin/activate
   pip install <name_of_package>

Install necessary packages
............
To use ``pyodbc``, first install it using pip:

.. code-block:: console

   (name_of_your_venv) $ pip install pyodbc

Setting the connection
----------------

To retrieve a list of random ingredients,
you can use the ``lumache.get_random_ingredients()`` function:

.. autofunction:: lumache.get_random_ingredients

The ``kind`` parameter should be either ``"meat"``, ``"fish"``,
or ``"veggies"``. Otherwise, :py:func:`lumache.get_random_ingredients`
will raise an exception.

.. autoexception:: lumache.InvalidKindError

For example:

>>> import lumache
>>> lumache.get_random_ingredients()
['shells', 'gorgonzola', 'parsley']

Retrieving data
----------------

.. _odbc-ref
Generating your ODBC.ini
----------------
To get started with connecting to our databases, you need to generate an ``.odbc.ini`` file in your home folder. After you have created that 
