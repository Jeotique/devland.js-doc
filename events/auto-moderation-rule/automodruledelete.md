---
description: Emitted when a auto mod rule is deleted
---

# autoModRuleDelete

```javascript
bot.on("autoModRuleDelete", (rule) => {
    console.log(`${rule.creator.tag} just deleted ${rule.name}'s rule in ${rule.guild.name}`)
})
```
