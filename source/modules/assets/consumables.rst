Consumables
===========

In a consumable's form, several pieces of information are available:

-   General characteristics such as manufacturer, type, reference code, etc
-   Management information such as the technician responsible for the consumable, storage location, etc

The alert threshold is the number of the consumable remaining at which an alert is triggered to inform you of a low stock.

.. todo::
   The notification page does not exist yet. We will need a link to it in the note below when it gets created.
   See https://glpi-project.org/DOC/EN/glpi/config_notification.html
.. note::
   For alerts to work, notifications must be enabled. Notifications are configured from the Setup > Notifications menu.

To change a consumable from new to used, it is necessary to give it to a user or group.

Shared inventory management is possible by defining the item as recursive on an entity. The items will then be available for all sub-entities.


The different tabs
------------------

.. _add-consumables-to-model:

Consumables
~~~~~~~~~~~

It is from this tab that you can add as many consumables as you need one at a time or in bulk.

Un premier tableau liste les consommables neufs, le second tableau liste les consommables utilisés avec notamment le nom du groupe ou de la personne à qui il a été donné.

C'est depuis les actions de masse de cet onglet que sont attribuer les consommables (Actions **Donner**).

Figure 1. Onglet Consommables
![image](docs/image/consumable.png)

.. include:: ../tabs/gestion.rst

.. include:: ../tabs/documents.rst

.. include:: ../tabs/liens.rst

.. include:: ../tabs/notes.rst

.. include:: ../tabs/debug.rst

.. include:: ../tabs/all.rst

The Different Actions
---------------------

In addition to :doc:`the common actions <../generalites/actions>`, there are some actions specific to consumables:

* :ref:`Adding new consumables to a model <add-consumables-to-model>` ;
* Lister les consommables attribués
   ![image](docs/image/resumeConsumable.png)
   L'icone de droite permet d'avoir un résumé des consommables prêtés
   ![image](docs/image/resumeConsumableExample.png)
