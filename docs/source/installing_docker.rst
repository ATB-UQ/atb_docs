Installing Docker
=================

Installing Docker Engine
------------------------

ATB - Containerized Version uses `Docker Engine <https://docs.docker.com/engine/>`_ to both download and run the associated container.  

Distribution-specific instructions for installing Docker Engine are available `from Docker <https://docs.docker.com/engine/install/#server>`_.

.. warning::
    `Docker Desktop <https://www.docker.com/products/docker-desktop>`_ is a different product to Docker Engine and is distributed under a different license.  
    
    To avoid licensing issues, ensure that you select a download from the \"Server\" category rather than \"Desktop\".


After completing this step, confirm that the installation has completed correctly by checking the output of:

.. code-block:: bash

    docker

(Optional) Configure Docker to Be Managed by Non-Root User
----------------------------------------------------------

As per the `Docker Documentation <https://docs.docker.com/engine/install/linux-postinstall/>`_:
    
    The Docker daemon binds to a Unix socket instead of a TCP port. By default that Unix socket is owned by the user root and other users can only access it using sudo. The Docker daemon always runs as the root user.

    If you don\'t want to preface the docker command with sudo, create a Unix group called docker and add users to it. When the Docker daemon starts, it creates a Unix socket accessible by members of the docker group.


Instructions for configuring Docker commands to be run without being prefaced by ``sudo`` are available from `Docker <https://docs.docker.com/engine/install/linux-postinstall/>`_.

.. warning::
    If this optional step is skipped, all ``docker`` commands listed in the rest of these installation instructions should be run with ``sudo``.


