---
description: Emitted when a new scheduled event is created
---

# guildScheduledEventCreate

```javascript
bot.on("guildScheduledEventCreate", (event) => {
    console.log(`New event created on ${event.guild.name}`)
    console.log(`Event name : ${event.name}`)
    console.log(`Creator tag : ${event.creator.tag}`)
})
```
