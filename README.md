# Twitch-Chat-vs-Streamer-Lichess

## How to use:

1) Create a file named config.js with the following code:
```
module.exports = {
	STREAMER: (String) streamer's twitch username,
	STREAMER_LICHESS: (String) streamer's lichess username,
	AUTHORIZED_USERS: [(String)] twitch users allowed to use the !setvotingperiod command - might just make mods only later,
	TWITCH_OAUTH: (String) oauth token for bot's twitch account,
	LICHESS_OAUTH: (String) oauth token for bot's lichess account,
	CHAT_COOLDOWN: (int) time in milliseconds to wait between sending messages (1-2 seconds is good) not needed if bot is vip or mod,
	VOTING_PERIOD: (int) time in seconds that chat has to vote,
	ACKNOWLEDGE_VOTE: (Boolean) whether or not the twitch bot should acknowledge users' votes in chat
};
```

(You can get the twitch oauth token [here](https://twitchapps.com/tmi/), and the lichess oauth token [here](https://lichess.org/api#operation/botAccountUpgrade))

2) The streamer needs to challenge the lichess bot-it should automatically accept it and the game will begin with instructions sent to chat!

## To-do:
 - [ ] vote to offer draw
 - [ ] vote to resign
 - [x] web page to put on stream that visualizes the voting process
 - [ ] multiple streamers at once! shouldn't be too hard with current setup
 	- Update: won't work unless lichess authorizes the host ip to bypass their rate limiting
