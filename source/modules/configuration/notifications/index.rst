Notifications
=============

.. _configure_notifications:
GLPI has a notification feature that allows it to send messages to users via email, browser notifications, and other methods (expandable by plugins).
The notifications can be customized through templates.
Each notification definition comprises of a template, an event (Ticket creation), and a list of recipients.

GLPI comes with notification definitions pre-defined and they can be used out of the box right away after enabling notifications.

- :doc:`Configure the sending of notification via email <email_notifications>`
- :doc:`Alarm/alert options <alarm_options>`
- :doc:`Customize notification templates <templates>`
- :doc:`Configure notification definitions <definitions>`

How notifications work
--------------------------------

The notification processing mechanism is powerful but can be complex if you use entities.
It is based on the following algorithm:

1. An action has triggered an event that requires a notification
2. GLPI searches for notifications that correspond to the event in the entity of the object which triggered the notification and in parent entities
3. For each notification GLPI retrieves the list of recipients:

    - A translation of the template exists for the user's language:
        GLPI uses it to send the notification
    - No translation exists:
        GLPI uses the default translation
    - GLPI keeps in memory that this user has already been notified so that it does not send duplicate notifications.

The sending of notifications is done in a synchronous way, that is to say that they are triggered by GLPI at the time of the triggering of an event.

.. note::
    If a notification is defined as visible in the sub-entities, it will be executed even if the administrator of a child entity does not redeclare it.