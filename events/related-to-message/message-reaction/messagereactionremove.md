---
description: Emitted when a user remove a reaction to a message.
---

# messageReactionRemove

```javascript
bot.on("messageReactionRemove", (data) => {
    if(!data.channel)
        return console.log("Invalid reaction")
    if(data.guild)
        console.log(`${data.user.tag} unreacted with ${data.emoji.name} to a message in ${data.guild.name}`)
    else
        console.log(`${data.user.tag} unreacted with ${data.emoji.name} to a private message`)
})
```
