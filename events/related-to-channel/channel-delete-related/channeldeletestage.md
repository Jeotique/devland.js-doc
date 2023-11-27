---
description: Emitted when a stage channel has been delete
---

# channelDeleteStage

```javascript
bot.on("channelDeleteStage", (channel) => {
    if(!channel.data_is_available) 
        return console.log("Channel cache has been disabled")
    
    console.log(`The stage channel : ${channel.name} has been deleted`)
})
```
