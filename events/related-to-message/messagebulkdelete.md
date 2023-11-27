---
description: Emitted when multiple messages are deleted at once in a channel
---

# messageBulkDelete

```javascript
bot.on("messageBulkDelete", (data) => {
     console.log(`Multiple messages deleted in ${data.channel.name} (${data.guild.name})`)
     if(data.messages.size < 1)
     {
          console.log(`Message cache is disabled`)
          console.log(`The following messages were deleted : ${data.messageIds.join(", ")}`)
     } else {
          data.messages.map(message => {
               console.log(`${message.author.tag} | ${message.content}`)
          })
     }
})
```
