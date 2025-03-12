Logging In
----------

Once docker is installed, use the following command to log into the Docker Hub account linked to your organization-specific repository:

.. code-block:: bash

    docker login
    
Supply your Docker Hub username and password when prompted.

Pulling the Container
---------------------

Once logged in, pull the ATB container image from your organization-specific repository.

.. code-block:: bash

    docker pull YOURREPO
    
Replace ``YOUREPO`` with the full name of your organization-specific repository.  The full name should be in the format ``UPLOADERNAME/REPONAME``.

Once docker is installed, ensure you have access to the ATB Docker Hub repository.  Then pull the image from the repository using the following command:


.. code-block:: bash

   docker run -d -p 8080:80 --name atb-server -v atbvol:/atb martinstroet/atb-dev:atb-dev


Load the docker image (may take a few minutes).

.. code-block:: bash

    docker load -i atb-docker.tar


Running the Container
---------------------

.. code-block:: python

    docker run -d -p 8080:80 --name atb-server -v atbvol:/atb atb





     
