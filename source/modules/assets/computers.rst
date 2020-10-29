Computers
=========

In the form of a computer, there is a certain amount of information including general characteristics (manufacturer, model, type, serial number), management information (technical manager, status, location) and users of the workstation (known or not known in GLPI).

Other fields are informative, such as `Network` (type of connection to the workstation), and the `Update Source` which is a dropdown indicating where the updates of a workstation come from (yes/no, Windows update, yum, apt, etc).

It is possible to use :doc:`templates with computers <../generalites/gabarits>`.

.. note::

   * In the case of using GLPI coupled with an inventory tool, different import information is also available.
   * A computer can be at any time a server, a desktop computer or a laptop. To differentiate between them, you can use the type field.

The Different Tabs
------------------

.. include:: tabs/os.rst

.. include:: tabs/components.rst

.. include:: tabs/volumes.rst

.. include:: tabs/software.rst

.. include:: tabs/connections.rst

.. include:: tabs/network-ports.rst

.. include:: ../tabs/gestion.rst

.. include:: ../tabs/contrats.rst

.. include:: ../tabs/documents.rst

.. include:: tabs/virtualization.rst

.. include:: tabs/antivirus.rst

.. include:: ../tabs/tickets.rst

.. include:: ../tabs/problems.rst

.. include:: ../tabs/changes.rst

.. include:: tabs/links.rst

.. include:: ../tabs/notes.rst

.. todo::
   Add a reservations tab page.
   See commontabs/item_reservations.rst as reference.
   None of those files seem to be linked anywhere.

.. include:: ../tabs/historique.rst

.. include:: ../tabs/debug.rst

.. include:: ../tabs/all.rst

The Different Actions
---------------------

In addition to :doc:`the common actions <../generalites/actions>`, there are some actions specific to computers:

* **Installing a software license on a computer**
   From the *Software* tab, add a license by choosing the software name followed by the license name.
   From the mass actions in the summary table, choose **Install**.

   .. warning::

      A software can only be installed if its license has a purchase and/or use version.
