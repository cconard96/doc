Monitors
========

In the monitor form, several fields are available:

- On the management of the monitor (the technical manager, his status, his location...),
- On the general characteristics of the workstation (manufacturer, model, type, serial number...),
- On the users of the workstation (known or not in GLPI, user group...),
- On its specifications (its size, its port types: VGA, DVI, HDMI, DisplayPort, if it has speakers or its connectivity).

**Description of the type of management:**

It is possible to manage the monitors in a unitary or global way.

Unit management corresponds to classic management (one monitor for one computer) whereas in global management the monitor becomes a global virtual element that will be connected to several computers.

Global management makes it possible to limit the number of elements to be managed if they do not constitute strategic data in the management of the computer park.

It is possible to use :doc:`templates with monitors  <../generalites/gabarits>`.

The Different Tabs
------------------

.. _connection_monitor:

.. include:: tabs/connections.rst

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

In addition to :doc:`common actions <../generalites/actions>`, some actions are specific to the monitors:

* :ref:`connect a monitor to a computer <connection_monitor>`
