---
label: Odd Jobs
order: 10
icon: ":supervillain:"
---

*Random tasks, for the unskilled and the fearless. These jobs are readily available and do not require you to Find an employer. However they vary wildly in profitability and safety.*

!!!
For the full help text, use `!help odd <job name>` in [!badge icon="/images/discord-mark-blue.svg" variant="info" text="#bot-dump"](https://discord.com/channels/512870694883950598/519131071502221313).
!!!

!!!warning Remember to [set up your Lifestyle](/downtime/lifestyle/) before running DTDs!
It is optional, but if you would like to do DTD, you have to pay Lifestyle.

Be sure to follow the [DTD Rules](/downtime/dtd/#downtime-days-dtd-rules) when running DTDs too.
!!!

## Community Center Service

*Distribute food and other necessities among the needy at the community center. Simple job to earn some coins.*

In [!badge icon="/images/discord-mark-blue.svg" variant="info" text="#dtd-automated-log"](https://discord.com/channels/512870694883950598/579777361117970465):

```
!odd community
```

## Street Performance

*Earn money by performing in the street! Try not to get beaten up if people hate your act.*

In [!badge icon="/images/discord-mark-blue.svg" variant="info" text="#dtd-automated-log"](https://discord.com/channels/512870694883950598/579777361117970465):
- Skill options: Acrobatics, Performance, Sleight of Hand, or a musical instrument.

```
!odd perform <skill>
```

> Examples: 
> - `!odd perform Lyre`
> - `!odd perform “Sleight of Hand”` (Use quotes around multi-word arguments)

## Petty Crime
*Scrounge some gold from the pockets of the locals! Be careful though, you might get caught if things go poorly.*
 
In [!badge icon="/images/discord-mark-blue.svg" variant="info" text="#dtd-automated-log"](https://discord.com/channels/512870694883950598/579777361117970465):
- Skill options: Deception, Sleight of Hand, Stealth, Thieve's tools

```
!odd petty <skill>
```

> Example: `!odd petty “Sleight of Hand”` (Use quotes around multi-word arguments)

## Precarious Contracts

*Some people around town might find themselves in need of a hired hand for a riskier one-off job. These jobs may include things like big game hunting or locating a "lost item". Comes with a risk of injury if things don't go well, but the pay is good!*

In [!badge icon="/images/discord-mark-blue.svg" variant="info" text="#dtd-automated-log"](https://discord.com/channels/512870694883950598/579777361117970465):
- `<Check 1>` options: Acrobatics, Athletics, Stealth
- `<Check 2>` options: Animal Handling, Deception, Intimidation, Investigation, Nature, Perception

```
!odd contract <Check 1> <Check 2>
```

> Example: `!odd contract Stealth Deception`

Note: This DTD automatically uses an attack roll with the highest attack modifier from your character sheet.
