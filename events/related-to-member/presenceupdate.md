---
description: Emitted when a user's presence is updated
---

# presenceUpdate

```javascript
bot.on("presenceUpdate", (old_presence, presence) => {
    if(!old_presence.data_is_available)
        return console.log("Presence cache is disabled")
        
    console.log(`The presence of user ${presence.user.tag} has been updated in guild ${presence.guild_id}`)
    if(old_presence.status === "offline" && presence.status !== "offline")
        console.log(`${presence.user.tag} is now online`)
    else if(old_presence.status !== "offline" && presence.status === "offline")
        console.log(`${presence.user.tag} is now offline`)
})
```
