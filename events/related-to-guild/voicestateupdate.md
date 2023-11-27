---
description: Emitted when a user's voice state changes
---

# voiceStateUpdate

```javascript
bot.on("voiceStateUpdate", (old_voice, voice) => {
    if(old_voice.data_is_available)
        return console.log("Voice cache is disabled")
    if(!voice.guild)
        return console.log("Invalid guild for voice state update")
    if(!old_voice.channelId && voice.channelId)
        return console.log(`${voice.user.tag} joined ${voice.channel.name}`)
    else if(old_voice.channelId && !voice.channelId)
        return console.log(`${voice.user.tag} leaved ${old_voice.channel.name}`)
    else if(old_voice.channelId !== voice.channelId)
        return console.log(`${voice.user.tag} moved from ${old_voice.channel.name} to ${voice.channel.name}`)
    else
        return console.log(`Something else, look the value properties`)
})
```
