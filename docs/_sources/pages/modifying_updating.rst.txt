Saving a container
------------------

If you are interested in commiting (saving) your changes to your docker instance you just need to run the following
command:

.. code-block:: python

    docker commit atb-server updated-atb-server


This will save your updates to the container that was originally created **atb-server** to a new conatiner named
**updated-atb-sever**. Now to run the new container you would run:

.. code-block:: python

    docker run -d -p 8080:80 --name updated-atb-sever -v atbvol:/atb atb


If you want to run both at the same time you would need to use a different port to **8080**, e.g. **8181**.


Updating a container
--------------------

Updates to the container will be hosted on docker-hub and you can pull the image as so (this is private so you'll need
 a login). Note, your changes if you have updated your container (e.g. with users, or molecules) will be overridden in
this update.

.. code-block:: python

    docker pull atb_docker


If you have updated your container you will need to export your database (as **SQL**) before updating the container.
You will then need to add this SQL to the updated container, this can be performed via the following two commands:

First make sure you have an instance of your **atb-server** running, then to export the database run:

.. code-block:: python

    docker exec atb-server /usr/bin/mysqldump -u root --password=THE_PASSWORD_WE_GAVE_YOU atb > backup_atb.sql


Now after pulling the new version of the docker instance, you need to insert the database back in using the following
command:

.. code-block:: python

    docker exec atb-server  /usr/bin/mysql -u root --password=THE_PASSWORD_WE_GAVE_YOU atb < backup_atb.sql


This should now all work. 
