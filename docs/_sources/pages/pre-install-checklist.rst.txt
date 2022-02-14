Installation Prerequisites
==========================

Before beginning installation, ensure that the following prerequisites are met:

GAMESS
------

A downloaded copy of `GAMESS <https://www.msg.chem.iastate.edu/gamess/>`_ is required to use ATB - Containerized Version.  

As per the `GAMESS User License Agreement <https://www.msg.chem.iastate.edu/gamess/License_Agreement.html>`_, GAMESS may not be redistributed.  

Please request a copy of GAMESS here by entering an e-mail address and selecting any of the Source Code Distributions.  A link will then be sent to you with download instructions.   

.. note::
    It may take up to several days to receive an e-mail with the GAMESS download link.
    
Once you have received the e-mail link, download the archive and note its location as it will be needed during installation.  The provided archive should not be extracted.  

Docker Hub Account
------------------

ATB - Containerized Version is distributed through `Docker Hub <https://hub.docker.com/>`_.  In order to access the container images referenced later in the installation procedure, your organization must first have `created a Docker Hub account <https://hub.docker.com/>`_ and contacted the ATB to request access to the repository containing your organization-specific container image.  

Note the name of this repository, as it will be required later in the installation procedure.  

ATB Server Credentials
----------------------

Along with access to the appropriate Docker Hub repository, your organization should have been provided with a container-specific set of administrator credentials for accessing the web interface of ATB - Containerized Version after deployment.  

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

System Environment
------------------

The installation procedure for ATB - Containerized Version involves the use of `Docker Engine <https://docs.docker.com/engine/>`_.  Docker Engine is presently available only for Linux.  

Users wishing to run ATB - Containerized Version on Windows should follow the subsequent installation instructions from within `WSL <https://docs.microsoft.com/en-us/windows/wsl/>`_.  

Users of other operating systems should configure a type-2 hypervisor running `a supported Linux distribution <https://docs.docker.com/engine/install/>`_ before proceeding.  
