---
label: Downtime Days
order: 14
icon: ":bed:"
---

**Downtime Day (DTD)** activities can enable you to earn some extra gold, copy spells, and other neat features.

## DownTime Days (DTD) Rules

- You have 5 DTD points per week when you pay lifestyle, and they expire every Monday at midnight server time (EST). Therefore, you may not stock up the unused DTD points.
- You can only do 1 DTD per day. The day is determined by the server time (EST).
- Lifestyle and other factors may affect the DC for your rolls. The details are intentionally undisclosed to prevent min-maxing and metagaming.
- Only passive effects may be applied, for example: Jack of All Trades, proficiency, Expertise, Tireless Precision.
- Some DTDs require manual reviews from staff, and this may take more than one day. You do not need to wait for the previous day’s manual DTD to be processed before doing today’s DTD.

## Find

Use Find DTD to find:
> - Employer for Part-Time Work DTD
> - Employer for High-Risk Work DTD
> - Guild aide
> - Medical help (for injury recovery)

DMs may use Find DTD for other purposes.

For each Find DTD, you need following information:
> - **Seeking**: What/Who you are looking for
> - **Search Location**: Area/Region of Snowhaven where you are searching. An RP channel name.
> - **Search Method**: Description of your search
> - **Skill**: Choose from Perception, Investigation, or Persuasion

*Not everything can be found in the humble village of Snowhaven, nor is everything known. It may be impossible to Find some things, although if you're lucky you might stumble upon clues as to where would be a better place to look.*

Put this command with the information in `#dtd-manual-log`:

```
!find <Seeking> <Search Location> <Search Method> <Skill>
```

> Example: `!find "Employment at a smithy" "Market District" "Searching the market district for any signs of a forge by checking the skies for smoke and listening for the sounds of hammers on metal." "Investigation"`

You will receive a ping in `#dtd-results` when your log is processed.


## Learning

*Ever curious what those people in the tavern were whispering to one another or wanted to pick up a hobby? With Learning DTD you can learn to play new instruments, use new tools, and even speak a new language!*

