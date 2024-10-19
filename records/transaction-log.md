---
label: "Transactions"
icon: ":money_with_wings:"
order: 9
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

### Buying Pets

When buying pets, use this format:
```
!transaction "Pet Shop: Buying <Species Name>" -Xgp
```
Example: `!transaction "Pet Shop: Buying Frog" -20gp`

## Black Marks

> - `!transaction "Reason" +/-<amount>m`<br>
> Example: ```!transaction "Pit Fight: Pitmaster Returns" +2m```

## Magic Item Transactions

✅ Magic Item Transactions include:
- Buying and selling from the [**Black Market Bin**](https://docs.google.com/document/d/166Do3cLcg_NYRZqSaAN34LQxY9C5xda5WDb9kYezJMM)
- Scheduled NPC magic item purchases/sales in [#black-market-registry](https://discordapp.com/channels/512870694883950598/742720804525178900)
- Transfer of magic items between players (P2P transactions)

❌ Transactions do NOT include:
- Items obtained from DM events
- Birthday items
- Items obtained through the Cushion rule 

Please use the following templates for the transaction, including the title.
```
__Black Market Transaction Log__
**Character:** [Name], [Level]
**Player Discord ID:**
**Item:** [Name], [Rarity]
**Buying or Selling:** [Buying/Selling]
**Link(s) to Gold / Marks transactions:**
```

!!!A bot should react to your form with 🎐 `:wind_chime` automatically, but if for some reason the bot fails, do add the react manually.
!!! 

If you are trading in an item not on the Black Market Bin, please use the following template. Refer to the[ Black Market document](https://docs.google.com/document/d/166Do3cLcg_NYRZqSaAN34LQxY9C5xda5WDb9kYezJMM) for prices.
```
__Unlisted Magic Item Trade-In Log__
**Character:** [Name], [Level]
**Player Discord ID:**
**Item:** [Name], [Rarity]
**Trade-in for:** [Gold/Marks]
**Link(s) to Gold / Marks transaction:**
```

### Magic Item Benefactor Rules
#### 1. Level Limitations
> - Characters (or guilds) may only give magic items of certain rarity to other characters based on the table below.
> ```
> Common: Level 1+
> Uncommon: Level 4+
> Rare: Level 8+
> Very Rare: Level 12+
> Legendary: Level 16+
> ```
#### 2. Lending/Borrowing
> - Characters (or guilds) may freely lend magic items if they are listed in the Black Market document, following the Level Limitations above.
> - Homebrew items are not allowed to be lent/borrowed.
> - Non-homebrew items that are not on the black market bin list can be borrowed for RP purposes following the Level Limitations above. For games, the DM running the game has the final say in whether the borrowed item is allowed in their game.
> - You do not need to fill in the "Magic Item Transfer" form for borrowing an item.
#### 3. Ownership Transfer
> - Transferring the ownership of a magic item needs to be recorded in `#transaction-log` using the following form:
> ```
> **Magic Item Transfer Between Players Log**
> **Item:** [Name], [Rarity]
> **Previous owner**
> Character: [Name], [Level]
> Player Discord ID:
> **New owner**
> Character: [Name], [Level]
> Player Discord ID: 
> ```
> - Characters (or guilds) may freely transfer the ownership of magic items if they are listed in the Black Market document, following the Level Limitations above.
> - For permanently transferring the ownership of a magic item that is not listed in the Black Market document, the transfer needs to be approved via `@FanMail`.
> - Auctions count as Ownership Transfers: the seller needs to send a FanMail prior to beginning the auction, if applicable.
> - Putting the item on the will count as Ownership Transfer: the writer of the will needs to send a FanMail prior to posting the will, if applicable.