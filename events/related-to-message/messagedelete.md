---
description: This event is emitted when a message is deleted
---

# messageDelete

```javascript
bot.on("messageDelete", (message) => {
    if (!message.data_is_available)
         return console.log("Message cache is disabled")
         
    console.log(`${message.content} | ${message.author.tag}`)
})
```
