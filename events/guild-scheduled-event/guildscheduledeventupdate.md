---
description: Emitted when a scheduled event is updated
---

# guildScheduledEventUpdate

```javascript
bot.on("guildScheduledEventUpdate", (event) => {
    console.log(`Event updated on ${event.guild.name}`)
    console.log(`Event name : ${event.name}`)
    console.log(`Creator tag : ${event.creator.tag}`)
    if(event.status === 2) 
        console.log(`Event started`)
    else if(event.status === 3)
        console.log(`Event completed`)
    else if(event.status === 4)
        console.log(`Event canceled`)
})
```
