---
description: Emitted when a voice channel has been update
---

# channelUpdateVoice

```javascript
bot.on("channelUpdateVoice", (old_channel, channel) => {
    if(!old_channel.data_is_available)
        return console.log("Channel cache is disabled")
        
    console.log(`The next voice channel has been updated : ${old_channel.name} -> ${channel.name}`)
})
```
