---
description: This event is emitted every time the bot receive a message
---

# message

<pre class="language-javascript"><code class="lang-javascript">bot.on("message", (message) => {
    if(!message.webhookId)
        message.reply(`Hello ${message.author.tag}`)     
<strong>}) 
</strong></code></pre>
