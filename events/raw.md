---
description: Emitted at every events, with raw data (directly from the discord api)
---

# raw

```javascript
bot.on('raw', event => {
    const {data} = event
    switch(event.eventName) {
        case 'READY': 
            console.log(`${bot.user.tag} connected`)
        break;
        case 'MESSAGE_CREATE':
            console.log(`Message sended by ${data.author.username} :`)
            console.log(`${data.content??'no content'}`)
        break;
    }
})
```
