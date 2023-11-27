---
description: Emitted when a user leave a scheduled event
---

# guildScheduledEventUserRemove

```javascript
bot.on("guildScheduledEventUserRemove", (event, user) => {
    console.log(`Event subscribers update on ${event.guild.name}`)
    console.log(`Event name : ${event.name}`)
    console.log(`Creator tag : ${event.creator.tag}`)
    console.log(`${user.tag} leaved`)
})
```
