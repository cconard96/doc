Components
~~~~~~~~~~

Hardware component management information is visible in the `Components` tab.

.. image:: /modules/assets/images/component.png
   :alt: Components screen
   :align: center

.. note::

   The creation / management of components can be found in the menu :doc:`Setup > Components <.../configuration/components>`.

.. note::
   If several components of the same type are used they will be grouped together.

   .. image:: /modules/assets/images/component_group.png
      :alt: Component groups
      :align: center

You can add a component by selecting the type from the drop-down list at the top of the table, then its name and the number of components to be added.

.. image:: /modules/assets/images/component_add.png
   :alt: Add a component
   :align: center


From an asset, you can modify a component by clicking on the link of its name.

.. image:: /modules/assets/images/component_update.png
   :alt: Modify a component
   :align: center


To perform an action on several components (modify a common field, activating or changing financial information, deleting financial information, etc), select them in the right-hand column and then use the Actions button at the top or bottom of the list.

If you select several different types of components that do not have the same fields available to modify, you will be asked which component type you wish to work on.

.. image:: /modules/assets/images/component_computer_massives_actions.png
   :alt: Screen for massive actions on a component
   :align: center


The selection in the left-hand column allows you to select all the components of the same name in one go.

.. image:: /modules/assets/images/component_select_group_left.png
   :alt: Component selection (left)
   :align: center


The selection on the right of the type row (grey line) allows you to select all the components of this type (Processor, Memory, Network card...).

.. image:: /modules/assets/images/component_select_group_right.png
   :alt: Component selection (right)
   :align: center


.. note::

   -  **It is possible to change the characteristics of a component only for the computer**

      From the *Eléments* tab of the component, click on the **Update** link.

      .. image:: /modules/assets/images/component_update_link.png
         :alt: Modifier un composant
         :align: center

      Several tabs are then displayed:

      *  "Component type name" Tab: Lists the characteristics of this component
      *  :doc:`"Management" <../onglets/gestion>` Tab: Manage financial and administrative information
      *  :doc:`"Documents" <../onglets/documents>` Tab: Attached documents
      *  :doc:`"Historical" <../onglets/historique>` Tab: History of modifications
      *  :doc:`"Contract" <../gestion/contrat>` Tab: Manage contracts
      *  :doc:`"Debug" <../onglets/debug>` Tab: Only shown if you are in Debug mode
      *  :doc:`"All" <../onglets/all>` Tab: All information is displayed on one page

.. note::

   Any deletion or addition of a component is recorded in the assets's history.

.. note::

   If an inventory tool is used, this information could be automatically imported and updated.