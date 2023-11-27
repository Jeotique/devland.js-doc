---
description: Emitted when a text channel has been delete
---

# channelDeleteText



```javascript
bot.on("channelDeleteText", (channel) => {
    if(!channel.data_is_available) 
        return console.log("Channel cache has been disabled")
    
    console.log(`The text channel : ${channel.name} has been deleted`)
})
```
