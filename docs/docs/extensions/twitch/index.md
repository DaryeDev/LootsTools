# LootsToolsEX for Twitch

<sup style="font-size: 90%">(This is a feature unlocked with [***Loot's Tools Plus***](../../plus). A ***Plus*** Account is required.)</sup>

![TwitchEX](img/TwitchEX.png){: style="height: 150px;width: 150px;float: left;margin: 20px;"}

*LootsToolsEX for Twitch* is an *EXtension* which allows the interactivity between **Twitch.tv** and ***Loot's Tools***.

It makes possible things like **changing the** **Stream's Title** and **Game**, **sending messages** to Chat, **marking a moment** on the VOD, **getting the Stream's info** (Useful for [Advanced Cards](../../cards/advCards.md)), manage **VIPs** (*VIPing* and *unVIPing*), and **bans** (*banning* and *unbanning*).

---

## Installation

You can install *LootsToolsEX for Twitch* with [LaTEX](../../additionalFeatures/latex) by clicking here:

[[Download 'Loot's Tools EX for Twitch' with LaTEX](https://lootstrading.darye.dev/latex/twitchEX)]

---

## Setup

After installing the *EXtension*, you need to provide some values in order for this *EXtension* to work:

- An OAuth Twitch Chat Token ([You can get it here](https://twitchapps.com/tmi/))
- A ClientID and a Client Secret of the same account ([You can learn how to get it here](http://faq.demostoreprestashop.com/faq.php?fid=144&pid=41))

Then, go to the ```/extensions/``` folder, then on ```/twitchEX/```, and edit on ```twitchEX.py```, the values ```oauth_token```, ```client_id``` and ```client_secret``` with yours.

---

## Commands

(Note: the name between parenthesis is the function's name, used for calling them with [Advanced Cards](../../cards/advCards.md)' Scripts)

### TWITCHSEND (twitchSend)

This command sends a message to your Chat on Twitch.

#### Usage

```TWITCHSEND {message}```

#### Arguments

- **message** [str]: The message you want to send.

### TWITCHMARKER (twitchMarker)

This command marks a moment in the VOD.

#### Usage

```TWITCHMARKER {markerDescription}```

#### Arguments

- **markerDescription** [str] (Optional): The description of the marker.


### TWITCHGETSTREAM (twitchGetStream)

This command gets the info of your Twitch's stream.

#### Usage

```TWITCHGETSTREAM```

#### Arguments

-

### TWITCHSETGAME (twitchSetGame)

This command sets the game of your Twitch's stream.

#### Usage

```TWITCHSETGAME {game}```

#### Arguments

- **game** [str]: The name of the game.


### TWITCHSETTITLE (twitchSetTitle)

This command sets the game of your Twitch's stream.

#### Usage

```TWITCHSETTITLE {title}```

#### Arguments

- **title** [str]: The title you want to put on your Twitch's stream.


### TWITCHVIP (twitchVIP)

This command makes a user VIP on your Twitch's chat.

#### Usage

```TWITCHVIP {user}```

#### Arguments

- **user** [str]: The user you want to make VIP.


### TWITCHUNVIP (twitchUnVIP)

This command takes away a user's VIP on your Twitch's chat.

#### Usage

```TWITCHUNVIP {user}```

#### Arguments

- **user** [str]: The user from who you want to take away its VIP.


### TWITCHBAN (twitchBan)

This command bans a user from your Twitch's chat.

#### Usage

```TWITCHBAN {user}```

#### Arguments

- **user** [str]: The user you want to ban.

### TWITCHUNBAN (twitchUnban)

This command unbans a user from your Twitch's chat.

#### Usage

```TWITCHUNBAN {user}```

#### Arguments

- **user** [str]: The user you want to unban.
