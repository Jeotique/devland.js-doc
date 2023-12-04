# 🤖 Declare Client

_**Wanna use the shard system ? Go**_ [_**here**_](use-shards.md)_**.**_

{% code title="index.js" lineNumbers="true" %}
```javascript
const {Client} = require("devland.js")
const bot = new Client({
    intents: ["GUILDS", "GUILD_MEMBERS", "GUILD_PRESENCES"]
    // or (best method) : 
    /* const {IntentFlags} = require('devland.js')
       intents: [IntentFlags.FLAGS.GUILDS, IntentFlags.FLAGS.GUILD_MEMBERS, IntentFlags.FLAGS.GUILd_PRESENCES]
    */
    guildsLifeTime: 7200000, 
    // here we ask to the module to cache all guilds during 2h
    // after all events with a guild as target, the life time will be reset to 2h
    connect: true,
    // represent the auto-connect, if true you will need to provid the token here
    token: "YOUR TOKEN" 
    //token is optional if 'connect' is on false, you will be invited to put
    // the token in the next page (Connect Client)
})
```
{% endcode %}

**All cache options available for the client :**&#x20;

```javascript
guildsLifeTime: milliseconds, //will unlock bot.guilds
channelsLifeTime: milliseconds, //will unlock bot.<type>Channels (ex : bot.textChannels)
usersLifeTime: milliseconds, //will unlock bot.users
messagesLifeTime: milliseconds, //will unlock bot.messages
threadsLifeTime: milliseconds, //will unlock bot.threadChannels
membersLifeTime: milliseconds, //will unlock <guild>.members
rolesLifeTime: milliseconds, //will unlock <guild>.roles
invitesLifeTime: milliseconds, //will unlock <guild>.invites
presencesLifeTime: milliseconds, //will unlock <guild>.presences & <member>.presence
voicesLifeTime: milliseconds, //will unlock <guild>.voicesStates & <member>.voice 
enableAllCaches: boolean, //enable all caches of the client
waitCacheBeforeReady: boolean, //wait for all caches enabled to be completed before emit the ready event, by default set to true

// warning, for the members, roles, presences, voices & invites cache the guilds cache must be enabled too
```

**All ws options available for the client :**

```javascript
large_threshold: number,
compress: boolean,
properties: propertiesOptions,

propertiesOptions = {
    $os: string | NodeJS.Platform,
    $browser: string,
    $device: string
}
```

**All presence options available for the client :**

```javascript
status: string, //dnd, online, invisible, idle, offline
afk: boolean,
activities: simpleActivity[],
since: number,

simpleActivity = {
    name: string,
    type: ActivityType,
    url: string,
}

ActivityType = {
    Game = 0,
    Streaming = 1,
    Listening = 2,
    Watching = 3,
    Custom = 4,
    Competing = 5
}
```

**All others options available for the client :**&#x20;

```javascript
connectionTimeout: number, //how many time before throwing a error if still not connected, default set to 30000 (30s)
maxReconnectAttempts: number, //how attempts to reconnect the gateway after a error, default set to Infinity
maxResumeAttempts: number, //how many attempts to resume the gateway connection after a disconnect, default set to 10
invalidCommandValueReturnNull: boolean, //<interaction>.getCommandValue() must return a null value or undefined if invalid, default set to true (null returned)
```
