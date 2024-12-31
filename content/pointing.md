---
title: Pointing
aliases:
- /Pointing
---

# Pointing
**Pointing** means to look at something with the crosshair (which is in the center of your screen) on it while being close enough to it. When something is pointed, it is highlighted, either by a wireframe or by some sort of “halo”. Pointing things is neccessary for tasks like [mining](https://wiki.luanti.org/Mining "Mining"), [building](https://wiki.luanti.org/Building "Building"), [using](https://wiki.luanti.org/Using "Using") …

The default distance for pointing is less than 4 blocks away. In [Minetest Game](https://wiki.luanti.org/Games/Minetest_Game "Games/Minetest Game"), this distance increases to 10 when using [creative mode](https://wiki.luanti.org/Creative_mode "Creative mode"). It is possible for items and held nodes to have their own pointing range.

Most [blocks](https://wiki.luanti.org/Blocks "Blocks") can be pointed at, but not all. [Liquids](https://wiki.luanti.org/Liquid "Liquid") are usually not be pointed at, but there are [special items](https://wiki.luanti.org/Category:Liquid_pointers "Category:Liquid pointers") which are capable of pointing to liquids. Examples are [buckets](https://wiki.luanti.org/Bucket "Bucket") and [boats](https://wiki.luanti.org/Boat "Boat"). A few blocks like [Air](https://wiki.luanti.org/Air "Air") can never be pointed. Also, [items](https://wiki.luanti.org/Items "Items") on the ground can be pointed (in order to collect them).

It is only possible to point at one thing at a time.

By default, a thin black rectangular wireframe will be shown around the block or entity which you currently point. The colour and thickness of the selection box can be changed with `selectionbox_color` and `selectionbox_width`. It is also possible to change it from an outline to a highlight which tints the pointed node with a configurable colour.