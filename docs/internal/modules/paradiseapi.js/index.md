---
title: paradiseapi.js
---

An official NPM Module for interacting with the  Paradise API

---

## Installation
`npm install paradisebotsapi.js` - Coming Soon (Buggy)

## GitHub Package Install
Append the Line below to your package.json
```
    "paradisebotsapi.js": "https://github.com/ParadiseBotList/paradisebotsapi.js",
```

• Save and profit

---

## Response

> [ Error ] 429 : `[PBL] (429): Your are being ratelimited, 1 request per 5 mins.`

> [ Error ] 404 : `[PBL] (404): Can't find server_count.`

> [ Error ] 404 : `[PBL] (404): Authorization header not found.`

> [ Error ] 400 : `[PBL] (400): server_count not integer.`

> [ Error ] 404 : `[PBL] (404): Bot not found!`

> [ Error ] 400 : `[PBL] (400): Incorrect authorization token.`

> [ Error ] 404 : `[PBL] (404): Go generate auth token for your bot!`

> [ Error ] 400 : `[PBL] (400): shard_count not integer.`


> [ Success ] 200 : **[200]: Your Stats Has Been Posted.**

```js
const Discord = require("discord.js")
const client = new Discord.Client()
const prefix = "!";
const PBL = require("paradisebotsapi.js")
const pbl = new PBL.get(client.user.id,"bot-auth-token")

client.on("ready", () => {
console.log(`Logged in as ${client.user.tag}.`)
setInterval(() => {
    pbl.post(client.guilds.cache.size)
    //pbl.post(client.guilds.cache.size, client.shard.count)
    //to post shard count!
})

client.on("message", message => {
    if(message.author.bot) return
    if(message.content == prefix + "ping"){
        message.reply(`Pong! it took ${client.ws.ping}`)
    }
})

client.login("token")

```
