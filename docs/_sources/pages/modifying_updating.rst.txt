Committing Changes to a Container
---------------------------------

It may be desirable to save changes made to the filesystem of the container to a new image.  To do this, execute the following command:

.. code-block:: bash

    docker commit atb-server name-of-new-container

Execution of this command will result in the current state of the **atb-server** container being saved to a new container named **name-of-new-container**.  This new container can be run using the same commands as used to run the **atb-server** container in any of the other instructions given in this documentation.

Execute the following command to start the new container:

.. code-block:: bash

    docker run -d -p 8080:80 --name name-of-new-container -v atbvol:/atb atb

To run two containers simultaneously, change the port binding (e.g. **8080** to **8181**) to ensure that conflicts do not exist between running containers.

Updating ATB - Containerized Version
------------------------------------

Updates to ATB - Containerized Version will be released on Docker Hub and can be pulled in the same manner described in Installing and Starting the ATB.  

.. Warning::
    Pulling a new container will overwrite all modifications to the container (e.g. all user accounts, all submitted molecules).  To retain this information, it is     essential to export the relevant database first by following these instructions

First make sure you have an instance of your **atb-server** running, then to export the database run:

.. code-block:: bash

    docker exec atb-server /usr/bin/mysqldump -u root --password=THE_PASSWORD_WE_GAVE_YOU atb > backup_atb.sql

Then, pull the updated container from Docker Hub using the following command:

.. code-block:: bash

    docker pull atb_docker

Finally, after pulling the new version of the container, import the database from the backup:

.. code-block:: bash

    docker exec atb-server  /usr/bin/mysql -u root --password=THE_PASSWORD_WE_GAVE_YOU atb < backup_atb.sql
