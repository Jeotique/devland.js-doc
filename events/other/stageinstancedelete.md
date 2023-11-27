---
description: Emitted when a stageInstance has been delete
---

# stageInstanceDelete

```javascript
bot.on("stageIntanceDelete", (stage) => {
    console.log(`Stage deleted in ${stage.guild_id} with the next topic : ${stage.topic}`)
})
```
