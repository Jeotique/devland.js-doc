---
description: Emitted when a user use a bot interaction
---

# interaction

```javascript
bot.on("interaction", (interaction) => {
    if (interaction.isSlashCommand) {
        interaction.reply("Devland.js is incredible")
        console.log(interaction.commandName)
    }
})
```
