---
description: Emitted when a announcement channel has been update
---

# channelUpdateAnnouncement



```javascript
bot.on("channelUpdateAnnouncement", (old_channel, channel) => {
    if(!old_channel.data_is_available)
        return console.log("Channel cache is disabled")
        
    console.log(`The next announcement channel has been updated : ${old_channel.name} -> ${channel.name}`)
})
```
