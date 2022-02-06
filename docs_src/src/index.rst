********
ATB: Docker Version
********


-------------------
The ATB
-------------------

The ATB automates the generation of classical molecular force field parameters for user-submitted compounds.  Specifically, the ATB provides:


- Access to classical force fields in formats compatible with GROMACS, GROMOS and LAMMPS simulation packages and CNS, Phenix, CCP4, Refmac5 and CYANA X-ray and NMR refinement packages
- A GROMOS to AMBER topology file converter
- Optimised geometries for molecules in the database

These can be used in a wide range of applications:

- Studying biomolecule-ligand complexes
- Structure-based drug design
- Material engineering
- Refinement of x-ray crystal complexes

-------------------
Docker Version
-------------------

The Docker version of the ATB allows a user to deploy the ATB web interface and processing pipelines on a server for internal organizational use.  
This document explains the procedure for installing, running, and updating the Docker version of the ATB.


.. toctree::
   :caption: Getting started
   :maxdepth: 1

   install-docker/index
   install-container/index
   install-run/index
   
.. toctree::
   :caption: Using the ATB
   :maxdepth: 1

   running-login/index
   running-submit/index
   running-searching/index
   

.. toctree::
   :caption: About
   :maxdepth: 1

   faq
   changelog
   references
