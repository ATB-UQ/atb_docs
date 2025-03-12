.. _FAQ:

FAQ
==========

What are the conditions of use?
-------------------------------
Access to the ATB is provided free to academic users from publically funded teaching or research institutions. Access for academic use is conditional on: i) any molecule submitted to the ATB being made publically available and ii) the source of any material downloaded from the ATB being properly acknowledged in any publications or other forms in which research using this material is disseminated. Use of the ATB by other parties, or academic users wishing to restrict the access of others to specific molecules, is considered to be commercial in nature. Commercial access is available by licence or collaborative agreement. Parties interested in commercial licencing or other arrangements should contact Prof Alan E. Mark. 

Why do I need a licensing or collaborative agreement for commercial use?
------------------------------------------------------------------------
The Automated Topology Builder (ATB) and Repository has been developed and is made publicly available with support from the University of Queensland (UQ), the Australian Research Council (ARC) and the Queensland Cyber Infrastructure Foundation (QCIF). The ATB also relies heavily on access to publicly funded computational resources. Specific arrangements are required for commercial use of these publicly funded facilities or if the results obtained are not made publicly available. A range of licensing and collaborative arrangements are possible and will be considered on a case-by-case basis depending on the intended use. 

Are there any advantages in being a commercial user?
----------------------------------------------------
Commercial users (or academic users operating under a collaborative agreement) can restrict access to molecules they submit, share molecules with groups of existing users and gain access to additional functionality depending on the nature of the agreement.

How can I find an existing molecule on the ATB?
----------------------------------------------
Under the "Existing Molecules" tab on the ATB there is a search utility under "Match" a field. One can search for a molecule using a molecular formula, IUPAC name, common name or Canonical SMILES. The easiest way to search is using a molecular formula as the primary search criteria and select the appropriate molecule from either IUPAC name and/or Canonical SMILES. For a more detailed explanation please refer to `this page <https://github.com/ATB-UQ/atb_docs/blob/main/docs/source/general/searching_molecules.rst>`_.

My submitted structure is already in the database, how can I use an existing ATB output with my submitted coordinates?
----------------------------------------------------------------------------------------------------------------------
The ATB site provides a tool for modifying the atom names, atom order and residue names of a query PDB file to match that of a reference PDB file: `PDB Match and Reorder <https://atb.uq.edu.au/index.py?tab=reorder_pdb>`_. This tool can be used to generate a PDB file which is compatible with an existing molecule in the ATB database while retaining a particular set of coordinates i.e. those of a ligand in a crystal structure. Your submitted conformation either matched the initial or optimised geometry of an existing entry, PDBs for both these geometries are available on the **Molecular Dynamics (MD) Files** tab of the matching molecule, under the subheading **Structure Files**. Thus you may need to test both the **All-Atom PDB (optimised geometry)** and **All-Atom PDB (original geometry)** structure files to match the submitted conformation. Note that in order to use this tool your query PDB will need to contain connectivity information, `OpenBabel <https://openbabel.org/>`_ can be used to generate connect records by performing a PDB-to-PDB conversion. 

Can I submit a ligand (heteromolecule) molecule as is from a PDB file?
----------------------------------------------------------------------
No. The ligand molecules in most PDB files only contain HEAVY ATOMS. The complete ligand molecule (with all HYDROGEN atoms and correct tautomeric and protonation states as well as its formal charge) must be submitted to the ATB. Only then isit possible for the ATB to generate a complete topology file. A range of programs such as `ArgusLab <http://www.arguslab.com/arguslab.com/Welcome.html>`_ or `Avogadro <https://avogadro.cc/>`_ can be used to edit the hydrogen atoms in a ligand molecule. 

By default the ATB only generates a complete topology for molecules containing < 40 atoms. How can I generate a reliable topology for a larger molecule?
-------------------------------
By default the ATB only generates a complete topology (based on optimization at the B3LYP/6-31G* level of theory + Hessian) for molecules containing < 40 atoms when submitted by an academic user. Molecules up to 50 atoms are optimization at the B3LYP/6-31G* level of theory but no Hessian is generated. The ATB will still generate an initial template for a larger molecules (< 500 atoms) based on semi-empirical methods. This template contains all atom-type information and bonded parameters. In some cases, initial estimates of the charges may also be given. Before use, these templates need to be examined and where necessary edited manually. In order to obtain more precise parameters, a larger molecule can be broken into smaller fragments and the parameters from these fragments can be used to complete the template of the larger molecule. 

