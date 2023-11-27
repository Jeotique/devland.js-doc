---
description: Emitted when a stage channel has been update
---

# channelUpdateStage



```javascript
bot.on("channelUpdateStage", (old_channel, channel) => {
    if(!old_channel.data_is_available)
        return console.log("Channel cache is disabled")
        
    console.log(`The next stage channel has been updated : ${old_channel.name} -> ${channel.name}`)
})
```
