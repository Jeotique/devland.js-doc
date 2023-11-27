---
description: Emitted when a new auto mod rule is created
---

# autoModRuleCreate

```javascript
bot.on("autoModRuleCreate", (rule) => {
    console.log(`${rule.creator.tag} just created ${rule.name}'s rule in ${rule.guild.name}`)
})
```