Why are there limits on the number of atoms?
--------------------------------------------
A limit on the number of atoms for academic users is required due to the cost of processing large molecules. These limits can varied for commercial users. 

The 2D sketch of the molecule appears to be incorrect.
------------------------------------------------------
The 2D sketch is automatically generated with `OpenBabel <https://openbabel.org/>`_ which makes assumptions about the nature of the molecule.

To visualize the molecule as it is stored in the database select "Show Structure" from the "Select Output" table. 

How do I use the JSME builder?
------------------------------
#. For those of you who don't know much about JSME and JSMol, JSME on the left hand side is 2D molecule builder and JSMol on the right hand side is a molecule viewer in 3D.
#. The function of buttons on JSME molecule builder is straightforward, but it is still worth mentioning that the "white rectangular" shaped button is used to wipe out the molecule to rebuild from the start."+/-" labeled button can add and move hydrogen atoms to create ions. The the pike-shaped button works as chirality specifier. For more information about how to use JSME, please look in the `manual <https://www.webassign.net/jme/ks_jme_help.pdf>`_. 
#. To submit a molecule, you need to click on the pink button to feed and visualize the structure in Jmol before clicking submit to generate the structure in PDB format and close the popup window.

How can I generate a topology for a peptide/protein or polysaccharide?
----------------------------------------------------------------------
The ATB is designed to generate the force field topology for a ligand molecule (up to ~100 atoms). To generate larger polymeric molecules such as proteins or polysacharides there are specific tools (make_top in GROMOS and pdb2gmx in GROMACS) available to combine building block files containing individual amino acids or sugars to generate the complete topologies for a larger molecule. These building blocks are highly optimized and should be used in preference to the topologies generated directly by the ATB. 

Can I submit a ligand molecule containing a metal atoms such as metal:ligand complexes?
---------------------------------------------------------------------------------------
At present, the ATB has a limited capacity to handle metal ions. Currently, the GROMOS force field does not include paramaters for transition metals other than for Cu+, Cu2+, Zn2+ and Fe2+. If a molecule is submitted that contains other metal ions, the ATB will terminate after the generation of the initial template topology. To generate a complete topology file for a metal:ligand complex, each ligand should be submitted separately to the ATB. The parameters for the individual ligands can then be transferred to the template of the complete complete complex. The charges on the metal ion and any changes to the ligand topology would need to be added manually. We recommended to use ab initio quantum mechanical or density functional theory methods to study metal ion coordination in detail. 

Why does the 3D visualization with JSMol not work for some molecules?
---------------------------------------------------------------------
This occurs for manually curated molecules that are missing PDB files or have a PDB file with formatting issues. This does not indicate that there are issues with the associated forcefield files. 

Why are certain email addresses blocked?
----------------------------------------
The following emails providers are not accepted for commercial or academic access: gmail.* yahoo.* hotmail.* 163.* 126.* mail.ru qq.*outlook.* yandex.* ymail.* live.* msn.* icloud.* foxmail.*. We can only accept an email address that is affiliated with a business or academic institution. The reason we do not accept private email addresses is that we cannot verify whether or not the site is being used for academic purposes. We understand that some institutions do not not provide email addresses but we are unable to make exceptions. 

My molecule is symmetric but some of the parameters are not identical. 
----------------------------------------------------------------------
n some rare cases in which a molecules contains multiple diasteriotopic atoms in combination with higher order symmetry in the molecule the algorithm can fail to assign symmetry correctly (e.g. tartaric acid `molid 31488 <http://atb.uq.edu.au/molecule.py?molid=31488>`_). For this reason molecules with multiple diasteriotopic atoms should be checked manually. This problem should be addressed in future versions. 

The web browser times out while trying to communicate with the ATB server. 
--------------------------------------------------------------------------
There are two main reasons this can occur. The first is that the system is too large. The ATB is designed to process small molecules (or fragments of larger molecules). The system can also be used to generate templates for larger molecules into which parameters can be inserted by hand. Systems that are too large to process will either fail due to the system timing out or will be terminated automatically after the initial template is generated. The second main reason why the response to the system can be slow is that the database is backed up every evening. This occurs at approximately 22:00 or 10 pm Australian eastern time. Access to parts of the database is restricted during this process. 

During submission of a molecule I appear to be automatically logged off and have to login again. 
------------------------------------------------------------------------------------------------
Your login and authentication is based on your IP address. If your IP address changes during a session you will effectively be logged out. This can occur if your IP address is dynamically allocated and you change networks or wireless access points or in some cases if you are accessing the site via a proxy server. 

