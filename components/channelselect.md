---
description: You can create a channel menu component to add it into in a message.
---

# ChannelSelect

```javascript
const {ChannelSelect, ActionRow} = require('devland.js')

let select = new ChannelSelect()
select.customId = "my_select"
select.placeholder = "select a channel"
let row = new ActionRow(select)
// look the "Button" page to understand why we are creating a ActionRow

<channel>.send({components: [row]})
<interaction>.send({components: [row]})
```

**All ChannelSelect** **options available :**

<pre class="language-javascript"><code class="lang-javascript">&#x3C;ChannelSelect>.customId = string,&#x3C;-| // you can set only one of them
    .custom_id = string, &#x3C;---------|
    .placeholder = string,
    .max_length = string,
    .min_length = string,
    .disabled = boolean,
    .channel_types = channelType[],
    .channelTypes = channelType[]
    
channelType = {
    GUILD_TEXT = 0,
    DM = 1,
    GUILD_VOICE = 2,
<strong>    GROUP_DM = 3,
</strong>    GUILD_CATEGORY = 4,
    GUILD_ANNOUNCEMENT = 5,
    ANNOUNCEMENT_THREAD = 10,
    PUBLIC_THREAD = 11,
    PRIVATE_THREAD = 12,
    GUILD_STAGE_VOICE = 13,
    GUILD_DIRECTORY = 14,
    GUILD_FORUM = 15,
    GUILD_MEDIA = 16
}
</code></pre>
