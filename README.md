# PM2-Telegram-bot
  This bot let you control [PM2](https://pm2.io/doc/) with Telegram
# The difference from original MrMarble bot
  Added env variable at config.json of bot owner telegram id, which prevents unauthorized users from command access
  ```{
    "name": "PM2 Bot",
    "script": "bot.js",
    "watch": true,
    "env": {
      "TOKEN": "your token from botfather here",
      "ID": 111111111
    }
  }
  ```
## How to install
1. Clone the repository in the same computer/server where pm2 is running
2. Run `npm install` in the same directory as the project files to install all the dependencies
3. you have two options to run the bot:
  1. Open `bot.js` and add the telegram token that [@botFather](https://t.me/BotFather) gave you and then run `node bot.js`:
  ```javascript
  const TOKEN = process.env.TOKEN || "YOUR TOKEN HERE";
  ```
  2. Open `config.json` and add the telegram token that [@botFather](https://t.me/BotFather) gave you and then run `pm2 start config.json`:
```json
"TOKEN": "",
```

## Usage
For now there are only two commands available, list and restart.

### /list, /ls
  List all the processes that pm2 is managing 
  
  ![](assets/markdown-img-paste-20180819124409749.png) ![](assets/markdown-img-paste-20180819124449325.png)
### /restart
Let you restart or start a process by the name or the id, you can also use `all` to restart all the proccesses.

![](assets/markdown-img-paste-2018081912521625.png)
