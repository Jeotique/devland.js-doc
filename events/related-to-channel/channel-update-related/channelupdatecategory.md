---
description: Emitted when a category has been update
---

# channelUpdateCategory

```javascript
bot.on("channelUpdateCategory", (old_channel, channel) => {
    if(!old_channel.data_is_available)
        return console.log("Channel cache is disabled")
        
    console.log(`The next category has been updated : ${old_channel.name} -> ${channel.name}`)
})
```
