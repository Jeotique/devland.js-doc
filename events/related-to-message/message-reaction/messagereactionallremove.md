---
description: Emitted when all reactions are removed from a message
---

# messageReactionAllRemove

```javascript
bot.on("messageReactionAllRemove", (guild, channel, message) => {
    if(!channel || !message)
        return console.log("Invalid message")
    if(guild)
        console.log(`All reactions have been removed from the message ${message.id} in channel ${channel.name} in guild ${guild.name}`)
    else
        console.log(`All reactions have been removed from the message ${message.id} in channel ${channel.name} in private`)
})
```
