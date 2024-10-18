---
label: Spellbook DTDs
order: 7
icon: ":book:"
---
<style>
h1:before { content: "📖 " }
</style>

# Spellbook DTDs

Spellbook DTDs are for spellcasters who require a **Spellbook** for casting spells.

> - Classes: Wizard, Cardmaster, Spellsword
> - Others: Pact of the Tome Warlock, Ritual Caster feat


## Copying Spells

A few things for Copying Spells in **Dnd World** are different from the D&D 5e Basic Rules.

- For copying a new spell into your spellbook, the process takes 2 hours and costs **20 gp** per spell level (Basic Rule is 50gp).
- For copying a spell you’ve already learned, the process takes 1 hour and costs **5gp** per spell level (Basic Rule is 10gp). This includes copying from one spellbook of yours to another spellbook of yours, as well as copying from your own research note (info is in Spell Research DTD) to your own spellbook.
- If you are a Wizard specialized in the school of magic of the spell you are copying, the gold and time you must spend to copy the spell into your spellbook is halved.
- Wizards with the **Order of Scribes** subclass may copy any number of spells per DTD. The gold cost of it stays the same.
- If you are copying a spell from a spell scroll, the process follows the same rules as copying a new spell from a spellbook. The scroll is **not** consumed at the end of this process. 
- Maximum **8 hours per day** can be spent for copying spells. Therefore, any spell that would require more than 8 hours would require multiple DTD. 
- You may copy multiple spells using one DTD as long as the total processing time is within 8 hours.

### Copying Spells How-To

- Each day you are copying spells, log the payment in `#transaction-log`, and fill in the following form and post in `#dtd-manual-log`.

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

```
!cc dtd -1
```

## Spell Research

*"Knowledge is power"*

If you have knowledge about a spell you haven’t learned, and do not have access to a spellbook or scroll with the spell written on it, you can still spend your days researching the spell in order to learn it.

#### Rules & Limitations

*Information on spells above 3rd level cannot be found readily in the literature available in Snowhaven, and so must be invented or developed personally, increasing the difficulty.*

- The spell you choose to research needs to be a spell you can cast in the end. This means, the spell needs to be on the spell list for your class, or your character is capable of casting it by other means.
- You **cannot** learn spells of 7th level and above with Spell Research DTD
- After completing your research, you produce research notes for the spell which only you can comprehend. You (and only you) can use these research notes to copy the researched spell into your spellbook, using the **Copying Spells** downtime activity. The spell you have researched is considered "known" to you can be copied into your spellbook at a cost of 5gp and one hour per spell level.


### Spell Research DTD How-To

1. Pay the cost

- Each day you perform the Spell Research DTD, make a payment of 5gp in `#transaction-log`. This represents access to certain repositories of knowledge, such as research articles and restricted library sections. 
- Characters with the **Cloistered Scholar background** pay only half, thanks to the Library Access background feature.

2. Log the research

- Each spell requires a different amount of research points depending on the level of the spell.
```
Spell | Research
Level | Points
======+=========
    1 | 50
    2 | 100
    3 | 150
    4 | 400
    5 | 500
    6 | 600
   7+ | Unavailable
```

- Fill in the form and post in `#dtd-manual-log`.

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

3. Do the research!

- Make an **Arcana check** after the form, and deduct 1 DTD point to represent the day spent researching spells. The result of the Arcana Check is the amount of Research Points you gain towards the completion of your research. Adjust "Research Progress" field accordingly.
- On a Natural 1, you make no progress. On a Natural 20, you make double progress.

```
!check arcana

!cc dtd -1
```

## Bonuses to Spell Research

- If you are a **Wizard** specialized in the school of magic of the spell you are researching, the Research Points needed is reduced by half as you already have a strong understanding of theoretical foundations of the spell. 
 
- Characters with the **Sage** background have advantage on their Arcana Check, as they are skilled at research and know where to look first for the information they seek.

```
!check arcana adv -phrase "Adv from Sage background"
```
- Characters with the **Cloistered Scholar** gain a +1 bonus to their Arcana check as they have preferential treatment in the library.

```
!check arcana -b 1 -phrase "Bonus from Clostered Scholar background"
```