Learning DTD gives you __proficiency in instruments, tools, or languages__. Each subset requires a different amount of learning points.
```
Instrument           75 Learning Points
Gaming Set           75 Learning Points
Artisan Tool         85 Learning Points
Misc. Tool          100 Learning Points
Standard Language    90 Learning Points
Exotic Language     125 Learning Points
```
- [!badge icon="link-external" variant="info" text="List of tools/instruments"](https://www.dndbeyond.com/sources/basic-rules/equipment#Tools)
- [!badge icon="link-external" variant="info" text="List of languages"](https://www.dndbeyond.com/sources/basic-rules/personality-and-background#Languages)

- *[!badge icon="link-external" variant="info" text="Koume Sign Language (KSL)"](https://docs.google.com/document/d/1ZysB8Jyc3LfVMKOtiQwODfT1s2oI38shuTeCnbyOSPs/#heading=h.3msemhbc7iyt) has been added to the list of languages that can be learnt.*
- *Note that Thieves' Cant and Druidic cannot be learnt through the Learning DTD without a specific Guild Perk.*


### Learning Cap

> - You may learn a total number of instruments, tools, and languages equal to 1 + your **natural** Intelligence modifier. You cannot gain additional proficiencies using Learn DTD if you have a negative intelligence modifier.

> - If a character's learning cap has been reached, one of the learned instruments/gaming sets/tools/languages may be replaced by learning a new one.

### Learning DTD Command

> In [!badge icon="/images/discord-mark-blue.svg" variant="info" text="#dtd-automated-log"](https://discord.com/channels/512870694883950598/579777361117970465):<br>
> ```
> !learn <Subject>
> ```
> Example: `!learn "Smith's Tools" [options]`

> - **Subject**: the instrument/gaming set/tool/language you wish to learn
> - By default, this command rolls an Intelligence check. For __instruments and gaming sets__, you can choose between Intelligence and Charisma. To use charisma score, add `cha` in the command.

> ℹ️ For the full help text including the options, use `!help learn` in [!badge icon="/images/discord-mark-blue.svg" variant="info" text="#bot-dump"](https://discord.com/channels/512870694883950598/519131071502221313).

### Learning Bonuses

> - Items such as a *Headband of Intellect* do not increase the number of instruments/tools/languages you can learn, but you may apply the bonuses when making the learning checks.

> - If you have the **Anthropologist** background, you have advantage on learning languages.

> - If you know a subset of Primordial (Auran, Aquan, Ignan, or Terran), you have advantage on learning the full language of Primordial.




## Combat Training

*"Practice makes perfect!"*

Combat Training DTD provides a small amount of XP depending on success rate.

- The cost is **1gp per character level**. This is automatically deducted from the coin purse when you use the alias.
- Some guild modules and aides may provide a bonus to the combat training DTD. For more information, please refer to the pinned messages of each guild’s channel.
- ⚠️ You **cannot** transfer RPXP to XP with combat training. This can only be done after the character has participated in a DM sanctioned event.

1️⃣ In [!badge icon="/images/discord-mark-blue.svg" variant="info" text="#dtd-automated-log"](https://discord.com/channels/512870694883950598/579777361117970465):
```
!train [arguments]
```
2️⃣ Add the earned XP in [!badge icon="/images/discord-mark-blue.svg" variant="info" text="#xp-tracker"](https://discord.com/channels/512870694883950598/531014104098537481), following the output of the combat training.
```
!dxp train <xp>
```

ℹ️ For the full help text, use `!help train` in [!badge icon="/images/discord-mark-blue.svg" variant="info" text="#bot-dump"](https://discord.com/channels/512870694883950598/519131071502221313).

## Guild DTDs

Each guild has one or two Guild Types. Depending on the type(s) of the guild, different DTDs are available to the members of the guild. For more information on guild types and DTD, please refer to the [!badge icon="link-external" variant="info" text="Guild doc"](https://docs.google.com/document/d/1A8sVmnksKwb9MX98f7Z6lfmdDgfxft85JPaQKejxXj0/).

To pull up the help text for each guild DTD, use following command in `bot-dump`.

```
!help guild [Name of DTD]
```

For help in joining a guild, please refer to [Joining a Guild (Optional)](/start-playing/start-playing/#joining-a-guild-optional)

## Business DTD

If you have a registered business for your house in `#registered-businesses`, you may use Business DTD corresponding to the category of business you have. For more information on Businesses and categories of businesses, please refer to the [!badge icon="link-external" variant="info" text="Business document"](https://docs.google.com/document/d/1_BlD8lANtdI6qJKwAOXoi6OzRI2BzbE8WYMCipsX5ac/).

To pull up the help text for Business DTD, use following command in `bot-dump`.

```
!help business
```

There is no risk of infamy points (IP) or injuries with Business DTD, but on a rainy day, your business may not yield any profits.

## Special Case: Catch-Up DTD

Catch-Up DTD is for characters who returned from being Quest-Locked for a multi-session bounty. The number of DTD points are determined by the DM at the end of the bounty.

### Catch-Up DTD Rules

- You need to pay the lifestyle cost in order to perform the Catch-Up DTDs. Each lifestyle payment covers 5 DTD points, just as the normal lifestyle payment does.
- Catch-Up DTDs can be performed all in one day. 
- You need to use up the Catch-Up DTD points **before** attending any other DM events or performing normal DTDs. Unused Catch-Up DTD points are voided.
- For automated DTDs, make sure to **add a note** indicating that you are performing Catch-Up DTDs.
- **Injuries** are accumulated as normal during the Catch-Up. For the injury recovery purposes, consider there is one long rest per each day of catch-up DTD, and for each set of 5 DTDs, consider there to be 7 long rests.