Installing and Starting the ATB
===============================

Logging In
----------

Once docker is installed, use the following command to log into the Docker Hub account linked to the organization-specific repository provided by the ATB:

.. code-block:: bash

    docker login

Supply your Docker Hub username and password when prompted.

Pulling the Container
---------------------

Once logged in, pull the ATB container image from your organization-specific repository:

.. code-block:: bash

    docker pull YOURREPO

Replace ``YOUREPO`` with the full name of your organization-specific repository provided by the ATB. The full name should be in the format ``UPLOADERNAME/REPONAME``.

Starting the Container
----------------------

Now that the container has been pulled from the repository, start an instance of it using the following command:


.. code-block:: bash

   docker run -d -p 8080:80 --name atb-server -v atbvol:/atb YOUREPO

Again, remember to replace ``YOUREPO`` with the full name of your organization-specific repository.

.. note::
    Some of the arguments in the ``docker run`` command above can be modified if needed.  These include the host port (8080), container name (atb-server) and volume name (atbvol).
    Please note that the volume stil must be mounted in the location ``/atb`` irrespective of the volume name chosen.

An instance of the container should now be running.  Verify this by navigating to http://localhost:8080/ (assuming you used the default port number shown in the example above) in a web browser.  If you can see the ATB home page, the container has been successfully launched.  

Additional steps, however, must be completed for the local ATB server to function properly.  
