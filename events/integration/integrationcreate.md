---
description: Emitted when a integration has been create
---

# integrationCreate

<pre class="language-javascript"><code class="lang-javascript">bot.on("integrationCreate", (integration) => {
<strong>    console.log(`The integration ${integration.name} has been created in ${integration.guild.name}`)
</strong>})
</code></pre>
