---
title: Bot Embeds
---

Embeds or "Widgets" are images that can display your bots stats on your own website! On this page we will tell you how to access and customise them.

---

## Get Embed

<Route method="GET" path="/api/embed/{bot.id}" />

---

## Usage
To use the embed, you can insert the following link as an IFrame or Image into your website / documentation.

* Iframe
```markdown
<Iframe src="https://www.paradisebots.net/api/embed/:ID"/>
```

* Image
```markdown
https://www.paradisebots.net/api/embed/:ID.png
```

---

## Preview IFrame

<Iframe src="https://www.paradisebots.net/api/embed/727779650738323497"/>

---

In this example we used just a plain embed which defaults to .svg, We also used a Iframe to display the example
