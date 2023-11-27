---
description: Emitted when the voice server for a guild is updated
---

# voiceServerUpdate

```javascript
bot.on("voiceServerUpdate", (voiceServer) => {
    const guild = voiceServer.guild
    const token = voiceServer.token
    const endpoint = voiceServer.endpoint
    if(!guild)
        return console.log("Invalid guild for voice server update")
    console.log(`Voice server has been updated for guild ${guild.name}`)
    console.log(`Token : ${token}`)
    console.log(`Endpoint : ${endpoint}`)
})
```

