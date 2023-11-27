---
description: Emitted when a roles of members has been update
---

# memberUpdate

```javascript
bot.on("memberUpdate", (old_member, member) => {
    if(!old_member.data_is_available)
        return console.log("Member cache is disabled")
        
    console.log(`${old_member.nick} -> ${member.nick}`)
})
```
