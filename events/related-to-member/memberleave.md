---
description: Emitted when a member leave the server
---

# memberLeave

```javascript
bot.on("memberLeave", (member) => {
    if(!member.data_is_available) 
        return console.log("Member cache is disabled")
        
    console.log(`${member.user.tag} has leaved : ${member.guild.name}`)
})
```
