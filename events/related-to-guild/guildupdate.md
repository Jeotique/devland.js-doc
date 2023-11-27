---
description: Emitted when a guild is updated
---

# guildUpdate

```javascript
bot.on("guildUpdate", (old_guild, guild) => {
    if(!old_guild.data_is_available)
         return console.log("Guild cache is disabled")
    
    console.log(`${old_guild.name} -> ${guild.name}`)
})
```
