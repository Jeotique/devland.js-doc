---
description: Emitted when a scheduled event is deleted
---

# guildScheduledEventDelete

```javascript
bot.on("guildScheduledEventDelete", (event) => {
    console.log(`Event deleted on ${event.guild.name}`)
    console.log(`Event name : ${event.name}`)
    console.log(`Creator tag : ${event.creator.tag}`)
})
```
