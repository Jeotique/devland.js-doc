---
description: Emitted when a forum channel has been update
---

# channelUpdateForum

```javascript
bot.on("channelUpdateForum", (old_channel, channel) => {
    if(!old_channel.data_is_available)
        return console.log("Channel cache is disabled")
        
    console.log(`The next forum channel has been updated : ${old_channel.name} -> ${channel.name}`)
})
```
