---
description: Emitted when a voice channel has been delete
---

# channelDeleteVoice

```javascript
bot.on("channelDeleteVoice", (channel) => {
    if(!channel.data_is_available) 
        return console.log("Channel cache has been disabled")
    
    console.log(`The voice channel : ${channel.name} has been deleted`)
})
```
