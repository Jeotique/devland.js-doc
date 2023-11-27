# Components collector

**Create and receive components response :**

_For the component type :_ [types.md](types.md "mention")

```javascript
const {Button, ActionRow, ComponentsType} = require('devland.js')

client.on('message', async(message) => {
    if(message.content !== "!collector") return;
    let button = new Button({
        label: "Edit message",
        custom_id: "edit"
    });
    let row = new ActionRow(button);
    let msg = await message.reply({content: "base message", components: [row]});
    const collector = msg.createComponentsCollector({componentType: ComponentsType.Button, filter: (m) => m.user.id === message.authorId, time: 60000});
    collector.on('collected', async(button) => {
        if(button.customId !== "edit") return;
        await msg.edit("edited message");
        await button.reply({content: "Message edited", ephemeral: true});
    })
    collector.on('end', () => {
        msg.removeComponents()
    })
})
```

**Collector params :**

```javascript
type collectorOptions = {
        type: "message" | "component",
        count: number,
        time: number,
        componentType: ComponentsType, //check Types page
        filter: Function
}
```

**Filter exemple :** `filter: (m) => m.user.id === message.authorId`

`m` _represent a Interaction_

The `end` event will be emitted when the `time` is elapsed or when `count` is declared and `count` component response is received
