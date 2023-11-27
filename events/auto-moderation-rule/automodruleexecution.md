---
description: Emitted when a auto mod rule is triggered
---

# autoModRuleExecution

```javascript
bot.on("autoModRuleExecution", async(data) => {
    let guild = bot.guilds.get(data.guild_id) || await bot.fetchGuild(data.guild_id)
    let member = guild.members.get(data.user_id) || await guild.fetchMember(data.user_id)
    let rule = guild.fetchAutoModRule(data.rule_id)
    console.log(`${member.user.tag} just triggered ${rule.name} in ${guild.name}`)
})
```
