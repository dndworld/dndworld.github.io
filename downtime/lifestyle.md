---
label: Lifestyle
order: 20
icon: ":bread:"
---
# Lifestyle

**Lifestyle** payment is a representation of your living costs. It is optional, but if you would like to do DTD, you have to pay Lifestyle.

### Why do Lifestyles Matter?

Depending on which lifestyle you choose, your character’s lodging option changes.

> - [!badge icon="/images/discord-mark-blue.svg" text="#community-center"](https://discordapp.com/channels/512870694883950598/586370313755820032): **Poor** and **Squalid** living for the masses and the less fortunate.
> - [!badge icon="/images/discord-mark-blue.svg" text="#cozy-yeti-estates"]: **Modest** accommodations for those in need of a place to rest their head.
> - [!badge icon="/images/discord-mark-blue.svg" text="#cozy-yeti-upstairs"](https://discordapp.com/channels/512870694883950598/562928113793630228) & [!badge icon="/images/discord-mark-blue.svg" text="#white-dragon-hotel"](https://discordapp.com/channels/512870694883950598/561895920216702976): **Comfortable** living for those that want a little extra luxury in their stay.
> - [!badge icon="/images/discord-mark-blue.svg" text="#white-dragon-hotel"](https://discordapp.com/channels/512870694883950598/561895920216702976): **Wealthy** and **Aristocratic** living for those that have only the highest standards and the deepest pockets.

- **Self-sufficient** lifestyle is an option for those well-versed in surviving in the wilds. In order to gain this lifestyle, follow the instructions of [Self-sufficient Living DTD](lifestyle#self-sufficient-living).
- Some backgrounds provide free or discounted lifestyles for your character. Check [Lifestyle modifying backgrounds](lifestyle#lifestyle-modifying-backgrounds) for more information.

### What if I am not paying Lifestyle yet?

Lifestyle and DTD are optional mechanics on this server. Any characters not paying lifestyle are considered to be benefiting from Snowhaven’s Full Time Adventurer scheme and stay in the [!badge icon="/images/discord-mark-blue.svg" text="#cozy-yeti-estates"](https://discordapp.com/channels/512870694883950598/611385164060295168) with all expenses covered. As you are considered a "full time" adventurer, you may not do DTDs. 

## Step-By-Step Guide to Lifestyle

In order to do DownTime Days (DTD) activities, you need to pay Lifestyle **weekly** for each character. You may log lifestyle once a week on Mondays. The two halves of the lifestyle costs are **Lodging** and **Food**. 

### 1. Choosing Lifestyle

The base price of each lifestyle is as follows:

```
LIFESTYLE          PRICE/WEEK
Wretched †         Free
Squalid            7 sp
Poor               1g 4 sp
Self-sufficient ‡  Free
Modest             7 gp
Comfortable        14 gp
Wealthy            28 gp
Aristocratic       70gp

†) Free lifestyle still needs to be logged weekly
‡) Self-sufficient lifestyle requires Self-sufficient Living DTD
```

- Skip to [Step 2. "How to Set Up Lifestyle"](lifestyle#2-how-to-set-up-lifestyle)

#### Special Cases
> - If your character does not require food to survive, you only need to pay for the lodging. Therefore, the lifestyle cost is halved. Add `-div 2` to the end of your `!lifestyle` command.
> - If you have a spell which produces food or shelter, you may halve (or nullify if you have both) the cost of your lifestyle, given that you are casting the spell(s) daily. The spell must be appropriately logged in [!badge icon="/images/discord-mark-blue.svg" text="#spell-effects-log"] following the instructions of logging repeatedly-casted spells, then you may add `-div 2` or `-null` (whichever is applicable) to the end of your `!lifestyle` command.

### 2. How to Set Up Lifestyle ⭐

**First time only**

1. Choose a lifestyle for your character from the previous section 
- Your background may give you an alternative lifestyle option. Check out [Lifestyle modifying backgrounds](lifestyle#lifestyle-modifying-backgrounds) section for more information. 

2. In [!badge icon="/images/discord-mark-blue.svg" text="#lifestyle-log"](https://discordapp.com/channels/512870694883950598/586471153141284866), type the following command:

```
!lifestyle <your lifestyle> [options]
```

> Examples: 
> - `!lifestyle Poor`
> - `!lifestyle Modest -background "Acolyte"`

### 3. Logging Weekly
You can pull up the full help text by doing `!help lifestyle` in [!badge icon="/images/discord-mark-blue.svg" variant="info" text="#bot-dump"](https://discord.com/channels/512870694883950598/519131071502221313).
 
1. [Optional] React with ⏰ in [!badge icon="/images/discord-mark-blue.svg" text="#roles"](https://discordapp.com/channels/512870694883950598/535365321134178324) for a weekly reminder to log your lifestyle.
 
2. Every Monday, log your lifestyle in [!badge icon="/images/discord-mark-blue.svg" text="#lifestyle-log"](https://discordapp.com/channels/512870694883950598/586471153141284866).

```
!lifestyle <lifestyle> [options]
```

Whenever you run `!lifestyle` with any arguments, it will save those arguments for next time; so if your arguments do not change, you can just run `!lifestyle` (no arguments).
 
> Examples:
> - `!lifestyle`
> - `!lifestyle Poor`
> - `!lifestyle Modest -background "Acolyte"`

## Lifestyle modifying backgrounds
- Some backgrounds provide free or discounted lifestyles for your character. Even if your background makes the lifestyle free, **you need to log it weekly** in [!badge icon="/images/discord-mark-blue.svg" text="#lifestyle-log"](https://discordapp.com/channels/512870694883950598/586471153141284866) with the note stating the background. 

- You don’t have to choose the lifestyle that comes with the background, but if you choose any other lifestyle, you do not get the benefit from the background. Therefore, you need to pay the full price for the lifestyle.

> - **Acolyte**: Half of Modest lifestyle cost. You are assumed to stay at the [!badge icon="/images/discord-mark-blue.svg" text="#temple-to-the-gods"](https://discordapp.com/channels/512870694883950598/542431801394855936).
> - **Battlefield Medic**: Poor lifestyle for free. Troops and guards welcome you whenever you offer your assistance.
> - **Entertainer / Gladiator**: Comfortable lifestyle for 2 DTD points. In exchange for your performances, you receive free lodging and food.
> - **Faction Agent**: Modest lifestyle for free. Your lodging is covered by the faction you serve.
> - **Fisher**: Modest lifestyle for 1 DTD point. In exchange for the fresh catch you bring, you receive free lodging and food.
> - **Folk Hero / Haunted One**: Poor lifestyle for free, thanks to the common folks helping you out.
> - **Guild Artisan**: Modest lifestyle for free, with your monthly membership payment of 5gp. Add `-background "guild artisan"` to your `!lifestyle`, which will make the weekly cost 1.25 gp.
> - **Knight of the Order**: Half of Modest lifestyle cost. You only need to pay for food, as your lodging is covered..
> - **Mercenary Veteran**: Comfortable lifestyle for 2 DTD points. In exchange for your mercenary work, you receive free loging and food.
> - **Noble / Waterdhavian Noble / Knight (Noble Variant)**: Half of Comfortable lifestyle cost. You only need to pay for the food, as your lodging is covered.
> - **Outlander / Uthgardt Tribe Member**: Modest lifestyle for 2 DTD points, as you are able to live self-sufficiently if you spend some time preparing food and shelter for the week. You do not need to go through the normal process of Self-sufficient Living DTD.
> - **Smuggler**: Poor lifestyle for free, thanks to the support from the allies of your cause.

### To benefit from the Lifestyle Modifying Backgrounds

Each week you benefit from the background, log the lifestyle in [!badge icon="/images/discord-mark-blue.svg" text="#lifestyle-log"](https://discordapp.com/channels/512870694883950598/586471153141284866) with the `-background` flag.

Full command:

```
!lifestyle <lifestyle> -background <background>
```

!!!
For Lifestyle Modifying Backgrounds, `-div`, `null`, `-override`, `-dtd` are automatically applied.
!!!

> Example:
> - `!lifestyle poor -background "Folk Hero"`
> - `!lifestyle modest -background "Outlander"`

- Skip to [Step 3. "Logging Weekly"](lifestyle#3-logging-weekly)

## Self-sufficient Living

*It is possible to survive in the forest outside of town if you are skilled enough to hunt and make your own shelter. This can take up much of your downtime and is not without risks, but it does allow you to survive for free.*

Characters with **Outlander** or **Uthgardt Tribe Member** background do not need to go through the normal process of Self-sufficient Living DTD. More information in the [Lifestyle Modifying Backgrounds](lifestyle#lifestyle-modifying-backgrounds) section.

For each week you choose to find your own shelter and food with self-sufficient living, follow the next steps.

1. Fill in the form below in [!badge icon="/images/discord-mark-blue.svg" text="#dtd-manual-log"](https://discordapp.com/channels/512870694883950598/534036939368824848)

```
Self-Sufficient Living DTD

Character Name: 
Background: 

Nature check: [result]
Survival check: [result]
Nature or Survival: [result]

Notes: 
Consumes 2 DTD of weekly total.
```

2. Roll for food and shelter!

Make **all 3 checks** right after the form.
> - Nature: `!check Nature`
> - Survival: `!check Survival`
> - another Nature or Survival (your choice)

The Nature check is for gathering food, and the Survival check is for finding/making shelter. If any of the “Lifestyle: Special Cases” applies to your character, mark the corresponding check as “Auto-success” in the form and leave the details in the note.

3. Wait for the DTD to be processed.

You will be pinged in [!badge icon="/images/discord-mark-blue.svg" text="#dtd-results"](https://discordapp.com/channels/512870694883950598/586462271056904212)
 once it is processed. You gain a different lifestyle depending on how successful the checks were.

Follow the instruction and log your lifestyle in [!badge icon="/images/discord-mark-blue.svg" text="#lifestyle-log"](https://discordapp.com/channels/512870694883950598/586471153141284866).

```
!lifestyle <lifestyle gained> -null -dtd 2 -note “Self-sufficient living DTD”
```

## Appendix

### Characters Living in Guild Barracks & House
Guild barracks and Houses provide lifestyles for any character who lives there. To do so, guild taxes should be paid directly to your guild, and house tax should be logged in `⁠#tax-registration-log` following the rules in the Housing Document in [Advanced Play Rules](housing.md). After doing so, log the lifestyle with the `null` argument to nullify the lifestyle cost. Make sure to add a `-note` explaining the source of the benefited lifestyle.

> e.g.
> - `!lifestyle comfortable null -note "Large House Occupant"`
> - `!lifestyle wealthy null -note "Guild ABC guild barracks"`


### Quest-Locked Characters

While your character is participating in a multi-session bounty, your character is “Quest-Locked”. Quest-locked characters do not need to pay lifestyle, and are not allowed to do DTDs unless directed by the DM. (They are adventuring full-time!) 

In some cases, the quest-locked characters may be granted catch-up DTDs once the bounty is done. For more information, please refer to the [Catch-Up DTD section](dtd#special-case-catch-up-dtd).
