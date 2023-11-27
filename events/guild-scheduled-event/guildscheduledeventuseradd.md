---
description: Emitted when a user join a scheduled event
---

# guildScheduledEventUserAdd

```javascript
bot.on("guildScheduledEventUserAdd", (event, user) => {
    console.log(`Event subscribers update on ${event.guild.name}`)
    console.log(`Event name : ${event.name}`)
    console.log(`Creator tag : ${event.creator.tag}`)
    console.log(`${user.tag} joined`)
})
```
