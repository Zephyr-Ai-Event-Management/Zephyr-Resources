When a ticket reaches the point where it's confirmed to be an event and is attendable, we store that ticket in our DB. 

Data store is structred like this:
```json
{
    "author": 755493797160288286,
    "id": 1104068604892291102,
    "isEvent": true,
    "invites": {
       "one": {
        "claimedBy": null,
        "claimed": false,
        "event": {
            "id": 12371,
            "location": "Kouvola (Lintukainen)",
            "destination": "Pori (Baltic Metalgury)",
            "meetup": 1684863000,
            "departure": 1684864800
        },
        "finished": false
       }
     },
    "global_finish": false,
    "invite_count": 0
}
```

Each ticket channel gets its own `ticket_object` in the tickets collection. Once a channel/ticket is deleted, that ticket's object is deleted from the collection.

An object contains the following:
| Name | Type | Value | 
| ---- | ---- | ------ |
| author | int   | The discordID of the author of the ticket    |
| id | init   | The ID of the discord channel for that ticket |
| isEvent | boolean   | This will always be true. It indicates whether the ticket is an event ticket or not     |
| invites | array | An array that contains information event invites sent within a channel |
| one | str | Which invite it is. I.e one, two. These are decided based on invite_count. |
| claimedBy | int | The discordId of the user who claimed the invite/ticket |
| claimed | boolean | Indicates whether or not the ticket/invite is currently claimed |

