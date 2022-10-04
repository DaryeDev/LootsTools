# Gift Packs with Twitch Channel Points

!!! note

    This is meant to be taken as a Start Guide for those that want to Gift Streamloots' Packs with Twitch Channel Points, and then explore the tool deeply.

    As this guide is focused on new users, we will start from the absolute start.

    If you are only interested on a part of the Guide, you can skip to your point of interest on the Index.

Gifting Streamloots’ Packs is one of most requested feature on Streamloots Automations, but with Loot's Tools it can be done easy, quick and simple.

Let me take you through the process of incorporating this into your Streams, with some examples and some insights on Loot's Tools, to meet this tool and learn about some of the things it can do for you.

---

## Install Loot’s Tools

First of all, we'll need to install and setup Loot's Tools.

Loot's Tools is an automation tool focused on **Streamloots**, made by a Content Creator, for Content Creators.

However, Loot's Tools can automate much more than only Streamloots Cards, like Subscriptions or Packs Purchases, or, outside of Streamloots for example, Twitch Channel Points Rewards, Chat Messages and Commands, Subscriptions or Donations, but we'll talk about it later.

Find out how to install and set it up here: [Getting Started](../gettingStarted)

---

## Test Gifting and how to make Pack-gifting Cards

You have Loot's Tools installed? Great! Let's get on Gifting Packs here.

Let's first learn how to edit Cards and Events:

### Let's make a Card that Gifts a Pack

