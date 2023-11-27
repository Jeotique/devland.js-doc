---
description: You can create a mentionable menu component to add it into in a message.
---

# MentionableSelect

```javascript
const {MentionableSelect, ActionRow} = require('devland.js')

let select = new MentionableSelect()
select.customId = "my_select"
select.placeholder = "select a mentionable"
let row = new ActionRow(select)
// look the "Button" page to understand why we are creating a ActionRow

<channel>.send({components: [row]})
<interaction>.send({components: [row]})
```

**All MentionableSelect** **options available :**

```javascript
<MentionableSelect>.customId = string,<-| // you can set only one of them
    .custom_id = string, <---------|
    .placeholder = string,
    .max_length = string,
    .min_length = string,
    .disabled = boolean
```
