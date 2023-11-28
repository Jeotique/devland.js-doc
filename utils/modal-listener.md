# Modal listener

**Create and receive modal response :**

```javascript
const {Modal, textInputStyle} = require('devland.js')

client.on('interaction', async(interaction) => {
    if(!interaction.isCommand) return;
    if(interaction.commandName !== "modal") return;
    let modal = new Discord.Modal()
    modal.name = "Test modal"
    modal.customId = "test_modal"
    modal.components = [{
        label: "First input",
        custom_id: "first_input",
        style: textInputStyle.Short,
        required: true
    }]
    await interaction.submitModal(modal)
    const collector = interaction.createModalListener({time: 60000})
    collector.on('collected', async(m) => {
        await m.deferUpdate()
        let text = m.getModalValue("first_input")
        console.log(text)
        interaction.channel.send({content: text})
    })
    collector.on('end', () => {
    
    })
})
```
