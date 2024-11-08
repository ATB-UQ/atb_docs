Installation Prerequisites
==========================

Before beginning installation, ensure that the following prerequisites are met:

GAMESS
------

A downloaded copy of `GAMESS <https://www.msg.chem.iastate.edu/gamess/>`_ is required to use ATB - Containerized Version.  

As per the `GAMESS User License Agreement <https://www.msg.chem.iastate.edu/gamess/License_Agreement.html>`_, GAMESS may not be redistributed.  

Please request a copy of GAMESS from `the GAMESS Registration System <https://www.msg.chem.iastate.edu/GAMESS/download/register/>`_ after reviewing the license agreement. You can select any of the Source Code Distribution options.
A link will then be sent to you with download instructions as well as a username and password to authenticate the download.  

.. note::
    It may take several days to receive an e-mail with the GAMESS download credentials.

Once you have received this e-mail, do not click on the link contained within.  Instead, use `this persistent download link <https://www.msg.chem.iastate.edu/GAMESS/download/source/gamess.Jul152024R2.tar.gz>`_ to the specific version of GAMESS used by the ATB.  Enter the username and password from the e-mail sent by GAMESS to begin the download.  Note the location the download is saved to, as it will be needed during installation.  The provided archive does not require extraction.

Docker Hub Account
------------------

.. note::
    The preferred distribution method for the ATB - Containerized Version is through `Docker Hub <https://hub.docker.com/>`_.  
    
    These installation instructions will assume your organization is using this distribution method.  
    
    Alternatively, a .tar archive containing ATB - Containerized Version can be provided upon request if required.

In order to access the container images referenced later in the installation procedure, you will need to have access to a Docker Hub account.  If your organization does not have access to one, you can create one
`here <https://hub.docker.com/signup>`_.

You will need to provide the details of your Docker Hub account to an ATB contact so that access can be granted to the repository containing your organization-specific container image.

.. note::
    The name of your organization-specific container image will be required later in the installation procedure.

ATB Server Credentials
----------------------

Along with access to the appropriate Docker Hub repository, your organization should have been provided with a container-specific set of administrator credentials for accessing admin features on the web interface of the ATB - Containerized Version after deployment.

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
    Additional resources may be required after installation to perform certain operations when running ATB - Containerized Version.
    
    The ATB - Containerized Version runs computationally-intensive quantum mechanical calculations with GAMESS on the host hardware.
    
    Parallelisation testing on typical ATB jobs has found GAMESS to retain up to 90% of single-core efficiency when utilizing up to 48 cores.  The exact efficiency of this scaling will depend on molecule size.
    Memory requirements also scale with the size of the molecules being processed. 
    
    Insufficient memory allocation will result in a processing failure; a minimum of 3 GB per CPU core is recommended.

System Environment
------------------

The current installation procedure for ATB - Containerized Version is limited to the use of `Docker Engine <https://docs.docker.com/engine/>`_ which is presently available only for Linux and is distributed under an open-source license.

The ATB - Containerized Version can alternatively be installed with Docker Desktop, however, this alternative will require a paid subscription for most organizations.  Licensing details for Docker Desktop are available here: `Docker Pricing <https://www.docker.com/pricing>`_.

Users wishing to run ATB - Containerized Version on Windows should follow the subsequent installation instructions from within `WSL <https://docs.microsoft.com/en-us/windows/wsl/>`_.  

Users of other operating systems should configure a type-2 hypervisor running `a supported Linux distribution <https://docs.docker.com/engine/install/>`_ before proceeding.
