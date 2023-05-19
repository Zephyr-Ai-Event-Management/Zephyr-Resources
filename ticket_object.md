Ticket Object
=============

This object represents a ticket/channel in a Discord server related to events. It contains information about the ticket and any associated invites.

Properties
----------

- `author` (integer): The Discord ID of the message author.
- `id` (integer): The Discord channel ID for the ticket.
- `isEvent` (boolean): Indicates whether the ticket is related to an event. This property will always be `true` for event tickets.
- `invites` (array): An array of invite objects sent in the ticket/channel.

Invite Object
-------------

An invite object represents an invitation associated with the ticket.

Properties
----------

- `id` (integer): The TruckersMP event ID for the event invitation.
- `acceptable` (boolean or null): Indicates whether we can attend the event or not. If the value is `null`, it means the invitation is pending review.
- `claimedBy` (integer or null): The Discord ID of the person who has currently claimed the ticket. If no one has claimed the ticket, the value will be `null`.
- `claimed` (boolean): Indicates whether the ticket is currently claimed (`true`) or not claimed (`false`).

Example Ticket Object
---------------------
```json
{
  "author": 755493797160288286,
  "id": 1104068604892291102,
  "isEvent": true,
  "invites": [
    {
      "id": 12371,
      "acceptable": null,
      "claimedBy": null,
      "claimed": false
    }
  ]
}
```
