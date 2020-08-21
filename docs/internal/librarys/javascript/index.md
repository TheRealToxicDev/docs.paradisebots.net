---
title: Paradise JavaScript Library
---

This is our official JavaScript Library for Paradise Bots, if you have any issues please submit an issue on our github or join our discord.
* [Github Link](https://github.com/ParadiseBotList/paradiseapi.js/issues)
* [Discord Link](https://discord.gg/ZAgkp2Q)
* [Official NPM Module](https://help.paradisebots.net/docs/examples/paradiseapi.js)

---
To start using server counts on a bot, 
* Go to your bot edit page, 
* Click the Authorization Token link at the bottom of the page. This will generate an auth token.

---

## Example
Example of posting server count with supported libraries (Discord.js and Eris)

```js
var myHeaders = new Headers();
myHeaders.append("authorization", "YOUR_AUTH_TOKEN");
myHeaders.append("Content-Type", "application/json");

var requestOptions = {
  method: 'POST',
  headers: myHeaders,
  body: JSON.stringify({"server_count": 1500}); // Replace this number with the server count
};

fetch("https://paradisebots.net/api/auth/stats/:botid", requestOptions) // Make sure you include the domain
  .then(response => response.text())
  .then(console.log)
  .catch(console.error);
```

---
