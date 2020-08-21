---
title: Paradise Python Library
---

This is our official Python Library for Paradise Bots, if you have any issues please submit an issue on our github or join our discord
* [Github Link](https://github.com/ParadiseBotList)
* [Discord Link](https://discord.gg/ZAgkp2Q)

---
To start using server counts on a bot, 
* Go to your bot edit page, 
* Click the Authorization Token link at the bottom of the page. This will generate an auth token.

---

## Example
Example with Automatic Server Count
```jsx harmony
url = "https://paradisebots.net/api/auth/stats/:botid" # Make sure you include the domain

payload = "{\"server_count\": 1500}" # Replace this number with the server count
headers = {
  'authorization': 'YOUR_AUTH_TOKEN',
  'Content-Type': 'application/json'
}

response = requests.request("POST", url, headers=headers, data = payload)
print(response.text.encode('utf8'))

```

---

**Last Updated:** 08/16/2020
