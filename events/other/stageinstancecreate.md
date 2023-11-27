---
description: Emitted when a stageInstance has been create
---

# stageInstanceCreate

```javascript
bot.on("stageIntanceCreate", (stage) => {
    console.log(`Stage created in ${stage.guild_id} with the next topic : ${stage.topic}`)
})
```
