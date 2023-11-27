---
description: Emitted when a integration has been update
---

# integrationUpdate

```javascript
bot.on("integrationUpdate", (integration) => {
    console.log(`The integration ${integration.name} has been updated in ${integration.guild.name}`)
})
```
