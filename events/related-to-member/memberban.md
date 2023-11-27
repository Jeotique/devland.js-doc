---
description: Emitted when a member was banned
---

# memberBan



```javascript
bot.on("memberBan", (user, guild) => {
    console.log(`The member ${user.tag} has been banned from ${guild.name}`)
})
```
