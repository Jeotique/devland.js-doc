---
description: You can create a select menu component to add it into in a message.
---

# StringSelect

```javascript
const {StringSelect, ActionRow} = require('devland.js')

let select = new StringSelect()
select.customId = "my_select"
select.addOptions({
    label: "my first option",
    description: "this is the first option of this select menu",
    value: "first_option"
})
let row = new ActionRow(select)
// look the "Button" page to understand why we are creating a ActionRow

<channel>.send({components: [row]})
<interaction>.send({components: [row]})
```

**All StringSelect options available :**

```javascript
<StringSelect>.customId = string,<-| // you can set only one of them
    .custom_id = string, <---------|
    .placeholder = string,
    .max_length = string,
    .min_length = string,
    .disabled = boolean,
    .options = selectOptions[]
    
selectOptions = {
    label: string,
    value: string,
    description: string,
    emoji: APIEmoji | Emoji | string,
    default: string
}
```
