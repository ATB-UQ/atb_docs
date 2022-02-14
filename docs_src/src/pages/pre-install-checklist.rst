Installation Prerequisites
==========================

Before beginning installation, ensure that the following prerequisites are met:

GAMESS
------

A downloaded copy of `GAMESS <https://www.msg.chem.iastate.edu/gamess/>`_ is required to use ATB - Containerized Version.  

As per the `GAMESS User License Agreement <https://www.msg.chem.iastate.edu/gamess/License_Agreement.html>`_, GAMESS may not be redistributed.  

Please request a copy of GAMESS from: `Download GAMESS <https://www.msg.chem.iastate.edu/gamess/License_Agreement.html>`_. You can select any of the Source Code Distributions.
A link will then be sent to you with download instructions.

.. note::
    It may take several days to receive an e-mail with the GAMESS download link.

Once you have received the e-mail link, download the archive and note its location as it will be needed during installation.  The provided archive does not require extraction.

Docker Hub Account
------------------

The preferred distribution method for the ATB - Containerized Version is through `Docker Hub <https://hub.docker.com/>`_, however, a tar file can be provided if required.

In order to access the container images referenced later in the installation procedure, you will need to have access to a Docker Hub account:
`created a Docker Hub account <https://hub.docker.com/>`_.
You will need to provide these account details to an ATB contact so that access can be grated to the repository containing your organization-specific container image.

.. note::
    The name of your organization-specific container image will be required later in the installation procedure.

ATB Server Credentials
----------------------

Along with access to the appropriate Docker Hub repository, your organization should have been provided with a
container-specific set of administrator credentials for accessing admin features on the web interface of the ATB - Containerized Version after deployment.

If you are not sure if your organization has received these credentials, please contact the ATB.


System Resource Requirements
----------------------------

.. warning::
    ATB - Containerized Version presently only supports x86-64 architectures. 

These specifications should be met to ensure a successful installation:

- 4-core processor
- 16 GB RAM
- 50 GB free storage space

.. note::
    Additional resources may be required to perform certain operations when running ATB - Containerized Version after installation.
    The ATB - Containerized Version runs computationally intensive quantum mechanical calculations with GAMESS on the host hardware.
    Parallelisation testing on typical ATB jobs has found GAMESS to be over 90% efficient on up to 48 CPU (results will depend on molecule size).
    Note that memory requirements scale with the size of the molecules being processed and insufficient memory allocation will result in a processing failure; 3 GB per CPU core is recommended.

System Environment
------------------

The current installation procedure for ATB - Containerized Version is limited to the use of `Docker Engine <https://docs.docker.com/engine/>`_ which is presently available only for Linux.

The ATB - Containerized Version can be easily installed with Docker Desktop, however, a paid subscription will be required for most organisations: `Docker Pricing <https://www.docker.com/pricing>`_.

Users wishing to run ATB - Containerized Version on Windows should follow the subsequent installation instructions from within `WSL <https://docs.microsoft.com/en-us/windows/wsl/>`_.  

Users of other operating systems should configure a type-2 hypervisor running `a supported Linux distribution <https://docs.docker.com/engine/install/>`_ before proceeding.

