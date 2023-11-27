---
description: Emitted when a role has been delete
---

# roleDelete

```javascript
bot.on("roleDelete", (role) => {
    if(!role.data_is_available)
        return console.log("Role cache is disabled")
        
    console.log(`The role : ${role.name} has been deleted`)
})
```
