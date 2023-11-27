---
description: You can create a role menu component to add it into in a message.
---

# RoleSelect

```javascript
const {RoleSelect, ActionRow} = require('devland.js')

let select = new RoleSelect()
select.customId = "my_select"
select.placeholder = "select a role"
let row = new ActionRow(select)
// look the "Button" page to understand why we are creating a ActionRow

<channel>.send({components: [row]})
<interaction>.send({components: [row]})
```

**All RoleSelect options available :**

```javascript
<RoleSelect>.customId = string,<-| // you can set only one of them
    .custom_id = string, <---------|
    .placeholder = string,
    .max_length = string,
    .min_length = string,
    .disabled = boolean
```
