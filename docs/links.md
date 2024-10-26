
## Internal Links
Use normal Markdown links for internal pages:
```
[DISPLAY TEXT](LINK)
```
```
/folder/page-name/
/folder/page-name/#section
page-in-same-folder/
```

## Discord Links
Use this badge for Discord links: ([!badge icon="/images/discord-mark-blue.svg" variant="info" text="Sample"]())
```
[!badge icon="/images/discord-mark-blue.svg" variant="info" text="
DISPLAY TEXT
"](LINK)
```
Domains:
```
https://
  discord.com
  discord.gg
```
When convenient, convert these links to `discord.com` links first:
```
  discordapp.com
  canary.discord.com
```
## Other External Links
Use this badge for all other domains: ([!badge icon="link-external" variant="info" text="Sample"]())
```
[!badge icon="link-external" variant="info" text="
DISPLAY TEXT
"](LINK)
```
```
https://
  docs.google.com
  gsheet2.avrae
  avrae.readthedocs.io
  www.dndbeyond.com
  v1.dicecloud.com
  dicecloud.com
  www.youtube.com
  critrole.com
  media.wizards.com
  youtu.be
  github.com
  retype.com
  mojee.io
  support.discord.com
  www.howtogeek.com
  www.patreon.com
  rpgbot.net
  avrae.io
  tailwindcss.com
  www.dieharddice.com
  www.reddit.com
  bg3.wiki
  dustybot.info
```
When convenient, `docs.google.com` links can be truncated by removing everything after the final `/`. If there is a `#` after that point, keep the `#` and anything after that point, e.g.
```js
1   https://docs.google.com/document/d/1ZysB8Jyc3LfVMKOtiQwODfT1s2oI38shuTeCnbyOSPs/edit?usp=sharing
2   https://docs.google.com/document/d/1ZysB8Jyc3LfVMKOtiQwODfT1s2oI38shuTeCnbyOSPs/

3   https://docs.google.com/document/d/1ZysB8Jyc3LfVMKOtiQwODfT1s2oI38shuTeCnbyOSPs/edit?tab=t.0#heading=h.3msemhbc7iyt
4   https://docs.google.com/document/d/1ZysB8Jyc3LfVMKOtiQwODfT1s2oI38shuTeCnbyOSPs/#heading=h.3msemhbc7iyt

```
- link 2: remove everything after `/`; leads to the same document as link 1
- link 4: remove everything after `/` but before `#`; leads to the same document and heading as link 3