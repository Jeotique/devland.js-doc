---
description: Emitted when a guildAuditlogEntry has been create
---

# guildAuditLogEntryCreate

```javascript
bot.on("guildAuditLogEntryCreate", (log) => {
    console.log(`New audit log entry has been created in guild ${log.guild.name}`)
    const action = log.type
    const executor = log.executor
    const target = log.targetId
    console.log(`Action : ${action}`)
    console.log(`Executor : ${executor.tag} (${executor.id})`)
    console.log(`Target : ${target}`)
})
```
