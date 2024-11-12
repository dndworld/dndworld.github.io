---
label: "Bot FAQ"
icon: ":robot_face:"
order: 0
---
<style>
h1:before { 
  content: "🤖 ";
}
</style>

## Notices

### Avrae Scheduled Update Window

Avrae's scheduled update window is 1400-1500 EST (2PM-3PM), Tuesday afternoons. During these periods, Avrae may go offline for up to 30 minutes.

Any unscheduled updates will be shown in [!badge icon="/images/discord-mark-blue.svg" variant="info" text="#bot-statuses"](https://discord.com/channels/512870694883950598/744861406158913566)

### Gsheet: Black Error Boxes

If you are seeing black boxes in your Gsheet, that's because some of the images for its style were lost to the void. The images are purely cosmetic and do not affect Gsheet's functionality, so it's optional to fix them.

[!badge icon="link-external" variant="info" text="The official template"](https://gsheet2.avrae.io/) and the DW HB variant have been (mostly) fixed, so you can copy-paste the necessary formulas from them and onto your sheet. Tabs with missing images are:
- `v2.1` (several on the top section, one in the bottom section)
- `?` (the formulas for the Proficiencies box in `v2.1` work for the missing images here too)
- `Attack Info`, `Gear Info`, `Race Info`, `Class Info` (the same formula works for each of the missing images in each of these)

## Player Resources

[!badge icon="link-external" variant="info" text="Blood Hunter Commands"](https://avrae.io/dashboard/workshop/5f6f9b1e192fdca3888bc29d)
- `!level` gvar: `a55768e6-9b31-4dfc-9fbd-2a601e419823`

## Aliasing and Automation Resources

### Quick Links

**[!badge icon="link-external" variant="info" text="Aliasing Help/Documentation"](https://avrae.readthedocs.io/en/latest/)**
- [!badge icon="link-external" variant="info" text="Basics"](https://avrae.readthedocs.io/en/latest/aliasing/aliasing.html)
- [!badge icon="link-external" variant="info" text="API"](https://avrae.readthedocs.io/en/latest/aliasing/api.html)
- [!badge icon="link-external" variant="info" text="Tutorials"](https://avrae.readthedocs.io/en/latest/aliasing/aliasing_tut.html)

**Attack/Spell Automation (Making Spells/Attacks Work)**
- [!badge icon="link-external" variant="info" text="Reference"](https://avrae.readthedocs.io/en/latest/automation_ref.html)

**Cheatsheets**
- [!badge icon="link-external" variant="info" text="Getting Started"](https://avrae.readthedocs.io/en/latest/cheatsheets/get_started.html)
- [!badge icon="link-external" variant="info" text="DM Combat Guide"](https://avrae.readthedocs.io/en/latest/cheatsheets/dm_combat.html)
- [!badge icon="link-external" variant="info" text="Player Combat Guide"](https://avrae.readthedocs.io/en/latest/cheatsheets/pc_combat.html)

### Quick Start to Automation

- Output an embed (Do **not** use this for RP -> [Rule 7️⃣](/rules/))
More on embed arguments can be found in `!help embed`
> ```
> !alias [alias name] embed -title "My Title" -desc "My description" -f "Field 1|Field text"
> ```

- Deal additional damage (e.g. Spellsword's Incantation)
> ```
> !snippet incan_fire -d 1d4[fire] -f "Spellsword's Incantation|Description goes here"
> ```

### Breakdown of `!a add` (Adds Custom Attacks)

First, we have the command itself, which says we want to add an attack called `Greatsword`
> ```
> !a add "Greatsword"
> ```
Next we want to cover for the to hit modifier, so we use the `-b` argument:
> ```
> -b strengthMod+proficiencyBonus
> ```
With this, we specify that we want the bonus to the the strength modifier plus the proficiency bonus

Next we need the damage, so we use the `-d` argument:
> ```
> -d 2d6+{strengthMod}[slashing]
> ```
We state that we want the damage to be 2d6 + strength modifier damage.
In this case, since the damage involves dice and damage, etc, we need `{}` around the variable `strengthMod`.
The brackets signify that we want to use variables as part of a math expression.

Now in your case, we want to add great weapon fighting as well, and this is where the `ro<3` comes in (which means reroll any 1's or 2's once, and keep the second roll even if it is a 1 or 2 again)
We add it to the end of the dice part:
> ```
> -d 2d6ro<3+{strengthMod}[slashing]
> ```

Now if you want to add a description, you would add it like this:
> ```
> -desc "This is the description of the attack"
> ```
But in this example, it won't be used.

Finally, let's put it all together:
> ```
> !a add "Greatsword" -b strengthMod+proficiencyBonus -d 2d6ro<3+{strengthMod}[slashing]
> ```
