Feature List
============

User Interface
--------------

* Submission of molecules with molecular drawer, SMILES or PDB file.
* Search a database of pre-calculate molecules with various descriptors including 3D structures. ref::
* Links molecules in other databases including `CheMBL <https://www.ebi.ac.uk/chembl/>`_, `RCSB PDB <https://www.rcsb.org/>`_, and `ChemSpider <http://www.chemspider.com/>`_. 
* Save molecules of interest
* Provision of an API for automated access to the database (on request).
* Tools to visualize and compare parameters for molecules submitted in alternative conformations and for users to flag problems with specific molecules. 
* A tool to match and reorder PDB files for identical molecules with alternative atom names and/or atom order: `PDB Match and Reorder <https://atb.uq.edu.au/index.py?tab=reorder_pdb>`_.

Parameter Generation
--------------------

* Lennard Jones parameters refined against experimental solvation and pure liquid properties.
* ATB parametrisation and validation is performed using a single-range 1.4 nm cutoff for both Lennard Jones and Coulomb interactions (see `FAQ <https://github.com/ATB-UQ/atb_docs/blob/main/docs/source/faq.rst>`_)
* Atomic charges fitted to QM electrostatic potentials at B3LYP/6-31G* level of theory (for molecules < 50 atoms).
* Robust symmetry routines to ensure identical parameters are assigned to chemically equivalent atoms, bonds and angles.
* Bonded parameter assignment using force constants estimated from Hessian (B3LYP/6-31G*, for molecules < 40 atoms).

Automated Calculation Pipeline
------------------------------
* Automated QM calculation pipeline with error recovery (low failure rate).
* Automated QM and MM energy minimised structure comparison.
* Automated calculation of solvation free energies (restricted).

Output Formats
--------------
* `GROMACS <www.gromacs.org>`_ (GROMOS 54A7).
* `GROMOS96 <https://www.gromos.net/>`_ (GROMOS 54A7).
* `GROMOS11 <https://www.gromos.net/>`_ (GROMOS 54A7).
* `LAMMPS <lammps.sandia.gov>`_ (GROMOS 54A7).
* `APBS <https://www.poissonboltzmann.org/>`_ (Adaptive Poisson-Boltzmann Solver) file format (.pqr).
* CNS (Crystallography & NMR System).
* CCD CIF (compatible with the `Phenix <https://phenix-online.org/>`_, `CCP4 <www.ccp4.ac.uk>`_, `Refmac5 <https://www.ccp4.ac.uk/html/refmac5.html>`_ and `CYANA <https://link.springer.com/article/10.1007/s10858-015-9959-y>`_ X-ray and NMR refinement packages).
* eLBOW CIF (compatible with the `Phenix <https://phenix-online.org/>`_ X-ray refinement packages).
* An extended and generalized mmCIF format incorporating a complete description of all force field parameters including units.
* `AMBER <http://ambermd.org/>`_ via a tool to convert GROMOS system topology files (.top) to the AMBER format (.prmtop).
