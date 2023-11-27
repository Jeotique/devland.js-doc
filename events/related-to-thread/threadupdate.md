---
description: Emitted when a thread has been update
---

# threadUpdate

```javascript
bot.on("threadUpdate", (old_thread, thread) => {
    if(!old_thread.data_is_available) 
        return console.log("Thread cache has been disabled")
    
    console.log(`${old_thread.name} -> ${thread.name}`)
})
```
