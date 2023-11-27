---
description: Emitted when a auto mod rule is updated
---

# autoModRuleUpdate

```javascript
bot.on("autoModRuleUpdate", (rule) => {
    console.log(`${rule.creator.tag} just updated ${rule.name}'s rule in ${rule.guild.name}`)
})
```
