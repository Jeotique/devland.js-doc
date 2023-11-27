---
description: You can create a user menu component to add it into in a message.
---

# UserSelect

```javascript
const {UserSelect, ActionRow} = require('devland.js')

let select = new UserSelect()
select.customId = "my_select"
select.placeholder = "select a user"
let row = new ActionRow(select)
// look the "Button" page to understand why we are creating a ActionRow

<channel>.send({components: [row]})
<interaction>.send({components: [row]})
```

**All UserSelect options available :**

```javascript
<UserSelect>.customId = string,<-| // you can set only one of them
    .custom_id = string, <---------|
    .placeholder = string,
    .max_length = string,
    .min_length = string,
    .disabled = boolean
```
