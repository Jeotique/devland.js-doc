---
description: This event is emitted when a message is updated
---

# messageUpdate

```javascript
bot.on("messageUpdate", (old_message, message) => {
    if(!old_message.data_is_available)
        return console.log("Message cache is disabled")
        
    console.log(`${old_message.content} -> ${message.content}`)
})
```
