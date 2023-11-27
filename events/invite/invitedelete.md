---
description: Emitted when a invite has been delete
---

# inviteDelete

```javascript
bot.on("inviteDelete", (invite) => {
    if(!invite.data_is_available)
        return console.log("Invite cache is disabled")
        
    console.log(`The invite ${invite.code} has been deleted from ${invite.guild.name}`)
})
```
