---
description: Emitted when a user starts typing in a channel
---

# userTypingStart

```javascript
bot.on("userTypingStart", (guild, channel, user, member, timestamp) => {
    if(!guild)
        return console.log(`${user.tag} started typing in private`)
    
    console.log(`${user.tag} started typing in channel ${channel.name} in guild ${guild.name} at ${new Date(timestamp).toLocaleString()}`)
})
```

