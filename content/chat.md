---
title: Chat
aliases:
- /Chat
- /Chat_window
---

# Chat


_This page is all about the in-game chat of Luanti. If you are interested in general Luanti chatter, refer to [IRC](/irc "IRC")._

The **in-game chat functionality** allows players to communicate with each other with short text messages inside a [server](https://wiki.luanti.org/Server "Server"). This article also covers the chat log which is used for purposes other than showing chat messages as well.

Sending messages
----------------

First of all, before you can chat anything at all, you require the “shout” [privilege](https://wiki.luanti.org/Privileges "Privileges"). Don’t worry, most servers give you this privilege by default.

You can chat either by opening the [chat window](https://wiki.luanti.org/Chat_window "Chat window") or the [console](https://wiki.luanti.org/Console "Console") which can be opened with the keys T or F10, respectively (assuming you use the [default key bindings](https://wiki.luanti.org/Controls "Controls")). Use the chat window or the console to enter a chat message. There are two types of chat messages: Public and direct.

### Public messages

A public message is a message which is visible to all connected players.

#### Ordinary public messages

Your chat message is a normal public message if it doesn’t begin with a “/”. It appears like this in the chat log:

```
<player> message

```


Example: If you enter “Hello, how are you?” as Alberto, then this will appear in the chat log:

```
<Alberto> Hello, how are you?

```


#### `/me` messages

This function is more like a gimmick than anything else. A `/me` message is a special case of a public message. The only real difference from the ordinary one is its appearance in the chat log. A `/me` message can be entered with:

```
/me <message>

```


Replace “`<message>`” with the actual message. You will get a message in the chat log which looks like this:

```
* player <message>

```


Example: Assume you want to say that you think that Luanti is awesome, in the third person. If you enter “`/me thinks Luanti is awesome.`”, you get:

```
* Alberto thinks Luanti is awesome.

```


### Direct messages

A direct message is a chat message which appears only on the chat logs of the sender and a chosen receiver of the message.

You can send a direct message (DM) to someone by using the “`/msg`” [server command](https://wiki.luanti.org/Server_commands "Server commands"). Say something in the form of:

```
/msg <player> <message>

```


Replace “`<message>`” by your actual message and “`<player>`” by the name of the player you want to send the message to. The message won’t be publicly visible in the chatlog and only appears to you and the other player. Be aware that direct messages are not _really_ secret, some people could still, in principle, intercept them.

Example: If your name is “Alberto” and you entered “`/msg Presto I want to show you my hidden chest.`”, then this will appear in the chat log of Presto:

```
DM from Alberto: I want to show you my hidden chest.

```


Chat log
--------

The chat log’s primary function is to log and show the chat messages in the order of appearance. The lastest message appears at the lowest line.

You see the chatlog on the [HUD](https://wiki.luanti.org/HUD "HUD") at the upper left part of the screen and in the console. You need to have the HUD enabled or the console opened in order to see the chat log. You can toggle the HUD on and off with F1 (default key binding). The chatlog you see on the HUD is somewhat short and only shows the messages for a limited time. Use the console for a full scrollable chatlog.

These are the following types of messages which can appear in the chat log:

*   Chat messages
*   Server messages
*   System messages

### Chat messages

A public chat message appears in the format of

```
<player> message

```


`/me` messages look like this:

```
* player message

```


When you receive a direct message (DM):

```
DM from player: message

```


### Server messages

Server messages are messages that are sent from the server, not from a player. The format is:

```
Server -!- message

```


Server messages may be sent to one, some or to all connected players. It depends on the event.

You receive server messages on various events. For example as a response to a server command (message to you) or when the server is about to shut down (message to all) etc.

### System messages

System messages are messages which directly come from the Luanti program which runs on your machine. An example for a system message is:

```
issued command: /privs

```


This message appears right after you issued the `/privs` [command](https://wiki.luanti.org/Controls "Controls").