Network ports
~~~~~~~~~~~~~

The network port management information is visible in the `Network ports` tab.

.. image:: /modules/assets/images/ports.png
   :alt: List of network ports
   :align: center

A network port allows the output of a network interface to be modelled on a given material. Each port is characterised by a number and a name.

On this port, it is possible to add one or several VLANs, these can be defined by a name, a comment and a number (VLAN tag ID).

.. image:: /modules/assets/images/ports_vlan.png
   :alt: VLAN
   :align: center


On each network port, one or more :doc:`network names <../configuration/intitules/internet>` can be associated.
You can add several network names by going to the "Network ports" name.

.. image:: /modules/assets/images/ports_network_name.png
   :alt: Network name
   :align: center

.. note::
   When there is only one network name, it will be displayed in the form of the network port and it will be possible to modify it directly.
   You can also change the network name through its own form (with its tabs) by clicking on the title just above the part of the form that concerns him.

   When there are several network names, it is no longer possible to change the network name in the network port form. You must always use the tab.

The network ports can be of different types. There are ports (Ethernet, Wifi ...), term:`Virtual network port` (local loop, alias, aggregates ...), point-to-point (switched line) ...

The network ports tab represents all the ports available at the equipment in a table.

In the header of the table, next to the total number of ports, there is a link to choose options network port display.

It is thus possible to display or hide information such as network information (anything that is not in the concerns the Internet), the intrinsic characteristics of the port (ie. depending on its type), MAC addresses, VLANs ...

.. note::

   GLPI allows you to faithfully represent complext network connections with associated Wifi and/or Ethernet port aliases to VLANs grouped in aggregates

Management of Ethernet type network ports
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The Ethernet protocol is the one typically used in internal networks.

An Ethernet port is characterised by its type (twisted pair, fibre, etc.) optical single/multimode ...), a bit rate (10Mb, 100Mb, 1Gb, 10Gb, 10Gb...) and its MAC address. It is possible to associate a network as well as a network socket.

Ethernet connections are made by connecting two Ethernet ports between them. For this to happen, there must be a free port on each of them materials. In general, connections will be made between a port present on a computer, peripheral device or printer and a port present on a network hardware (hub, switch).

Management of Wifi type network ports
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The Wifi protocol is the one typically used for the networks without wires.

A Wifi port is characterised by the mode of operation of the card (Ad-Hoc, Access Point, repeater...), the version of the protocol Wifi (ab, g ...) and its MAC address.

As with the Ethernet ports, it is possible to associate a network.

You can associate a Wifi network to a given port. In addition to its name, a Wifi network contains an ESSID and is characterised by its type:

*Infrastructure:* Wifi network with one or more access points
   and clients who log on to it.
*Ad-hoc:* Wifi network between equivalent systems without point
   access.

Management of local loop type network ports
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The local loop is a virtual port used by most equipment in order to communicate internally. It is this port that is requested when trying to communicate with the machine Localhost (127.0.0.1).

The local loop has no specific attributes.

Managing network port aliases
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

A network port alias is a virtual port that can specialise a physical wear.

Under Linux, each VLAN, when transmitted `"tagged" <glossary/tagged_vlan.html>`__, is associated an alias of port (eth2.50 to represent the VLAN 50 on the eth2 port).

A port alias has its port of origin (i.e. the one on which it is supported) and a MAC address.

Disclaimer : When changing the home port, the MAC address of the new home port is assigned to the port alias.

Managing network port aggregates
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

A network port aggregate is a virtual port that allows to group several physical ports together.

Core routers are often linked together by aggregates in order to make redundancy and/or increase of bandwidth.

We can consider that a network equipment is composed of ports physical networks that are linked together by port aggregates.
The latter correspond to the VLANs physically defined on equipment. Naturally, its management IP addresses are associated with the aggregates associated with the VLAN for managing the switch or the router.

On Linux machines, the aggregates are represented by `bridges <http://www.linuxfoundation.org/collaborate/workgroups/networking/bridge>`__ which connect different ports.
Similarly, a Ethernet firewall will use a bridge which will connect the interfaces to the filter.

A port aggregation contains the ports of origin (i.e. those on which it relies on) and a MAC address.

.. note::

   Any deletion or addition of a network port is recorded in the assets's history.

.. note::

   If an inventory tool is used, this information could be automatically imported and updated.
