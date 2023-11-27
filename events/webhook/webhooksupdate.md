---
description: Emitted when a channel's webhooks are created, updated, deleted
---

# webhooksUpdate

```js
bot.on("webhooksUpdate", (channel) => {
    console.log(`Webhooks in channel ${channel.name} in guild ${channel.guild.name} have been created, updated or deleted`)
})
```
