---
description: Emitted when a text channel has been update
---

# channelUpdateText

```javascript
bot.on("channelUpdateText", (old_channel, channel) => {
    if(!old_channel.data_is_available)
        return console.log("Channel cache is disabled")
        
    console.log(`The next text channel has been updated : ${old_channel.name} -> ${channel.name}`)
})
```
