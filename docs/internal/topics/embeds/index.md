---
title: Bot Embeds
---

Embeds or "Widgets" are images that can display your bots stats on your own website! On this page we will tell you how to access and customise them.


## Usage
To use the embed, you can insert the following link as an IFrame or Link into your website / documentation.

```markdown
https://www.paradisebots.net/api/embed/:ID
```

## Preview IFrame

<Iframe src="https://www.paradisebots.net/api/embed/650872568374493185"/>

![](https://www.paradisebots.net/api/embed/650872568374493185)

In this example we use just a plain embed but it can also be .svg, .png. We recommend SVG for the best quality.
https://top.gg/api/widget/owner/:ID.svg
Preview

The /owner/ can be replaced with the following to get the 4 other smaller widgets: status,upvotes,servers and lib. You can also append a querystring to hide the avatar on the smaller widgets: ?noavatar=true
Preview

Customization
The current sections of the widget available for customization are as follows
Widget Querystring Parameters
Parameter	Large Widget	Small Widget	Value
topcolor	✓		Hexadecimal
middlecolor	✓		Hexadecimal
usernamecolor	✓		Hexadecimal
certifiedcolor	✓		Hexadecimal
datacolor	✓		Hexadecimal
labelcolor	✓		Hexadecimal
highlightcolor	✓		Hexadecimal
avatarbg		✓	Hexadecimal
leftcolor		✓	Hexadecimal
rightcolor		✓	Hexadecimal
lefttextcolor		✓	Hexadecimal
righttextcolor		✓	Hexadecimal
Example of Customization
This is an example of changing the colors of the large widget
https://top.gg/api/widget/270904126974590976.svg?usernamecolor=FFFFFF&topcolor=000000
This is a preview of the examples output.


https://www.paradisebots.net/api/embed/650872568374493185
