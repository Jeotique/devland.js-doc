---
description: You can create a button component to add it into in a message.
---

# Button

```javascript
const {Button, ActionRow} = require('devland.js')

let button = new Button()
button.label = "my button text"
button.customId = "my_button"
let row = new ActionRow(button)
// you need to create a action row to send it into a message
// you can add only 5 components per row
// one row can contains only one component type

<channel>.send({components: [row]})
<interaction>.send({components: [row]})
```

**All button options available :**

```javascript
<button>.label = string, // optional if 'emoji' is not undefined
    .customId = string, // <|
    .custom_id = string, // you can set only one of them 
    .emoji = emoji | string, // optional if 'label' is not undefined
    .style = ButtonStyle, // 1 by default
    .url = string,
    .disabled = boolean
    
ButtonStyle = {
    Primary = 1,
    Secondary = 2,
    Success = 3,
    Danger = 4,
    Link = 5
}
```
