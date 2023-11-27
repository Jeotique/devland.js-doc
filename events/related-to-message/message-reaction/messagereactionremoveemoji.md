---
description: Emitted when a custom emoji reaction is removed from a message
---

# messageReactionRemoveEmoji

```javascript
bot.on("messageReactionRemoveEmoji", (guild, channel, message, emoji) => {
    if(!channel || !message || !emoji)
        return console.log("Invalid reaction")
    if(guild)
        console.log(`The emoji ${emoji.name} has been removed from the message ${message.id} in channel ${channel.name} in guild ${guild.name}`)
    else
        console.log(`The emoji ${emoji.name} has been removed from the message ${message.id} in channel ${channel.name} in private`)
})
```
