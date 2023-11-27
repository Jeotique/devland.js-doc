---
description: Create a user context command
---

# USER

```javascript
const {GuildCommand} = require('devland.js')

let command = new GuildCommand({
    name: "test-command",
    type: 2, //USER
})

<client>.on('interaction', interaction => {
    if(!interaction.isUserContext)
        return;
    
    if(interaction.commandName === "test-command") {
        let user = interaction.getTargetUser()
        interaction.reply({
            content: `command received with success !\nUsed on ${user.tag}`,
            ephemeral: true //make the answer visible only by the command user
        })
    }
})
```

**All GuildCommand options available for user context :**

```javascript
<GuildCommand>.name = string,
    .type = commandType,
    .default_member_permissions = PermissionString[] | PermissionResolvable,
    .name_localization = localizationsOptions,
    .nsfw = boolean
    
localizationsOptions = {
    id = string,
    da = string,
    de = string,
    "en-GB" = string,
    "en-US" = string,
    "es-ES" = string,
    fr = string,
    hr = string,
    it = string,
    lt = string,
    hu = string,
    nl = string,
    no = string,
    pl = string,
    "pt-BR" = string,
    ro = string,
    fi = string,
    "sv-SE" = string,
    vi = string,
    tr = string,
    cs = string,
    el = string,
    bg = string,
    ru = string,
    uk = string,
    hi = string,
    th =  string,
    "zh-CN" =  string,
    ja = string,
    "zh-TW" = string,
    ko = string
 }
```
