Installing and Starting the ATB
===============================

Logging In
----------

Once docker is installed, use the following command to log into the Docker Hub account linked to your organization-specific repository:

.. code-block:: bash

    docker login
    
Supply your Docker Hub username and password when prompted.

Pulling the Container
---------------------

Once logged in, pull the ATB container image from your organization-specific repository:

.. code-block:: bash

    docker pull YOURREPO
    
Replace ``YOUREPO`` with the full name of your organization-specific repository.  The full name should be in the format ``UPLOADERNAME/REPONAME``.

Starting the Container
----------------------

Now that the container has been pulled from the repository, start an instance of it using the following command:


.. code-block:: bash

   docker run -d -p 8080:80 --name atb-server -v atbvol:/atb YOUREPO

Again, remember to replace ``YOUREPO`` with the full name of your organization-specific repository.

An instance of the container should now be running.  Additional steps, however, must be completed for the local ATB server to function properly.  


     
