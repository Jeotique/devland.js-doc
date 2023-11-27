---
description: Emitted when a forum channel has been delete
---

# channelDeleteForum

```javascript
bot.on("channelDeleteForum", (channel) => {
    if(!channel.data_is_available) 
        return console.log("Channel cache has been disabled")
    
    console.log(`The forum channel : ${channel.name} has been deleted`)
})
```
