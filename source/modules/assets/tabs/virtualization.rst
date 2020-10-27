Virtualization
~~~~~~~~~~~~~~

In this tab, you will find all virtualization systems (virtual machines, containers, sandboxes, etc) associated with a host or the host on which a virtualisation system is installed.
The information available varies from one system to another, depending on the information that can actually be obtained.

For example, for a virtual machine, you can find its name, virtualization system, and virtualization model, the virtual machine status, allocated memory, and the physical (host) machine name and number of logical processors.

GLPI currently makes the connection between a host and a virtual machine based on the unique identifier (UUID).
In certain cases, it happens that the UUID is different within the physical and virtual machine, the link is then impossible.

The only way to manually associate a virtual machine with a physical machine is to assign to the virtual machine declared on the host and to the virtual machine in GLPI an identical UUID.

.. note::

   If an inventory tool is used, this information could be automatically imported and updated.
