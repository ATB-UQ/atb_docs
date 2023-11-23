Methodology
===========

The ATB uses a knowledge-based approach in combination with QM calculations to assign force field parameters. 

A submitted molecule is initially optimised at the HF/STO-3G (or AM1 or PM3) level of theory after which an initial draft output is available. Molecules with < 50 atoms are then re-optimised at the B3LYP/6-31G* level of theory with the PCM implicit solvent model for water. The QM electrostatic potential (ESP) is then calculated from the B3LYP optimised structure from which the ATB uses to obtain ESP fitted charges. Finally the QM Hessian is calculated for molecules with < 40 atoms which is used to improve the assignment of bond and angle terms.

The parameter assignment includes the following steps:

* The molecular topology is constructed from on the PDB connectivity records with the bond, angle and dihedral (torsion) degrees of freedom identified.
* Atoms are reordered to reflect the atom connectivity.
* Atom types and masses are obtained from the submitted PDB file.
* An initial list of 1-2 and 1-3 exclusions is generated based on connectivity. 
* The symmetry within the molecules is determined and used subsequently to ensure chemically equivalent groups are assigned identical parameters.
* Atomic charges are obtained for all-atom and united-atom models by fitting directly to QM ESP surfaces.
* Bond and angle types are assigned based on (1) element types, (2) bond lengths or bond angles in the QM optimised geometry and (3) matching force constants derived from the Hessian (where available). Multiple options are listed in ambiguous cases and new types introduced if required.
* Dihedral parameters are assigned based on (1) multiplicity (as determined from the connectivity and substituents) (2) the phase shift (3) atom element types involved.
* Aromatic rings and planar groups are identified based on atom type, connectivity and the optimised geometry.
* Particular 1-4 exclusions are introduced e.g. aromatic systems to prevent buckling of planer structures.
* Molecular building block files are produced in a range of formats.
