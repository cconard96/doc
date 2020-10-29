Software
========

GLPI allows the management of software and their versions as well as licences (which may or may not be associated with versions).

A software is by default associated with an entity: that is to say that there will be as many software in the database as there are entities. Making a software visible in the sub-entities allows for more detailed management.

Financial management is carried out at the level of licences, whereas the financial management present in the software only serves as a model for the licences associated with it.

The software can be imported automatically from a third-party inventory tool and in this case a dictionary can be used to filter or clean the data (see [Configure data dictionaries](07_Module_Administration/06_Dictionaries.rst "Dictionaries are managed from the Administration > Dictionaries menu")).

Some fields are specific in the software file: 

- **Update** is an informative data, from which no processing is carried out and which indicates that the software is an update of another one. 
- **Category** allows groupings by nature on a computer's software list. 
- **Associable to a ticket** defines the visibility of the software in the "Hardware" drop-down list of a ticket.

**Good practices :**

1.  Creating the software (without version in the name)
2.  Create versions
3.  Create licenses

***Tip:*** in multi-entity mode, the list of software can become long, partly due to duplicates (1 software per entity). A fine management of software, licences and versions can consist in grouping identical software in the same entity (see *grouping* tab below), then making recursive the elements that can be recursive.

It is possible to use the :doc:`templates with the software <../generalites/gabarits>`.

The Different Tabs
------------------

.. _versions_soft:

Versions
~~~~~~~~

Principles and management of software versions in GLPI

A software version is the item that can be installed on a computer. See also :ref:`the Installations tab <onglet-logiciels-installations>`.

The main view lists the number of installations of the version.

Specific fields :

* **Name**: corresponds to the version number
* **Status**: in ITIL recommendations, it allows to follow the DSL (storage library of authorized versions)
* **Operating system**: the operating system on which this software version is running
* **Installations**: number of installations of the version
* **Comments**


Licences
~~~~~~~~

Principles and management of software licences in GLPI

.. _onglet-logiciels-installations:

Installations
~~~~~~~~~~~~~

Principes et gestion des installations logiciels dans GLPI.

L'installation d'un logiciel sur un poste est visualisée au travers d'une :ref:`version <versions_soft>` et consultable sur la fiche d'un logiciel (liste des ordinateurs ayant au moins une version installée), sur celle d'une version (ordinateurs ayant cette version installée) ou enfin sur la fiche de l'ordinateur (liste des versions de logiciels installées, triées par catégories).

.. note::

   * La colonne licence est remplie uniquement lorsque la licence est affectée à l'ordinateur concerné.
   * L'affichage initial des différentes catégories dépend des préférences utilisateur. Voir [Gérer ses préférences](01-premiers-pas/03_Utiliser_GLPI/04_Gérer_ses_préférences.rst").

Deux options sont disponibles sur la liste des installations de logiciels d'un ordinateur. Au dessus de la liste, **Installer** manuellement une version d'un logiciel sur le poste (nécessite de sélectionner le logiciel et la version) : si une licence est associée à celui-ci la "version d'utilisation" de la licence est automatiquement renseignée.

Pour **Désinstaller** une version d'un logiciel, il faut utiliser le système d'actions massives : sélectionner les versions à supprimer puis choisir **Supprimer définitivement**. Si une licence est affectée à l'ordinateur elle le reste, mais sa "version d'utilisation" est effacée.

A la suite des versions installées, la liste des licences affectées mais non installées est affichée. Vous pouvez ajouter une nouvelle licence associée à cet ordinateur. Le système d'actions massives permet, via l'action **Installer**, d'installer les versions d'utilisation des licences sélectionnées.

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

Regroupement
~~~~~~~~~~~~

Comment regrouper des logiciels homonymes dans des sous-entités.

.. note::

   Cette option n'est disponible que pour les plateformes multi-entités.

Elle permet de regrouper les logiciels des entités filles sur l'entité mère.

Comment réaliser un regroupement :

#. Si le logiciel n'existe pas dans l'entité mère :
   Créer un logiciel dont le nom est strictement identique au nom du logiciel dans les entités filles ;
#. Ouvrir la fiche du logiciel de l'entité mère ;
#. Activer la récursivité (sous-entités à Oui en haut à droite) ;
   Un nouvel onglet "Regroupement" apparaît après l'onglet "Historique".
#. Ouvrir cet onglet ;
   Une liste indique les logiciels des entités filles ayant le même nom.
#. Sélectionner les lignes souhaitées et valider le regroupement.

.. warning::

    Cette opération est irréversible.

Effets du regroupement :

* Les licences sont attachées au logiciel de l'entité mère, mais restent dans les sous-entités d'origine ;
* Les versions sont fusionnées (plus de doublon dans l'entité mère);
* Les anciens logiciels sont déplacés dans la corbeille ;

.. note::

    Lors de l'utilisation d'un outil d'inventaire tiers, ne pas oublier :

    * de vider la corbeille à la fin du regroupement (sinon la synchronisation restaurera le logiciel en cas de nouvelle version) ;
    * d'affecter le même fabricant au nouveau logiciel (la synchronisation vérifiant le nom du fabricant, un nouveau logiciel serait créé).

.. include:: ../onglets/debug.rst

.. include:: ../onglets/all.rst

The Different Actions
---------------------

In addition to :doc:`the common actions <../generalites/actions>`, there are some actions specific to software:

* :ref:`Ajouter une version à un logiciel <versions_soft>`
* **[Gérer les licences](03_Module_Parc/04_Logiciels/Onglet_Licences.rst)**
    Depuis le menu ***Parc > Logiciels*** cliquer sur le nom de la licence dans l'onglet *Licences*.
