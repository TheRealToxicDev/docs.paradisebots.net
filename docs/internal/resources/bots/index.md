---
title: Bot Object
---

## Bot Structure
Field |	Type	| Description | Status
|--------------|----------|--------------|--------------|
id	| Snowflake	| The id of the bot | **ACTIVE**
username	| String	| The username of the bot | **ACTIVE**
discriminator |	String	| The discriminator of the bot | **ACTIVE**
avatar?	| String	| The avatar hash of the bot's avatar | **BACK END**
defAvatar	| String	| The cdn hash of the bot's avatar if the bot has none | **BACK END**
lib	| String	| The library of the bot | **COMING SOON**
prefix	| String	| The prefix of the bot | **ACTIVE**
shortdesc	| String	| The short description of the bot | **ACTIVE**
longdesc?	| String	| The long description of the bot. Can contain Markdown | **ACTIVE**
tags	| Array of Strings	| The tags of the bot. Featured on the bot page | **COMING SOON**
website?	| String	| The website url of the bot | **COMING SOON**
support?	| String	| The support server invite code of the bot | **COMING SOON**
github? |	String	| The link to the github repo of the bot | **COMING SOON**
owners	| Array of Snowflakes	| The owners of the bot. First one in the array is the main owner | **ACTIVE**
guilds	| Array of Snowflakes	| The guilds featured on the bot page | **COMING SOON**
invite?	| String	| The custom bot invite url of the bot | **ACTIVE**
date	| Date	| The date when the bot was approved | **BACK END**
verifiedBot	| Boolean	| The verified status of the bot on our list | **BACK END**
certifiedBot | Boolean | The certified status of the bot | **COMING SOON**
vanity?	| String	| The vanity url of the bot | **ACTIVE**

---

## Get Bots
Use this endpoint to gain information about different bots as well as a list of all approved bots
<Route method="GET" path="/bots" />

---

## Get Bots (Unfiltered)
Use this endpoint to gain information about different bots as well as a list of all approved **and** unapproved bots
<Route method="GET" path="/bots/search" />

---

## Get Bot
Use this endpoint to gain information about a specific bot
<Route method="GET" path="/bots/{bot.id}" />

---
## Query String Params
Field	| Type | Description | Default
|--------------|----------|--------------|--------------|
limit	| Number	| The amount of bots to return. Max. 500	| 50
offset	| Number	| Amount of bots to skip	| 0
search	| String	| A search string in the format of field: value field2: value2 |
sort	| String	| The field to sort by. Prefix with - to reverse the order |
fields	| String	| A comma separated list of fields to show. |	All fields

---

## Response fields
Field	| Type	| Description
|--------------|----------|--------------|
results	| Array of bot objects | The matching bots
limit	| Number	| The limit used
offset	| Number	| The offset used
count	| Number | The length of the results array
total | Number | The total number of bots matching your search
