---
description: Emitted when a emojis of guild has been update
---

# guildEmojisUpdate

```javascript
bot.on("guildEmojisUpdate", (guild, emojis) => {
    console.log(`Emojis have been updated in guild ${guild.name}`)
    console.log(`The guild contains now ${emojis.size} emojis`)
})
```
