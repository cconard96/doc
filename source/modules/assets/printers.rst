Printers
========

Dans la fiche d'une imprimante, plusieurs informations sont disponibles:

-   Sur les caractéristiques générales de l'imprimante (le fabricant, le modèle, le type, le numéro de série...) ;
-   Sur la gestion de l'imprimante (le responsable technique, son statut, le lieu où elle se trouve...) ;
-   Sur les usagers de l'imprimante (connus ou non dans GLPI, groupe d'utilisateurs...) ;
-   Sur ses spécifications (le compteur de page initial, les types de ports...).

**Description du type de gestion :**

Il est possible de gérer les imprimantes de manière unitaire ou globale.

La gestion unitaire correspond à une gestion classique (une imprimante pour un ordinateur) alors que dans la gestion globale, l'imprimante devient un élément virtuel global qui sera connecté à plusieurs ordinateurs.

La gestion globale permet de limiter le nombre d'éléments à gérer dans le cas où ceux-ci ne constituent pas une donnée stratégique dans la gestion du parc informatique.

**[Gérer les gabarits](Les_différentes_actions/Gérer_les_gabarits.rst)**

The Different Tabs
------------------

.. include:: onglets/composants.rst

Cartridges
~~~~~~~~~~

Les cartouches associées au modèle d'imprimante sélectionnée.

Il se décompose en deux parties :

* Les cartouches utilisées, avec comme information les dates d'ajout et d'utilisation,
* Les cartouches usagées, avec comme information le modèle de cartouche, les dates d'ajout, d'utilisation et de fin de vie, le compteur de l'imprimante ainsi que le nombre de pages imprimées depuis le dernier changement de cartouche.

.. note::

   Pour la création ou la suppression de cartouche reportez-vous à :doc:`la gestion des cartouches <cartouches>`.

.. include:: tabs/connections.rst

.. include:: tabs/network-ports.rst

.. include:: ../tabs/gestion.rst

.. include:: ../tabs/contrats.rst

.. include:: ../tabs/documents.rst

.. include:: ../tabs/tickets.rst

.. include:: ../tabs/problems.rst

.. include:: ../tabs/liens.rst

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

Printers do not have any specific actions beyond the :doc:`common actions <../generalites/actions>`.
