# Custom-Discord-Filter

This is a Customizable discord word filter, if the user types the word/phrase, it will be deleted. It is fully customizable, with an optional custom status.



# How to Setup

1. Launch your preferred Coding Application.

2. Create a file.

3. Drag/Open the file in the coding application.

4. Create 2 Folders inside, server.js and index.js

5. Install [discord.js](https://discord.js.org) in the folder.

6. Paste This Code:

```
let Discord = require("discord.js")
let client = new Discord.Client()

//Filter

client.on("message", message => {
if(message.content === "word1") {
  message.delete()
  message.channel.send("Warn Text")
    client.user.setActivity('ActivityHere', { type: "PLAYING"})
 }
})   
    

client.login("Token")


```


# How to Customize

## Going Online

One of the most important things about the bot is to get it online. Replace "Token" in `client.login` to your token, it should look like this :`client.login("MyBotToken")`

## Customizing the filter

Another important thing is the filter itself, thats the bot's purpose. change "word1" in `if(message.content ===` to the word. It should look like this: `if(message.content === "very bad word")`

## Warn Message

This will notify the user who said the word/phrase to not do it again. Change `Warn Text` in `message.channel.send` to the message. It should look like this: `message.channel.send("**Hey!** Dont Say That! Be nice to others and follow the rules.")`

## Custom Status

Make your bot stand out by using a custom status. Change the `type=PLAYING` in `client.user.setActivity('ActivityHere', { type: "PLAYING"})` to anything, this can be PLAYING, LISTENING, STREAMING, WATCHING, etc. 

### Custom Status Text

To Change the thing that is actually being played, change `activityHere` with the activity. It should look like this: 
`client.user.setActivity('My Bot is awesome!', { type: "STREAMING"})`


### I hope this helps moderate your server!


 
