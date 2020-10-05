---
title: Paradise JavaScript Library
---

This is our official JavaScript Library for Paradise Bots, if you have any issues please submit an issue on our github or join our discord.
* [Github Link](https://github.com/ParadiseBotList/paradisebotsapi.js/issues)
* [Discord Link](https://discord.gg/Cqy99Pt)
* [Official NPM Module](https://help.paradisebots.net/docs/examples/paradiseapi.js)

---
To start using server counts on a bot, 
* Go to your bot edit page, 
* Click the Authorization Token button. This will generate an auth token.

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

fetch("https://paradisebots.net/api/v1/bot/:botid", requestOptions) // Make sure you replace "botid" with your Bots Client ID
  .then(response => response.text())
  .then(console.log)
  .catch(console.error);
```

## Example
Example of posting server count using superagent

```js
client.on("ready", async () => {
            const servercount = client.guilds.cache.size
            superagent.post(`https://paradisebots.net/api/v1/bot/:botid`)
                .set('Authorization', 'KEY')
                .send({
                    server_count: servercount,
                    shard_count: "1"
                })
                .then(console.log('Updated your stats'))
                .catch(e => console.warn('Paradise API is down spam Toxic Dev'));
            superagent.post(`https://paradisebots.net/api/v1/bot/:botid`)
                .set('Authorization', 'KEY')
                .send({
                    server_count: servercount,
                    shard_count: "1"
                })
                .then(console.log('Updated your stats'))
                .catch(e => console.warn('Paradise API is down spam Toxic Dev'));
        } catch (err) {
            return;
        }
    }, 3600000);
});
```

---
