Ticket Object
=============

This object represents a ticket/channel in a Discord server related to events. It contains information about the ticket and any associated invites.

Properties
----------

- `author` (string): The Discord ID of the message author.
- `id` (string): The Discord channel ID for the ticket.
- `isEvent` (boolean): Indicates whether the ticket is related to an event. This property will always be `true` for event tickets.
- `invites` (array): An array of invite objects sent in the ticket/channel.

Invite Object
-------------

An invite object represents an invitation associated with the ticket.

Properties
----------

- `id` (integer): The TruckersMP event ID for the event invitation.
- `location` (string): The city and location (slot/company) where the event/convoy begins.
- `destination` (string): The city and location (slot/company) where the event/convoy ends.
- `meetup` (integer): The timestamp in milliseconds 30 minutes before the departure time. This is when the convoy is due to meetup.
- `departure` (integer): The timestamp in milliseconds. This is the time when the convoy is due to depart.
- `embed` (string): The ID of the event info embed, used by the bot to identify event information and make buttons work.

Example Ticket Object
---------------------
```json
{
    "author": "755493797160288286",
    "id" : "1104068604892291102",
    "isEvent": true,
    "invites": [
        {
            "id": 12371,
            "location": "Kouvola (Lintukainen)",
            "destination": "Pori (Baltic Metalgury)",
            "meetup": 1684863000000,
            "departure": 1684864800000,
            "embed": "1108963092064383007"
        }
    ]
}