Additional Lennard Jones atom types used by the ATB e.g. HS14. 
--------------------------------------------------------------
Some of the Lennard Jones atom types used by the ATB are not found in the official GROMOS force field. If a molecule contains one of these atom types an updated parameter file is required and can be downloaded from that molecules page. Note that the updated parameter file will work for all molecules downloaded at that point in time, however it may become outdated in the future and a new version will be required. The additional Lennard Jones atom types are: 

* **HS14** - Polar hydrogen atoms in the Gromos force field are represented by a point charge (no Lennard Jones terms, type 21). A special polar hydrogen type (HS14) is used to prevent collapse of positively charged hydrogen atom onto a negatively charged atom at the 3rd neighbour position (1-4 interaction). The HS14 atom type has Lennard Jones terms but for the 1-4 interactions only (the value were taken from hydrogen atom type 20, used for apolar hydrogens). That is, only 1-4 interactions involving a HS14 atom have been changed by the use of this atom type in place of type 21 from the official GROMOS force field.
* **CLOpt** - Optimised aliphatic Chlorine parameter.
* **CLAro** - Optimised aromatic Chlorine parameter.
* **BROpt** - Optimised Bromine parameter.
* **I** - Iodine parameters have not been fully optimised but some parameterisation has been done. Note: for simulation with the GROMOS simulation package the correct mass (126.90447 amu) is replaced by 99.99 amu till a Gromos++ make_top bug is fixed.
* **B** - The Boron parameters have not been optimised, they have simply been copied from Carbon.
* **SE** - The Selenium parameters have not been optimised, they have simply been copied from Sulfur.

What cutoff scheme was used in the development of the ATB parameters?
---------------------------------------------------------------------
The ATB 3.0 parameters have been developed and tested for use with a single 1.4 nm cutoff and either a reaction field correct or Ewald summation for treating the long rang interactions. 

What cutoff scheme should I use with the GROMOS protein parameters in GROMACS?
------------------------------------------------------------------------------
In the current versions of GROMACS a single cutoff of at least 1.4 nm should be used for the Lennard-Jones interactions. A single Coulomb cutoff of 1.4 nm should be used with a reaction field. With Ewald summation and related techniques, a real space cutoff or at least 1.0 nm is recommended. 

Why can't the twin range approach be used in the latest versions of GROMACS?
----------------------------------------------------------------------------
The GROMOS protein force field was originally parametrized with a twin range 0.8/1.4 cutoff. This gives almost identical results to a single range 1.4 cutoff using a standard leap frog or velocity Verlet algorithm. The twin range method assumes the long-range forces evolve more slowly than the short-range forces. Note it also requires that the pairlist and long-range forces are updated regularly (~10 fs for a protein in water at ~300K) and cannot be used with the Verlet pairlist update scheme. The twin range cutoff cannot be used in GROMACS because the standard leap frog algorithm have been replaced by the Trotter expansion. This multi-time step approach allows different degrees of freedom to be integrated on different time scales. However, this is only correct if the degrees of freedom are decoupled. For example, due to the difference in frequency bond vibrations are largely decoupled from non-bonded interactions. The Trotter expansion cannot be used with a twin-range approach as the short-and long-range components are intrinsically coupled. A single range cutoff must be used instead. 

Moltemplate encounters an error when using ATB '.lt' files to generate LAMMPS input files.
------------------------------------------------------------------------------------------
Moltemplate version 2.5.1 (3rd October 2017) has a known bug that makes it incompatible with ATB outputs. This has been fixed in later versions, which can be downloaded via the Moltemplate website: `moltemplate.org <http://moltemplate.org/>`_. 

How do I generate a CYANA building block file?
----------------------------------------------
CYLIB compatible CIF files are located under the heading "PDB Chemical Component Dictionary (CCD) CIF" on the tab "X-Ray - Docking Files" on all molecule pages. To generate a CYANA building block file using CYLIB requires that:

#. the protein backbone of a molecule be capped in a standard way; and
#. the protein backbone atom names match a standard naming convention.

The capping requirement used for amino acids in the PDB CCD is a H- on the N-terminus and an OH- on the C-terminus. The non-zwiterionic form which is only stable in vacuum. The ATB database already contains 200+ amino acids molecules capped in this way e.g. `norleucine <http://atb.uq.edu.au/molecule.py?molid=32357#panel-xray>`_. More L-amino acids capped in this way can be found by searching for "(2S)-2-amino" on the "Existing Molecules" tab. The standard naming requirement has not yet been implemented. However, it is very easy to modify the files manually. The standard atom names along the backbone are: HXT, OXT, C, O, CA, N. 

