---
description: Emitted when a integration has been delete
---

# integrationDelete

```javascript
bot.on("integrationDelete", (guild, applicationId) => {
    console.log(`The integration ${applicationId} has been deleted in ${guild.name}`)
})
```
