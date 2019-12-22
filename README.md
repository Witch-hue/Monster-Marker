# monster-marker
A Tera Proxy module that alerts you when an Event Mob is on your characters vicinity.

Spawns a Loot beam (Vergos head) next to event mob.

Currently working on Santas (patch 88 NA)


Oringal Author Seren, Updated and upkept by Witch


## Updates
Latest Version: Patch 88

Note: Special (event) mob searching is enabled by default and can be disabled in config.json, under `specialMobSearch`.

## Requirements and Information
Requires:
- Commands module by Pinkie-Pie: https://github.com/pinkipi/command

Supports:
- Auto Update using Caali's Proxy

To find more mob ids, you can use mob-id-finder: https://github.com/SerenTera/Mob-id-finder

A Tera Proxy module that warns you when specific objects(mobs like mongos/blue boxes) are in your VISIBLE vicinity (ie: IN YOUR SIGHT) and puts a marker on them. WILL NOT TELL U ANYTHING IF U CANT SEE IT DON'T ASK HOW TO DO THAT TY. Use common sense and do not use this module/ disable mobmarkers for mob targets with very common spawn rate, instead of complaining of lags >.> This is made for rare spawn events in mind.

This only warns you when the object is loaded onto your visible vicinity (ie. you can see it around you). A mob marker (vergos head) is spawned on mob(bluebox) and despawned when mob is dead/out of range.

Warning is done via client sided system notices (displays a message in the middle of your screen) as default, but system messages (chat messages) can be turned on. To turn on chat message notification, set 'messager=true' under defaults in index.js or false to disable chat message notifications.

## Config
Configuration can be done via config.json. If not present, it will be generated on first startup.

- `enabled`:Default enabling of the module. True to always enable on startup
- `markenabled`: Enables item markers on monsters. True to spawn item markers.
- `messager`: Enables Messaging via chats. True to enable
- `alerts`: Enable flashing messages for alert. True to enable.
- `Item_ID`: Item ID of item marker
- `Monster_ID`: List of Mobs to look out for. Format: `"<huntingZoneId>_<templateId>" : "<Name of mob>"`
- `specialMobSearch`: Searches for specialMobs based on bySpawnEvent field

## Commands:
Use the commands in /proxy chat. If you want to use it outside of /proxy chat, make sure you prefix the commands with '!'.
- `warn info` - Infomation on the module commands

- `warn toggle` - Toggles the module. Disabling the module will clear all markers as well.

- `warn alert` - Toggles system notices

- `warn marker` - Toggles display of mobmarkers (switch on or off mob markers via toggle)-

- `warn clear` - Attempts to clear all markers and reset the module. Use if vergos head failed to despawn for some weird reason

- `warn add <huntingZoneId> <templateId> <name of entry>` - Adds and save a custom entry to the config.

Currently supports World Bams and Big Blue Boxes. Can be modified for other objects.
Many thanks to teralove for the work on party death markers for codes on markers (https://github.com/teralove/party-death-markers)

## ID List - NA Tera specific
- Hunting zone ids:
Bluebox-1023 | Caiman-1023 | 'summer event crabs'-6553782

- Template ids:
Bluebox-88888888 | Caiman-99999999,99999991,99999992 | 'summer event crabs'-1021
