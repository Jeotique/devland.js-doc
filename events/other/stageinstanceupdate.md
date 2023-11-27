---
description: Emitted when a stageInstance has been update
---

# stageInstanceUpdate

```javascript
bot.on("stageIntanceUpdate", (stage) => {
    console.log(`Stage update in ${stage.guild_id} with the next topic : ${stage.topic}`)
})
```
