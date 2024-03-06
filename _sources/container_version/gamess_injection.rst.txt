Installing GAMESS
=================

With the ATB container running, navigate to the folder containing the downloaded copy of GAMESS mentioned in the Installation Prerequisites.  

From the directory containing the download, copy the archive into the root directory of the running ATB container:

.. code-block:: bash

    docker cp gamess-current.tar.gz atb-server:/

Then run the following command to build GAMESS inside the running ATB container:
    
.. code-block:: bash

    docker exec atb-server /build_GAMESS.sh 

.. note::
    Building GAMESS typically takes between 15 and 20 minutes.
