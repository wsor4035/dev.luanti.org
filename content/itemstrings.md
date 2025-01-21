---
title: Itemstrings
aliases:
- /Itemstrings
---

# Itemstrings


**Itemstrings** are the internal names for items, blocks, nodes (everything which can be stored in an [inventory](https://wiki.luanti.org/Inventory "Inventory")).

Syntax
------

An usual itemstring consists of a the name of the [mod](https://wiki.luanti.org/Mods "Mods") where the item originates from followed by a “:” followed by an item name. All itemstrings are case sensitive.

```
<mod_name>:<item_name>

```


Examples:

*   `default:torch` — a [torch](https://wiki.luanti.org/Torch "Torch") (from mod “default”)
*   `default:dirt` — [dirt](https://wiki.luanti.org/Dirt "Dirt") (from mod “default”)
*   `farming:bread` — [bread](https://wiki.luanti.org/Bread "Bread") (from mod “farming”)
*   `wool:orange` — orange [wool](https://wiki.luanti.org/Wool "Wool") (from mod “wool”)
*   `screwdriver:screwdriver` — [screwdriver](https://wiki.luanti.org/Screwdriver "Screwdriver") (from mod “screwdriver”)

There are itemstrings which don’t follow the syntax rules, see [#Special itemstrings](#Special_itemstrings).

Usages
------

Itemstrings can be used as arguments used for the `/give` and `/giveme` [commands](https://wiki.luanti.org/Server_commands "Server commands").

Example: `/giveme default:torch`—give yourself a [torch](https://wiki.luanti.org/Torch "Torch")

Special itemstrings
-------------------

There are itemstrings which do not follow the usual syntax rules. These itemstrings are always available, regardless of the activated [mods](https://wiki.luanti.org/Mods "Mods"):

*   [`air`](https://wiki.luanti.org/Air "Air")
*   [`ignore`](https://wiki.luanti.org/Ignore "Ignore")

See also
--------

*   [Items](https://wiki.luanti.org/Items "Items")
*   [Blocks](https://wiki.luanti.org/Blocks "Blocks")