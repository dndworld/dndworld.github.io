---
label: Rolling Dice
icon: ":game_die:"
order: 100
---
<style>
h1:before { 
  content: "🎲 ";
}
</style>

# Avrae Commands

Avrae is our virtual dice bot that we use to make all dice rolls on the server. This page lists the most commonly used Avrae commands along with a few examples.

For the complete list of the commands, visit:
<https://avrae.io/commands/>

- `!help`: sends you a full list of commands to PM.
- `!tutorial quickstart`: starts a step-by-step guide.
<br><br>
- Our partner server The Starry Shore have created [The Ultimate Avrae Discord Bot Tutorial: Beginner’s Guide](<https://youtu.be/im0vDcYFIbI>), a short YouTube video to help with some basic Avrae commands.


!!!warning
Don't forget to use **quotes** `" "` around an argument if it __has multiple words__! This includes the name of an action, spell, or custom counter.
!!!

=== Table of Contents
- [Quickstart](#quickstart)
- [Basic Rolls](#basic-rolls)
- [Actions](#actions)
- [Casting Spells](#casting-spells)
- [Custom Counters](#custom-counters)
- [Playing the Game](#playing-the-game)
- [Combat with Avrae](#combat-with-avrae)
- [Initiative Management](#initiative-management)
- [Content Lookup](#content-lookup)
- [Other Commands](#other-commands)
===

---

## Quickstart

- All Avrae commands start with `!`

### Character Management

> - `!char list`<br>
> Shows the list of your characters. The list is tied to your discord account, therefore if you have characters outside of this server, they will be included in this list.
> <br><br>
> - `!char`<br>
> Shows the current active character.
> <br><br>
> - `!char <character name>`<br>
> Changes the active character.
> <br><br>
> - `!char delete <character name>`<br>
> Deletes named character from Avrae's database.
> <br><br>
> - `!sheet`<br>
> Shows the sheet of your current active character.
> <br><br>
> - `!vsheet`<br>
> Shows a more detailed sheet of your current active character, as well as the Character Sheet URL.
> <br><br>
> - `!update`<br>
> Updates the data from the original source of the sheet.

---

## Basic Rolls

> - `!roll <dice>` or `!r <dice>`<br>
> Rolls one or more dice, <br>e.g. `!r d20` rolls one d20 dice, `!r 4d6` rolls four d6 dice.
> For full list of supported operators and selectors, use `!help roll`.
> <br><br>
> - `!check <skill>` or `!c <skill>`<br>
> Rolls a skill check for your current active character, <br>e.g. `!c acrobatics`
> <br><br>
> - `!save <ability>` or `!s <ability>`<br>
> Rolls a save for your current active character, <br>e.g. `!s dex`
> <br><br>
> - `!action <action>` or `!a <action>`<br>
> Performs an action (attack or ability) for the current active character, <br>e.g. `!a "unarmed strike"`

---

## Actions

> - `!action list` or `!a list`<br>
> Lists the actions that are available to your current active character.
> <br><br>
> - `!action <action>` or `!a <action>`<br>
> Performs an action (attack or ability), <br>e.g. `!a "unarmed strike"`
>   - `-t <name>`: targets a creature
>   - `-phrase "<phrase>"`: adds flavor text
>   - `adv/dis`: rolls with advantage/disadvantage
>   - `hit`: automatic hit
>   - `miss`: automatic miss
>   - `crit`: automatically applies crit damage on hit
> <br><br>
> - `!help action`<br>
> Sends you a full list of options for `action` command.

---

## Casting Spells

> - `!spellbook` or `!sb`<br>
> Shows your current active character's list of spells.
> <br><br>
> - `!cast <name of spell>`<br>
> Casts a spell, <br>e.g. `!cast "Hellish Rebuke"`
>   - `-l <slot level>`: casts spell at a higher level, <br>e.g. `!cast "Cure Wounds" -l 4`
>   - `-t`: targets a creature with the spell, <br>e.g. `!cast "Healing Word" -t "Adult Blue Dragon"`
> - For targeting **multiple creatures**, make sure to put `-t` in front of each target, <br>e.g. `!cast "Magic Missile" -t "Bandit1" -t "Bandit2" -t "Bandit3"`
> <br><br>
> - `!game spellslot <slot level> <number>` or `!g ss <slot level> <br><number>`
> Modifies the leveled spell slots, <br>e.g. `!g ss 1 +1` to gain a level 1 spell slot.

---

## Custom Counters

> - `!customcounter list` or `!cc list`<br>
> Shows a summary/list of all custom counters attached to your current active character.
> <br><br>
> - `!cc <name>`<br>
> Shows the custom counter with the name.
> <br><br>
> - `!cc <name> +/-<number>`<br>
> Modifies the custom counter of your current active character.
> <br><br>
> - `!cc reset <name>`<br>
> Resets the custom counter to its default value.
> <br><br>
> - `!cc create <name> [args]`<br>
> Creates a new custom counter. For the list of arguments, use `!help cc create`.
> <br><br>
> - `!cc delete <name>`<br>
> Deletes a custom counter.

---

## Playing the Game

> - `!game status` or `!g status`
> Shows your active character's current, maximum, and temporary hit points, as well as any counters associated with the character: spell slots, special abilities (Breath Weapon for Dragonborns, Wild Shape for Druids, etc.), and any other custom counters.
> <br><br>
> - `!game hp <amount>` or `!g hp <amount>`<br>
> Modifies the hit points of your current active character, <br>e.g. `!g hp -5` 
> - `!g hp max`: sets hp to max<br>
> - `!g hp set <number>`: sets hp to the number<br>
> - `!g hp +/-<number>`: adjusts the hp<br>
> <br><br>
> - `!game thp <amount>` or `!g thp <amount>`<br>
> Sets the temporary hit points for your current active character, <br>e.g. `!g thp 5`
> <br><br>
> - `!game deathsave` or `!g ds`<br>
> - `!save death` or `!s death`<br>
> Rolls a death save.
> <br><br>
> - `!help game`<br>
> Sends you a full list of options for `game` command.
> <br><br>
> - `!lr` (Improved from Avrae's default `!game longrest`)<br>
> Performs a Long Rest and resets applicable counters.
> - `!lr ?`: shows the help text for this command.<br>
> <br><br>
> - `!sr` (Improved from Avrae's default `!game shortrest`)<br>
> Performs a Short Rest and resets applicable counters.
> - `!sr <number>`: uses a number of hit dice, rolls them and adds the result to your HP.
> - `!sr ?`: shows the help text for this command<br>

---

## Combat with Avrae

> - `!init begin` or `!i begin`<br>
> Begins a combat initiatives in the channel. This command is either run by a DM or whoever is managing the initiatives in spar RPs.
> <br><br>
> - `!init join` or `!i join`<br>
> Rolls an initiative for your current active character.
>   - `-p <number>`: places your character at a specific place on the initiative.
> <br><br>
> - `!init status <name>` or `!i status <name>`<br>
> Outputs the status of the combatant.
> <br><br>
> - `!init effect <combatant> <effect name>`<br>
> Adds an effect text to the combatant.
> <br><br>
> - `!init re <combatant> <effect name>`<br>
> Removes an effect from the combatant.
> <br><br>
> - `!init next ` or `!i n`<br>
> Ends your turn and move to the next on the turn order.
> <br><br>
> - `!help init [subcommand]`<br>
> Sends you a full list of options for `init` command and its subcommands, <br>e.g. `!help init join`

---

## Initiative Management

This section is for DMs or the person who is running the initiative in sparring RPs.
For the full list of options for each command, use `!help <command> [subcommand]`, <br>e.g. `!help init effect`.

> - `!init begin` or `!i begin`<br>
> Begins a combat initiatives in the channel.
> <br><br>
> - `!init opt <combatant> [args]`<br>
> Edits the options of a combatant. For the full list of options, run `!help init opt`.
>   - `-h`: hides HP, AC, resistance, etc. 
>   - `-ac <number>`: modifies the combatant's AC.
>   - `-group <group name>`: adds the combatant to the group. Remove them from the group by using `-group None`
> <br><br>
> - `!init a` or `!init cast`<br>
> Makes an attack or casts a spell as the combatant of the turn.
> <br><br>
> - `!init aoo <combatant> <attack name> -t <target> [args]`<br>
> Makes an attack of opportunity as the combatant.
> <br><br>
> - `!init reactcast <combatant> <spell name> [args]`<br>
> Casts a spell as the combatant off-turn.
> <br><br>
> - `!init status <combatant/group> [args]`<br>
> Outputs the HP and status of the combatant or the group.
>   - `private`: Sends the status via private message instead.
> <br><br>
> - `!init hp <combatant> +/-<number>`<br>
> Modifies HP of the combatant.
>   - `!i hp <combatant> set <number>`: sets the combatant's HP.
>   - `!i hp <combatant> max`: sets the combatant's HP to max.
> <br><br>
> - `!init thp <combatant> <number>`<br>
> Sets the THP of the combatant.
> <br><br>
> - `!init effect <combatant> <effect name> [args]`<br>
> Attaches a status effect to the combatant.
>   - `-dur <duration>`: specifies the duration of the effect. `<duration>` equals to number of rounds.
> <br><br>
> - `!init re <combatant> <effect name>`<br>
> Removes the status effect from the combatant.
> <br><br>
> - `!init remove <combatant/group>`<br>
> Removes the combatant or the group from the combat.
> <br><br>
> - `!init end`<br>
> Ends the combat in the channel.

---

## Content Lookup

> You can lookup items, status effects, rules, etc. By default, Avrae only supports content from Basic Rules. For gaining access to paid material on D&D Beyond via content sharing links, follow the instructions pinned in [`#ddb-link-request`](https://discord.com/channels/512870694883950598/756319993616138310).
> - Connect your Discord account with D&D Beyond account. This can be done from "Account Settings" page in D&D Beyond. Confirm the connection by running:
> <br><br>
> ```
> !ddb
> ```

> ### Available commands:
> - `!class <name> [level]`
> - `!subclass <name>`
> - `!race <name>`: works for both race and subrace.
> <br><br>
> - `!classfeat <name>`
> - `!racefeat <name>`
> - `!feat <name>`
> <br><br>
> - `!background <name>`
> - `!spell <spell name>`
> - `!item <item name>`
> <br><br>
> - `!rule <name>`
> - `!condition <name>`

> ### Homebrew Lookup
> - `!hb` to see all lookup options
> <br><br>
> - `!hb class <name>`
> - `!hb subclass <subclass name>`
> - `!hb race <name>`
> <br><br>
> - `!hb classfeat <name>`
> - `!hb feat <name>`
> - `!hb invocation <name>`
> <br><br>
> - `!hb background <name>`
> - `!hb spelllist "<class name> ([spell level])"`, <br>e.g. `!hb <br>spelllist "Witch Doctor (2)"`

---

## Other Commands

> - `!portrait`<br>
> Shows the image of your current active character.
> <br><br>
> - `!portrait update <link>`<br>
> Sets a portrait for the character.
> <br><br>
> - `!desc`<br>
> Shows the description of your current active character.
> <br><br>
> - `!desc update "<text>"`<br>
> Sets a description for the character.
> <br><br>
> - `!csettings color <color>`<br>
> Changes the embed color of your current active character, <br>e.g. `!csettings color blue` or `!csettings color 0000FF` (no "#" for the hex code)
> <br><br>
> - `!br`<br>
> Makes a scene break.
> <br><br>
> - `!servalias` and `!servsnippet`<br>
> Shows the list of available server alias and server snippets.
> <br><br>
> - `!alias` and `!snippet`<br>
> Shows the list of available personal alias.
> For more information on alias and snippet, use `!help alias` and `!help snippet`.
> <br><br>
> - `!rr <number of times> <dice type>`<br>
> Rolls number of times the same dice, <br>e.g. `!rr 5 d10`
> <br><br>
> - `!rrr <number of times> <dice type> <DC>`<br>
> Rolls dice with DC, <br>e.g. `!rrr 5 d20 14`
