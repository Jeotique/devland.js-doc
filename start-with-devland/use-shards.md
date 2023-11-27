# 📚 Use shards

```javascript
const {ShardingManager} = require('devland.js')
const shardSystem = new ShardingManager('./bot.js', { //bot.js represent the file where we declare our client
    token: "YOUR TOKEN BOT",
    autospawn: true, //will create shard(s) automatically (1000 guilds per shard)
})
shardSystem.on('shardCreate', shard => {
    console.log(`[CREATED] Shard ${shard.id}`)
    shard.on('ready', () => console.log(`[READY] Shard ${shard.id}`))
    shard.on('disconnect', () => console.log(`[DISCONNECT] Shard ${shard.id}`))
    shard.on('reconnecting', () => console.log(`[RECONNECTING] Shard ${shard.id}`))
    shard.on('spawn', () => console.log(`[SPAWN] Shard ${shard.id}`))
    shard.on('message', message => {
        console.log(`--------------------`)
        console.log(`[MESSAGE] Shard ${shard.id} :`)
        console.log(message)
        console.log(`--------------------`)
    })
   shard.on('error', error => {
        console.log(`--------------------`)
        console.log(`[ERROR] Shard ${shard.id} :`)
        console.log(error)
        console.log(`--------------------`)
    })
})
```

**Get total guilds size :**

```javascript
bot.on('ready', async() => {
    console.log(`${bot.user.tag}`)
    //GUILDS CACHE MUST BE ENABLED (https://devland-1.gitbook.io/devland.js/start-with-devland/declare-client)
    console.log(`${bot.guilds.size} guilds on this shard`)
    
    //can't create a error if all shards are not in 'ready' state, add a timeout before fetching if needed. By default all shards creation are separed by 5,5 seconds
    let data = await bot.shard.fetchClientValues('guilds.size') //will return an array with all results of every shards
    console.log(`${data.reduce((prev, val) => prev+val, 0)} total guilds`)
})
```

**All ShardingManager options :**&#x20;

```javascript
file: string; //represent the file to execute per shard
options = {
    totalShards: number|'auto', //'auto' by default, the total shard count to create, auto will fetch the recommended for your bot from discord api
    token: string, //your bot token, needed only if 'totalShards' is set to 'auto'
    respawn: boolean, //'true' by default, are shard respawning after a error ?
    shardArgs: string[],
    execArgv: string[],
    autospawn: boolean, //'false' by default, do the manager spawn shard(s) directly after his declaration ?
}
/*
    if 'autospawn' is set on false you will need to call :
    <ShardingManager>.spawn() //you can set in parameter the shard count you want (this is overwrite the totalShards from the options)
*/
```
