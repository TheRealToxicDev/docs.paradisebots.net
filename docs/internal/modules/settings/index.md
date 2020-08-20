---
title: paradiseapi.js
---

An official NPM Module for interacting with the  Paradise API

---

## Installation
`npm install ` - Coming Soon

## Hard-Coded Install
Append the Line below to your package.json
```
    "paradiseapi.js": "https://github.com/ParadiseBotList/paradiseapi.js",
```

• Save and profit

---

## Examples

Example of posting server count with supported libraries (Discord.js and Eris)
```jsx harmony
const Discord = require("discord.js");
const client = new Discord.Client();
const PARADISE = require("paradiseapi.js");
const paradise = new PARADISE('Your Paradise API Token', client);

// Optional events
paradise.on('posted', () => {
  console.log('Server count posted!');
})

paradise.on('error', e => {
 console.log(`Oops! ${e}`);
})
```
