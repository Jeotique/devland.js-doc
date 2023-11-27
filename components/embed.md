---
description: With devland you can create easly some embeds.
---

# Embed

```javascript
const {Embed} = require('devland.js')

let embed = new Embed()
embed.title = "My embed title"
embed.description = "My embed description"
embed.timestamp = Date.now()

<channel>.send({embeds: [embed]})
<interaction>.reply({embeds: [embed]})
```

**All embed options available :**

```javascript
<embed>.title = string,
    .description = string,
    .color = string | number,
    .timestamp = string | number | Date,
    .author = authorOptions,
    .footer = footerOptions,
    .image = imageOptions,
    .thumbnail = thumbnailOptions,
    .url = string,
    .fields = fieldOptions[]
    
authorOptions = {
    name: string,
    icon_url: string
}
footerOptions = {
    text: string,
    icon_url: string
}
imageOptions = {
    url: string
}
thumbnailOptions = {
    url: string
}
fieldOptions = {
    name: string,
    value: string,
    inline: boolean
}
```