![Test Gift](https://lh4.googleusercontent.com/uroLxoUOnvg_X90GQR7JML0I8aK8rGOUQ6uB7BnRlwzGRZMylzfFWYq6MV7ZqRiAo-ALQa4xAo9QwSy2Z-TbTWyslo0pLI8qArMfyrJGzf6TphNXbMeeN6Ee86zlmnyHdpotK05GljMvin9H6A){: style="width: 80%;"}

1. [Enhance a Card to test](../../desktop/cards/enhanceCards), then edit its Commands by clicking on the Card and selecting “Edit Card Commands”.

2. Press TAB and choose “**Gift Pack**”.

3. With that Command we can choose **the number of Packs** we want to gift, **the Collection they are from**, **who to give them to**, and **how many Cards** they have (1-3).

    On Giftee’s username, we’d like to tell Loot’s Tools to give it to who had used the Card, so we’ll use [Tags](../../desktop/cards/normalCards#tags), to introduce variables on Commands

    In this case, we’ll use **{user}**, which will be changed for the user that used that Card when the Command executes.

4. **Save your Card.**

### So let's test it, shall we?

You can do it from Streamloots or directly from Loot’s Tools (Clicking the Card and then on "**Test Card**").

If we go now to Streamloots, we will see that the user that used the Card will have received a Pack.

![Streamloots Pack Opening](https://lh4.googleusercontent.com/so-oZlo2VOUACPF7EbB_g2d6wcskjvf43EksZefzjgn1kQ8imvuTW3_e09YCdpY3YrVb4On0zfMZXRJ4Qmvh3fAj8NPgvgPuOPbNFzVU6nBMdsxoOIPoZSNArMPVEebsWtVm21FFjBPxVawNPw){: style="width: 80%;"}

**Note: If you won’t be using this Card for Gifting Packs, I’d delete its commands, just in case.**

---

## Ok, but how could we do it with Channel Points?

Before anything, to use Commands on Events such as Channel Points Redeems on Twitch, we’ll need [Twitch's EXtension](https://lootstools.darye.dev/docs/extensions/twitch).

### EXtensions and Loot’s Tools Plus

EXtensions are for **expanding the uses of Loot's Tools**, like *sending Messages* to Twitch Chat, doing *stuff on OBS*, executing *commands on Minecraft*, or, what is of our interest now, **Automating Channel Points**.

Using EXtensions requires a *Plus account*, so we’ll need to upgrade our account before continuing if it isn’t yet. If you want to upgrade, you can do it by clicking on “**Upgrade to Plus**” when the popup opens when opening Loot’s Tools.

![Upgrade to Plus Popup](https://lh6.googleusercontent.com/J3TqEA48JBQFwQz9X1y0cx6HC0aByCPqF69AXxzNS1UAIdel41k8yXWw-Tdka06-YuEOss7irbMf6Jg_V0BubBrp4Orrn_E1Djx1wyP18M6YKoiIpVcAYWG6fFRCz0ki7MJOhz4mgnjJAbuZjg){: style="width: 80%;"}

… or by clicking on “**Upgrade to Plus**” on the User’s Page on the UI:

![Upgrade to Plus button on User's Page on the UI](https://lh5.googleusercontent.com/XlZD5EzsAvU9fr8aRcj0QJ3s-Yj8QloiQknAbMyMwofYcjSqWq193rxpjaRQitt30C-NdSK9-x328UrDfiP564-wVjjMY2LfF2gUwFgVErQfeQQ8dwF6PLIYbqpHlZScl4WS5G5-9gIE0-D4jQ){: style="width: 80%;"}

Upgrading to Plus also unlock **Events that execute Commands**, like Pack Purchases and Gifts (Also to the Community) or Streamloots Subscriptions, as we said earlier, **using EXtensions** and making more use of the tool; the ability to use **Python Scripts on Events** (Like Card redemptions, the aforementioned, and those given by EXtensions); and also you **support the development of Loot’s Tools and EXtensions**.

### Installing Twitch’s EXtension

Installing EXtensions is extremely easy: **Simply click a link.**

In Twitch’s case, and if you have a Plus Account, you can install it with the following link:

[Install LootsToolsEX for Twitch](https://lootstrading.darye.dev/latex/twitchEX){ .md-button .md-button--primary }

&nbsp;

When it installs, it will open a new tab on your browser, asking you for permission for “LootsToolsBot”, Loot’s Tools’ Bot on Twitch, to do its job.

Once allowed, Events such as Messages sent to chat, Chat Commands that you can configure on the EXtension’s Page on the UI, Channel Point Rewards redeems, Bits Donations, and Subscriptions will be available to automate with Loot’s Tools

### Remember the Card we did before…

With it, we could gift a Pack to the person that used it. With Channel Points, this will be similar, but we’ll need to change a couple of things.

![Gift Packs from Twitch's Channel Point Redeems](https://lh5.googleusercontent.com/yFGS5L9wFeutZ8Xchvm9dJl90253TmJL9UzoG4ROwKWoPBzWAdML3PycNxmBJXjm_diw8P_u-jA2v5Id3Qw6sNrQYia6Auu7nbU9ROsaj03D7Z9XcprJa2NbEN7G13isTzyWTJZoa1liRFhCog){: style="width: 80%;"}

We’ll open Loot’s Tools Editor, on the Cards’ Page on the UI, and we’ll select on the top part dropdown the Channel Point Reward we want to automate, in my case, that will be “Cofresito”.

When we are on this Event on the Editor, we will do the same as with the Card before: New Command, “Gift Pack”, select the Collection, but this time we’ll need to change the user.

This Event saves the username of who was redeemed the Reward on the variable, or [Tag](https://lootstools.darye.dev/docs/cards/normalCards#tags), “twitchChannelPointUser”. So, if we wanted it to gift a Pack to those who have redeemed the Reward, on the user we’ll need to write {twitchChannelPointUser}.

---

## Testing time

If we now test this Channel Point Reward on our Twitch Chat, a Pack will be given to us on your Streamloots Page.

![Test Channel Points Pack](https://lh5.googleusercontent.com/U9Fu-4BZFKeTPbpb2k_u66K258aqt1hXlxvE19SfQuUgppvQzu_3D9d5QQGrYZ64tyiSKQsfN6_j8Qw_rzbeEiys4b2NJyMXm1AgHx2DWy5Dakh2hk3qQqyZh7q7iM1RuzjMKrpFn7dFLXFK_Q){: style="width: 80%;"}

## Epilogue: More things with Twitch’s EXtension

With it, we said we could receive more Events, such as, for example, **Subs**

I have on my channel a promotion also found on many other channels: **1 Free Pack to those who sub**.

This would be made the same way as the Channel Point Reward one, but with the **Twitch Sub Event** and the **user being this time {twitchSubUserName}**.

You can find the Events and Commands of Twitch’s EXtension here: [LootsToolsEX for Twitch](https://lootstools.darye.dev/docs/extensions/twitch); and the rest of EXtensions here: [EXtensions](https://lootstools.darye.dev/docs/extensions)

If you have any issues or questions, don’t hesitate on sending me a message at Darye.#1315 on Discord or on my Discord Server: [DaryeHub](http://discord.io/Darye)
