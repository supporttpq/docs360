# Tickets attachments

Applies for Administrator users

This module allows the administrator of a Tourpaq company to set a certain document to be attached to the email that confirms the booking and sends the printed ticket. The module allows switching between the agencies of a company, and upload a different document to each agency.

The documents can be sent:

* as a separate file from the ticket
  * Terms\&Conditions PDF document that will be sent together with the ticket, as a separate attachment.
* as part of the ticket file, at the end of the ticket
  * Terms\&Conditions PDF document that will be added to end of the ticket in the same file.

Also there are multiple types of possible documents attached to a booking ticket:

* for all bookings: the terms\&conditions files mentioned above
* scenario specific documents
  * specific to a certain resort
  * to a hotel
  * to a specific hotel facility (with limitations)
    * Effect: if a holiday is in a hotel that uses that particular facility (example: Poolbar), then a facility specific document can be merged into the ticket explaining the rules of using the facility.
    * Limitations:
      * max 5 facility documents are merged. If the booking hotel contains more than 5 facilities that have attached documents to them, the system will not merge from 6th document upwards into the ticket, since it will produce a too large attachement and there is a risk of certain email platforms not receiving the important email (Thank you, BookingUpdated, etc.) at all.
      * max 1 Mb per document
      * the facility category to which the facility belongs to must be set to appear on the ticket.
  * to a transport
