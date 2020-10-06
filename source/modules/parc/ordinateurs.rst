Ordinateurs
===========

Dans la fiche d'un ordinateur, on trouve un certain nombre d'informations concernant le système d'exploitation (nom, version, service pack, numéro de série, product ID), les caractéristiques générales (fabricant, modèle, type, numéro de série), les informations de gestion (responsable technique, statut, localisation) et les usagers du poste (connus ou non dans GLPI).

D'autres champs sont informatifs, comme `Réseau` (type de connexion au poste), et la `source de la mise à jour` qui est un intitulé indiquant d'où proviennent les mises à jour d'un poste (oui/non, Windows update, yum, apt, etc).

Il est possible d'utiliser les :doc:`gabarits avec les ordinateurs <../generalites/gabarits>`.

.. note::

   * Dans le cas d'une utilisation de GLPI couplé avec un outil d'inventaire, différentes informations sur l'importation sont également disponibles.
   * Un ordinateur peut être à la fois un serveur, un ordinateur de bureau ou un portable. Pour les différencier, il est possible d'utiliser le champ type.

Les différents tabs
----------------------

.. include:: tabs/os.rst

.. include:: tabs/composants.rst

.. include:: tabs/volumes.rst

.. include:: tabs/logiciels.rst

.. include:: tabs/connexions.rst

.. include:: tabs/ports-reseaux.rst

.. include:: ../tabs/gestion.rst

.. include:: ../tabs/contrats.rst

.. include:: ../tabs/documents.rst

.. include:: tabs/virtualisation.rst

.. include:: tabs/antivirus.rst

.. include:: ../tabs/tickets.rst

.. include:: ../tabs/problemes.rst

.. include:: ../tabs/changements.rst

.. include:: tabs/liens.rst

.. include:: ../tabs/notes.rst

-   **[Onglet "Réservations"](Les_différents_tabs/Onglet_Réservations.rst)**
     Gestion des réservations pour un objet d'inventaire

.. include:: ../tabs/historique.rst

.. include:: ../tabs/debug.rst

.. include:: ../tabs/all.rst

Les différentes actions
-----------------------

Outre les :doc:`actions communes <../generalites/actions>` ; certaines actions sont spécifiques aux ordinateurs :

* **Installer un logiciel avec licence sur un ordinateur**
    Depuis l'onglet *Logiciels*, ajouter une licence en choisissant le nom du logiciel suivi du nom de la licence.
    Depuis les actions de masse du tableau récapitulatif, choisissez **Installer**.

    .. warning::

       Un logiciel ne peut être installé que si sa licence possède une version d'achat et/ou d'utilisation.
