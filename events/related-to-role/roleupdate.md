---
description: Emitted when a role has been update
---

# roleUpdate

```javascript
bot.on("roleUpdate", (old_role, role) => {
    if(!old_role.data_is_available)
        return console.log("Role cache is disabled")
        
    console.log(`The role : ${old_role.name} has been update to ${role.name}`)
})
```
