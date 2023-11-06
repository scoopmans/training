Getting started
================
Start by going to the SSO environment and starting a **JupyterLab** session. You will be auto-joined.

.. _installation:

Set-up your virtual environment
-------------------
Open a terminal, and type the following:

.. code-block:: console

   source create_virt_env.sh **<name_of_your_env>**

Installing packages
-----------------------
If you want to install an additional package (at a later stage), you have to activate your virtual environment in your terminal in the following manner:

.. code-block:: console

   source ~/.virtualenvs/**<name_of_your_env>**/bin/activate
   pip install <name_of_package>

Opening a notebook
----------------
You can now open a new Jupyter Notebook. When you are asked to choose a "Kernel", make sure you choose the virtual environment you have just made.

Cloning your GitHub repo
-------------
On the left side of your JupyterLab screen, the third button says "Git". Go there and select "Clone a Repository" to clone a new repository or choose "Open the FileBrowser" to select an existing Git project. In this panel, you can easily keep track of changes, see which branch you are working on and push/pull changes.

Setting database connection
---------------
To connect to our databases we use the Python package ``pyodbc``, which will be able to access our existing ``.odbc.ini``.

Ensure you have ``pyodbc`` installed
.............

Retrieving data
..............

Generating your ODBC.ini
..............
To get started with connecting to our databases, you need to generate an ``.odbc.ini`` file in your home folder. After you have created an empty file with the name ``.odbc.ini``, open that file and paste the following:

.. code-block:: console
