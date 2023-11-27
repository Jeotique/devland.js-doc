---
description: Emitted when a announcement channel has been delete
---

# channelDeleteAnnouncement

```javascript
bot.on("channelDeleteAnnouncement", (channel) => {
    if(!channel.data_is_available) 
        return console.log("Channel cache has been disabled")
    
    console.log(`The announcement channel : ${channel.name} has been deleted`)
})
```
