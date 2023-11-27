---
description: Emitted when a channel has been delete
---

# channelDelete

```javascript
bot.on("channelDelete", (channel) => {
    if(!channel.data_is_available) 
        return console.log("Channel cache has been disabled")
    
    console.log(`${channel.name} has been deleted`)
})
```
