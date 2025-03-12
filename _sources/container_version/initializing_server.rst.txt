Initializing the ATB Database
=============================

After building GAMESS, the ATB server database must be initialized before many functions of the site can be used.

.. warning::
    Many critical aspects of the ATB web interface will not function correctly if the server is not initialized by submitting a molecule as described in these instructions.

Logging in as Administrator
---------------------------

Access the web interface for the server from: http://0.0.0.0:8080/

Navigate to the \"Login\" tab of the top navigation menu and enter your organization-specific administrator username (in the email address field) and password.

Submitting Your First Molecule
------------------------------

ATB - Containerized Version as provided in the container is is provided with an uninitialized (empty) database.  To submit your first molecule and initialize the database, navigate to the \"Submit\" tab of the top navigation menu and select the following options:

- Molecule type: heteromolecule
- Net charge (e): 0
- Coordinates: 4 - Paste PDB
- Visibility: Public

In the field provided for pasting a PDB structure, paste the following PDB structure for methane with pre-optimized geometry:

.. code-block::

    HETATM    1   H5 METH    0       0.904   0.005  -0.617  1.00  0.00           H
    HETATM    2   C1 METH    0      -0.000  -0.000   0.000  1.00  0.00           C
    HETATM    3   H2 METH    0      -0.010   0.888   0.638  1.00  0.00           H
    HETATM    4   H3 METH    0      -0.010  -0.898   0.625  1.00  0.00           H
    HETATM    5   H4 METH    0      -0.883   0.005  -0.646  1.00  0.00           H
    CONECT    1    2
    CONECT    2    1    3    4    5
    CONECT    3    2
    CONECT    4    2
    CONECT    5    2

.. note::
    Any PDB structure (or structure from the JME builder) can be submitted to initialize the database.  Methane has been provided as an example as it is a small molecules and the coordinates above correspond to an already-optimized geometry. This results in a short processing time.
    
Click \"Next\" to view a preview of your submission, then click \"Submit This Molecule\" to finalize your submission.  

After your molecule has been successfully submitted, ATB - Containerized Version should now be ready for use.   

You can monitor the progress of your submitted molecule (as well as all other notifications that are typically delivered via e-mail on the live ATB server) from the \"Notifications\" tab of the Admin drop-down interface: http://0.0.0.0:8080/index.py?tab=notifications
