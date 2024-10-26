---
label: Employment
order: 12
icon: ":briefcase:"
---

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

- In order to use the tool, you must own the tool. Please refer to the [!badge icon="link-external" variant="info" text="Snowhaven Market"](https://docs.google.com/document/d/131lUJSH1DX0FLMfKKlO9irCnfG6zjwbjjG5-HKstWsU/) doc for the details.
- Make sure you add your tool proficiencies with `!tool` command.

> Examples:
> - `!tool pro "Mason's Tools"` to add proficiency
> - `!tool exp "Thieves' Tools"` to add expertise

!!!
For the full help text, use `!help tool` in [!badge icon="/images/discord-mark-blue.svg" variant="info" text="#bot-dump"](https://discord.com/channels/512870694883950598/519131071502221313)
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

- In order to do the Part-Time Work DTD, you need to first find the employer using [Find DTD](/downtime/dtd/#find).
- The starting wage for all PTW is **4gp** per day. You still get paid whether or not you pass the check, unless the output states otherwise.
- If you are using a tool for PTW, make sure to set up the proficiency with `!tool` alias. You can find the information under [Tool Checks](/downtime/dtd-employment/#tool-checks)

#### Raises and Pay Cuts
> If you consistently perform well at your job with successful checks, you may be given a raise. Likewise, failing the checks may result in a pay cut. If your pay drops to zero or you fail five checks in a week, you are fired and need to find a new job.
> 
> The maximum wage per day with PTW is 6gp. Successful checks for a full week gives a one time bonus of extra 5gp.

In ⁠`#dtd-automated-log`:

```
!ptw <employer> <wage> <skill> [arguments]
```

!!!
For the full help text, use `!help ptw` in [!badge icon="/images/discord-mark-blue.svg" variant="info" text="#bot-dump"](https://discord.com/channels/512870694883950598/519131071502221313).
!!!

## High-Risk Work (HRW) 💰

*"High risk, high reward."*

*Some jobs, such as working for the local militia as a guard, involve risks. These jobs require multiple skills and come with a risk of injury for each failed check. However, they pay more, and are more forgiving when things go wrong.*

- In order to do the High-Risk Work DTD, you need to first find the employer using [Find DTD](/downtime/dtd/#find).
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
