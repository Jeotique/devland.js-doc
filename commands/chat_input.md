---
description: Create a slash command
---

# CHAT\_INPUT

```javascript
const {GuildCommand} = require('devland.js')

let command = new GuildCommand({
    name: "test-command",
    type: 1, //CHAT_INPUT
    description: "This is a test command", //required for slash command
})

<client>.on('interaction', interaction => {
    if(!interaction.isSlashCommand)
        return;
    
    if(interaction.commandName === "test-command")
        interaction.reply({
            content: "command received with success !",
            ephemeral: true //make the answer visible only by the command user
        })
})
```

**All GuildCommand options available for slash command :**

```javascript
<GuildCommand>.name = string,
    .description = string, //required if type is 'CHAT_INPUT'
    .type = commandType,
    .options = commandOptions[],
    .default_member_permissions = PermissionString[] | PermissionResolvable,
    .name_localization = localizationsOptions,
    .description_localization = localizationsOptions,
    .nsfw = boolean
    
commandOptions = {
    type = commandOptionsType,
    name = string,
    name_localizations = localizationsOptions,
    description = string,
    description_localizations = localizationsOptions,
    required = boolean,
    choices = commandChoicesOptions[],
    options = commandOptions[],
    channel_types = channelType[],
    min_value = number,
    max_value = number,
    min_length = number,
    max_length = number,
    autocomplete = boolean
}
commandChoicesOptions = {
    name = string,
    name_localizations = localizationsOptions,
    value = string | number
}
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

**Create a slash command with Auto Complete choices :**

```javascript
const {GuildCommand} = require('devland.js')

let command = new GuildCommand({
    name: "test-autocomplete",
    type: 1,
    description: "This is a test command for autocomplete",
    options: [{
        name: "something",
        description: "What do you want to say ?",
        type: 3, // autocomplete can be used with STRING, NUMBER, INTEGER only
        autocomplete: true
    }]
})

<client>.on('interaction', interaction => {
    if(interaction.isAutoCompleteRequest)
        return interaction.sendAutoCompleteChoices([
            {
                name: "first-choice",
                value: "hello"
            },
            {
                name: "second-choice",
                value: "bye bye"
            }
        ])
    if(interaction.isSlashCommand)
        if(interaction.commandName === "test-autocomplete") {
            let selected = interaction.getCommandValue("second-choice") //bye bye
            interaction.reply({
            content: `You selected : ${selected}`,
            ephemeral: true //make the answer visible only by the command user
            })
        }
})
```
