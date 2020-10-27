Assets Module
=============

GLPI's inventory module is designed to manage the elements that make up the IT equipment fleet.

Inventory management in GLPI
----------------------------

For the management of the hardware and software in the fleet, GLPI allows you to natively list all the elements present within the organization you wish to administer.

However, it is possible to automate the information feedback from the equipment using a third-party tool. Thus GLPI proposes the use of 2 existing plugins:

* The plugin `Fusion Inventory <https://github.com/fusioninventory/fusioninventory-for-glpi/>`_

   It transforms GLPI into an inventory server (agents communicate directly with GLPI)

   You can also consult the `official FusionInventory site <https://www.fusioninventory.org>`_.

* The plugin `OCS Inventory NG <https://github.com/pluginsGLPI/ocsinventoryng>`_

   It allows the syncronization of GLPI with a `OCS Inventory NG <https://www.ocsinventory-ng.org>`_ server (agents communicate directly with the OCS Inventory server).

Asset Types
-----------
.. todo:: This needs updated to include the new asset types
.. toctree::
   :maxdepth: 1

   computers
   monitors
   software
   licenses
   network-equipment
   peripherals
   printers
   cartridges
   consumables
   phones
   global

.. todo::

   Referenced in the original doc, but not present :
   See https://glpi-project.org/DOC/EN/glpi/inventory_ip.html

   * **[Internet Protocol Management (IP)](../glpi/inventory_ip.html)**\
      The IP protocol is materialized in several forms: addresses
      IP, IP networks, but also FQDNs
