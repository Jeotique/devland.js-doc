---
description: Emitted when a user has been update
---

# userUpdate

```javascript
bot.on("userUpdate", (old_user, user) => {
    if(!old_user.data_is_available) 
        return console.log("User cache is disabled")
        
    console.log(`${old_user.username} -> ${user.username}`)
})
```
