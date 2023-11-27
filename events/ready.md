---
description: >-
  This event is emitted only one time when the bot is connected to the discord
  gateway.
---

# ready

```javascript
bot.on('ready', () => {
    console.log(`${bot.user.tag} connected`)
    // use this if the guilds cache is enabled :
    console.log(`I'm on ${bot.guilds.size} guilds`)
    // use this if not :
    bot.fetchGuilds().then(guilds => console.log(`I'm on ${guilds.size} guilds`))
    
})
```
