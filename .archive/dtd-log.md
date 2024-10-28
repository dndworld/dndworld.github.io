---
label: "DTD Log Pins"
icon: ""
order: 0
---
<!-- downtime -->
## `#lifestyle-log`

### [Step-By-Step Guide to Lifestyle](/downtime/lifestyle/#step-by-step-guide-to-lifestyle)

### [Logging Lifestyle Weekly ⭐ ](/downtime/lifestyle/#3-logging-weekly)

If anything has changed since the last time lifestyle was logged
```
!lifestyle <lifestyle> [options]
```

If nothing has changed
```
!lifestyle
```

Help text: `!help lifestyle` in `#bot-dump`

## `#dtd-automated-log`

### [Part-Time Work (PTW) 💰](/downtime/dtd-employment/#part-time-work-ptw)
```
!ptw <employer> <wage> <skill> [arguments]
```

### [High-Risk Work (HRW) 💰](/downtime/dtd-employment/#high-risk-work-hrw)
```
!hrw <employer> <check 1> <check 2> <check 3> [arguments]
```

!!!info
Even if you failed a PTW/HRW check, you still get paid normally.
!!!

## `#dtd-manual-log`

### Find DTD
- Please make sure to put the multi-word arguments "inside the quote"
```
!find <Seeking> <Search Location> <Search Method> <Skill>
```
Example: `!find "Employment at a smithy" "Market District" "Searching the market district for any signs of a forge by checking the skies for smoke and listening for the sounds of hammers on metal." "Investigation"`

### [Job Interview Check](/downtime/dtd-employment/#job-interview-checks)
```
JOB INTERVIEW CHECK

Interview opportunity: [1/3, 2/3, or 3/3]
Character Name:
Lifestyle:

Employer/Place of Work: 

Check: [check(s) requested]
Rolled: [result(s)]

RP: [describe how you are trying to impress your new boss!]
```
- Make the requested skill/tool check roll(s) after the form. Feel free to adjust the description of the RP accordingly.
- [Tool Check](/downtime/dtd-employment/#tool-checks)
```
!check [skill/tool check(s) requested]
```

### [Spell Research DTD](/downtime/dtd-spellbook/#spell-research)
```
Spell Research DTD

Character:
Type of Spellbook: [eg. Wizard Spellbook, Ritual Book, Book of Ancient Secrets, etc]
Character Background / Wizard School (if applicable):
Current Lifestyle:

Spell:
Spell level:
Required Research Point:

Arcana check roll: [result]
Research Progress: [Accumulated Point] / [Required Point]
Payment link: <>

Notes:
```
- Right after the form, make and **Arcana check**, and deduct 1 DTD point representing the day spent researching the spell. Adjust "Research Progress" field accordingly.
- On a Natural 1, you make no progress. On a Natural 20, you make double progress.
```py
!check arcana

!cc dtd -1
```

### [Copying Spells DTD Template](/downtime/dtd-spellbook/#copying-spells)
```
Copying Spells DTD

Character:
Current lifestyle:
[ Wizard School of Magic: (If applicable) ]

Spell(s) copying:
 - *[spell name]*: [source] -> [target]
 - ...

Time Spent / Required: [time spent]/[2 hours per spell slot level]
Gold Cost: [ ]gp
Payment link: <>
```
- Right after the form, deduct 1 DTD point representing the day spent copying spells.
```py
!cc dtd -1
```

### [Self-Sufficient Living DTD Template](/downtime/lifestyle/#self-sufficient-living)
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
Make **all 3 checks** right after the form.
> - Nature: `!check Nature`
> - Survival: `!check Survival`
> - Another Nature or Survival (your choice)

Wait for the DTD to be processed. You will be pinged in `#dtd-results`!

## injury-recovery-log

Moving from injury template to using the alias:

> 1) Run `!injury add "injury name"`<br>
> In case you have more than one injury, add them in the order you gained them.
> 
> 2) Run `!cc "Recovery Points" set [current progress]` to set the Recovery Points to match the latest injury recovery log.

### Injury Lookup
```
!injury list
```
### Add Injury
```
!injury add "<injury name>"
```
### List Character's Injuries
```
!injury
```
### Injury Recovery
> ```
> !injury recover
> ```
> Options:<br>
> `-note "Note goes here"` to add the notes<br>
> `-b #` to add bonuses from Medical Tent, Seeking Medical Help, Forage for Herbs, etc.<br>
> `-adv` to roll with advantage from Medic Aide, R&R, etc.<br>
> `-rr` for T5 Medical tent: rerolls 1s on the constitution saving throw.
> ```
> !injury recover base
> ```
> to roll the save without bonuses if arguments have already been saved.
> 
> Example: `!injury recover -note "T5 Medical tent, R&R" -adv -b 4 -rr`

### Injury Recovery by Spell (Regenerate)
```py
!injury remove all -note "(Link to the post in #spell-effects-log)"
```
### Injury Recovery at Healer’s Guild
```py
!injury remove "<name of the injury>" -note "(Link to the post in #dtd-automated-log)"
```
