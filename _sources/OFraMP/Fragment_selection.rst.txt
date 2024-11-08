Selecting Fragments
===================

Once you have imported your target molecule into OFraMP, you can start building it with fragments from pre-paramtrised molecules from the ATB database. An example target molecule is displayed in the image below.

.. image:: images/Loaded_target_OFraMP_molecule.png
   :width: 80%

To begin selecting fragments click on an atom group.

.. image:: images/select_atom_group.png
   :width: 67%

Its information will appear on a window to the left of the target molecule. This information includes the number of atoms in the atom group, the number of atoms in the group that have been parametrised, and any charges that may have been assigned to those atoms. If no charges have yet been assigned, the sections that show this information will be blank.

.. image:: images/atom_selection_window.png
   :width: 30%

A list of potential fragments that include the selected atom group will appear on a window to the right of the target molecule. The fragments are in descending order of the likelihood of it being the best match. 

.. image:: images/found_fragments_window.png
   :width: 30%

Click on one of the fragments in the list to view its prompts.

.. image:: images/view_fragment_options.png
   :width: 80%

You can view the pre-parametrised molecule the fragment is being pulled from by clicking 'Show molecule'.

.. image:: images/show_molecule_fragment.png
   :width: 67%

Click 'Select fragment' to use it for the parametrisation of your target molecule.

.. image:: images/select_fragment.png
   :width: 80%

Once you have selecteded a fragment, the atom groups in the target molecule will be coloured a light green.

.. image:: images/light_green_selected_fragment.png
   :width: 67%

Continue to select fragments until the target molecule has been fully parametrised. Some atom groups in your target molecule may be coloured red. These are `missing charges <https://atb-uq.github.io/atb_docs/OFraMP/OFraMP_information_page.html#>`_

Charge Clashes
--------------

The atom groups of selected atoms may overlap. The charge of the overlapping atom group may differ in each fragment. Atom groups with clashing charges will be coloured yellow in the target molecule. 

.. image:: images/charge_clash.png
   :width: 67%

If an fragment with a conflicting charge is selected, the window below will load. It will ask you to resolve the clash.

.. image:: images/charge_clash_window.png
   :width: 60%

You can resolve the clash by averaging the charges, by using the charge from the newly selected fragment, the current charge, or a custom charge.

.. image:: images/choose_clash_solution.png
   :width: 60%

Click 'Apply solution'.

.. image:: images/apply_clash_solution.png
   :width: 60%

Once your target molecule is fully parametrised, you can `send its charges to the ATB <https://atb-uq.github.io/atb_docs/OFraMP/Sending_charges_to_the_ATB.html>`_

