.. _installing:

Installing ATB docker
=====================


Installing Docker
-------------------

Install docker as per the documentation at `docker <https://docs.docker.com/get-docker/>`_.

Confirm docker is installed by verifying the following command runs:

.. code-block:: python

    docker

Installing ATB Docker Instance from File
------------------------------
Once docker is installed, download the ATB docker tar, this is approximately 9.8Gb (a link to the tar file is provided
when you buy a license with us, see our main `website <https://atb.uq.edu.au/>`_).

.. code-block:: python

    wget http://atb.uq.edu.au/example_link_to_docker_atb.tar


Load the docker image (may take a few minutes).

.. code-block:: python

    docker load -i atb-docker.tar


Running an instance
-------------------

.. code-block:: python

    docker run -d -p 8080:80 --name atb-server -v atbvol:/atb atb




.. list-table::
   :widths: 10 10
   :header-rows: 1

   * - ATB Release
     - Version
   * - 1
     - 3.0.0

Installing ATB Docker Instance from Docker Hub
------------------------------
Once docker is installed, ensure you have access to the ATB Docker Hub repository.  Then pull the image from the repository using the following command:

.. code-block:: python

    docker pull martinstroet/atb-dev:atb-dev


Running an instance
-------------------

.. code-block:: python

   docker run -d -p 8080:80 --name atb-server -v atbvol:/atb
martinstroet/atb-dev:atb-dev


.. list-table::
   :widths: 10 10
   :header-rows: 1

   * - ATB Release
     - Version
   * - 1
     - 3.0.0


