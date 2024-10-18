---
label: "Transactions"
icon: ":money_with_wings:"
order: 0
---
<style>
h1:before { 
  content: "💸 ";
}
</style>

All purchases, sales, and trades should be recorded in [#transaction-log](https://discordapp.com/channels/512870694883950598/531011819095982081).

## Making Transactions

> - Transaction Command:
> ```
> !transaction "<reason>" +Xgp
> ```
> Replace `<reason>` with the reason for your transaction, and keep the quotation marks. Please see the examples below.
> <br><br>
> - [Example] Adding Starting Gold:
> ```
> !transaction "Starting Gold: Folk Hero Background" +10gp
> ```
> - The command does not support decimals. Instead, you may use more than one currency at once:
> ```
> !transaction "Paying the bills" -7gp -5sp -11cp
> ```

## Coin Purse

> - `!transaction`: shows the coin purse.
> - `!transaction marks`: shows the coin purse including the Black Marks.
> <br><br>
> - `!csettings` > Cosmetic Settings > Toggle Compact Coin Display: to toggle the compact view. A compact view only shows the total in gp, instead of showing individual coin types.
> - `!coins convert` - Converts all of your coins into the highest value coins possible.

## Black Marks

> - `!transaction "Reason" +/-<amount>m`<br>
> Example: ```!transaction "Pit Fight: Pitmaster Returns" +2m```

## Magic Item Transactions

✅ Magic Item Transactions include:
- Buying and selling from the Black Market Bin
- Scheduled NPC magic item purchases/sales in <#597166678131867648> 
- Transfer of magic items between players (P2P transactions)

❌ Transactions do NOT include:
- Items obtained from DM events
- Birthday items
- Items obtained through the Cushion rule

### Automated React for Item Transactions

Please use the following templates for the transaction, including the title. Make sure the submitted form receives 🎐 `:wind_chime` automatically, but if for some reason the automation fails, make sure to add the react manually.

```
__Black Market Transaction Log__
**Character:** [Name], [Level]
**Player Discord ID:**
**Item:** [Name], [Rarity]
**Buying or Selling:** [Buying/Selling]
**Link(s) to Gold / Marks transactions:**
```

```
__Magic Item Transfer Between Players Log__
**Item:** [Name], [Rarity]
**Previous owner**
Character: [Name], [Level]
Player Discord ID:
**New owner**
Character: [Name], [Level]
Player Discord ID:
```

### Unlisted Magic Item Trade-In Log Template
```
__Unlisted Magic Item Trade-In Log__
**Character:** [Name], [Level]
**Player Discord ID:**
**Item:** [Name], [Rarity]
**Trade-in for:** [Gold/Marks]
**Link(s) to Gold / Marks transaction:**
```

### Buying Pets

When buying pets, use this format:
```
!transaction "Pet Shop: Buying <Species Name>" -Xgp
```
Example: `!transaction "Pet Shop: Buying Frog" -20gp`
