---
label: What's Next?
order: 100
icon: ":rocket:"
---

<style>
h1:before { content: "🚀" }
</style> 

# What's Next?

This page is to teach you what to do after creating your character. If you have not done so yet, check out [!badge icon="mark-github" variant="dark" text="Start Here"](/character-building/start-here/)

## Setting up Class, Race, Custom Counters (CCs)

**Custom Counters** are used to keep track of various resources, such as race ability (e.g. Half-Orc's Relentless Endurance), class ability (Fighter's use of Second Wind), ammunition, charges on a magic item, etc.

!!!success
For **D&D Beyond** sheets, this is **already done for you**.
!!!

For other sheets, setting up the class abilities is automated using Avrae. Run the commands below in [!badge icon="/images/discord-mark-blue.svg" text="#bot-dump"](https://discord.com/channels/512870694883950598/519131071502221313) for the setup.

For abilities not covered by `!level`/your sheet, manual counter creation may be required. See `Other` below.

#### Class

This command will pick up any **classes** you currently have. 

```
!level
```

> `!level [class] [subclass]`  will set your **subclasses** for you (e.g. `!level warlock celestial`)

#### Other

Homebrew classes are not supported, and non-Beyond sheets may not have the necessary counters. 
- See `!help cc create` for how to create your own CCs, and `!help cc` for general CC commands. 
- If you are using a homebrew subclass, see `!level template` for instructions on how to create a proper gvar for `!level`.

### Leveling Up

> - Once you've updated your character sheet, run `!update` and `!level` in [!badge icon="/images/discord-mark-blue.svg" text="#bot-dump"](https://discord.com/channels/512870694883950598/519131071502221313).
> - Make sure to react in [!badge icon="/images/discord-mark-blue.svg" text="#roles"](https://discord.com/channels/512870694883950598/535365321134178324) in order to receive game pings for the new level.

## Tracking Money

Money and XP are tracked on the server. They are **not** synced with your sheet, so it does not matter if your sheet is updated with this info (tracking XP is explained later below).

#### Check Coin Purse

Use `!transaction` to check your coin purse.

#### Make Transaction

Log your monetary transactions in [!badge icon="/images/discord-mark-blue.svg" text="#transaction-log"](https://discord.com/channels/512870694883950598/531011819095982081) with:

```
!transaction "reason for transaction" +Xgp
```

!!!warning
Transactions logged outside of [!badge icon="/images/discord-mark-blue.svg" text="#transaction-log"](https://discord.com/channels/512870694883950598/531011819095982081) are considered invalid.
!!! 

> You can chain multiple currencies to the command like so:

```!transaction "reason for transaction" +Xgp +Xsp +Xcp```

=== [Example] Adding Starting Gold

!!!success
For D&D Beyond users, Avrae should automatically handle this step. Your coin purse may sync the first time you run `!import`, so check your balance by running `!transaction` first. 
!!!

In [!badge icon="/images/discord-mark-blue.svg" text="#transaction-log"](https://discordapp.com/channels/512870694883950598/531011819095982081), replace **#** with the starting gold amount.
```
!transaction "Starting Gold" +#gp
```
 
> - `!transaction "Folk Hero Starting Gold" +10gp`
> - `!transaction "Haunted One Starting Gold" +1sp`
> - `!transaction "Monk Rolled Gold" +12gp`
===

## Roleplaying

Roleplaying (RP) gives your characters **RPXP**, which can later be turned into XP (The process is explained later below).

#### RP Channels

You can go to any of the channels in the Snowhaven: West/High Class/North/South, Underhaven, Nanam in Nature, and Arena categories to RP. 

- [!badge icon="/images/discord-mark-blue.svg" text="#drunken-yeti-inn"](https://discord.com/channels/512870694883950598/551901424276078602) is the most popular channel to RP, and a great place to start.
- [!badge icon="/images/discord-mark-blue.svg" text="#rp-board"](https://discord.com/channels/512870694883950598/893946822404493392) is where you can make a post to look for RP, or join one that is already posted.

#### Other Channels

- You cannot go into any of the channels marked under the DO NOT ENTER category.
- All channels listed under GAME CHANNELS # as well as the channels listed under TRAINEE GAMES category are reserved for DM events only.

#### Entering the Town

You may want to RP your character entering Snowhaven in [!badge icon="/images/discord-mark-blue.svg" text="#gates"](https://discord.com/channels/512870694883950598/611385612351569920). There is no set way to introduce yourself. However, most people write their introduction as if people are seeing them for the first time. 

They would describe how their character looks like and say what they are doing, which usually gives something other characters can interact with. 

!!!info Example
*Zoey enters the gates, taking in the sights around her. She is a 6‘0 tall human with long red hair, her shiny metal armor making clinks as she walks. Seeing a welcoming puff of smoke in the distance, she heads towards the tavern looking for a drink.*
!!!

#### Follow the Rules

Please use common sense and behave as you would in a public setting. Follow the [!badge icon="mark-github" variant="dark" text="rules"](/rules). Breaking things and crime will definitely get you thrown into jail as the RP channels are meant as a safe zone.

## RPXP

RPXP allows you to earn bankable credits for roleplaying. The full explanation can be found [!badge icon="mark-github" variant="dark" text="here"](games/).

#### First Time

Set up your counters: `!rpxp` in [!badge icon="/images/discord-mark-blue.svg" text="#xp-tracker"](https://discord.com/channels/512870694883950598/531014104098537481) (only need to do it once per character)

### Steps

1. React to your first RP post with :beginner: `:beginner:` and last RP post with :octagonal_sign: `:stop:`. Get the person you are RPing with to react as well.

2. Find out how long the RP session was. [!badge icon="/images/discord-mark-blue.svg" text="#rp-log"](https://discord.com/channels/512870694883950598/592249450789863434) picks up the messages reacted with :beginner: & :octagonal_sign:.

3. Log the RPXP in [!badge icon="/images/discord-mark-blue.svg" text="#xp-tracker"](https://discord.com/channels/512870694883950598/531014104098537481) by the increments of half an hour (rounded down)

`!rpxp <hours> [message]`

> Example:
> 
> ```
> !rpxp 1.5 "#the-library"
> ```

### Weekly Cap

**Every Monday (EST)** you can reset your Weekly RPXP Cap by running the following command in [!badge icon="/images/discord-mark-blue.svg" text="#xp-tracker"](https://discord.com/channels/512870694883950598/531014104098537481) :

```
!rpxp cap reset
``` 

## OOC Channels

OOC stands for **Out Of Character**. 

#### RP OOC channels

Snowhaven: West/High Class/North/South, Underhaven, Nanam in Nature, Shops, and Arena categories have respective `#[category]-ooc` channels for out-of-character conversations.

#### Other OOC channels

When you aren't RPing or taking part in events, you can chill in any of the OOC channels, where you can talk about character builds, recent bounties, real life, etc. Popular channels include [!badge icon="/images/discord-mark-blue.svg" text="#snowhaven-north-ooc"](https://discord.com/channels/512870694883950598/579940774574161942) and [!badge icon="/images/discord-mark-blue.svg" text="#guild-ooc"](https://discord.com/channels/512870694883950598/527458737892622361).

There are channels for specific content under the **DnD Chat** category. Please try to keep posts related to those topics contained to those channels. Similarly, please keep bot commands to [!badge icon="/images/discord-mark-blue.svg" text="#bot-dump"](https://discord.com/channels/512870694883950598/519131071502221313).

## Signing up for DM events

Full explanation on the available game types on the server can be found in [What's Next?](whats-next.md).

1. Wait for Level pings

Wait for a DM to ping your level for a bounty in [!badge icon="/images/discord-mark-blue.svg" text="#bounty-board"](https://discord.com/channels/512870694883950598/537744572848013314) or an arena/hunt/pit fight in [!badge icon="/images/discord-mark-blue.svg" text="#arena-board"](https://discord.com/channels/512870694883950598/626866757038112768). 

2. Check if signups are still Open

Event posts with a :x: or :negative_squared_cross_mark: reaction are closed for signups.

3. Signup

If the event is still open for signups, copy the **template** posted by that DM, fill it in, and post it in [!badge icon="/images/discord-mark-blue.svg" text="#game-signup"](https://discord.com/channels/512870694883950598/537341568462487597)

!!! How to check "RPXP Stored" and "XP to Next Level"
In [!badge icon="/images/discord-mark-blue.svg" text="#bot-dump"](https://discord.com/channels/512870694883950598/519131071502221313), run `!rpxp xp`
!!!

4. Acceptance

Game acceptance is announced in [!badge icon="/images/discord-mark-blue.svg" text="#game-acceptance"](https://discord.com/channels/512870694883950598/626865858916122654). If you are accepted, the DM will ping you to confirm your attendance. React with the appropriate emoji to confirm your acceptance.

5. Before the Game

The DM will ping you again in the appropriate OOC (out of character) channel for the game.

6. After the Game: Tracking XP

[!badge icon="/images/discord-mark-blue.svg" text="#xp-tracker"](https://discord.com/channels/512870694883950598/531014104098537481) for you to track *all* XP on this server using the `!dxp` command.

To add the XP from the game:

```
!dxp game <amount> <source>
```

> (e.g. `!dxp game 100 "Red Ruby Heist"`)

When you level up, adjust your sheet accordingly and run `!update` in [!badge icon="/images/discord-mark-blue.svg" text="#bot-dump"](https://discord.com/channels/512870694883950598/519131071502221313). No sheet link is required.


## Intoxication Counter (Optional)

Intoxication Counter follows a homebrew system which you can read more about in the pins of [!badge icon="/images/discord-mark-blue.svg" text="#drunken-yeti-inn"](https://discord.com/channels/512870694883950598/551901424276078602). This determines your state of drunkenness. 

Running `!drink [name of drink]` will automatically setup the counters you need.
> e.g.: `!drink "Dwarven Firewhiskey"`


**Interacting with the Intoxication Counters**

- `!cc intox` to view the counter
- `!cc intox set 0` to reset the counter

## Bag Management (Optional)

!!! 
Your character sheet needs to list your equipment.
!!!

Bag management within the server is completely optional. Should you want to track your items, you may do so in [!badge icon="/images/discord-mark-blue.svg" text="#bot-dump"](https://discord.com/channels/512870694883950598/519131071502221313)

- `!bag ?` to see all available commands
- `!bag $ "Backpack"` to create a bag called "Backpack"
- `!bag "Backpack" + "Item"` to add an item to the "Backpack"
- `!bag "Backpack" - "Item"` to remove an item
- `!bag "Backpack" + 2 "Item"` to add multiple of the same item
- `!bag "Backpack" - 2 "Item"` to remove multiple of the same item

> `!bag pack <pack type>` to add a pack from the Player's Handbook.
> 
> e.g. `!bag pack "Explorer's Pack"`

## Lifestyle & Downtime (Optional)

:warning: Note: Lifestyle is handled in the DW server (not in D&D Beyond).

**Lifestyle** payments are a representation of your living costs. It is optional, but if you would like to do Downtime activities, you have to pay Lifestyle.

**Downtime** enable you to earn some extra gold, copy spells, and other neat features.

The full explanation on Lifestyle and Downtime can be found in [!badge icon="mark-github" variant="dark" text="Lifestyle and DTD Rules"](/downtime-and-lifestyle/lifestyle).

If you do not pay Lifestyle, you are considered to be benefiting from the Snowhaven Full Time Adventurer scheme and will stay in the [!badge icon="/images/discord-mark-blue.svg" text="#cozy-yeti-estates"](https://discord.com/channels/512870694883950598/611385164060295168) with your expenses covered for. 

As the name suggests, you spend your days looking for quests and being on call by the Senate rather than performing any other downtime activities.


## Joining a Guild (Optional)

You can see the list of available guilds under the **GUILDS** category, as well as in this pinned message in [!badge icon="/images/discord-mark-blue.svg" text="#guild-ooc"](https://discord.com/channels/512870694883950598/527458737892622361/941358894951825419)

They are all player managed, and the requirements of joining a guild vary. Some guilds require members to be over a certain level threshold, or be of a certain class. Check their pinned messages for such requirements or inquire with their leader if they don't specify any.

Some guild channels are public: this indicates you may RP checking out the guild hall, but not use their facilities.
