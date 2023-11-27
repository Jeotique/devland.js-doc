---
description: Emitted when a user adds a reaction to a message.
---

# messageReactionAdd

```javascript
bot.on("messageReactionAdd", (data) => {
    if(!data.channel)
        return console.log("Invalid reaction")
    if(data.guild)
        console.log(`${data.user.tag} reacted with ${data.emoji.name} to a message in ${data.guild.name}`)
    else
        console.log(`${data.user.tag} reacted with ${data.emoji.name} to a private message`)
})
```
