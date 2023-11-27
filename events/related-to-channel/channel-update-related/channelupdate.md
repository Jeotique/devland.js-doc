---
description: This event is emitted when a channel is updated
---

# channelUpdate

```javascript
bot.on("channelUpdate", (old_channel, channel) => {
    if(!old_channel.data_is_available)
        return console.log("Channel cache is disabled")
        
    console.log(`${old_channel.name} -> ${channel.name}`)
})
```
