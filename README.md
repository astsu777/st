# My build of ST v0.8.4

![](https://i.postimg.cc/hGmcNfqD/screenshot-20210324-012.png)

This repository hosts the source code of my build of ST (Simple Terminal) made by [Suckless software](https://st.suckless.org/). It is based on ST v0.8.4 and different patches have been applied in order to provide the features I like. The list applied patches can be found in the *patches* folder. It features:

* Truecolor terminal with 256 colors supported (built-in)
* If *fontconfig* is installed, antialiased fonts are supported (built-in)
* Transparent background if configured
* Bold texts are not rendered using the bright variant of the current color
* Ability to configure multiple fonts (useful when main font cannot render certain characters)
* Full ligature support
* Built-in scrollback
* Vertically center lines in the available space
* Allows to launch an instance of ST in a specific directory (with the *-d* flag)
* Supports sending output of commands to external pipe

# Dependencies
The following packages are necessary in order to run this build of ST properly:

* ttf-jetbrains-mono
* noto-fonts-emoji

Used fonts can obviously be modified in the *config.def.h* file if you don't want to use the two mentioned above.

# Installation
Basically, just clone this repository (or download it), compile the build and install it. Type the following commands:

```
git clone --depth 1 https://github.com/GSquad934/st.git
cd st
sudo make clean install
```

This build of ST integrates nicely with [my custom build of DWM](https://github.com/GSquad934/dwm).

# Running ST
ST can be run simply with the *st* command. It has a number of flags available:

```
usage: st [-aiv] [-c class] [-d path] [-f font] [-g geometry] [-n name] [-o file]
          [-T title] [-t title] [-w windowid] [[-e] command [args ...]]
```

Each flag (except for *-d* which is explained above) is detailed in the ST [manpage](https://www.mankier.com/1/st).

# Scripts
The patches adding the ability to redirect output of ST to an external pipe allow some scripting possibilities. Two scripts present in this repository called *st-XXXX* allow different actions tht are bound to keybindings. The script keybindings are all bound to *ALT+<KEY>* (see the next chapter for more details).

# Key Bindings
The keybindings are the ones by default. They are all configured in the *config.def.h* file. Here is the list of the most important ones and what they actually do:

| Key binding | Action |
| :--- | :--- |
| `Mouse wheel UP/DOWN` | scroll up and down the buffer |
| `Mouse middle click` | paste text selection |
| `SHIFT + PageUp/PageDown` | scroll up and down the buffer |
| `CTRL + SHIFT + PageUp` | zoom in |
| `CTRL + SHIFT + PageDown` | zoom out |
| `CTRL + SHIFT + Home` | reset zoom |
| `CTRL + SHIFT + c` | copy selection to clipboard |
| `CTRL + SHIFT + y` | copy and quickly paste selection (copied data not stored in clipboard) |
| `CTRL + SHIFT + v` | paste clipboard content |
| `ALT + l` | parse URLs in the buffer, show them in a menu and open the chosen one |
| `ALT + y` | parse URLs in the buffer, show them in a menu and copy the chosen one to the clipboard |
| `ALT + o` | parse commands in the buffer, show them in a menu and copy its output to the clipboard |

# Contact
You can always reach out to me:

* [Twitter](https://twitter.com/gaetanict)
* [Email](mailto:gaetan@ictpourtous.com)
