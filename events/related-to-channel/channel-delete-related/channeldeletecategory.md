---
description: Emitted when a category has been delete
---

# channelDeleteCategory

```javascript
bot.on("channelDeleteCategory", (channel) => {
    if(!channel.data_is_available) 
        return console.log("Channel cache has been disabled")
    
    console.log(`The category : ${channel.name} has been deleted`)
})
```
