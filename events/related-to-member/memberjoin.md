---
description: Emitted when a member join the server
---

# memberJoin

```javascript
bot.on("memberJoin", (member) => {
    console.log(`${member.user.tag} has joined : ${member.guild.name}`)
})
```
