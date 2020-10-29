Phones
======

Dans la fiche d'un téléphone, plusieurs informations sont disponibles :

-   Sur les caractéristiques générales du téléphone (le fabricant, le modèle, le type, le numéro de série...) ;
-   Sur la gestion du poste (le responsable technique, son statut, le lieu où il se trouve...) ;
-   Sur les usagers du poste (connus ou non dans GLPI, groupe d'utilisateurs...) ;
-   Sur ses spécifications (l'alimentation, le firmware...).

**Description du type de gestion :**

Il est possible de gérer les téléphones de manière unitaire ou globale.

La gestion unitaire correspond à une gestion classique (un téléphone pour un ordinateur) alors que dans la gestion globale, le téléphone devient un élément virtuel global qui sera connecté à plusieurs ordinateurs.

La gestion globale permet de limiter le nombre d'élément à gérer dans le cas où ceux-ci ne constituent pas une donnée stratégique dans la gestion du parc informatique.

Il est possible d'utiliser les :doc:`gabarits avec les téléphones <../generalites/gabarits>`.

The Different Tabs
------------------

.. include:: tabs/components.rst

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

Phones do not have any specific actions beyond the :doc:`common actions <../generalites/actions>`.
