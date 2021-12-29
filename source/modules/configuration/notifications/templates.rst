Notification templates
======================

A template is a global object of GLPI that defines the information included in a notification and the formatting of the information.

The creation of a template is a complex operation, which impacts the users.
Therefore, templates can only be modified by Administrators with the *Update* permission for the *Config* right.
Moreover a template is not linked to an entity, which means that it is not possible to delegate its management to an administrator of a of a sub-entity.

A template reflects a communication to a user and can be available in several languages thanks to a translation mechanism.
The use of tags (i.e. markers that are independent of the language used) language used) makes it possible to create a generic translation, available for all the languages of GLPI.

GLPI comes with a set of pre-defined templates for all notifications (tickets, reservations, financial information, cartridges, consumables, licenses, MySQL synchronization ...).

Template tag
------------
A tag is of the form *##tag##*:
- *##field##*: displays the value of a field from the database.
- ##lang.field##: displays the string from the language file associated with a field (its name).
Example for a ticket
*##lang.title##* displays the label "Name" while *##title##* displays the ticket's name.

.. note::
    The tags providing links are adapted to the user depending on his authentication mode to GLPI.
    In particular, a user without login will not be offered the links.

There are 3 types of tags:
- **Simple**: 
    It allows to display a language string or the value of a field.
    *##Reservation.end##* indicates that you want to display the end date of a reservation.
- **Condition** (IF/ELSE/THEN):
    It allows to use conditional branching by testing the presence of a value for a field or by a particular value for it.
    The syntax of the tag is the following
    ::

        ##IFfieldname##
            Action for the IF
        ##ENDIFfieldname##
        ##ELSEfieldname##
            Action for the ELSE
        ##ENDELSEfieldname##

   Example to test if a ticket is assigned to a user
   ::
        ##IFticket.assigntouser## ... ##ENDIFticket.assigntouser##
   Example to display specific information if the status of a validation is "pending"
   ::
       ##IFvalidation.storestatus=2## ... ##ENDIFvalidation.storestatus##

- **Loops** (FOREACH):
    It allows to perform enumerations on lists of values such as a list of tickets, or a list of expired contracts.
    The syntax is as follows:

    - **Simple loop listing all elements**:
        ##FOREACHenumeration## ... ##ENDFOREACHenumeration##

    - **Loop to read the first element of the list**:
        ##FOREACH FIRST enumeration## ... ##ENDFOREACH enumeration##

    - **Loop to read the last item in the list**:
        ##FOREACH LAST enumeration## ... ##ENDFOREACH enumeration##

    - **Loop listing the first 10 elements of the enumeration**:
        ##FOREACH FIRST 10 enumeration## ... ##ENDFOREACH enumeration##'

    Example to display the last two followups in a ticket:
        ##FOREACH LAST 2 followups## ... ##ENDFOREACH followups##

    .. note::
        It is not possible to nest 2 FOREACH tags, but it is possible to place IF tags in FOREACH tags.

The different tabs
------------------

- **Notification templates**

    - Name: The name of the template.
    - Type: The type of item this template will be used for (Ticket, Cartridge, etc). This affects which tags will be available.
    - Comments: Additional information related to the template.
    - CSS: CSS stylesheet used for the template in HTML.
- **Template translations**:
    This is where you will define the content of your notification.
    It lists the different notifications by language and allows you to add a new language.
