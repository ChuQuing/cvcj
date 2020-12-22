# CVCJ Bot

## About 
CVCJ Bot is a customized version of [AssumeZero Bot](https://github.com/AstroCB/AssumeZero-Bot).

An additional `roast` functionality has been added to store and deliver the choicest roasts on group members.

## Usage

> !cvcj command [options]

To see a list of commands, use:

> !cvcj help

For accessing the roast functionality:

> !cvcj roast save me (do this while replying to a message you want to save as a roast)
> !cvcj roast me

# Setup

I've used an AWS EC2 free tier instance to host the server. Here are the steps to get your own instance running:

1. Create a new FB account for the bot.
2. Create a new account and a new cache on memcachier.
3. Make a new file, `src/credentials.js` and paste the following into it (specify fields as needed):
```js
// Facebook log-in credentials for bot account
exports.FACEBOOK_EMAIL = "";
exports.FACEBOOK_PASSWORD = "";
// MemCachier credentials (from MemCachier dashboard)
exports.MEMCACHIER_PASSWORD = "";
exports.MEMCACHIER_SERVERS = "";
exports.MEMCACHIER_USERNAME = "";
```
4. Create an AWS EC2 instance and connect to it (browser or SSH).
5. git clone your repository there and cd into the cloned dir.
4. `npm start`, and you should be good to go!

If you want to restart the bot, `npm restart` and then `npm run logs`.
