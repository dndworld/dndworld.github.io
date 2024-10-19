---
label: Next Steps
order: 100
icon: ":rocket:"
---

<style>
h1:before { content: "🚀" }
</style> 

# Next Steps

This page is to teach you what to do after creating your character. If you have not done so yet, check out [Start Here](/character-building/start-here/)

## Setting up Class, Race, Custom Counters (CCs)

**Custom Counters** are used to keep track of various resources, such as race ability (e.g. Half-Orc's Relentless Endurance), class ability (Fighter's use of Second Wind), ammunition, charges on a magic item, etc.

!!!success
For **D&D Beyond** sheets, this is **already done for you**. You can skip to [!button variant="success" text="Tracking Money"](start-playing/#tracking-money.md)
!!!

For other sheets, setting up the class abilities is automated using Avrae. Run the commands below in `#bot-dump` for the setup.

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

> - Once you've updated character sheet, run `!update` and `!level` in `#bot-dump`. You may need to set the subclass manually by running `!level [class] [subclass]`.
> - Once your character gains a level, make sure to change your reacts in `#roles` in order to receive the game post pings for the new level.

## Tracking Money

Money and XP are tracked on the server. They are **not** synced with your sheet, so it does not matter if your sheet is updated with this info (tracking XP is explained later in this channel).

#### Check Coin Purse

Use `!transaction` to check your coin purse.

#### Make Transaction

Log your monetary transactions in `#transaction-log` with:

```
!transaction "reason for transaction" +Xgp
```

!!!warning
Transactions logged outside of the appropriate channels are considered invalid.
!!! 

> You can chain multiple currencies to the command like so:
> 
> `!transaction "reason for transaction" +Xgp +Xsp +Xcp`

=== [Example] Adding Starting Gold

!!! 
For DDB importations, Avrae should automatically handle this step. Your coin purse may sync the first time you run `!import`, so check with `!transaction` first. 
!!!

In `#transaction-log`, replace **#** with the starting gold amount.
```
!transaction "Starting Gold" +#gp
```
 
> - `!transaction "Folk Hero Starting Gold" +10gp`
> - `!transaction "Haunted One Starting Gold" +1sp`
> - `!transaction "Monk Rolled Gold" +12gp`
===

## Roleplaying

Roleplaying (RP) gives your characters **RPXP**, which can later be turned into XP (The process is explained later in this channel).

#### RP Channels

You can go to any of the channels in the Snowhaven: West/High Class/North/South, Underhaven, Nanam in Nature, and Arena categories to RP. 

- `#drunken-yeti-tavern` is the most popular channel to RP, and a great place to start.
- `#rp-board` is where you can make a post to look for RP, or join one that is already posted.

#### Other Channels

- You cannot go into any of the channels marked under the DO NOT ENTER category.
- All channels listed under GAME CHANNELS # as well as the channels listed under TRAINEE GAMES category are reserved for DM events only.

#### Entering the Town

You may want to RP your character entering Snowhaven in `#gates`. There is no set way to introduce yourself. However, most people write their introduction as if people are seeing them for the first time. 

They would describe how their character looks like and say what they are doing, which usually gives something other characters can interact with. 

> [Example] *Zoey enters the gates, taking in the sights around her. She is a 6‘0 tall human with long red hair, her shiny metal armor making clinks as she walks. Seeing a welcoming puff of smoke in the distance, she heads towards the tavern looking for a drink.*

#### Follow the Rules

Please use common sense and behave as you would in a public setting. Follow the [rules](/rules). Breaking things and crime will definitely get you thrown into jail as the RP channels are meant as a safe zone.

## RPXP

Full explanation can be found in [How to Earn XP](earn-xp.md)

#### First time

Set up your counters: `!rpxp` in `#xp-tracker` (only need to do it once per character)

### Steps

1. React to your first RP post with :beginner: `:beginner:` and last RP post with :octagonal_sign: `:stop:`. Get the person you are RPing with to react as well.

2. Find out how long the RP session was. `#rp-log` picks up the messages reacted with :beginner: & :octagonal_sign:.

3. Log the RPXP in `#xp-tracker` by the increments of half an hour (rounded down)

`!rpxp <hours> [message]`

> Example:
> 
> ```
> !rpxp 1.5 "#the-library"
> ```

### Weekly Cap

**Every Monday (EST)** you can reset your Weekly RPXP Cap by running the following command in `#xp-tracker`:

```
!rpxp cap reset
``` 

## OOC Channels

OOC stands for **Out Of Character**. 

#### RP OOC channels

Snowhaven: West/High Class/North/South, Underhaven, Nanam in Nature, Shops, and Arena categories have respective `#[category]-ooc` channels for out-of-character conversations.

#### Other OOC channels

When you aren't RPing or taking part in events, you can chill in `#off-topic-general` where you can talk about character builds, recent bounties, real life stuff, etc. 

There are channels for specific content under the **DnD Chat** category. Please try to keep posts related to those topics contained to those channels. Similarly, please keep bot commands to `#bot-dump`.

## Signing up for DM events

Full explanation on the available game types on the server can be found in [How to Earn XP](earn-xp.md).

1. Wait for Level pings

Wait for a DM to ping your level for a bounty in `#bounty-board` or an arena/hunt/pit fight in `#arena-board`. 

2. Check if signups are still Open

Event posts with a :x: or :negative_squared_cross_mark: reaction are closed for signups.

3. Signup

If the event is still open for signups, copy the **template** posted by that DM, fill it in, and post it in `#game-signup`

!!! How to check "RPXP Stored" and "XP to Next Level"
In `#bot-dump`, run `!rpxp xp`
!!!

4. Acceptance

Game acceptance is announced in `#game-signup`. If you are accepted, the DM will ping you to confirm your attendance. React with the appropriate emoji to confirm your acceptance.

5. Before the Game

The DM will ping you again in the appropriate OOC (out of character) channel for the game.

6. After the Game: Tracking XP

`#xp-tracker` is used for you to track XP on this server.

To add the XP from the game:

```
!dxp game <amount> <source>
```

> (e.g. `!dxp game 100 "Red Ruby Heist"`)

All XP must be tracked in `#xp-tracker` with the `!dxp` alias. 

When you level up, adjust your sheet accordingly and run `!update` in `#bot-dump`. No sheet link is required.


## Intoxication Counter (Optional)

Intoxication Counter follows a homebrew system which you can read more about in the pins of `#drunken-yet-tavern`. This determines your state of drunkenness. 

Running `!drink [name of drink]` will automatically setup the counters you need.
> e.g.: `!drink "Dwarven Firewhiskey"`


**Interacting with the Intoxication Counters**

- `!cc intox` to view the counter
- `!cc intox set 0` to reset the counter

## Bag Management (Optional)

!!! 
Your character sheet needs to list your equipment.
!!!

Bag management within the server is completely optional. Should you want to track your items, you may do so in `#bot-dump`

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

Full explanation on Lifestyle and Downtime can be found in [Lifestyle and DTD Rules](/downtime-and-lifestyle/lifestyle).

:warning: Note: Lifestyle is handled in the DW server (not in D&D Beyond).

**Lifestyle** payment is a representation of your living costs. It is optional, but if you would like to do Downtime activities, you have to pay Lifestyle.

**Downtime** can enable you to earn some extra gold, copy spells, and other neat features.

If you do not pay Lifestyle, you are considered to be benefiting from the Snowhaven Full Time Adventurer scheme and will stay in the `#cozy-yeti-estates` with your expenses covered for. 

As the name suggests, you spend your days looking for quests and being on call by the Senate rather than performing any other downtime activities.


## Joining a Guild (Optional)

You can see the list of available guilds under the **GUILDS** category, as well as in this pinned message in [`#guild-ooc`](https://discord.com/channels/512870694883950598/527458737892622361/941358894951825419)

They are all player managed, and the requirements of joining a guild vary. Some guilds require members to be over a certain level threshold, or be of a certain class. Check their pinned messages for such requirements or inquire with their leader if they don't specify any.

Some guild channels are public: this indicates you may RP checking out the guild hall, but not use their facilities.
