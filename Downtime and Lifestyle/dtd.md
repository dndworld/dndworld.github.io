---
label: Downtime Days (DTDs)
order: 9
icon: 
---
# Downtime Days
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

## Job Interview Checks

Once you have found an employer for Part-Time Work DTD, or High-Risk Work DTD, you will be asked to make job interview checks in the ⁠`#dtd-results` post.

- Job Interviews __do not__ use DTD points.
- You can make one interview check per day, and you may have up to 3 interviews per employer.

Post the following form in `#⁠dtd-manual-log`. 

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

```
!check [skill check(s) requested]
```

## Tool Checks

- In order to use the tool, you must own the tool. Please refer to the [Snowhaven Market](https://docs.google.com/document/d/131lUJSH1DX0FLMfKKlO9irCnfG6zjwbjjG5-HKstWsU/) doc for the details.
- Make sure you add your tool proficiencies with `!tool` command.

> Examples:
> - `!tool pro "Mason's Tools"` to add proficiency
> - `!tool exp "Thieves' Tools"` to add expertise

!!!
For the full help text, use `!help tool` in `#bot-dump`
!!!

> Tool Check Example: `!tool "Carpenter's Tools" "STR"`

```
Alchemist's Supplies       INT / WIS
Brewer's Supplies          INT / WIS
Calligrapher's Supplies    DEX / WIS
Carpenter's Tools          STR / DEX

Cartographer's Tools       INT / WIS
Cobbler's Tools            DEX / INT
Cook's Utensils            DEX / WIS
Disguise Kit               DEX / CHA

Forgery Kit                DEX / CHA
Glassblower's Tools        DEX / INT
Herbalism Kit              INT / WIS
Jeweler's Tools            INT / CHA

Leatherworker's Tools      DEX / INT
Mason's Tools              STR / DEX

Musical instrument
"[Instrument Name]"        DEX / CHA

Painter's Supplies         DEX / CHA
Poisoner's Tools           INT / WIS
Potter's Tools             DEX / WIS
Smith's Tools              STR / DEX

Thieves' Tools             DEX / INT
Tinker's Tools             DEX / INT
Weaver's Tools             DEX / CHA
Woodcarver's tools         DEX / WIS
```

## Part-Time Work (PTW) 💰

*A part time job offers the promise of modest but consistent pay.*

- In order to do the Part-Time Work DTD, you need to first find the employer using [Find DTD](dtd#find).
- The starting wage for all PTW is **4gp** per day. You still get paid whether or not you pass the check, unless the output states otherwise.
- If you are using a tool for PTW, make sure to set up the proficiency with `!tool` alias. You can find the information under [Tool Checks](dtd#tool-checks)

#### Raises and Pay Cuts
> If you consistently perform well at your job with successful checks, you may be given a raise. Likewise, failing the checks may result in a pay cut. If your pay drops to zero or you fail five checks in a week, you are fired and need to find a new job.
> 
> The maximum wage per day with PTW is 6gp. Successful checks for a full week gives a one time bonus of extra 5gp.

In ⁠`#dtd-automated-log`:

```
!ptw <employer> <wage> <skill> [arguments]
```

!!!
For the full help text, use `!help ptw` in `#bot-dump`.
!!!

## High-Risk Work (HRW) 💰

*"High risk, high reward."*

*Some jobs, such as working for the local militia as a guard, involve risks. These jobs require multiple skills and come with a risk of injury for each failed check. However, they pay more, and are more forgiving when things go wrong.*

- In order to do the High-Risk Work DTD, you need to first find the employer using [Find DTD](dtd#find).
- The starting wage for all HRW is **6gp** per day. You still get paid whether or not you pass the check, unless the output states otherwise.

#### Raises and Pay Cuts
> If you consistently perform well at your job with successful checks, you may be given a raise. The maximum wage per day with HRW is 10gp.
> 
> Failing checks may result in a pay cut, or you may get fired. You can find out the details in the output of the `hrw` command.

In `⁠#dtd-automated-log`:

```
!hrw <employer> <check 1> <check 2> <check 3> [arguments]
```

!!!
For the full help text, use `!help hrw` in `bot-dump`.
!!!

> Example: `!hrw "Guard Barracks" "Perception" "Athletics" "Acrobatics"`

## Odd Jobs 💰

*Random tasks, for the unskilled and the fearless. These jobs are readily available and do not require you to Find an employer. However they vary wildly in profitability and safety.*

!!!
For the full help text, use `!help odd <job name>` in `#bot-dump`.
!!!

### Community Center Service

*Distribute food and other necessities among the needy at the community center. Simple job to earn some coins.*

In `#dtd-automated-log`:

```
!odd community
```

### Street Performance

*Earn money by performing in the street! Try not to get beaten up if people hate your act.*

In `#dtd-automated-log`:
- Skill options: Acrobatics, Performance, Sleight of Hand, or a musical instrument.

```
!odd perform <skill>
```

> Examples: 
> - `!odd perform Lyre`
> - `!odd perform “Sleight of Hand”` (Use quotes around multi-word arguments)

### Petty Crime
*Scrounge some gold from the pockets of the locals! Be careful though, you might get caught if things go poorly.*
 
In `#dtd-automated-log`:
- Skill options: Deception, Sleight of Hand, Stealth, Thieve's tools

```
!odd petty <skill>
```

> Example: `!odd petty “Sleight of Hand”` (Use quotes around multi-word arguments)

### Precarious Contracts

*Some people around town might find themselves in need of a hired hand for a riskier one-off job. These jobs may include things like big game hunting or locating a "lost item". Comes with a risk of injury if things don't go well, but the pay is good!*

In `#dtd-automated-log`:
- <Check 1> options: Acrobatics, Athletics, Stealth
- <Check 2> options: Animal Handling, Deception, Intimidation, Investigation, Nature, Perception

```
!odd contract <Check 1> <Check 2>
```

> Example: `!odd contract Stealth Deception`

Note: This DTD automatically uses an attack roll with the highest attack modifier from your character sheet.

## Guild DTDs

Each guild has one or two Guild Types. Depending on the type(s) of the guild, different DTDs are available to the members of the guild. For more information on guild types and DTD, please refer to the [Guild doc](https://docs.google.com/document/d/1A8sVmnksKwb9MX98f7Z6lfmdDgfxft85JPaQKejxXj0/edit).

To pull up the help text for each guild DTD, use following command in `bot-dump`.

```
!help guild [Name of DTD]
```

For help in joining a guild, please refer to [Joining a Guild (Optional)](/dwguide/start-playing/start-playing#joining-a-guild-optional/)

## Business DTD

If you have a registered business for your house in `#registered-businesses`, you may use Business DTD corresponding to the category of business you have. For more information on Businesses and categories of businesses, please refer to the [Business document](https://docs.google.com/document/d/1_BlD8lANtdI6qJKwAOXoi6OzRI2BzbE8WYMCipsX5ac/).

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