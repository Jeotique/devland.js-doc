# Send files

**Use a local image in a embed :**

```javascript
const {Embed} = require('devland.js')

let embed = new Embed({
    title: "Look my amazing logo",
    image: "attachment://Jeotique-Logo.png"
})
<channel>.send({
    embeds: [embed],
    files: ["./Jeotique-Logo.png"] //local path of the file (or online url)
    /*
    files: [{ //this method allows you to put a custom file name
        attachment: "./Jeotique-Logo.png",
        name: "logo.png"
    }] // embed.image = "attachment://logo.png"
    */
})
```

**Send a local image / file in a message :**

```javascript
<channel>.send({
    files: ["./Jeotique-Logo.png", "./document.txt"] //will send a image and a text file
})
```
