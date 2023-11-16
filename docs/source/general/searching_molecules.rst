Searching for Molecules
=======================

Before submitting a molecule, check if it already exists within the ATB database. This can be done by using a structure search or by using search terms to search through the database.

Structure Search
----------------

Finding a molecule in the ATB database using a structure can be done by navigating to the \"Structure Search"\  tab in the top navigation menu. Select the format of the coordinate file of the molecule you are searching for in the database. The ATB supports PDB, SDF, MOL and MOL2 coordinate files. 

Input the charge of your molecule.

Paste the contents of your file into the designated input box and press submit. 

If there is a matching molecule within the database it will appear beneath the submit button. Click on \"Show Molecule Page"\  to open a new tab that molecules information page. If you want to download the output files of this molecule please refer to the \"Downloading Outputs"\  page. There may be multiple versions of the molecule. These molecules can be compared so the version that is best suited to your work can be selected. For help in selecting the appropriate molecule for your work, please refer to the \"Comparing Molecules"\  section of this page. 

If a matching molecule is not within the ATB database you will see a message stating \"No matching molecules were found in the ATB database."\  beneath the submit button. The desired confirmation of your molecule may also not be available. If either of these are the case, please refer to the \"Submitting New Molecules"\  page. 

Database Search
---------------

Searching through the ATB database can also be done by navigating to the \"Existing Molecules"\  tab in the top navigation menu. You will be sent to a page with a number of search bars and a list of the 100 most recently processed molecules. 

You can search for the molecule in three ways.

* By entering a InChI key, IUPAC, common name, RNME or PDB hetID in the designated input box
* By entering the chemical formula of the desired molecule in the designated input box
* If known, putting the molID of the desired molecule in the designated input box. 

This search can be further refined to only include molecules that have clinical data available, molecules that have the experimental free energy available, molecules that are currently being processed, molecules that have had their tautomers enumerated, or a combination thereof by checking the appropriate boxes.

Once you click the \"Search"\  button, the list of molecules beneath the search bars will be reloaded to match your search terms. 

If you did not search for the molecule using molID you may be presented with multiple options that look appropriate for your work. For example, searching the ATB database using the search term ibuprofen yields multiple conformers of both possible enantiomers for the molecule. To know how to compare these molecules please refer to the \"Comparing Molecules"\  section of this page. 

If you cannot find the molecule you are looking for, you can submit the molecule for processing. For information on how to do this, please refer to the \"Submitting New Molecules"\  page.

Comparing Molecules
-------------------

A molecule page will have a list of other conformers of that have been submitted to the ATB. This list is beneath the \"Processing Information"\ . 

Each conformer will have a \"Compare with"\ button that you can click on, which will take you to a page which displays the GROMOS topology, and a RMSD Superposition of the reference molecule (green) and the molecule it is being compared with (blue). You can use these to determine which conformer is most suitable for your work. If none of the conformers will meaningfully affect the outcome of your work, choosing the one with the lowest QM energy is acceptable.
