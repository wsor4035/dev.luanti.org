---
title: Privileges
aliases:
- /Privileges
---

# Privileges

Every player has a set of privileges, which differ from server to server. Roughly spoken, one’s privileges determine what one is able to do and what not. Each privilege has a name (the meaning is described below). Privileges can be granted and revoked from other players by any player who has the privilege called “privs”. On a multiplayer server with a default configuration, new players start with the privileges called “interact” and “shout”. To view one’s own privileges, one can issue the [server command](/server-commands "Server commands") “/privs”.

Built-in privileges
-------------------

As of version 5.0.0, Luanti comes with the following privileges:

* gameplay-related:
  * **interact**—can [build](https://wiki.luanti.org/Building "Building")/[mine](https://wiki.luanti.org/Mining "Mining")/[use](https://wiki.luanti.org/Using "Using") blocks and drop/eat/craft/use items and [punch](https://wiki.luanti.org/Punching "Punching") things and interact with [objects](https://wiki.luanti.org/Objects "Objects") and [players](https://wiki.luanti.org/Player "Player")
  * **give**—can use the `/give` and `/giveme` commands
  * **teleport**—can use the `/teleport` command to teleport oneself to certain [coordinates](https://wiki.luanti.org/Coordinates "Coordinates") or to another [player](https://wiki.luanti.org/Player "Player")
  * **bring**—in combination with _**teleport**_, can use the `/teleport` command to teleport any player to certain coordinates or to yet another player
  * **fast**—allows the player to activate [fast mode](https://wiki.luanti.org/Controls#Movement_modes "Controls")
  * **fly**—allows the player to activate [fly mode](https://wiki.luanti.org/Controls#Movement_modes "Controls")
  * **noclip**—allows the player to activate ["noclip" mode](https://wiki.luanti.org/Controls#Movement_modes "Controls"), which allows them to fly through walls
* chat-related:
  * **shout**—can [chat](https://wiki.luanti.org/Chat "Chat") with other people
* world–manipulation-related:
  * **settime**—can set [time of day](https://wiki.luanti.org/Time_of_day "Time of day") using `/time`
* moderation-related:
  * **privs**—can set any privileges of players using `/grant` and `/revoke` (→[Server commands#Privilege manipulation](https://wiki.luanti.org/Server_commands#Privilege_manipulation "Server commands"))
  * **basic\_privs**—can set the privileges set as basic\_privs in the minetest.conf (default “interact” and “shout”) using `/grant` and `/revoke`
  * **kick**—can kick players with `/kick`
  * **ban**—can ban/unban IPs and names using `/ban` and `/unban`
  * **rollback**—can use the [rollback](https://wiki.luanti.org/index.php?title=Rollback&action=edit&redlink=1 "Rollback (page does not exist)") functionality
  * **protection\_bypass**—can bypass protection of blocks (e.g. can open [locked chests](https://wiki.luanti.org/Locked_Chest "Locked Chest") or [steel doors](https://wiki.luanti.org/Steel_Door "Steel Door") of everyone)
* administration-related:
  * **server**—can do server maintenance stuff such as `/shutdown`, `/clearobjects`, `/set`, …
  * **debug**—can access advanced [debug](https://wiki.luanti.org/Debug "Debug") features and information, such as the wirewrame in the debug screens (F5). It also prevents the game from restricting information in the debug screen and from restricting the “toggle block bounds” key.

Irrevokable privileges
----------------------

A player’s privileges may be irrevokable in certain situations. It is not possible to revoke these privileges with `/revoke` then.

In multiplayer [servers](https://wiki.luanti.org/Server "Server"), the player whose name equals the [minetest.conf](https://wiki.luanti.org/Minetest.conf "Minetest.conf") setting “name” automatically has all privileges and all of these are irrevokable. This is also the case for players who started a server (not a dedicated server). In [singleplayer](https://wiki.luanti.org/index.php?title=Singleplayer&action=edit&redlink=1 "Singleplayer (page does not exist)"), you start with **interact**, **shout**, **privs** and **basic\_privs**. These privileges are irrevokable.

Privileges from mods and [games](https://wiki.luanti.org/Games "Games")
-----------------------------------------------------------------------

### [Minetest Game](https://wiki.luanti.org/Games/Minetest_Game "Games/Minetest Game")

* **home**—can use `/home` and `/sethome`.

### Mods

[Mods](https://wiki.luanti.org/Mods "Mods") may make additional privileges available on the server. Issue the server command `/help privs` to receive a full list (and short descriptions) of all possible privileges on the server.

Server configuration
--------------------

Using the server’s configuration files, a lot of privilege-related stuff can be manipulated.

There is an option in the configuration file for setting the default privileges for new players. `default_privs = interact, shout`

* The player having the name in the “name” field of the configuration has all the privileges.

See also
--------

* [Server](https://wiki.luanti.org/Server "Server")
* [Server commands](https://wiki.luanti.org/Server_commands "Server commands")