Do I need to download a separate GROMOS54a7_ATB.ff for each molecule.
---------------------------------------------------------------------
The GROMOS54a7_ATB parameter file is progressively updated as required. The current version of the file includes all parameters required to describe the current molecule and all other molecules in the ATB database. As the name of the file suggests, this file also contains the parameters needed to describe all molecules that form part of the GROMOS 54A7 force field. This is so that the ATB and GROMOS 54A7 can be used in combination. Note that while some parameters are shared between the ATB and GROMOS 54A7, all molecules in the ATB have been parametrized independently using a fully automated procedures. For this reason the parameters assigned to a molecule by the ATB will not exactly match those assigned to equivalent (or similar) molecules in the GROMOS54A7 force field. For one, the procedure used to assign charges differs which has flow on effects. The key experimental data used for validation are nevertheless similar. 

Can I contribute to the development of the ATB?
-----------------------------------------------
Contributions to help further develop the functionality of the ATB either in the form of financial contributions or by assisting in the development of specific aspects of the code itself would be most welcome. 

How do I cite the Automated Topology Builder (ATB) and Repository?
------------------------------------------------------------------
The following papers describes the ATB and its validation: 

* Malde AK, Zuo L, Breeze M, Stroet M, Poger D, Nair PC, Oostenbrink C, Mark AE. An Automated force field Topology Builder (ATB) and repository: version 1.0. Journal of Chemical Theory and Computation, 2011, 7(12), 4026-4037. `DOI: 10.1021/ct200196m <https://pubs.acs.org/doi/abs/10.1021/ct200196m>`_
* Stroet M, Caron B, Visscher K, Geerke D, Malde AK, Mark AE. Automated Topology Builder version 3.0: Prediction of solvation free enthalpies in water and hexane. Journal of Chemical Theory and Computation 2018, 14(11), 5834-5845. `DOI:10.1021/acs.jctc.8b00768 <https://pubs.acs.org/doi/10.1021/acs.jctc.8b00768>`_

For ATB version 2.0 topologies please also cite:

* Canzar S, El-Kebir M, Pool R, Elbassioni K, Malde AK, Mark AE, Geerke DP, Stougie L, Klau GW. Charge Group Partitioning in Biomolecular Simulation. Journal of Computational Biology, 2013, 20, 188-198. `DOI:10.1089/cmb.2012.0239 <https://www.liebertpub.com/doi/10.1089/cmb.2012.0239>`_
* Koziara KB, Stroet M, Malde AK, Mark AE. Testing and validation of the Automated Topology Builder (ATB) version 2.0: prediction of hydration free enthalpies. Journal of Computer-Aided Molecular Design, 2014. `DOI: 10.1007/s10822-014-9713-7 <https://link.springer.com/article/10.1007/s10822-014-9713-7>`_

The following papers describe the various versions of the GROMOS force field used in the ATB. 

* Oostenbrink C, Villa A, Mark AE and van Gunsteren WF. A biomolecular force field based on the free enthalpy of hydration and solvation: The GROMOS force-field parameter sets 53A5 and 53A6. Journal of Computational Chemistry, 2004, 25, 1656-1676. `DOI: 10.1002/jcc.20090 <https://onlinelibrary.wiley.com/doi/abs/10.1002/jcc.20090>`_
* Poger D, Mark AE and van Gunsteren WF. A new force field for simulating phosphatidylcholine bilayers Journal of Computational Chemistry, 2010, 31, 1117-1125. `DOI: 10.1002/jcc.21396 <https://onlinelibrary.wiley.com/doi/abs/10.1002/jcc.21396>`_
* Poger D and Mark AE. On the Validation of Molecular Dynamics Simulations of Saturated and cis-Monounsaturated Phosphatidylcholine Lipid Bilayers: A Comparison with Experiment. Journal of Chemical Theory and Computation, 2010, 6, 325-336. `DOI: 10.1021/ct900487a <https://pubs.acs.org/doi/abs/10.1021/ct900487a>`_
* Schmid N, Eichenberger AP, Choutko A, Riniker S, Winger M, Mark AE and van Gunsteren WF. Definition and testing of the GROMOS force-field versions 54A7 and 54B7. European Biophysics Journal, 2011, 40, 843-856. `DOI: 10.1007/s00249-011-0700-9 <https://link.springer.com/article/10.1007/s00249-011-0700-9>`_
