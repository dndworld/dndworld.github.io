---
label: Consequences
order: 8
icon: ":adhesive_bandage:"
---

<style>
h1:before { content: "🩹 " }
</style>

# Consequences

*”High risk, high reward. High reward? High risk!”*

Some of the DTDs come with consequences, such as injury, infamy points, and/or fine.

!!!warning Remember to [set up your Lifestyle](/downtime/lifestyle/) before running DTDs!
It is optional, but if you would like to do DTD, you have to pay Lifestyle.

Be sure to follow the [DTD Rules](/downtime/dtd/#downtime-days-dtd-rules) when running DTDs too.
!!!

## Injuries

*Injuries that go beyond simple flesh wounds are more difficult to heal than a simple health restoring spell or potion.* 

While you have an injury, you will be hindered in some way. You may look up the **effect of an injury** with following command in [!badge icon="/images/discord-mark-blue.svg" variant="info" text="#bot-dump"](https://discord.com/channels/512870694883950598/519131071502221313):

```
!hb injury <name>
```

> Example: `!hb injury “fractured ankle”` (Use quotes around multi-word arguments)
> ```
> Recovery Points 75
> 
> Description
> Your ankle has been splinted and you are forced to move more slowly. Your movement speed is halved. Dis on acro.
> ```

If the injury you gained is unsuitable for the character’s body type, reflavor if possible. When in doubt, ask in [!badge icon="/images/discord-mark-blue.svg" variant="info" text="#dtd-ls-discussion"](https://discord.com/channels/512870694883950598/586697587932004362).

Each injury requires a different amount of Recovery Points (RP).
```
Injury            Recovery Point (RP)

Slipped Disc             90
Fractured hip            90
Fractured ankle          75
Fractured rib            75

Fractured wrist          75
Concussion               60
Black eye/eye injury     45
Infected wound           45
```

## Injury Recovery Basics

1. When you gain an injury from an automated DTD, the injury is added to the character **automatically**. You can check the current injuries by running the following.

```
!injury
```

In case you need to manually add the injuries, use `!injury add "<injury name>"`
> Example: `!injury add "Fractured ankle"`
 
2. As a representation of the course of natural recovery, each day (server time) you roll a **Constitution Saving throw**. This is automated by running the following command in [!badge icon="/images/discord-mark-blue.svg" variant="info" text="#dtd-injury-recovery-log"](https://discord.com/channels/512870694883950598/527370399667847188).

```
!injury recover
```
 
- The injury is automatically removed from your character when the Recovery Point is reached.
- If a character is affected by **multiple injuries**, you recover one injury at a time. If the accumulated RP (Recovery Point) exceeds the first injury's required RP, it is automatically carried over to the next injury.
- Because this represents the course of natural recovery, you may roll for any missed days after-the-fact. Please make sure that any penalty from the injuries were properly applied in any DM events or DTDs during the time.

!!!
Note that the DTD aliases automatically impose disadvantage on the relevant rolls (or change the ability score used for tools, if advantageous) if you're injured.
!!!

### Injury Recovery by Spell
- Casting the **Regenerate** spell on a character cures **all** injuries.
- The caster must properly log the casting of the spell in [!badge icon="/images/discord-mark-blue.svg" variant="info" text="#spell-effects-log"](https://discord.com/channels/512870694883950598/579612493345980447).
- Then, run the following command in [!badge icon="/images/discord-mark-blue.svg" variant="info" text="#dtd-injury-recovery-log"](https://discord.com/channels/512870694883950598/527370399667847188).

```
!injury remove all -note "(Link to the post in #spell-effects-log)"
```

### Injury Recovery at Healer’s Guild
- If a guild has the type “**Healer**”, the members of the guild may perform the Recover Injury DTD to cure **one** injury of a character.
- The guild member must run the following command in [!badge icon="/images/discord-mark-blue.svg" variant="info" text="#dtd-automated-log"](https://discord.com/channels/512870694883950598/579777361117970465).

```
!guild healer <Patient's Name> <Injury>
```

- Copy the messsage link of the Recovery Injury DTD output, and run the following command in [!badge icon="/images/discord-mark-blue.svg" variant="info" text="#dtd-injury-recovery-log"](https://discord.com/channels/512870694883950598/527370399667847188).

```
!injury remove "<name of the injury>" -note "(Link to the post in #dtd-automated-log)"
```

## Bonuses to Injury Recovery
 
There are a few things you can do to help with the injury recovery.
 
### Rest and Recovery (R&R) DTD

*You decide to take a full day off and rest.* 
 
- This uses 1 DTD point (you are resting!), and grants you advantage for the injury recovery Constitution save.
- In [!badge icon="/images/discord-mark-blue.svg" variant="info" text="#dtd-automated-log"](https://discord.com/channels/512870694883950598/579777361117970465):

```
!R&R
```
 
Then in [!badge icon="/images/discord-mark-blue.svg" variant="info" text="#dtd-injury-recovery-log"](https://discord.com/channels/512870694883950598/527370399667847188):

```
!injury recover -adv -note "Adv from R&R"
```
 
### Seeking Medical Help

- You can use **Find DTD** to find a doctor.
- If you successfully find a doctor, you can add +10 to your Constitution saves __each day until the injury is recovered__. This is effective for only **one** injury, which means you need to find a doctor again to gain the bonus for additional injuries.
- In [!badge icon="/images/discord-mark-blue.svg" variant="info" text="#dtd-injury-recovery-log"](https://discord.com/channels/512870694883950598/527370399667847188):

```
!injury recover -b 10 -note "Bonus from Medical Help"
```
!!!warning
This bonus does **not** stack with the bonus from the Forage for Herbs DTD.
!!!

### Forage for Herbs

*By searching the edges of the forest around town, various herbs and other natural remedies can be obtained.*

- In [!badge icon="/images/discord-mark-blue.svg" variant="info" text="#dtd-automated-log"](https://discord.com/channels/512870694883950598/579777361117970465):
 - Skill options: Nature or Survival

```
!forage <skill>
```

- For members of guilds with the Garden module, use `!forage Garden -note "Name of the Guild"` to handle the auto-success.

!!!
For the full help text, use `!help forage` in [!badge icon="/images/discord-mark-blue.svg" variant="info" text="#bot-dump"](https://discord.com/channels/512870694883950598/519131071502221313).
!!!

- If the result is a success, you can add +10 to your Constitution saves **each day until the injury is recovered**. This is effective for only **one** injury, which means you need to do Forage for Herbs DTD again to gain the bonus for additional injuries.

- In [!badge icon="/images/discord-mark-blue.svg" variant="info" text="#dtd-injury-recovery-log"](https://discord.com/channels/512870694883950598/527370399667847188):

```
!injury recover -b 10 -note “bonus from Forage for Herbs”
```

!!!warning Additional rules apply
- Herbs must be applied within 24 hours of being collected (when you get the result). 
- You may Forage for Herbs for another player’s character.
- This bonus does **not** stack with the bonus from the Seek Medical Help DTD.
!!!

## Consequences of Crime

See the [!badge icon="link-external" variant="info" text="Infamy & PvP document"](https://docs.google.com/document/d/1Y1f2yFzFxE2PgpTzqJVG95mtMms3iG_RAVuah84LvI0/) for a description of Infamy and list of punishments for crimes committed in Snowhaven. The sections below describe how to log these consequences.

## Infamy Points (IP)

Some DTD activities are considered crime or illegal, and there is a chance that you get caught in action and receive a number of **Infamy Points (IP)**.

When the DTD results indicate receiving IP, log it in [!badge icon="/images/discord-mark-blue.svg" variant="info" text="#infamy-log"](https://discord.com/channels/512870694883950598/762754975347507231) following the instructions in the channel pin.

## Community Service

As a consequence of committing a crime, you may be assigned to perform community services. *You will be pinged by a staff member if this is required.*

During this time, you need to perform at least 2 community services per week, otherwise you may find yourself facing additional penalties.

- (First time only) Set up the counters in [!badge icon="/images/discord-mark-blue.svg" variant="info" text="#dtd-automated-log"](https://discord.com/channels/512870694883950598/579777361117970465).

```
!CSDTD
```

- Perform the community service DTD in [!badge icon="/images/discord-mark-blue.svg" variant="info" text="#dtd-automated-log"](https://discord.com/channels/512870694883950598/579777361117970465).
```
!CS <number of days required>
```

## Snowhaven's Settlement Service

This DTD is for people who have fines they can't pay off. Until the fines are paid, the character is locked into this DTD alone (It will be made clear to you by the mods if you need this DTD).

- Each day you perform this DTD reduces your fine by 5gp.
- Post the following form in [!badge icon="/images/discord-mark-blue.svg" variant="info" text="#dtd-manual-log"](https://discord.com/channels/512870694883950598/534036939368824848) each day.

```
Snowhaven Settlement Service DTD

Character:

Total gold owed:
Gold repaid today: 5gp
Remaining balance:
```

- Right after the form, deduct 1 DTD point representing the day spent for the service.

```
!cc dtd -1
```

