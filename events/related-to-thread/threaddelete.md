---
description: Emitted when a thread has been delete
---

# threadDelete

```javascript
bot.on("threadDelete", (thread) => {
    if(!thread.data_is_available) 
        return console.log("Thread cache has been disabled")
    
    console.log(`The thread : ${thread.name} has been deleted`)
})
```
