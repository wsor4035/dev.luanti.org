---
title: Troubleshooting
aliases:
- /Troubleshooting
---

# Troubleshooting

This page lists common technical problems like crashes and error messages (enclosed in quotation marks) and possible solutions or explanations. For general questions, refer to [FAQ](https://wiki.luanti.org/FAQ "FAQ").

For information on how to report bugs, read [Reporting bugs](https://wiki.luanti.org/Reporting_bugs "Reporting bugs").

Graphics and sound
------------------

### The screen is too dark

If you feel the screen is too dark, you can adjust the display gamma to a more comfortable value. By default, it is set to 2.2 out of the possible choices between 1.0 and 3.0, with _higher_ numbers being brighter.

To change the display gamma, open your [minetest.conf](https://wiki.luanti.org/Minetest.conf "Minetest.conf") then add the line:

```
 display_gamma = 3.0

```


If the screen still appears too dark, there currently is no other easy solution apart from changing your display settings. If nothing else works and you still wish to increase the brightness, you will have to edit a text file. This only works with shaders enabled. Open `(Luanti directory)/client/shaders/nodes_shader/opengl_fragment.glsl` with a text editor, search for this line:

```glsl
vec4 base = texture2D(baseTexture, uv).rgba;

```


and change it to:

```glsl
vec4 base = texture2D(baseTexture, uv).rgba;
float factor = 1.2;
base.rgb *= factor;

```


You can try other values instead of 1.2, the higher the brighter. Add a decimal point even if you use integral values, for example `float factor = 2.0;` instead of `float factor = 2;`, as some drivers don't accept it otherwise.

### Everything in the game is in a weird color (particularly red), looks like rainbows, can partially see through things

Turn off shaders. Shaders are not supported by your graphics card.

### There is no sound under Windows

You need to download OpenAL to play sound on Windows (the file needed is [oalinst.exe](http://sfan.sf.funpic.de/oalinst.exe), you need to execute the program after it has finished downloading. Firefox and Chrome users may need to either save file or keep downloading, Internet Explorer users will need to just press run. Other browsers maybe the same or different. If one browser fails, try another.)

### The textures look blurry, but I want the pixels to show!

Turn off bilinear/trilinear filtering.

Error messages without crashes
------------------------------

### "unable to open database file"

If error message looks similar to the following, move the Luanti installation to a path that only contains ASCII characters. For example: move it to "C:\\Games\\Luanti\\"

```
AsyncErr: ServerThread::run Lua: Runtime error from mod '*builtin*' in callback on_prejoinplayer():
Failed to open SQLite3 database file C:\Users\ПЛАТЫ\Downloads\minetest-unzip\bin\..\worlds\newname
\auth.sqlite: unable to open database file

```


### “Unsupported texture format”

Don’t worry, this is completely normal. Luanti will still work.

### “Generating dummy image for \[…\].png”

This means that a faulty mod or texture pack does not supply an image for an object. Luanti will still work normally, but the specified object will use a replacement image (the “dummy image”); it will be a random color. This should normally be reported to the author of the mod or texture pack.

### "ERROR: No world name given or no game selected" in create world

You need to select a game, pick one you have installed from the gamebar at the bottom of the singleplayer tab.

Crashes
-------

_All sub-section titles in double quotes here mean that Luanti crashed with an error message like that._

### Any operating system

#### “Luanti can not load \[…\]/init.lua”

List of possible causes and the solution for each:

**Mod directory is named incorrectly**

Mod directories sometimes have an unwanted name termination. GitHub usually appends "-master" to the directory name, i.e. "modname-master". Also, mod makers may sometimes add version numbers to the name, such as "modname-v2.0" To solve this problem, simply remove the unwanted termination ("-master", "-v2.0") from the directory name and try again.

If you're unsure of the correct name: check the mod's topic title on the forum and copy the mod name which is found inside the square brackets \[ \].

**Invalid installation**

Ensure that you installed the mod correctly (empty mod directory?), read again [Installing Mods](https://wiki.luanti.org/Installing_Mods "Installing Mods").

**Still does not work**

If nothing helps, it might be a problem with the mod itself. Report the error to the mod author on the mod's forum page or, if available, the mod's GitHub page. Copy and paste the section in debug.txt that starts with "=====ERROR FROM LUA=====", or any relevant line about this problem.

#### ”attempt to index field `<any value>` (a nil value)”

These error may look like one these:

```
init.lua:2: attempt to index field 'settings' (a nil value)
init.lua:18: attempt to call field 'register_lbm' (a nil value)
tools.lua:61: attempt to call global 'nodeupdate' (a nil value)

```


The first two errors are caused by an outdated Luanti version, latter by an old mod which tries to call API functions which were removed. In the first case, you can [update Luanti](http://minetest.net/download) or try an in-development build to see whether it works. For the second case, check for mod updates or tell the author about your problem.

#### “Assertion '0' failed”

This is usually a mod error. Report it to the mod programmer or mod programmers. To find out the name of the mod, look for any error text directly above that gives a path to a mod's init.lua

```
 ERROR: An unhandled exception occurred: LuaError: error: mods/minetest/<modname>/init.lua:69: [...]

```


#### “ServerEnvironment::loadMeta(): EnvArgsEnd not found”

This means that _env\_meta.txt_ in your world folder got corrupted. Since it doesn't contain any important information you can simply delete the file and let Luanti re-create it.

### Windows

#### “MSCP2010.dll is not found” (or similar)

This is because Microsoft C++ Redistribute Package 2010 is not installed. [\[1\]](http://www.microsoft.com/en-us/download/details.aspx?id=5555%7CDownload)

#### Luanti doesn’t even start

If it stops working before the main window even opens, and there are no error messages in debug.txt, then try restarting your computer. (sometimes it crashes with a `0x00005` error, which is caused by Windows updates.) You can try looking in debug.txt for an error message or searching for a similar article in the forums.

Controls
--------

#### I have a trackpad and I can't walk and move my head at the same time

This is a problem with the trackpad configuration in your operating system, not with Luanti - some operating systems can be configured to disable keyboard input while the trackpad is being used.

To fix under the GNOME desktop environment, install and open "gnome-tweak-tool" and open the "Keyboard & Mouse" section. Then, flip the "Disable While Typing" switch.

To fix under other platforms please search the Web for instructions on changing this setting.