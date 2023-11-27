---
description: Emitted when a invite has been create
---

# inviteCreate

```javascript
bot.on("inviteCreate", (invite) => {
    console.log(`The invite ${invite.code} has been created for ${invite.guild.name}`)
})
```
