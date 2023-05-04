# Zephyr Help

👋 Welcome to Zephyr! This document is designed to help you get started with our AI-influenced event management bot and to provide guidance on how to use its features.

## Setting up Zephyr 🛠️

To get started with Zephyr, use the `/setup` command. This will guide you through a series of prompts to customize the bot's behavior for your server. Once all variables have been defined with the `/setup` command, the bot will save the server's config to our databases.

An example "guild_body" JSON object looks like:
```json
{
        "guild_id": 1103578895560749126,
        "guild_name": "Zephyr",
        "guild_owner": 755493797160288286,
        "guild_config": {
            "ticket_category": 1103613805411446804,
            "channel": 1103613860763664424,
            "role": 1103614077290430524,
            "style": "embed",
            "mode": "fully automatic"
        },
        "joined_at": 0,
        "blacklisted": false,
        "active_tickets": [],
        "active_events": [],
        "vtc_events": [],
        "truckersmp_info": null
}
```
You can use `/config` to view your server's configuration, which will include the options you set during the `/setup` process.

## 🔧 `/setup` Configuration Variables 🔨

Here's an overview of what each `/setup` variable does:

- `ticket_category` - The category to create tickets in.
- `channel` - The channel to create tickets in.
- `role` - The role to assign to users who create tickets.
- `style` - The style of event management to use (`fully automatic`, `balanced`, `manual`).
- `mode` - The mode to use for event management (detailed explanations below).

### 🎨 `style` Options 🎨

You can set the style variable to either embed or text. This determines what event announcements will look like.

If set to embed, event announcements will be sent in the form of an embed, while if set to text, they will be sent in plain text form.


### 🔍 `mode` Options 🔍

- `fully automatic` - The bot handles every aspect of event management by itself. It'll accept event invites if the schedule is clear and if the event matches any predetermined requirements. Predetermined requirements can be set using the [website](https://okayge.xyz/zephyr/settings#eventacceptance).
- `balanced` - The bot will handle some aspects of event management. Exactly what it will manage can be toggled on/off via the [website](https://okayge.xyz/zephyr/settings#eventacceptance). When balanced mode is selected, Zephyr will still remain scanning event tickets - unless toggled off.
- `manual` - The bot will do very little by itself, but users can still use some of its commands. With this preset mode selected,  Zephyr will **not** scan event tickets.

## 📚 Resources 📚

If you need further help or have any questions, please check out the `README.md` file linked above and the `contributing.md` file for more detailed information on how to use and configure Zephyr. Additionally, if you have any issues or suggestions, feel free to reach out to our team  for assistance.

